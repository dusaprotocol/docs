SafeMathU8

# Class: SafeMathU8

## Table of contents

### Constructors

-   [constructor](SafeMathU8.md#constructor)

### Methods

-   [add](SafeMathU8.md#add)
-   [sub](SafeMathU8.md#sub)

## Constructors

### constructor

• **new SafeMathU8**()

## Methods

### add

▸ `Static` **add**(`a`, `b`): `u8`

#### Parameters

| Name | Type |
| :--- | :--- |
| `a`  | `u8` |
| `b`  | `u8` |

#### Returns

`u8`

Returns the addition of two unsigned integers,
reverting on overflow.

#### Defined in

[assembly/libraries/SafeMath.ts:83](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/libraries/SafeMath.ts#L83)

---

### sub

▸ `Static` **sub**(`a`, `b`): `u8`

#### Parameters

| Name | Type |
| :--- | :--- |
| `a`  | `u8` |
| `b`  | `u8` |

#### Returns

`u8`

Returns the integer division of two unsigned integers. Reverts with custom message on
division by zero. The result is rounded towards zero.

#### Defined in

[assembly/libraries/SafeMath.ts:97](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/libraries/SafeMath.ts#L97)
