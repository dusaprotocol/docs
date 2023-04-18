[@dusalabs/core](../README.md) / [Exports](../modules.md) / WMAS

# Namespace: WMAS

## Table of contents

### References

- [DECIMALS\_KEY](WMAS.md#decimals_key)
- [NAME\_KEY](WMAS.md#name_key)
- [SYMBOL\_KEY](WMAS.md#symbol_key)
- [TOTAL\_SUPPLY\_KEY](WMAS.md#total_supply_key)
- [allowance](WMAS.md#allowance)
- [balanceOf](WMAS.md#balanceof)
- [constructor](WMAS.md#constructor)
- [decimals](WMAS.md#decimals)
- [decreaseAllowance](WMAS.md#decreaseallowance)
- [increaseAllowance](WMAS.md#increaseallowance)
- [name](WMAS.md#name)
- [received](WMAS.md#received)
- [symbol](WMAS.md#symbol)
- [totalSupply](WMAS.md#totalsupply)
- [transfer](WMAS.md#transfer)
- [transferFrom](WMAS.md#transferfrom)
- [version](WMAS.md#version)

### Functions

- [deposit](WMAS.md#deposit)
- [withdraw](WMAS.md#withdraw)

## References

### DECIMALS\_KEY

Re-exports [DECIMALS_KEY](ERC20.md#decimals_key)

___

### NAME\_KEY

Re-exports [NAME_KEY](ERC20.md#name_key)

___

### SYMBOL\_KEY

Re-exports [SYMBOL_KEY](ERC20.md#symbol_key)

___

### TOTAL\_SUPPLY\_KEY

Re-exports [TOTAL_SUPPLY_KEY](ERC20.md#total_supply_key)

___

### allowance

Re-exports [allowance](ERC20.md#allowance)

___

### balanceOf

Re-exports [balanceOf](ERC20.md#balanceof)

___

### constructor

Re-exports [constructor](ERC20.md#constructor)

___

### decimals

Re-exports [decimals](ERC20.md#decimals)

___

### decreaseAllowance

Re-exports [decreaseAllowance](ERC20.md#decreaseallowance)

___

### increaseAllowance

Re-exports [increaseAllowance](ERC20.md#increaseallowance)

___

### name

Re-exports [name](ERC20.md#name)

___

### received

Re-exports [received](ERC20.md#received)

___

### symbol

Re-exports [symbol](ERC20.md#symbol)

___

### totalSupply

Re-exports [totalSupply](ERC20.md#totalsupply)

___

### transfer

Re-exports [transfer](ERC20.md#transfer)

___

### transferFrom

Re-exports [transferFrom](ERC20.md#transferfrom)

___

### version

Re-exports [version](ERC20.md#version)

## Functions

### deposit

▸ **deposit**(`_`): `void`

Wrap wanted value.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `_` | `StaticArray`<`u8`\> | unused but mandatory. See https://github.com/massalabs/massa-sc-std/issues/18 |

#### Returns

`void`

#### Defined in

[assembly/contracts/WMAS.ts:16](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/contracts/WMAS.ts#L16)

___

### withdraw

▸ **withdraw**(`bs`): `void`

Unwrap wanted value.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `bs` | `StaticArray`<`u8`\> | Byte string |

#### Returns

`void`

#### Defined in

[assembly/contracts/WMAS.ts:35](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/contracts/WMAS.ts#L35)
