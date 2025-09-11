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

[assembly/libraries/SafeMath.ts:12](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/SafeMath.ts#L12)

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

[assembly/libraries/SafeMath.ts:58](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/SafeMath.ts#L58)

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

[assembly/libraries/SafeMath.ts:72](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/SafeMath.ts#L72)

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

[assembly/libraries/SafeMath.ts:40](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/SafeMath.ts#L40)

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

[assembly/libraries/SafeMath.ts:26](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/SafeMath.ts#L26)
