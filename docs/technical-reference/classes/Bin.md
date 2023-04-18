[@dusalabs/core](../README.md) / [Exports](../modules.md) / Bin

# Class: Bin

## Implements

- `Serializable`

## Table of contents

### Constructors

- [constructor](Bin.md#constructor)

### Properties

- [accTokenXPerShare](Bin.md#acctokenxpershare)
- [accTokenYPerShare](Bin.md#acctokenypershare)
- [reserveX](Bin.md#reservex)
- [reserveY](Bin.md#reservey)

### Methods

- [deserialize](Bin.md#deserialize)
- [serialize](Bin.md#serialize)
- [updateFees](Bin.md#updatefees)
- [updateReserves](Bin.md#updatereserves)

## Constructors

### constructor

• **new Bin**(`reserveX?`, `reserveY?`, `accTokenXPerShare?`, `accTokenYPerShare?`)

#### Parameters

| Name | Type | Default value |
| :------ | :------ | :------ |
| `reserveX` | `u64` | `0` |
| `reserveY` | `u64` | `0` |
| `accTokenXPerShare` | `u64` | `0` |
| `accTokenYPerShare` | `u64` | `0` |

#### Defined in

[assembly/structs/Bin.ts:7](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/structs/Bin.ts#L7)

## Properties

### accTokenXPerShare

• **accTokenXPerShare**: `u64` = `0`

#### Defined in

[assembly/structs/Bin.ts:10](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/structs/Bin.ts#L10)

___

### accTokenYPerShare

• **accTokenYPerShare**: `u64` = `0`

#### Defined in

[assembly/structs/Bin.ts:11](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/structs/Bin.ts#L11)

___

### reserveX

• **reserveX**: `u64` = `0`

#### Defined in

[assembly/structs/Bin.ts:8](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/structs/Bin.ts#L8)

___

### reserveY

• **reserveY**: `u64` = `0`

#### Defined in

[assembly/structs/Bin.ts:9](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/structs/Bin.ts#L9)

## Methods

### deserialize

▸ **deserialize**(`data`, `offset`): `Result`<`i32`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `data` | `StaticArray`<`u8`\> |
| `offset` | `i32` |

#### Returns

`Result`<`i32`\>

#### Implementation of

Serializable.deserialize

#### Defined in

[assembly/structs/Bin.ts:72](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/structs/Bin.ts#L72)

___

### serialize

▸ **serialize**(): `StaticArray`<`u8`\>

#### Returns

`StaticArray`<`u8`\>

#### Implementation of

Serializable.serialize

#### Defined in

[assembly/structs/Bin.ts:63](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/structs/Bin.ts#L63)

___

### updateFees

▸ **updateFees**(`pairFees`, `fees`, `swapForY`, `totalSupply`): `void`

Update the fees of the pair and accumulated token per share of the bin

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `pairFees` | [`FeesDistribution`](FeesDistribution.md) | The current fees of the pair information |
| `fees` | [`FeesDistribution`](FeesDistribution.md) | The fees amounts added to the pairFees |
| `swapForY` | `bool` | whether the token sent was Y (true) or X (false) |
| `totalSupply` | `u64` | The total supply of the token id |

#### Returns

`void`

#### Defined in

[assembly/structs/Bin.ts:22](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/structs/Bin.ts#L22)

___

### updateReserves

▸ **updateReserves**(`pair`, `swapForY`, `amountInToBin`, `amountOutOfBin`): `void`

Update reserves

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `pair` | [`PairInformation`](PairInformation.md) | The pair information |
| `swapForY` | `bool` | whether the token sent was Y (true) or X (false) |
| `amountInToBin` | `u64` | The amount of token that is added to the bin without fees |
| `amountOutOfBin` | `u64` | The amount of token that is removed from the bin |

#### Returns

`void`

#### Defined in

[assembly/structs/Bin.ts:41](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/structs/Bin.ts#L41)
