[@dusalabs/core](../README.md) / [Exports](../modules.md) / BinHelper

# Class: BinHelper

## Table of contents

### Constructors

- [constructor](BinHelper.md#constructor)

### Methods

- [\_getBPValue](BinHelper.md#_getbpvalue)
- [getPriceFromId](BinHelper.md#getpricefromid)
- [log2](BinHelper.md#log2)
- [power](BinHelper.md#power)

## Constructors

### constructor

• **new BinHelper**()

## Methods

### \_getBPValue

▸ `Static` **_getBPValue**(`_binStep`): `u64`

Returns the (1 + bp) value as a 32.32-decimal fixed-point number

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `_binStep` | `u64` | The bp value in [1; 100] (referring to 0.01% to 1%) |

#### Returns

`u64`

The (1+bp) value as a 32.32-decimal fixed-point number

#### Defined in

[assembly/libraries/BinHelper.ts:49](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/libraries/BinHelper.ts#L49)

___

### getPriceFromId

▸ `Static` **getPriceFromId**(`id`, `binStep`): `u128`

Returns the price corresponding to the given ID, as a 32.32-binary fixed-point number

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `id` | `u64` | the id |
| `binStep` | `u64` | the bin step |

#### Returns

`u128`

The price corresponding to this id, as a 32.32-binary fixed-point number

#### Defined in

[assembly/libraries/BinHelper.ts:37](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/libraries/BinHelper.ts#L37)

___

### log2

▸ `Static` **log2**(`x`): `i128`

#### Parameters

| Name | Type |
| :------ | :------ |
| `x` | `u128` |

#### Returns

`i128`

#### Defined in

[assembly/libraries/BinHelper.ts:185](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/libraries/BinHelper.ts#L185)

___

### power

▸ `Static` **power**(`x`, `y`): `u128`

Returns the value of x^y. It calculates `1 / x^abs(y)` if x is bigger than 2^32.
 At the end of the operations, we invert the result if needed.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `x` | `u64` | The unsigned 32.32-binary fixed-point number for which to calculate the power |
| `y` | `i64` | A relative number without any decimals, needs to be between ]-2^20; 2^20[ |

#### Returns

`u128`

The result of `x^y`

#### Defined in

[assembly/libraries/BinHelper.ts:62](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/libraries/BinHelper.ts#L62)
