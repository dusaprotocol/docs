# SafeMath256

## Table of contents

### Constructors

- [constructor](SafeMath256.md#constructor)

### Methods

- [add](SafeMath256.md#add)
- [div](SafeMath256.md#div)
- [mod](SafeMath256.md#mod)
- [mul](SafeMath256.md#mul)
- [sub](SafeMath256.md#sub)

## Constructors

### constructor

• **new SafeMath256**(): [`SafeMath256`](SafeMath256.md)

#### Returns

[`SafeMath256`](SafeMath256.md)

## Methods

### add

▸ **add**(`a`, `b`): `u256`

#### Parameters

| Name | Type |
| :------ | :------ |
| `a` | `u256` |
| `b` | `u256` |

#### Returns

`u256`

Returns the addition of two unsigned integers,
reverting on overflow.

#### Defined in

[assembly/libraries/SafeMath.ts:115](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/libraries/SafeMath.ts#L115)

___

### div

▸ **div**(`a`, `b`): `u256`

#### Parameters

| Name | Type |
| :------ | :------ |
| `a` | `u256` |
| `b` | `u256` |

#### Returns

`u256`

Returns the integer division of two unsigned integers. Reverts on
division by zero. The result is rounded towards zero.

#### Defined in

[assembly/libraries/SafeMath.ts:161](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/libraries/SafeMath.ts#L161)

___

### mod

▸ **mod**(`a`, `b`): `u256`

#### Parameters

| Name | Type |
| :------ | :------ |
| `a` | `u256` |
| `b` | `u256` |

#### Returns

`u256`

Returns the remainder of dividing two unsigned integers. (unsigned integer modulo),
Reverts with custom message when dividing by zero.

#### Defined in

[assembly/libraries/SafeMath.ts:175](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/libraries/SafeMath.ts#L175)

___

### mul

▸ **mul**(`a`, `b`): `u256`

#### Parameters

| Name | Type |
| :------ | :------ |
| `a` | `u256` |
| `b` | `u256` |

#### Returns

`u256`

Returns the multiplication of two unsigned integers, reverting on
overflow.

#### Defined in

[assembly/libraries/SafeMath.ts:143](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/libraries/SafeMath.ts#L143)

___

### sub

▸ **sub**(`a`, `b`): `u256`

#### Parameters

| Name | Type |
| :------ | :------ |
| `a` | `u256` |
| `b` | `u256` |

#### Returns

`u256`

Returns the integer division of two unsigned integers. Reverts with custom message on
division by zero. The result is rounded towards zero.

#### Defined in

[assembly/libraries/SafeMath.ts:129](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/libraries/SafeMath.ts#L129)
