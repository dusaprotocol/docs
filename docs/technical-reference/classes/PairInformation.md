[@dusalabs/core](../README.md) / [Exports](../modules.md) / PairInformation

# Class: PairInformation

## Implements

- `Serializable`

## Table of contents

### Constructors

- [constructor](PairInformation.md#constructor)

### Properties

- [activeId](PairInformation.md#activeid)
- [feesX](PairInformation.md#feesx)
- [feesY](PairInformation.md#feesy)
- [reserveX](PairInformation.md#reservex)
- [reserveY](PairInformation.md#reservey)

### Methods

- [deserialize](PairInformation.md#deserialize)
- [serialize](PairInformation.md#serialize)

## Constructors

### constructor

• **new PairInformation**(`activeId?`, `reserveX?`, `reserveY?`, `feesX?`, `feesY?`)

#### Parameters

| Name | Type | Default value | Description |
| :------ | :------ | :------ | :------ |
| `activeId` | `u32` | `0` | The current id used for swaps, this is also linked with the price |
| `reserveX` | `u64` | `0` | The sum of amounts of tokenX across all bins |
| `reserveY` | `u64` | `0` | The sum of amounts of tokenY across all bins |
| `feesX` | [`FeesDistribution`](FeesDistribution.md) | `undefined` | The current amount of fees to distribute in tokenX (total, protocol) |
| `feesY` | [`FeesDistribution`](FeesDistribution.md) | `undefined` | The current amount of fees to distribute in tokenY (total, protocol) |

#### Defined in

[assembly/structs/PairInformation.ts:13](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/structs/PairInformation.ts#L13)

## Properties

### activeId

• **activeId**: `u32` = `0`

The current id used for swaps, this is also linked with the price

#### Defined in

[assembly/structs/PairInformation.ts:14](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/structs/PairInformation.ts#L14)

___

### feesX

• **feesX**: [`FeesDistribution`](FeesDistribution.md)

The current amount of fees to distribute in tokenX (total, protocol)

#### Defined in

[assembly/structs/PairInformation.ts:17](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/structs/PairInformation.ts#L17)

___

### feesY

• **feesY**: [`FeesDistribution`](FeesDistribution.md)

The current amount of fees to distribute in tokenY (total, protocol)

#### Defined in

[assembly/structs/PairInformation.ts:18](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/structs/PairInformation.ts#L18)

___

### reserveX

• **reserveX**: `u64` = `0`

The sum of amounts of tokenX across all bins

#### Defined in

[assembly/structs/PairInformation.ts:15](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/structs/PairInformation.ts#L15)

___

### reserveY

• **reserveY**: `u64` = `0`

The sum of amounts of tokenY across all bins

#### Defined in

[assembly/structs/PairInformation.ts:16](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/structs/PairInformation.ts#L16)

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

[assembly/structs/PairInformation.ts:35](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/structs/PairInformation.ts#L35)

___

### serialize

▸ **serialize**(): `StaticArray`<`u8`\>

#### Returns

`StaticArray`<`u8`\>

#### Implementation of

Serializable.serialize

#### Defined in

[assembly/structs/PairInformation.ts:25](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/structs/PairInformation.ts#L25)
