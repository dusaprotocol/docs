# LBPairInformation

## Implements

- `Serializable`

## Table of contents

### Constructors

- [constructor](LBPairInformation.md#constructor)

### Properties

- [binStep](LBPairInformation.md#binstep)
- [createdByOwner](LBPairInformation.md#createdbyowner)
- [ignoredForRouting](LBPairInformation.md#ignoredforrouting)
- [pair](LBPairInformation.md#pair)

### Methods

- [deserialize](LBPairInformation.md#deserialize)
- [serialize](LBPairInformation.md#serialize)

## Constructors

### constructor

• **new LBPairInformation**(`binStep?`, `pair?`, `createdByOwner?`, `ignoredForRouting?`): [`LBPairInformation`](LBPairInformation.md)

#### Parameters

| Name | Type | Default value | Description |
| :------ | :------ | :------ | :------ |
| `binStep` | `u32` | `0` | The bin step of the LBPair |
| `pair` | [`IPair`](../interfaces/IPair.md) | `undefined` | The address of the LBPair |
| `createdByOwner` | `bool` | `false` | Whether the LBPair was created by the owner or the factory |
| `ignoredForRouting` | `bool` | `false` | Whether the LBPair is ignored for routing or not. An ignored pair will not be explored during routes finding |

#### Returns

[`LBPairInformation`](LBPairInformation.md)

#### Defined in

[assembly/structs/LBPairInformation.ts:13](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/structs/LBPairInformation.ts#L13)

## Properties

### binStep

• **binStep**: `u32` = `0`

The bin step of the LBPair

#### Defined in

[assembly/structs/LBPairInformation.ts:14](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/structs/LBPairInformation.ts#L14)

___

### createdByOwner

• **createdByOwner**: `bool` = `false`

Whether the LBPair was created by the owner or the factory

#### Defined in

[assembly/structs/LBPairInformation.ts:16](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/structs/LBPairInformation.ts#L16)

___

### ignoredForRouting

• **ignoredForRouting**: `bool` = `false`

Whether the LBPair is ignored for routing or not. An ignored pair will not be explored during routes finding

#### Defined in

[assembly/structs/LBPairInformation.ts:17](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/structs/LBPairInformation.ts#L17)

___

### pair

• **pair**: [`IPair`](../interfaces/IPair.md)

The address of the LBPair

#### Defined in

[assembly/structs/LBPairInformation.ts:15](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/structs/LBPairInformation.ts#L15)

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

[assembly/structs/LBPairInformation.ts:33](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/structs/LBPairInformation.ts#L33)

___

### serialize

▸ **serialize**(): `StaticArray`<`u8`\>

#### Returns

`StaticArray`<`u8`\>

#### Implementation of

Serializable.serialize

#### Defined in

[assembly/structs/LBPairInformation.ts:24](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/structs/LBPairInformation.ts#L24)
