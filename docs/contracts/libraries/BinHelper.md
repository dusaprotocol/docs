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

▸ **\_getBPValue**(`bp`): `u256`

Returns the (1 + bp) value as a 128.128-decimal fixed-point number

#### Parameters

| Name | Type  | Description                                         |
| :--- | :---- | :-------------------------------------------------- |
| `bp` | `u16` | The bp value in [1; 100] (referring to 0.01% to 1%) |

#### Returns

`u256`

The (1+bp) value as a 128.128-decimal fixed-point number

#### Defined in

[assembly/libraries/BinHelper.ts:50](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/BinHelper.ts#L50)

---

### getPriceFromId

▸ **getPriceFromId**(`id`, `binStep`): `u256`

Returns the price corresponding to the given ID, as a 128.128-binary fixed-point number

#### Parameters

| Name      | Type  | Description  |
| :-------- | :---- | :----------- |
| `id`      | `u64` | the id       |
| `binStep` | `u16` | the bin step |

#### Returns

`u256`

The price corresponding to this id, as a 128.128-binary fixed-point number

#### Defined in

[assembly/libraries/BinHelper.ts:39](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/BinHelper.ts#L39)

---

### power

▸ **power**(`x`, `y`): `u256`

Returns the value of x^y. It calculates `1 / x^abs(y)` if x is bigger than 2^128.
At the end of the operations, we invert the result if needed.

#### Parameters

| Name | Type   | Description                                                                     |
| :--- | :----- | :------------------------------------------------------------------------------ |
| `x`  | `u256` | The unsigned 128.128-binary fixed-point number for which to calculate the power |
| `y`  | `i64`  | A relative number without any decimals, needs to be between ]-2^20; 2^20[       |

#### Returns

`u256`

The result of `x^y`

#### Defined in

[assembly/libraries/BinHelper.ts:63](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/BinHelper.ts#L63)
