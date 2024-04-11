# SafeMathU8

## Table of contents

### Constructors

- [constructor](SafeMathU8.md#constructor)

### Methods

- [add](SafeMathU8.md#add)
- [sub](SafeMathU8.md#sub)

## Constructors

### constructor

• **new SafeMathU8**(): [`SafeMathU8`](SafeMathU8.md)

#### Returns

[`SafeMathU8`](SafeMathU8.md)

## Methods

### add

▸ **add**(`a`, `b`): `u8`

#### Parameters

| Name | Type |
| :------ | :------ |
| `a` | `u8` |
| `b` | `u8` |

#### Returns

`u8`

Returns the addition of two unsigned integers,
reverting on overflow.

#### Defined in

[assembly/libraries/SafeMath.ts:85](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/libraries/SafeMath.ts#L85)

___

### sub

▸ **sub**(`a`, `b`): `u8`

#### Parameters

| Name | Type |
| :------ | :------ |
| `a` | `u8` |
| `b` | `u8` |

#### Returns

`u8`

Returns the integer division of two unsigned integers. Reverts with custom message on
division by zero. The result is rounded towards zero.

#### Defined in

[assembly/libraries/SafeMath.ts:99](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/libraries/SafeMath.ts#L99)
