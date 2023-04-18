[@dusalabs/core](../README.md) / [Exports](../modules.md) / FeesDistribution

# Class: FeesDistribution

## Implements

- `Serializable`

## Table of contents

### Constructors

- [constructor](FeesDistribution.md#constructor)

### Properties

- [protocol](FeesDistribution.md#protocol)
- [total](FeesDistribution.md#total)

### Methods

- [deserialize](FeesDistribution.md#deserialize)
- [getTokenPerShare](FeesDistribution.md#gettokenpershare)
- [serialize](FeesDistribution.md#serialize)

## Constructors

### constructor

• **new FeesDistribution**(`total?`, `protocol?`)

#### Parameters

| Name | Type | Default value | Description |
| :------ | :------ | :------ | :------ |
| `total` | `u64` | `0` | The total amount of fees |
| `protocol` | `u64` | `0` | The amount of fees reserved for protocol |

#### Defined in

[assembly/structs/FeesDistribution.ts:10](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/structs/FeesDistribution.ts#L10)

## Properties

### protocol

• **protocol**: `u64` = `0`

The amount of fees reserved for protocol

#### Defined in

[assembly/structs/FeesDistribution.ts:10](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/structs/FeesDistribution.ts#L10)

___

### total

• **total**: `u64` = `0`

The total amount of fees

#### Defined in

[assembly/structs/FeesDistribution.ts:10](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/structs/FeesDistribution.ts#L10)

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

[assembly/structs/FeesDistribution.ts:34](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/structs/FeesDistribution.ts#L34)

___

### getTokenPerShare

▸ **getTokenPerShare**(`totalSupply`): `u64`

Calculate the tokenPerShare when fees are added

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `totalSupply` | `u64` | the total supply of a specific bin |

#### Returns

`u64`

#### Defined in

[assembly/structs/FeesDistribution.ts:17](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/structs/FeesDistribution.ts#L17)

___

### serialize

▸ **serialize**(): `StaticArray`<`u8`\>

#### Returns

`StaticArray`<`u8`\>

#### Implementation of

Serializable.serialize

#### Defined in

[assembly/structs/FeesDistribution.ts:30](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/structs/FeesDistribution.ts#L30)
