# FeesDistribution

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

• **new FeesDistribution**(`total?`, `protocol?`): [`FeesDistribution`](FeesDistribution.md)

#### Parameters

| Name | Type | Default value | Description |
| :------ | :------ | :------ | :------ |
| `total` | `u256` | `u256.Zero` | The total amount of fees |
| `protocol` | `u256` | `u256.Zero` | The amount of fees reserved for protocol |

#### Returns

[`FeesDistribution`](FeesDistribution.md)

#### Defined in

[assembly/structs/FeesDistribution.ts:11](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/structs/FeesDistribution.ts#L11)

## Properties

### protocol

• **protocol**: `u256` = `u256.Zero`

The amount of fees reserved for protocol

#### Defined in

[assembly/structs/FeesDistribution.ts:13](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/structs/FeesDistribution.ts#L13)

___

### total

• **total**: `u256` = `u256.Zero`

The total amount of fees

#### Defined in

[assembly/structs/FeesDistribution.ts:12](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/structs/FeesDistribution.ts#L12)

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

[assembly/structs/FeesDistribution.ts:37](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/structs/FeesDistribution.ts#L37)

___

### getTokenPerShare

▸ **getTokenPerShare**(`totalSupply`): `u256`

Calculate the tokenPerShare when fees are added

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `totalSupply` | `u256` | the total supply of a specific bin |

#### Returns

`u256`

#### Defined in

[assembly/structs/FeesDistribution.ts:21](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/structs/FeesDistribution.ts#L21)

___

### serialize

▸ **serialize**(): `StaticArray`<`u8`\>

#### Returns

`StaticArray`<`u8`\>

#### Implementation of

Serializable.serialize

#### Defined in

[assembly/structs/FeesDistribution.ts:33](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/structs/FeesDistribution.ts#L33)
