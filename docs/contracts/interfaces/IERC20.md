# IERC20

## Implements

- `Serializable`

## Table of contents

### Constructors

- [constructor](IERC20.md#constructor)

### Properties

- [\_origin](IERC20.md#_origin)

### Methods

- [allowance](IERC20.md#allowance)
- [balanceOf](IERC20.md#balanceof)
- [burn](IERC20.md#burn)
- [decimals](IERC20.md#decimals)
- [decreaseAllowance](IERC20.md#decreaseallowance)
- [deserialize](IERC20.md#deserialize)
- [equals](IERC20.md#equals)
- [increaseAllowance](IERC20.md#increaseallowance)
- [init](IERC20.md#init)
- [mint](IERC20.md#mint)
- [name](IERC20.md#name)
- [notEqual](IERC20.md#notequal)
- [received](IERC20.md#received)
- [serialize](IERC20.md#serialize)
- [symbol](IERC20.md#symbol)
- [totalSupply](IERC20.md#totalsupply)
- [transfer](IERC20.md#transfer)
- [transferFrom](IERC20.md#transferfrom)
- [version](IERC20.md#version)

## Constructors

### constructor

• **new IERC20**(`origin?`): [`IERC20`](IERC20.md)

#### Parameters

| Name | Type |
| :------ | :------ |
| `origin` | `Address` |

#### Returns

[`IERC20`](IERC20.md)

#### Overrides

TokenWrapper.constructor

#### Defined in

[assembly/interfaces/IERC20.ts:14](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/interfaces/IERC20.ts#L14)

## Properties

### \_origin

• **\_origin**: `Address`

#### Inherited from

TokenWrapper.\_origin

#### Defined in

node_modules/@massalabs/sc-standards/assembly/contracts/FT/wrapper.ts:20

## Methods

### allowance

▸ **allowance**(`ownerAccount`, `spenderAccount`): `u256`

Returns the allowance set on the owner's account for the spender.

#### Parameters

| Name | Type |
| :------ | :------ |
| `ownerAccount` | `Address` |
| `spenderAccount` | `Address` |

#### Returns

`u256`

#### Inherited from

TokenWrapper.allowance

#### Defined in

node_modules/@massalabs/sc-standards/assembly/contracts/FT/wrapper.ts:96

___

### balanceOf

▸ **balanceOf**(`account`): `u256`

Returns the balance of an account.

#### Parameters

| Name | Type |
| :------ | :------ |
| `account` | `Address` |

#### Returns

`u256`

#### Inherited from

TokenWrapper.balanceOf

#### Defined in

node_modules/@massalabs/sc-standards/assembly/contracts/FT/wrapper.ts:74

___

### burn

▸ **burn**(`nbTokens`): `void`

Burn nbTokens on the caller address

#### Parameters

| Name | Type |
| :------ | :------ |
| `nbTokens` | `u256` |

#### Returns

`void`

#### Inherited from

TokenWrapper.burn

#### Defined in

node_modules/@massalabs/sc-standards/assembly/contracts/FT/wrapper.ts:184

___

### decimals

▸ **decimals**(): `u8`

#### Returns

`u8`

#### Defined in

[assembly/interfaces/IERC20.ts:23](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/interfaces/IERC20.ts#L23)

___

### decreaseAllowance

▸ **decreaseAllowance**(`spenderAccount`, `nbTokens`): `void`

Decreases the allowance of the spender on the owner's account
by the given amount.

This function can only be called by the owner.

#### Parameters

| Name | Type |
| :------ | :------ |
| `spenderAccount` | `Address` |
| `nbTokens` | `u256` |

#### Returns

`void`

#### Inherited from

TokenWrapper.decreaseAllowance

#### Defined in

node_modules/@massalabs/sc-standards/assembly/contracts/FT/wrapper.ts:134

___

### deserialize

▸ **deserialize**(`data`, `offset`): `Result`<`i32`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `data` | `StaticArray`<`u8`\> |
| `offset` | `i32` |

#### Returns

`Result`<`i32`\>

#### Implementation of

Serializable.deserialize

#### Defined in

[assembly/interfaces/IERC20.ts:46](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/interfaces/IERC20.ts#L46)

___

### equals

▸ **equals**(`other`): `bool`

#### Parameters

| Name | Type |
| :------ | :------ |
| `other` | [`IERC20`](IERC20.md) |

#### Returns

`bool`

#### Defined in

[assembly/interfaces/IERC20.ts:56](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/interfaces/IERC20.ts#L56)

___

### increaseAllowance

▸ **increaseAllowance**(`spenderAccount`, `nbTokens`): `void`

Increases the allowance of the spender on the owner's account
by the given amount.

This function can only be called by the owner.

#### Parameters

| Name | Type |
| :------ | :------ |
| `spenderAccount` | `Address` |
| `nbTokens` | `u256` |

#### Returns

`void`

#### Inherited from

TokenWrapper.increaseAllowance

#### Defined in

node_modules/@massalabs/sc-standards/assembly/contracts/FT/wrapper.ts:116

___

### init

▸ **init**(`name`, `symbol`, `decimals`, `supply`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `name` | `string` |
| `symbol` | `string` |
| `decimals` | `u8` |
| `supply` | `u256` |

#### Returns

`void`

#### Defined in

[assembly/interfaces/IERC20.ts:18](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/interfaces/IERC20.ts#L18)

___

### mint

▸ **mint**(`toAccount`, `nbTokens`): `void`

Mint an amount of nbTokens tokens from to the toAccount address .

#### Parameters

| Name | Type |
| :------ | :------ |
| `toAccount` | `Address` |
| `nbTokens` | `u256` |

#### Returns

`void`

#### Inherited from

TokenWrapper.mint

#### Defined in

node_modules/@massalabs/sc-standards/assembly/contracts/FT/wrapper.ts:175

___

### name

▸ **name**(): `string`

Returns the name of the token.

#### Returns

`string`

name of the token.

#### Inherited from

TokenWrapper.name

#### Defined in

node_modules/@massalabs/sc-standards/assembly/contracts/FT/wrapper.ts:46

___

### notEqual

▸ **notEqual**(`other`): `bool`

#### Parameters

| Name | Type |
| :------ | :------ |
| `other` | [`IERC20`](IERC20.md) |

#### Returns

`bool`

#### Defined in

[assembly/interfaces/IERC20.ts:52](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/interfaces/IERC20.ts#L52)

___

### received

▸ **received**(`reserve`, `fees`): `u256`

Returns the amount of token received by the pair

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `reserve` | `u256` | The total reserve of token |
| `fees` | `u256` | The total fees of token |

#### Returns

`u256`

- The amount received by the pair

#### Defined in

[assembly/interfaces/IERC20.ts:36](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/interfaces/IERC20.ts#L36)

___

### serialize

▸ **serialize**(): `StaticArray`<`u8`\>

#### Returns

`StaticArray`<`u8`\>

#### Implementation of

Serializable.serialize

#### Defined in

[assembly/interfaces/IERC20.ts:42](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/interfaces/IERC20.ts#L42)

___

### symbol

▸ **symbol**(): `string`

Returns the symbol of the token.

#### Returns

`string`

token symbol.

#### Inherited from

TokenWrapper.symbol

#### Defined in

node_modules/@massalabs/sc-standards/assembly/contracts/FT/wrapper.ts:54

___

### totalSupply

▸ **totalSupply**(): `u256`

Returns the total token supply.

The number of tokens that were initially minted.

#### Returns

`u256`

number of minted tokens.

#### Inherited from

TokenWrapper.totalSupply

#### Defined in

node_modules/@massalabs/sc-standards/assembly/contracts/FT/wrapper.ts:65

___

### transfer

▸ **transfer**(`toAccount`, `nbTokens`): `void`

Transfers tokens from the caller's account to the recipient's account.

#### Parameters

| Name | Type |
| :------ | :------ |
| `toAccount` | `Address` |
| `nbTokens` | `u256` |

#### Returns

`void`

#### Inherited from

TokenWrapper.transfer

#### Defined in

node_modules/@massalabs/sc-standards/assembly/contracts/FT/wrapper.ts:86

___

### transferFrom

▸ **transferFrom**(`ownerAccount`, `recipientAccount`, `nbTokens`): `void`

Transfers token ownership from the owner's account to
the recipient's account using the spender's allowance.

This function can only be called by the spender.
This function is atomic:
- both allowance and transfer are executed if possible;
- or if allowance or transfer is not possible, both are discarded.

#### Parameters

| Name | Type |
| :------ | :------ |
| `ownerAccount` | `Address` |
| `recipientAccount` | `Address` |
| `nbTokens` | `u256` |

#### Returns

`void`

#### Inherited from

TokenWrapper.transferFrom

#### Defined in

node_modules/@massalabs/sc-standards/assembly/contracts/FT/wrapper.ts:156

___

### version

▸ **version**(): `string`

Returns the version of the smart contract.
This versioning is following the best practices defined in https://semver.org/.

#### Returns

`string`

#### Inherited from

TokenWrapper.version

#### Defined in

node_modules/@massalabs/sc-standards/assembly/contracts/FT/wrapper.ts:37
