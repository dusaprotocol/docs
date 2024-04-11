# IERC20

## Hierarchy

- `TokenWrapper`

  ↳ **`IERC20`**

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

[assembly/interfaces/IERC20.ts:20](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/interfaces/IERC20.ts#L20)

## Properties

### \_origin

• **\_origin**: `Address`

#### Inherited from

TokenWrapper.\_origin

#### Defined in

node_modules/@massalabs/sc-standards/assembly/contracts/FT/wrapper.ts:26

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

node_modules/@massalabs/sc-standards/assembly/contracts/FT/wrapper.ts:125

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

node_modules/@massalabs/sc-standards/assembly/contracts/FT/wrapper.ts:103

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

node_modules/@massalabs/sc-standards/assembly/contracts/FT/wrapper.ts:213

___

### decimals

▸ **decimals**(): `u8`

#### Returns

`u8`

#### Overrides

TokenWrapper.decimals

#### Defined in

[assembly/interfaces/IERC20.ts:29](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/interfaces/IERC20.ts#L29)

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

node_modules/@massalabs/sc-standards/assembly/contracts/FT/wrapper.ts:163

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

[assembly/interfaces/IERC20.ts:75](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/interfaces/IERC20.ts#L75)

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

[assembly/interfaces/IERC20.ts:85](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/interfaces/IERC20.ts#L85)

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

node_modules/@massalabs/sc-standards/assembly/contracts/FT/wrapper.ts:145

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

#### Overrides

TokenWrapper.init

#### Defined in

[assembly/interfaces/IERC20.ts:24](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/interfaces/IERC20.ts#L24)

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

node_modules/@massalabs/sc-standards/assembly/contracts/FT/wrapper.ts:204

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

node_modules/@massalabs/sc-standards/assembly/contracts/FT/wrapper.ts:65

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

[assembly/interfaces/IERC20.ts:81](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/interfaces/IERC20.ts#L81)

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

[assembly/interfaces/IERC20.ts:42](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/interfaces/IERC20.ts#L42)

___

### serialize

▸ **serialize**(): `StaticArray`<`u8`\>

#### Returns

`StaticArray`<`u8`\>

#### Implementation of

Serializable.serialize

#### Defined in

[assembly/interfaces/IERC20.ts:71](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/interfaces/IERC20.ts#L71)

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

node_modules/@massalabs/sc-standards/assembly/contracts/FT/wrapper.ts:73

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

node_modules/@massalabs/sc-standards/assembly/contracts/FT/wrapper.ts:94

___

### transfer

▸ **transfer**(`toAccount`, `nbTokens`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `toAccount` | `Address` |
| `nbTokens` | `u256` |

#### Returns

`void`

#### Overrides

TokenWrapper.transfer

#### Defined in

[assembly/interfaces/IERC20.ts:48](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/interfaces/IERC20.ts#L48)

___

### transferFrom

▸ **transferFrom**(`ownerAccount`, `recipientAccount`, `nbTokens`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `ownerAccount` | `Address` |
| `recipientAccount` | `Address` |
| `nbTokens` | `u256` |

#### Returns

`void`

#### Overrides

TokenWrapper.transferFrom

#### Defined in

[assembly/interfaces/IERC20.ts:58](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/interfaces/IERC20.ts#L58)

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

node_modules/@massalabs/sc-standards/assembly/contracts/FT/wrapper.ts:56
