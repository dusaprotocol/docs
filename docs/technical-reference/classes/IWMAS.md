IWMAS

# Class: IWMAS

## Hierarchy

-   [`IERC20`](IERC20.md)

    ↳ **`IWMAS`**

## Table of contents

### Constructors

-   [constructor](IWMAS.md#constructor)

### Properties

-   [\_origin](IWMAS.md#_origin)

### Methods

-   [allowance](IWMAS.md#allowance)
-   [balanceOf](IWMAS.md#balanceof)
-   [burn](IWMAS.md#burn)
-   [decreaseAllowance](IWMAS.md#decreaseallowance)
-   [deposit](IWMAS.md#deposit)
-   [deserialize](IWMAS.md#deserialize)
-   [equals](IWMAS.md#equals)
-   [increaseAllowance](IWMAS.md#increaseallowance)
-   [init](IWMAS.md#init)
-   [mint](IWMAS.md#mint)
-   [name](IWMAS.md#name)
-   [notEqual](IWMAS.md#notequal)
-   [received](IWMAS.md#received)
-   [serialize](IWMAS.md#serialize)
-   [symbol](IWMAS.md#symbol)
-   [totalSupply](IWMAS.md#totalsupply)
-   [transfer](IWMAS.md#transfer)
-   [transferFrom](IWMAS.md#transferfrom)
-   [version](IWMAS.md#version)
-   [withdraw](IWMAS.md#withdraw)

## Constructors

### constructor

• **new IWMAS**(`origin?`)

#### Parameters

| Name     | Type      |
| :------- | :-------- |
| `origin` | `Address` |

#### Inherited from

[IERC20](IERC20.md).[constructor](IERC20.md#constructor)

#### Defined in

[assembly/interfaces/IERC20.ts:6](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/interfaces/IERC20.ts#L6)

## Properties

### \_origin

• **\_origin**: `Address`

#### Inherited from

[IERC20](IERC20.md).[\_origin](IERC20.md#_origin)

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

[IERC20](IERC20.md).[allowance](IERC20.md#allowance)

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

[IERC20](IERC20.md).[balanceOf](IERC20.md#balanceof)

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

[IERC20](IERC20.md).[burn](IERC20.md#burn)

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

[IERC20](IERC20.md).[decreaseAllowance](IERC20.md#decreaseallowance)

#### Defined in

[assembly/interfaces/TokenWrapper.ts:119](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/interfaces/TokenWrapper.ts#L119)

---

### deposit

▸ **deposit**(`value`): `void`

#### Parameters

| Name    | Type  |
| :------ | :---- |
| `value` | `u64` |

#### Returns

`void`

#### Defined in

[assembly/interfaces/IWMAS.ts:10](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/interfaces/IWMAS.ts#L10)

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

#### Inherited from

[IERC20](IERC20.md).[deserialize](IERC20.md#deserialize)

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

#### Inherited from

[IERC20](IERC20.md).[equals](IERC20.md#equals)

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

[IERC20](IERC20.md).[increaseAllowance](IERC20.md#increaseallowance)

#### Defined in

[assembly/interfaces/TokenWrapper.ts:106](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/interfaces/TokenWrapper.ts#L106)

---

### init

▸ **init**(`name?`, `symbol?`, `decimals?`, `supply?`): `void`

#### Parameters

| Name       | Type     | Default value     |
| :--------- | :------- | :---------------- |
| `name`     | `string` | `"Wrapped Massa"` |
| `symbol`   | `string` | `"WMAS"`          |
| `decimals` | `u8`     | `9`               |
| `supply`   | `u64`    | `0`               |

#### Returns

`void`

#### Overrides

[IERC20](IERC20.md).[init](IERC20.md#init)

#### Defined in

[assembly/interfaces/IWMAS.ts:6](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/interfaces/IWMAS.ts#L6)

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

[IERC20](IERC20.md).[mint](IERC20.md#mint)

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

[IERC20](IERC20.md).[name](IERC20.md#name)

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

#### Inherited from

[IERC20](IERC20.md).[notEqual](IERC20.md#notequal)

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

#### Inherited from

[IERC20](IERC20.md).[received](IERC20.md#received)

#### Defined in

[assembly/interfaces/IERC20.ts:23](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/interfaces/IERC20.ts#L23)

---

### serialize

▸ **serialize**(): `StaticArray`<`u8`\>

#### Returns

`StaticArray`<`u8`\>

#### Inherited from

[IERC20](IERC20.md).[serialize](IERC20.md#serialize)

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

[IERC20](IERC20.md).[symbol](IERC20.md#symbol)

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

[IERC20](IERC20.md).[totalSupply](IERC20.md#totalsupply)

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

[IERC20](IERC20.md).[transfer](IERC20.md#transfer)

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

[IERC20](IERC20.md).[transferFrom](IERC20.md#transferfrom)

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

[IERC20](IERC20.md).[version](IERC20.md#version)

#### Defined in

[assembly/interfaces/TokenWrapper.ts:36](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/interfaces/TokenWrapper.ts#L36)

---

### withdraw

▸ **withdraw**(`value`): `void`

#### Parameters

| Name    | Type  |
| :------ | :---- |
| `value` | `u64` |

#### Returns

`void`

#### Defined in

[assembly/interfaces/IWMAS.ts:14](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/interfaces/IWMAS.ts#L14)
