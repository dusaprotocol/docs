# SafeMath

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

• **new SafeMath**(): [`SafeMath`](SafeMath.md)

#### Returns

[`SafeMath`](SafeMath.md)

## Methods

### add

▸ **add**(`a`, `b`): `u64`

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

[assembly/libraries/SafeMath.ts:11](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/libraries/SafeMath.ts#L11)

___

### div

▸ **div**(`a`, `b`): `u64`

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

[assembly/libraries/SafeMath.ts:57](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/libraries/SafeMath.ts#L57)

___

### mod

▸ **mod**(`a`, `b`): `u64`

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

[assembly/libraries/SafeMath.ts:71](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/libraries/SafeMath.ts#L71)

___

### mul

▸ **mul**(`a`, `b`): `u64`

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

[assembly/libraries/SafeMath.ts:39](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/libraries/SafeMath.ts#L39)

___

### sub

▸ **sub**(`a`, `b`): `u64`

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

[assembly/libraries/SafeMath.ts:25](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/libraries/SafeMath.ts#L25)
