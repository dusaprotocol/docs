WMAS

# Namespace: WMAS

## Table of contents

### References

-   [DECIMALS_KEY](WMAS.md#decimals_key)
-   [NAME_KEY](WMAS.md#name_key)
-   [SYMBOL_KEY](WMAS.md#symbol_key)
-   [TOTAL_SUPPLY_KEY](WMAS.md#total_supply_key)
-   [allowance](WMAS.md#allowance)
-   [balanceOf](WMAS.md#balanceof)
-   [constructor](WMAS.md#constructor)
-   [decimals](WMAS.md#decimals)
-   [decreaseAllowance](WMAS.md#decreaseallowance)
-   [increaseAllowance](WMAS.md#increaseallowance)
-   [name](WMAS.md#name)
-   [received](WMAS.md#received)
-   [symbol](WMAS.md#symbol)
-   [totalSupply](WMAS.md#totalsupply)
-   [transfer](WMAS.md#transfer)
-   [transferFrom](WMAS.md#transferfrom)
-   [version](WMAS.md#version)

### Functions

-   [deposit](WMAS.md#deposit)
-   [withdraw](WMAS.md#withdraw)

## References

### DECIMALS_KEY

Re-exports [DECIMALS_KEY](ERC20.md#decimals_key)

---

### NAME_KEY

Re-exports [NAME_KEY](ERC20.md#name_key)

---

### SYMBOL_KEY

Re-exports [SYMBOL_KEY](ERC20.md#symbol_key)

---

### TOTAL_SUPPLY_KEY

Re-exports [TOTAL_SUPPLY_KEY](ERC20.md#total_supply_key)

---

### allowance

Re-exports [allowance](ERC20.md#allowance)

---

### balanceOf

Re-exports [balanceOf](ERC20.md#balanceof)

---

### constructor

Re-exports [constructor](ERC20.md#constructor)

---

### decimals

Re-exports [decimals](ERC20.md#decimals)

---

### decreaseAllowance

Re-exports [decreaseAllowance](ERC20.md#decreaseallowance)

---

### increaseAllowance

Re-exports [increaseAllowance](ERC20.md#increaseallowance)

---

### name

Re-exports [name](ERC20.md#name)

---

### received

Re-exports [received](ERC20.md#received)

---

### symbol

Re-exports [symbol](ERC20.md#symbol)

---

### totalSupply

Re-exports [totalSupply](ERC20.md#totalsupply)

---

### transfer

Re-exports [transfer](ERC20.md#transfer)

---

### transferFrom

Re-exports [transferFrom](ERC20.md#transferfrom)

---

### version

Re-exports [version](ERC20.md#version)

## Functions

### deposit

▸ **deposit**(`_`): `void`

Wrap wanted value.

#### Parameters

| Name | Type                 | Description                                                                   |
| :--- | :------------------- | :---------------------------------------------------------------------------- |
| `_`  | `StaticArray`<`u8`\> | unused but mandatory. See https://github.com/massalabs/massa-sc-std/issues/18 |

#### Returns

`void`

#### Defined in

[assembly/contracts/WMAS.ts:16](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/contracts/WMAS.ts#L16)

---

### withdraw

▸ **withdraw**(`bs`): `void`

Unwrap wanted value.

#### Parameters

| Name | Type                 | Description |
| :--- | :------------------- | :---------- |
| `bs` | `StaticArray`<`u8`\> | Byte string |

#### Returns

`void`

#### Defined in

[assembly/contracts/WMAS.ts:35](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/contracts/WMAS.ts#L35)
