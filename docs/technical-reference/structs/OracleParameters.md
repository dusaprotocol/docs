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

• **new OracleParameters**(`oracleSampleLifetime`, `oracleSize`, `oracleActiveSize`, `oracleLastTimestamp`, `oracleId`, `min?`, `max?`)

#### Parameters

| Name | Type | Default value |
| :------ | :------ | :------ |
| `oracleSampleLifetime` | `u32` | `undefined` |
| `oracleSize` | `u32` | `undefined` |
| `oracleActiveSize` | `u32` | `undefined` |
| `oracleLastTimestamp` | `u64` | `undefined` |
| `oracleId` | `u32` | `undefined` |
| `min` | `u32` | `0` |
| `max` | `u32` | `0` |

#### Defined in

[assembly/structs/OracleParameters.ts:4](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/structs/OracleParameters.ts#L4)

## Properties

### max

• **max**: `u32` = `0`

#### Defined in

[assembly/structs/OracleParameters.ts:11](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/structs/OracleParameters.ts#L11)

___

### min

• **min**: `u32` = `0`

#### Defined in

[assembly/structs/OracleParameters.ts:10](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/structs/OracleParameters.ts#L10)

___

### oracleActiveSize

• **oracleActiveSize**: `u32`

#### Defined in

[assembly/structs/OracleParameters.ts:7](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/structs/OracleParameters.ts#L7)

___

### oracleId

• **oracleId**: `u32`

#### Defined in

[assembly/structs/OracleParameters.ts:9](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/structs/OracleParameters.ts#L9)

___

### oracleLastTimestamp

• **oracleLastTimestamp**: `u64`

#### Defined in

[assembly/structs/OracleParameters.ts:8](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/structs/OracleParameters.ts#L8)

___

### oracleSampleLifetime

• **oracleSampleLifetime**: `u32`

#### Defined in

[assembly/structs/OracleParameters.ts:5](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/structs/OracleParameters.ts#L5)

___

### oracleSize

• **oracleSize**: `u32`

#### Defined in

[assembly/structs/OracleParameters.ts:6](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/structs/OracleParameters.ts#L6)

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

[assembly/structs/OracleParameters.ts:30](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/structs/OracleParameters.ts#L30)

___

### serialize

▸ **serialize**(): `StaticArray`<`u8`\>

#### Returns

`StaticArray`<`u8`\>

#### Implementation of

Serializable.serialize

#### Defined in

[assembly/structs/OracleParameters.ts:18](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/structs/OracleParameters.ts#L18)
