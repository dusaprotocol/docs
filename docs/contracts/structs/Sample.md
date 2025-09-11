# Sample

## Implements

- `Serializable`

## Table of contents

### Constructors

- [constructor](Sample.md#constructor)

### Properties

- [cumulativeBinCrossed](Sample.md#cumulativebincrossed)
- [cumulativeId](Sample.md#cumulativeid)
- [cumulativeVolatilityAccumulated](Sample.md#cumulativevolatilityaccumulated)
- [timestamp](Sample.md#timestamp)

### Methods

- [deserialize](Sample.md#deserialize)
- [serialize](Sample.md#serialize)
- [update](Sample.md#update)

## Constructors

### constructor

• **new Sample**(`timestamp?`, `cumulativeId?`, `cumulativeVolatilityAccumulated?`, `cumulativeBinCrossed?`): [`Sample`](Sample.md)

#### Parameters

| Name | Type | Default value | Description |
| :------ | :------ | :------ | :------ |
| `timestamp` | `u64` | `0` | The timestamp of the sample |
| `cumulativeId` | `u256` | `ZERO` | The weighted average cumulative id |
| `cumulativeVolatilityAccumulated` | `u256` | `ZERO` | The weighted average cumulative volatility accumulated |
| `cumulativeBinCrossed` | `u256` | `ZERO` | The weighted average cumulative bin crossed |

#### Returns

[`Sample`](Sample.md)

#### Defined in

[assembly/structs/Sample.ts:14](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/structs/Sample.ts#L14)

## Properties

### cumulativeBinCrossed

• **cumulativeBinCrossed**: `u256` = `ZERO`

The weighted average cumulative bin crossed

#### Defined in

[assembly/structs/Sample.ts:18](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/structs/Sample.ts#L18)

___

### cumulativeId

• **cumulativeId**: `u256` = `ZERO`

The weighted average cumulative id

#### Defined in

[assembly/structs/Sample.ts:16](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/structs/Sample.ts#L16)

___

### cumulativeVolatilityAccumulated

• **cumulativeVolatilityAccumulated**: `u256` = `ZERO`

The weighted average cumulative volatility accumulated

#### Defined in

[assembly/structs/Sample.ts:17](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/structs/Sample.ts#L17)

___

### timestamp

• **timestamp**: `u64` = `0`

The timestamp of the sample

#### Defined in

[assembly/structs/Sample.ts:15](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/structs/Sample.ts#L15)

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

[assembly/structs/Sample.ts:67](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/structs/Sample.ts#L67)

___

### serialize

▸ **serialize**(): `StaticArray`<`u8`\>

#### Returns

`StaticArray`<`u8`\>

#### Implementation of

Serializable.serialize

#### Defined in

[assembly/structs/Sample.ts:58](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/structs/Sample.ts#L58)

___

### update

▸ **update**(`_activeId`, `_volatilityAccumulated`, `_binCrossed`): [`Sample`](Sample.md)

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `_activeId` | `u64` | The active index of the pair during the latest swap |
| `_volatilityAccumulated` | `u64` | The volatility accumulated of the pair during the latest swap |
| `_binCrossed` | `u64` | The bin crossed during the latest swap |

#### Returns

[`Sample`](Sample.md)

Sample The updated sample

**`Notice`**

Function to update a sample

#### Defined in

[assembly/structs/Sample.ts:28](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/structs/Sample.ts#L28)
