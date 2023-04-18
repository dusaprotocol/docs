IERC20

# Class: IERC20

## Hierarchy

-   `TokenWrapper`

    ↳ **`IERC20`**

    ↳↳ [`IWMAS`](IWMAS.md)

## Implements

-   `Serializable`

## Table of contents

### Constructors

-   [constructor](IERC20.md#constructor)

### Properties

-   [\_origin](IERC20.md#_origin)

### Methods

-   [allowance](IERC20.md#allowance)
-   [balanceOf](IERC20.md#balanceof)
-   [burn](IERC20.md#burn)
-   [decreaseAllowance](IERC20.md#decreaseallowance)
-   [deserialize](IERC20.md#deserialize)
-   [equals](IERC20.md#equals)
-   [increaseAllowance](IERC20.md#increaseallowance)
-   [init](IERC20.md#init)
-   [mint](IERC20.md#mint)
-   [name](IERC20.md#name)
-   [notEqual](IERC20.md#notequal)
-   [received](IERC20.md#received)
-   [serialize](IERC20.md#serialize)
-   [symbol](IERC20.md#symbol)
-   [totalSupply](IERC20.md#totalsupply)
-   [transfer](IERC20.md#transfer)
-   [transferFrom](IERC20.md#transferfrom)
-   [version](IERC20.md#version)

## Constructors

### constructor

• **new IERC20**(`origin?`)

#### Parameters

| Name     | Type      |
| :------- | :-------- |
| `origin` | `Address` |

#### Overrides

TokenWrapper.constructor

#### Defined in

[assembly/interfaces/IERC20.ts:6](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/interfaces/IERC20.ts#L6)

## Properties

### \_origin

• **\_origin**: `Address`

#### Inherited from

TokenWrapper.\_origin

#### Defined in

[assembly/interfaces/TokenWrapper.ts:19](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/interfaces/TokenWrapper.ts#L19)

## Methods

### allowance

▸ **allowance**(`ownerAccount`, `spenderAccount`): `u64`

Returns the allowance set on the owner's account for the spender.

#### Parameters

| Name             | Type      |
| :--------------- | :-------- |
| `ownerAccount`   | `Address` |
| `spenderAccount` | `Address` |

#### Returns

`u64`

#### Inherited from

TokenWrapper.allowance

#### Defined in

[assembly/interfaces/TokenWrapper.ts:93](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/interfaces/TokenWrapper.ts#L93)

---

### balanceOf

▸ **balanceOf**(`account`): `u64`

Returns the balance of an account.

#### Parameters

| Name      | Type      |
| :-------- | :-------- |
| `account` | `Address` |

#### Returns

`u64`

#### Inherited from

TokenWrapper.balanceOf

#### Defined in

[assembly/interfaces/TokenWrapper.ts:73](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/interfaces/TokenWrapper.ts#L73)

---

### burn

▸ **burn**(`nbTokens`): `void`

Burn nbTokens on the caller address

#### Parameters

| Name       | Type  |
| :--------- | :---- |
| `nbTokens` | `u64` |

#### Returns

`void`

#### Inherited from

TokenWrapper.burn

#### Defined in

[assembly/interfaces/TokenWrapper.ts:155](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/interfaces/TokenWrapper.ts#L155)

---

### decreaseAllowance

▸ **decreaseAllowance**(`spenderAccount`, `nbTokens`): `void`

Decreases the allowance of the spender on the owner's account
by the given amount.

This function can only be called by the owner.

#### Parameters

| Name             | Type      |
| :--------------- | :-------- |
| `spenderAccount` | `Address` |
| `nbTokens`       | `u64`     |

#### Returns

`void`

#### Inherited from

TokenWrapper.decreaseAllowance

#### Defined in

[assembly/interfaces/TokenWrapper.ts:119](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/interfaces/TokenWrapper.ts#L119)

---

### deserialize

▸ **deserialize**(`data`, `offset`): `Result`<`i32`\>

#### Parameters

| Name     | Type                 |
| :------- | :------------------- |
| `data`   | `StaticArray`<`u8`\> |
| `offset` | `i32`                |

#### Returns

`Result`<`i32`\>

#### Implementation of

Serializable.deserialize

#### Defined in

[assembly/interfaces/IERC20.ts:33](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/interfaces/IERC20.ts#L33)

---

### equals

▸ **equals**(`other`): `bool`

#### Parameters

| Name    | Type                  |
| :------ | :-------------------- |
| `other` | [`IERC20`](IERC20.md) |

#### Returns

`bool`

#### Defined in

[assembly/interfaces/IERC20.ts:43](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/interfaces/IERC20.ts#L43)

---

### increaseAllowance

▸ **increaseAllowance**(`spenderAccount`, `nbTokens`): `void`

Increases the allowance of the spender on the owner's account
by the given amount.

This function can only be called by the owner.

#### Parameters

| Name             | Type      |
| :--------------- | :-------- |
| `spenderAccount` | `Address` |
| `nbTokens`       | `u64`     |

#### Returns

`void`

#### Inherited from

TokenWrapper.increaseAllowance

#### Defined in

[assembly/interfaces/TokenWrapper.ts:106](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/interfaces/TokenWrapper.ts#L106)

---

### init

▸ **init**(`name`, `symbol`, `decimals`, `supply`): `void`

#### Parameters

| Name       | Type     |
| :--------- | :------- |
| `name`     | `string` |
| `symbol`   | `string` |
| `decimals` | `u8`     |
| `supply`   | `u64`    |

#### Returns

`void`

#### Defined in

[assembly/interfaces/IERC20.ts:10](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/interfaces/IERC20.ts#L10)

---

### mint

▸ **mint**(`toAccount`, `nbTokens`): `void`

Mint an amount of nbTokens tokens from to the toAccount address .

#### Parameters

| Name        | Type      |
| :---------- | :-------- |
| `toAccount` | `Address` |
| `nbTokens`  | `u64`     |

#### Returns

`void`

#### Inherited from

TokenWrapper.mint

#### Defined in

[assembly/interfaces/TokenWrapper.ts:146](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/interfaces/TokenWrapper.ts#L146)

---

### name

▸ **name**(): `string`

Returns the name of the token.

#### Returns

`string`

name of the token.

#### Inherited from

TokenWrapper.name

#### Defined in

[assembly/interfaces/TokenWrapper.ts:45](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/interfaces/TokenWrapper.ts#L45)

---

### notEqual

▸ **notEqual**(`other`): `bool`

#### Parameters

| Name    | Type                  |
| :------ | :-------------------- |
| `other` | [`IERC20`](IERC20.md) |

#### Returns

`bool`

#### Defined in

[assembly/interfaces/IERC20.ts:39](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/interfaces/IERC20.ts#L39)

---

### received

▸ **received**(`reserve`, `fees`): `u64`

Returns the amount of token received by the pair

#### Parameters

| Name      | Type  | Description                |
| :-------- | :---- | :------------------------- |
| `reserve` | `u64` | The total reserve of token |
| `fees`    | `u64` | The total fees of token    |

#### Returns

`u64`

-   The amount received by the pair

#### Defined in

[assembly/interfaces/IERC20.ts:23](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/interfaces/IERC20.ts#L23)

---

### serialize

▸ **serialize**(): `StaticArray`<`u8`\>

#### Returns

`StaticArray`<`u8`\>

#### Implementation of

Serializable.serialize

#### Defined in

[assembly/interfaces/IERC20.ts:29](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/interfaces/IERC20.ts#L29)

---

### symbol

▸ **symbol**(): `string`

Returns the symbol of the token.

#### Returns

`string`

token symbol.

#### Inherited from

TokenWrapper.symbol

#### Defined in

[assembly/interfaces/TokenWrapper.ts:53](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/interfaces/TokenWrapper.ts#L53)

---

### totalSupply

▸ **totalSupply**(): `u64`

Returns the total token supply.

The number of tokens that were initially minted.

#### Returns

`u64`

number of minted tokens.

#### Inherited from

TokenWrapper.totalSupply

#### Defined in

[assembly/interfaces/TokenWrapper.ts:64](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/interfaces/TokenWrapper.ts#L64)

---

### transfer

▸ **transfer**(`toAccount`, `nbTokens`): `void`

Transfers tokens from the caller's account to the recipient's account.

#### Parameters

| Name        | Type      |
| :---------- | :-------- |
| `toAccount` | `Address` |
| `nbTokens`  | `u64`     |

#### Returns

`void`

#### Inherited from

TokenWrapper.transfer

#### Defined in

[assembly/interfaces/TokenWrapper.ts:83](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/interfaces/TokenWrapper.ts#L83)

---

### transferFrom

▸ **transferFrom**(`ownerAccount`, `recipientAccount`, `nbTokens`): `void`

Transfers token ownership from the owner's account to
the recipient's account using the spender's allowance.

This function can only be called by the spender.
This function is atomic:

-   both allowance and transfer are executed if possible;
-   or if allowance or transfer is not possible, both are discarded.

#### Parameters

| Name               | Type      |
| :----------------- | :-------- |
| `ownerAccount`     | `Address` |
| `recipientAccount` | `Address` |
| `nbTokens`         | `u64`     |

#### Returns

`void`

#### Inherited from

TokenWrapper.transferFrom

#### Defined in

[assembly/interfaces/TokenWrapper.ts:136](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/interfaces/TokenWrapper.ts#L136)

---

### version

▸ **version**(): `string`

Returns the version of the smart contract.
This versioning is following the best practices defined in https://semver.org/.

#### Returns

`string`

#### Inherited from

TokenWrapper.version

#### Defined in

[assembly/interfaces/TokenWrapper.ts:36](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/interfaces/TokenWrapper.ts#L36)
