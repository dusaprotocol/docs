# BinHelper

## Table of contents

### Constructors

- [constructor](BinHelper.md#constructor)

### Methods

- [\_getBPValue](BinHelper.md#_getbpvalue)
- [convert64x64PriceToDecimal](BinHelper.md#convert64x64pricetodecimal)
- [convertDecimalPriceTo64x64](BinHelper.md#convertdecimalpriceto64x64)
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

[assembly/libraries/BinHelper.ts:62](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/libraries/BinHelper.ts#L62)

___

### convert64x64PriceToDecimal

▸ `Static` **convert64x64PriceToDecimal**(`price64x64`): `u64`

#### Parameters

| Name | Type |
| :------ | :------ |
| `price64x64` | `u128` |

#### Returns

`u64`

#### Defined in

[assembly/libraries/BinHelper.ts:274](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/libraries/BinHelper.ts#L274)

___

### convertDecimalPriceTo64x64

▸ `Static` **convertDecimalPriceTo64x64**(`price`): `u128`

#### Parameters

| Name | Type |
| :------ | :------ |
| `price` | `u64` |

#### Returns

`u128`

#### Defined in

[assembly/libraries/BinHelper.ts:264](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/libraries/BinHelper.ts#L264)

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

[assembly/libraries/BinHelper.ts:50](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/libraries/BinHelper.ts#L50)

___

### log2

▸ `Static` **log2**(`x`): `i128`

Calculates the binary logarithm of x.

**`Dev`**

Based on the iterative approximation algorithm.
https://en.wikipedia.org/wiki/Binary_logarithm#Iterative_approximation

Requirements:
- x must be greater than zero.

Caveats:
- The results are not perfectly accurate to the last decimal, due to the lossy precision of the iterative approximation
Also because x is converted to an unsigned 129.127-binary fixed-point number during the operation to optimize the multiplication

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `x` | `u128` | The unsigned 128.128-binary fixed-point number for which to calculate the binary logarithm. |

#### Returns

`i128`

result The binary logarithm as a signed 128.128-binary fixed-point number.

#### Defined in

[assembly/libraries/BinHelper.ts:202](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/libraries/BinHelper.ts#L202)

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

[assembly/libraries/BinHelper.ts:78](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/libraries/BinHelper.ts#L78)
