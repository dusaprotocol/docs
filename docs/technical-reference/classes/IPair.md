IPair

# Class: IPair

## Table of contents

### Constructors

-   [constructor](IPair.md#constructor)

### Properties

-   [\_origin](IPair.md#_origin)

### Methods

-   [balanceOf](IPair.md#balanceof)
-   [balanceOfBatch](IPair.md#balanceofbatch)
-   [burn](IPair.md#burn)
-   [collectFees](IPair.md#collectfees)
-   [feeParameters](IPair.md#feeparameters)
-   [findFirstNonEmptyBinId](IPair.md#findfirstnonemptybinid)
-   [forceDecay](IPair.md#forcedecay)
-   [getBin](IPair.md#getbin)
-   [getFactory](IPair.md#getfactory)
-   [getPairInformation](IPair.md#getpairinformation)
-   [getTokenX](IPair.md#gettokenx)
-   [getTokenY](IPair.md#gettokeny)
-   [getUserBins](IPair.md#getuserbins)
-   [init](IPair.md#init)
-   [isApprovedForAll](IPair.md#isapprovedforall)
-   [mint](IPair.md#mint)
-   [name](IPair.md#name)
-   [pendingFees](IPair.md#pendingfees)
-   [safeBatchTransferFrom](IPair.md#safebatchtransferfrom)
-   [safeTransferFrom](IPair.md#safetransferfrom)
-   [setApprovalForAll](IPair.md#setapprovalforall)
-   [setFeesParameters](IPair.md#setfeesparameters)
-   [swap](IPair.md#swap)
-   [symbol](IPair.md#symbol)
-   [totalSupply](IPair.md#totalsupply)

## Constructors

### constructor

• **new IPair**(`at`)

Wraps a smart contract exposing standard token FFI.

#### Parameters

| Name | Type      | Description                    |
| :--- | :-------- | :----------------------------- |
| `at` | `Address` | Address of the smart contract. |

#### Defined in

[assembly/interfaces/IPair.ts:25](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/interfaces/IPair.ts#L25)

## Properties

### \_origin

• **\_origin**: `Address`

#### Defined in

[assembly/interfaces/IPair.ts:18](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/interfaces/IPair.ts#L18)

## Methods

### balanceOf

▸ **balanceOf**(`_account`, `_id`): `u64`

#### Parameters

| Name       | Type      |
| :--------- | :-------- |
| `_account` | `Address` |
| `_id`      | `u64`     |

#### Returns

`u64`

#### Defined in

[assembly/interfaces/IPair.ts:148](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/interfaces/IPair.ts#L148)

---

### balanceOfBatch

▸ **balanceOfBatch**(`_accounts`, `_ids`): `u64`[]

#### Parameters

| Name        | Type        |
| :---------- | :---------- |
| `_accounts` | `Address`[] |
| `_ids`      | `u64`[]     |

#### Returns

`u64`[]

#### Defined in

[assembly/interfaces/IPair.ts:153](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/interfaces/IPair.ts#L153)

---

### burn

▸ **burn**(`_ids`, `_amounts`, `_to`): [`BurnReturn`](BurnReturn.md)

#### Parameters

| Name       | Type      |
| :--------- | :-------- |
| `_ids`     | `u64`[]   |
| `_amounts` | `u64`[]   |
| `_to`      | `Address` |

#### Returns

[`BurnReturn`](BurnReturn.md)

#### Defined in

[assembly/interfaces/IPair.ts:91](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/interfaces/IPair.ts#L91)

---

### collectFees

▸ **collectFees**(`account`, `ids`): [`GetFeesReturn`](GetFeesReturn.md)

#### Parameters

| Name      | Type      |
| :-------- | :-------- |
| `account` | `Address` |
| `ids`     | `u64`[]   |

#### Returns

[`GetFeesReturn`](GetFeesReturn.md)

#### Defined in

[assembly/interfaces/IPair.ts:183](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/interfaces/IPair.ts#L183)

---

### feeParameters

▸ **feeParameters**(): [`FeeParameters`](FeeParameters.md)

#### Returns

[`FeeParameters`](FeeParameters.md)

#### Defined in

[assembly/interfaces/IPair.ts:39](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/interfaces/IPair.ts#L39)

---

### findFirstNonEmptyBinId

▸ **findFirstNonEmptyBinId**(`id`, `sentTokenY`): `u32`

#### Parameters

| Name         | Type   |
| :----------- | :----- |
| `id`         | `u32`  |
| `sentTokenY` | `bool` |

#### Returns

`u32`

#### Defined in

[assembly/interfaces/IPair.ts:115](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/interfaces/IPair.ts#L115)

---

### forceDecay

▸ **forceDecay**(): `void`

#### Returns

`void`

#### Defined in

[assembly/interfaces/IPair.ts:129](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/interfaces/IPair.ts#L129)

---

### getBin

▸ **getBin**(`_id`): [`Bin`](Bin.md)

#### Parameters

| Name  | Type  |
| :---- | :---- |
| `_id` | `u32` |

#### Returns

[`Bin`](Bin.md)

#### Defined in

[assembly/interfaces/IPair.ts:44](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/interfaces/IPair.ts#L44)

---

### getFactory

▸ **getFactory**(): `Address`

#### Returns

`Address`

#### Defined in

[assembly/interfaces/IPair.ts:120](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/interfaces/IPair.ts#L120)

---

### getPairInformation

▸ **getPairInformation**(): [`PairInformation`](PairInformation.md)

#### Returns

[`PairInformation`](PairInformation.md)

#### Defined in

[assembly/interfaces/IPair.ts:105](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/interfaces/IPair.ts#L105)

---

### getTokenX

▸ **getTokenX**(): [`IERC20`](IERC20.md)

#### Returns

[`IERC20`](IERC20.md)

#### Defined in

[assembly/interfaces/IPair.ts:97](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/interfaces/IPair.ts#L97)

---

### getTokenY

▸ **getTokenY**(): [`IERC20`](IERC20.md)

#### Returns

[`IERC20`](IERC20.md)

#### Defined in

[assembly/interfaces/IPair.ts:101](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/interfaces/IPair.ts#L101)

---

### getUserBins

▸ **getUserBins**(`account`): `u32`[]

#### Parameters

| Name      | Type      |
| :-------- | :-------- |
| `account` | `Address` |

#### Returns

`u32`[]

#### Defined in

[assembly/interfaces/IPair.ts:110](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/interfaces/IPair.ts#L110)

---

### init

▸ **init**(`factory`, `tokenX`, `tokenY`, `activeId`, `fp`): `void`

Calls the constructor

#### Parameters

| Name       | Type                                |
| :--------- | :---------------------------------- |
| `factory`  | `Address`                           |
| `tokenX`   | `Address`                           |
| `tokenY`   | `Address`                           |
| `activeId` | `u32`                               |
| `fp`       | [`FeeParameters`](FeeParameters.md) |

#### Returns

`void`

#### Defined in

[assembly/interfaces/IPair.ts:34](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/interfaces/IPair.ts#L34)

---

### isApprovedForAll

▸ **isApprovedForAll**(`_owner`, `_spender`): `bool`

#### Parameters

| Name       | Type      |
| :--------- | :-------- |
| `_owner`   | `Address` |
| `_spender` | `Address` |

#### Returns

`bool`

#### Defined in

[assembly/interfaces/IPair.ts:159](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/interfaces/IPair.ts#L159)

---

### mint

▸ **mint**(`_ids`, `_distributionX`, `_distributionY`, `_to`): [`MintReturn`](MintReturn.md)

Mint new LB tokens for each bins where the user adds liquidity.
This function will not transfer the tokens from the caller, it is expected that the tokens have already been
transferred to this contract through another contract.
That is why this function shouldn't be called directly, but through one of the add liquidity functions of the
router that will also perform safety checks.
Any excess amount of token will be sent to the `to` address. The lengths of the arrays must be the same.

#### Parameters

| Name             | Type      | Description                                                                                                |
| :--------------- | :-------- | :--------------------------------------------------------------------------------------------------------- |
| `_ids`           | `u64`[]   | The ids of the bins where the liquidity will be added. It will mint LB tokens for each of these bins.      |
| `_distributionX` | `u64`[]   | The percentage of token X to add to each bin. The sum of all the values must not exceed 100%, that is 1e9. |
| `_distributionY` | `u64`[]   | The percentage of token Y to add to each bin. The sum of all the values must not exceed 100%, that is 1e9. |
| `_to`            | `Address` | The address that will receive the LB tokens and the excess amount of tokens.                               |

#### Returns

[`MintReturn`](MintReturn.md)

#### Defined in

[assembly/interfaces/IPair.ts:81](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/interfaces/IPair.ts#L81)

---

### name

▸ **name**(): `string`

#### Returns

`string`

#### Defined in

[assembly/interfaces/IPair.ts:133](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/interfaces/IPair.ts#L133)

---

### pendingFees

▸ **pendingFees**(`account`, `ids`): [`GetFeesReturn`](GetFeesReturn.md)

#### Parameters

| Name      | Type      |
| :-------- | :-------- |
| `account` | `Address` |
| `ids`     | `u64`[]   |

#### Returns

[`GetFeesReturn`](GetFeesReturn.md)

#### Defined in

[assembly/interfaces/IPair.ts:177](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/interfaces/IPair.ts#L177)

---

### safeBatchTransferFrom

▸ **safeBatchTransferFrom**(`_from`, `_to`, `_ids`, `_amounts`): `void`

#### Parameters

| Name       | Type      |
| :--------- | :-------- |
| `_from`    | `Address` |
| `_to`      | `Address` |
| `_ids`     | `u64`[]   |
| `_amounts` | `u64`[]   |

#### Returns

`void`

#### Defined in

[assembly/interfaces/IPair.ts:172](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/interfaces/IPair.ts#L172)

---

### safeTransferFrom

▸ **safeTransferFrom**(`_from`, `_to`, `_id`, `amount`): `void`

#### Parameters

| Name     | Type      |
| :------- | :-------- |
| `_from`  | `Address` |
| `_to`    | `Address` |
| `_id`    | `u64`     |
| `amount` | `u64`     |

#### Returns

`void`

#### Defined in

[assembly/interfaces/IPair.ts:168](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/interfaces/IPair.ts#L168)

---

### setApprovalForAll

▸ **setApprovalForAll**(`_approved`, `_sender`): `void`

#### Parameters

| Name        | Type      |
| :---------- | :-------- |
| `_approved` | `bool`    |
| `_sender`   | `Address` |

#### Returns

`void`

#### Defined in

[assembly/interfaces/IPair.ts:164](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/interfaces/IPair.ts#L164)

---

### setFeesParameters

▸ **setFeesParameters**(`fp`): `void`

#### Parameters

| Name | Type                                |
| :--- | :---------------------------------- |
| `fp` | [`FeeParameters`](FeeParameters.md) |

#### Returns

`void`

#### Defined in

[assembly/interfaces/IPair.ts:124](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/interfaces/IPair.ts#L124)

---

### swap

▸ **swap**(`swapForY`, `to`): `u64`

Swap tokens iterating over the bins until the entire amount is swapped.
Will swap token X for token Y if `_swapForY` is true, and token Y for token X if `_swapForY` is false.
This function will not transfer the tokens from the caller, it is expected that the tokens have already been
transferred to this contract through another contract.
That is why this function shouldn't be called directly, but through one of the swap functions of the router
that will also perform safety checks.

#### Parameters

| Name       | Type      | Description                                                                       |
| :--------- | :-------- | :-------------------------------------------------------------------------------- |
| `swapForY` | `bool`    | Whether you've swapping token X for token Y (true) or token Y for token X (false) |
| `to`       | `Address` | The address to send the tokens to                                                 |

#### Returns

`u64`

#### Defined in

[assembly/interfaces/IPair.ts:61](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/interfaces/IPair.ts#L61)

---

### symbol

▸ **symbol**(): `string`

#### Returns

`string`

#### Defined in

[assembly/interfaces/IPair.ts:138](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/interfaces/IPair.ts#L138)

---

### totalSupply

▸ **totalSupply**(`_id`): `u64`

#### Parameters

| Name  | Type  |
| :---- | :---- |
| `_id` | `u64` |

#### Returns

`u64`

#### Defined in

[assembly/interfaces/IPair.ts:143](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/interfaces/IPair.ts#L143)
