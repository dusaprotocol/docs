---
sidebar_class_name: hidden
sidebar_position: 10
sidebar_label: Vesting System
---

# Vesting System

## TLDR:

- Enables time-based unlocking of MRC-20 tokens on Massa  
- Create on-chain vesting sessions with configurable cliff and linear schedules  
- Supports an initial release, cliff period, and linear vesting thereafter  
- Beneficiaries claim unlocked tokens any time after they vest  
- Fully on-chain calculation—no off-chain components required  
- Sessions are cleared once fully claimed to reclaim storage

## What is the Vesting System?

The Vesting System is a suite of smart contracts allowing projects to lock ERC-20 tokens for a beneficiary and release them gradually according to a predefined schedule. It helps align incentives by ensuring tokens are only accessible over time, with an optional immediate release and cliff period before linear vesting.  

## Core Components

1. **Main Contract** (`createVestingSession`, `claimVestingSession`, `clearVestingSession`)  
2. **`VestingSessionInfo`** class (schedule parameters & unlocked-amount logic)  
3. **Utils** (`createUniqueId`, storage key generation)

---

## How to Create a Vesting Session

```ts
export function createVestingSession(args: StaticArray<u8>): StaticArray<u8>
````

### Arguments (serialized):

| Field                    | Type    | Description                                           |
| ------------------------ | ------- | ----------------------------------------------------- |
| `to_addr`                | Address | Beneficiary wallet                                    |
| `token_addr`             | Address | MRC-20 token contract                                 |
| `total_amount`           | u256    | Total tokens to vest                                  |
| `start_timestamp`        | u64     | Timestamp in millisecond when vesting starts          |
| `initial_release_amount` | u256    | Tokens unlocked immediately at `start_timestamp`      |
| `cliff_duration`         | u64     | Milliseconds after start before linear vesting begins |
| `linear_duration`        | u64     | Milliseconds over which the remaining tokens vest     |
| `tag`                    | string  | Optional identifier (max 127 chars)                   |

### Workflow

1. **Input validation**: checks that `initial_release_amount ≤ total_amount` and tag length.
2. **Session ID**: generates a unique `u64` ID via on-chain counter.
3. **Storage**:

   * Stores serialized `VestingSessionInfo` under key `(0x02, beneficiary, sessionId)`.
   * Initializes claimed-amount counter (u256 zero) under `(0x03, beneficiary, sessionId)`.
4. **Token Transfer**: pulls `total_amount` tokens from caller into the vesting contract.
5. **Return**: serialized `sessionId` for off-chain tracking.

---

## Claiming Vested Tokens

```ts
export function claimVestingSession(args: StaticArray<u8>): StaticArray<u8>
```

### Arguments (serialized):

| Field        | Type | Description                           |
| ------------ | ---- | ------------------------------------- |
| `session_id` | u64  | ID returned by `createVestingSession` |
| `amount`     | u256 | Amount of tokens to claim             |

### Logic

1. **Deserialize** inputs and load `VestingSessionInfo` & already `claimedAmount`.
2. **Compute**

   ```ts
   unlocked = vestingInfo.getUnlockedAt(currentTimestamp);
   claimable = unlocked – claimedAmount;
   ```
3. **Check** `amount ≤ claimable`, else revert.
4. **Update** claimed counter in storage.
5. **Transfer** requested tokens to beneficiary.

---

## Clearing Completed Sessions

```ts
export function clearVestingSession(args: StaticArray<u8>): StaticArray<u8>
```

### Arguments (serialized):

| Field        | Type | Description              |
| ------------ | ---- | ------------------------ |
| `session_id` | u64  | Vesting session to clear |

### Logic

1. **Verify** all tokens have been claimed (`claimedAmount == totalAmount`).
2. **Delete** both vesting info and claimed-amount storage entries.
3. **Free** on-chain storage and gas for subsequent operations.

---

## VestingSessionInfo Class

Encapsulates schedule parameters and vesting-calculation logic.

```ts
export class VestingSessionInfo {
  toAddr: Address;
  tokenAddr: Address;
  totalAmount: u256;
  startTimestamp: u64;
  initialReleaseAmount: u256;
  cliffDuration: u64;
  linearDuration: u64;
  tag: string;

  /** Returns total unlocked at Unix `timestamp` */
  public getUnlockedAt(timestamp: u64): u256 { … }
}
```

### `getUnlockedAt(timestamp)`

1. **Before start** (`timestamp < start`): returns `0`.
2. **During cliff** (`t < start + cliff`): returns `initialReleaseAmount`.
3. **After cliff + linear** (`t ≥ start + cliff + linear`): returns `totalAmount`.
4. **During linear**:

   ```ts
   linearAmount = totalAmount – initialReleaseAmount
   timeElapsed = timestamp – start – cliffDuration
   linearReleased = linearAmount × timeElapsed / linearDuration
   return initialReleaseAmount + linearReleased
   ```

---

## Utility Functions

* **`createUniqueId(): u64`**
  On-chain counter with prefix `0x01`, increments each call to guarantee unique session IDs.

* **Storage Key Builders**

  * `getVestingInfoKey(addr, sessionId)`: prefix `0x02` + `addr` + `sessionId`
  * `getClaimedAmountKey(addr, sessionId)`: prefix `0x03` + `addr` + `sessionId`

---

## Example Workflow

1. **Deploy** vesting contract.
2. **Sender** calls `createVestingSession` with beneficiary, token, amounts, and schedule.
3. **Beneficiary** periodically calls `claimVestingSession` to withdraw vested tokens.
4. **After** full vesting, either party calls `clearVestingSession` to delete the session and reclaim storage.

---

With this system, teams can trustlessly automate token vesting on Massa, providing transparent schedules and on-chain verifiability for beneficiaries.
