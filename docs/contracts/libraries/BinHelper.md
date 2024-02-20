# BinHelper

## Table of contents

### Constructors

- [constructor](BinHelper.md#constructor)

### Methods

- [\_getBPValue](BinHelper.md#_getbpvalue)
- [getPriceFromId](BinHelper.md#getpricefromid)
- [power](BinHelper.md#power)

## Constructors

### constructor

• **new BinHelper**(): [`BinHelper`](BinHelper.md)

#### Returns

[`BinHelper`](BinHelper.md)

## Methods

### \_getBPValue

▸ **_getBPValue**(`_binStep`): `u256`

Returns the (1 + bp) value as a 128.128-decimal fixed-point number

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `_binStep` | `u64` | The bp value in [1; 100] (referring to 0.01% to 1%) |

#### Returns

`u256`

The (1+bp) value as a 128.128-decimal fixed-point number

#### Defined in

[assembly/libraries/BinHelper.ts:37](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/libraries/BinHelper.ts#L37)

___

### getPriceFromId

▸ **getPriceFromId**(`id`, `binStep`): `u256`

Returns the price corresponding to the given ID, as a 128.128-binary fixed-point number

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `id` | `u64` | the id |
| `binStep` | `u64` | the bin step |

#### Returns

`u256`

The price corresponding to this id, as a 128.128-binary fixed-point number

#### Defined in

[assembly/libraries/BinHelper.ts:25](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/libraries/BinHelper.ts#L25)

___

### power

▸ **power**(`x`, `y`): `u256`

Returns the value of x^y. It calculates `1 / x^abs(y)` if x is bigger than 2^128.
 At the end of the operations, we invert the result if needed.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `x` | `u256` | The unsigned 128.128-binary fixed-point number for which to calculate the power |
| `y` | `i64` | A relative number without any decimals, needs to be between ]-2^20; 2^20[ |

#### Returns

`u256`

The result of `x^y`

#### Defined in

[assembly/libraries/BinHelper.ts:59](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/libraries/BinHelper.ts#L59)
