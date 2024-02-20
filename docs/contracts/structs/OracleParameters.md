# OracleParameters

## Implements

- `Serializable`

## Table of contents

### Constructors

- [constructor](OracleParameters.md#constructor)

### Properties

- [max](OracleParameters.md#max)
- [min](OracleParameters.md#min)
- [oracleActiveSize](OracleParameters.md#oracleactivesize)
- [oracleId](OracleParameters.md#oracleid)
- [oracleLastTimestamp](OracleParameters.md#oraclelasttimestamp)
- [oracleSampleLifetime](OracleParameters.md#oraclesamplelifetime)
- [oracleSize](OracleParameters.md#oraclesize)

### Methods

- [deserialize](OracleParameters.md#deserialize)
- [serialize](OracleParameters.md#serialize)

## Constructors

### constructor

• **new OracleParameters**(`oracleSampleLifetime?`, `oracleSize?`, `oracleActiveSize?`, `oracleLastTimestamp?`, `oracleId?`, `min?`, `max?`): [`OracleParameters`](OracleParameters.md)

#### Parameters

| Name | Type | Default value | Description |
| :------ | :------ | :------ | :------ |
| `oracleSampleLifetime` | `u32` | `0` | The lifetime of a sample, it accumulates information for up to this timestamp |
| `oracleSize` | `u32` | `0` | The size of the oracle (last ids can be empty) |
| `oracleActiveSize` | `u32` | `0` | The active size of the oracle (no empty data) |
| `oracleLastTimestamp` | `u64` | `0` | The timestamp of the creation of the oracle's latest sample |
| `oracleId` | `u32` | `0` | The index of the oracle's latest sample |
| `min` | `u32` | `0` | The min delta time of two samples |
| `max` | `u32` | `0` | The safe max delta time of two samples |

#### Returns

[`OracleParameters`](OracleParameters.md)

#### Defined in

[assembly/structs/OracleParameters.ts:14](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/structs/OracleParameters.ts#L14)

## Properties

### max

• **max**: `u32` = `0`

The safe max delta time of two samples

#### Defined in

[assembly/structs/OracleParameters.ts:21](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/structs/OracleParameters.ts#L21)

___

### min

• **min**: `u32` = `0`

The min delta time of two samples

#### Defined in

[assembly/structs/OracleParameters.ts:20](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/structs/OracleParameters.ts#L20)

___

### oracleActiveSize

• **oracleActiveSize**: `u32` = `0`

The active size of the oracle (no empty data)

#### Defined in

[assembly/structs/OracleParameters.ts:17](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/structs/OracleParameters.ts#L17)

___

### oracleId

• **oracleId**: `u32` = `0`

The index of the oracle's latest sample

#### Defined in

[assembly/structs/OracleParameters.ts:19](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/structs/OracleParameters.ts#L19)

___

### oracleLastTimestamp

• **oracleLastTimestamp**: `u64` = `0`

The timestamp of the creation of the oracle's latest sample

#### Defined in

[assembly/structs/OracleParameters.ts:18](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/structs/OracleParameters.ts#L18)

___

### oracleSampleLifetime

• **oracleSampleLifetime**: `u32` = `0`

The lifetime of a sample, it accumulates information for up to this timestamp

#### Defined in

[assembly/structs/OracleParameters.ts:15](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/structs/OracleParameters.ts#L15)

___

### oracleSize

• **oracleSize**: `u32` = `0`

The size of the oracle (last ids can be empty)

#### Defined in

[assembly/structs/OracleParameters.ts:16](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/structs/OracleParameters.ts#L16)

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

[assembly/structs/OracleParameters.ts:40](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/structs/OracleParameters.ts#L40)

___

### serialize

▸ **serialize**(): `StaticArray`<`u8`\>

#### Returns

`StaticArray`<`u8`\>

#### Implementation of

Serializable.serialize

#### Defined in

[assembly/structs/OracleParameters.ts:28](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/structs/OracleParameters.ts#L28)
