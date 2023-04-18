[@dusalabs/core](../README.md) / [Exports](../modules.md) / SafeMath

# Class: SafeMath

## Table of contents

### Constructors

- [constructor](SafeMath.md#constructor)

### Methods

- [add](SafeMath.md#add)
- [div](SafeMath.md#div)
- [mod](SafeMath.md#mod)
- [mul](SafeMath.md#mul)
- [sub](SafeMath.md#sub)

## Constructors

### constructor

• **new SafeMath**()

## Methods

### add

▸ `Static` **add**(`a`, `b`): `u64`

#### Parameters

| Name | Type |
| :------ | :------ |
| `a` | `u64` |
| `b` | `u64` |

#### Returns

`u64`

Returns the addition of two unsigned integers,
reverting on overflow.

#### Defined in

[assembly/libraries/SafeMath.ts:9](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/libraries/SafeMath.ts#L9)

___

### div

▸ `Static` **div**(`a`, `b`): `u64`

#### Parameters

| Name | Type |
| :------ | :------ |
| `a` | `u64` |
| `b` | `u64` |

#### Returns

`u64`

Returns the integer division of two unsigned integers. Reverts on
division by zero. The result is rounded towards zero.

#### Defined in

[assembly/libraries/SafeMath.ts:55](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/libraries/SafeMath.ts#L55)

___

### mod

▸ `Static` **mod**(`a`, `b`): `u64`

#### Parameters

| Name | Type |
| :------ | :------ |
| `a` | `u64` |
| `b` | `u64` |

#### Returns

`u64`

Returns the remainder of dividing two unsigned integers. (unsigned integer modulo),
Reverts with custom message when dividing by zero.

#### Defined in

[assembly/libraries/SafeMath.ts:69](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/libraries/SafeMath.ts#L69)

___

### mul

▸ `Static` **mul**(`a`, `b`): `u64`

#### Parameters

| Name | Type |
| :------ | :------ |
| `a` | `u64` |
| `b` | `u64` |

#### Returns

`u64`

Returns the multiplication of two unsigned integers, reverting on
overflow.

#### Defined in

[assembly/libraries/SafeMath.ts:37](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/libraries/SafeMath.ts#L37)

___

### sub

▸ `Static` **sub**(`a`, `b`): `u64`

#### Parameters

| Name | Type |
| :------ | :------ |
| `a` | `u64` |
| `b` | `u64` |

#### Returns

`u64`

Returns the integer division of two unsigned integers. Reverts with custom message on
division by zero. The result is rounded towards zero.

#### Defined in

[assembly/libraries/SafeMath.ts:23](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/libraries/SafeMath.ts#L23)
