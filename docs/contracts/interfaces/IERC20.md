# IERC20

## Hierarchy

- `MRC20Wrapper`

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

MRC20Wrapper.constructor

#### Defined in

[assembly/interfaces/IERC20.ts:21](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/interfaces/IERC20.ts#L21)

## Properties

### \_origin

• **\_origin**: `Address`

#### Inherited from

MRC20Wrapper.\_origin

#### Defined in

node_modules/@massalabs/sc-standards/assembly/contracts/MRC20/wrapper.ts:26

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

MRC20Wrapper.allowance

#### Defined in

node_modules/@massalabs/sc-standards/assembly/contracts/MRC20/wrapper.ts:138

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

MRC20Wrapper.balanceOf

#### Defined in

node_modules/@massalabs/sc-standards/assembly/contracts/MRC20/wrapper.ts:110

___

### burn

▸ **burn**(`nbTokens`): `void`

Burn nbTokens on the caller address

Coins is left to zero as this function does not need storage entry creation.

#### Parameters

| Name | Type |
| :------ | :------ |
| `nbTokens` | `u256` |

#### Returns

`void`

#### Inherited from

MRC20Wrapper.burn

#### Defined in

node_modules/@massalabs/sc-standards/assembly/contracts/MRC20/wrapper.ts:236

___

### decimals

▸ **decimals**(): `u8`

#### Returns

`u8`

#### Overrides

MRC20Wrapper.decimals

#### Defined in

[assembly/interfaces/IERC20.ts:25](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/interfaces/IERC20.ts#L25)

___

### decreaseAllowance

▸ **decreaseAllowance**(`spenderAccount`, `nbTokens`): `void`

Decreases the allowance of the spender on the owner's account
by the given amount.

This function can only be called by the owner.
Coins is left to zero as this function does not need storage entry creation.

#### Parameters

| Name | Type |
| :------ | :------ |
| `spenderAccount` | `Address` |
| `nbTokens` | `u256` |

#### Returns

`void`

#### Inherited from

MRC20Wrapper.decreaseAllowance

#### Defined in

node_modules/@massalabs/sc-standards/assembly/contracts/MRC20/wrapper.ts:182

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

[assembly/interfaces/IERC20.ts:72](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/interfaces/IERC20.ts#L72)

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

[assembly/interfaces/IERC20.ts:82](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/interfaces/IERC20.ts#L82)

___

### increaseAllowance

▸ **increaseAllowance**(`spenderAccount`, `nbTokens`, `coins?`): `void`

Increases the allowance of the spender on the owner's account
by the given amount.

This function can only be called by the owner.

#### Parameters

| Name | Type | Default value |
| :------ | :------ | :------ |
| `spenderAccount` | `Address` | `undefined` |
| `nbTokens` | `u256` | `undefined` |
| `coins` | `u64` | `0` |

#### Returns

`void`

#### Inherited from

MRC20Wrapper.increaseAllowance

#### Defined in

node_modules/@massalabs/sc-standards/assembly/contracts/MRC20/wrapper.ts:159

___

### init

▸ **init**(`name`, `symbol`, `decimals`, `supply`, `coins?`): `void`

Initializes the smart contract.

#### Parameters

| Name | Type | Default value | Description |
| :------ | :------ | :------ | :------ |
| `name` | `string` | `undefined` | Name of the token. |
| `symbol` | `string` | `undefined` | Symbol of the token. |
| `decimals` | `u8` | `undefined` | Number of decimals of the token. |
| `supply` | `u256` | `undefined` | Initial supply of the token. |
| `coins` | `u64` | `0` | Number of coins to send to the smart contract. |

#### Returns

`void`

#### Inherited from

MRC20Wrapper.init

#### Defined in

node_modules/@massalabs/sc-standards/assembly/contracts/MRC20/wrapper.ts:46

___

### mint

▸ **mint**(`toAccount`, `nbTokens`, `coins?`): `void`

Mint an amount of nbTokens tokens from to the toAccount address .

#### Parameters

| Name | Type | Default value |
| :------ | :------ | :------ |
| `toAccount` | `Address` | `undefined` |
| `nbTokens` | `u256` | `undefined` |
| `coins` | `u64` | `0` |

#### Returns

`void`

#### Inherited from

MRC20Wrapper.mint

#### Defined in

node_modules/@massalabs/sc-standards/assembly/contracts/MRC20/wrapper.ts:225

___

### name

▸ **name**(): `string`

Returns the name of the token.

#### Returns

`string`

name of the token.

#### Inherited from

MRC20Wrapper.name

#### Defined in

node_modules/@massalabs/sc-standards/assembly/contracts/MRC20/wrapper.ts:72

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

[assembly/interfaces/IERC20.ts:78](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/interfaces/IERC20.ts#L78)

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

[assembly/interfaces/IERC20.ts:38](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/interfaces/IERC20.ts#L38)

___

### serialize

▸ **serialize**(): `StaticArray`<`u8`\>

#### Returns

`StaticArray`<`u8`\>

#### Implementation of

Serializable.serialize

#### Defined in

[assembly/interfaces/IERC20.ts:68](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/interfaces/IERC20.ts#L68)

___

### symbol

▸ **symbol**(): `string`

Returns the symbol of the token.

#### Returns

`string`

token symbol.

#### Inherited from

MRC20Wrapper.symbol

#### Defined in

node_modules/@massalabs/sc-standards/assembly/contracts/MRC20/wrapper.ts:80

___

### totalSupply

▸ **totalSupply**(): `u256`

Returns the total token supply.

The number of tokens that were initially minted.

#### Returns

`u256`

number of minted tokens.

#### Inherited from

MRC20Wrapper.totalSupply

#### Defined in

node_modules/@massalabs/sc-standards/assembly/contracts/MRC20/wrapper.ts:101

___

### transfer

▸ **transfer**(`toAccount`, `nbTokens`, `coins?`): `void`

#### Parameters

| Name | Type | Default value |
| :------ | :------ | :------ |
| `toAccount` | `Address` | `undefined` |
| `nbTokens` | `u256` | `undefined` |
| `coins` | `u64` | `0` |

#### Returns

`void`

#### Overrides

MRC20Wrapper.transfer

#### Defined in

[assembly/interfaces/IERC20.ts:44](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/interfaces/IERC20.ts#L44)

___

### transferFrom

▸ **transferFrom**(`ownerAccount`, `recipientAccount`, `nbTokens`, `coins?`): `void`

#### Parameters

| Name | Type | Default value |
| :------ | :------ | :------ |
| `ownerAccount` | `Address` | `undefined` |
| `recipientAccount` | `Address` | `undefined` |
| `nbTokens` | `u256` | `undefined` |
| `coins` | `u64` | `0` |

#### Returns

`void`

#### Overrides

MRC20Wrapper.transferFrom

#### Defined in

[assembly/interfaces/IERC20.ts:54](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/interfaces/IERC20.ts#L54)

___

### version

▸ **version**(): `string`

Returns the version of the smart contract.
This versioning is following the best practices defined in https://semver.org/.

#### Returns

`string`

#### Inherited from

MRC20Wrapper.version

#### Defined in

node_modules/@massalabs/sc-standards/assembly/contracts/MRC20/wrapper.ts:63
