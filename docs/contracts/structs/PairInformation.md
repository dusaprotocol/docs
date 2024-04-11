# PairInformation

## Implements

- `Serializable`

## Table of contents

### Constructors

- [constructor](PairInformation.md#constructor)

### Properties

- [activeId](PairInformation.md#activeid)
- [feesX](PairInformation.md#feesx)
- [feesY](PairInformation.md#feesy)
- [oracleActiveSize](PairInformation.md#oracleactivesize)
- [oracleId](PairInformation.md#oracleid)
- [oracleLastTimestamp](PairInformation.md#oraclelasttimestamp)
- [oracleSampleLifetime](PairInformation.md#oraclesamplelifetime)
- [oracleSize](PairInformation.md#oraclesize)
- [reserveX](PairInformation.md#reservex)
- [reserveY](PairInformation.md#reservey)

### Methods

- [deserialize](PairInformation.md#deserialize)
- [serialize](PairInformation.md#serialize)

## Constructors

### constructor

• **new PairInformation**(`activeId?`, `reserveX?`, `reserveY?`, `feesX?`, `feesY?`, `oracleSampleLifetime?`, `oracleSize?`, `oracleActiveSize?`, `oracleLastTimestamp?`, `oracleId?`): [`PairInformation`](PairInformation.md)

#### Parameters

| Name | Type | Default value | Description |
| :------ | :------ | :------ | :------ |
| `activeId` | `u32` | `0` | The current id used for swaps, this is also linked with the price |
| `reserveX` | `u256` | `u256.Zero` | The sum of amounts of tokenX across all bins |
| `reserveY` | `u256` | `u256.Zero` | The sum of amounts of tokenY across all bins |
| `feesX` | [`FeesDistribution`](FeesDistribution.md) | `undefined` | The current amount of fees to distribute in tokenX (total, protocol) |
| `feesY` | [`FeesDistribution`](FeesDistribution.md) | `undefined` | The current amount of fees to distribute in tokenY (total, protocol) |
| `oracleSampleLifetime` | `u32` | `0` | - |
| `oracleSize` | `u32` | `0` | - |
| `oracleActiveSize` | `u32` | `0` | - |
| `oracleLastTimestamp` | `u64` | `0` | - |
| `oracleId` | `u32` | `0` | - |

#### Returns

[`PairInformation`](PairInformation.md)

#### Defined in

[assembly/structs/PairInformation.ts:14](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/structs/PairInformation.ts#L14)

## Properties

### activeId

• **activeId**: `u32` = `0`

The current id used for swaps, this is also linked with the price

#### Defined in

[assembly/structs/PairInformation.ts:15](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/structs/PairInformation.ts#L15)

___

### feesX

• **feesX**: [`FeesDistribution`](FeesDistribution.md)

The current amount of fees to distribute in tokenX (total, protocol)

#### Defined in

[assembly/structs/PairInformation.ts:18](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/structs/PairInformation.ts#L18)

___

### feesY

• **feesY**: [`FeesDistribution`](FeesDistribution.md)

The current amount of fees to distribute in tokenY (total, protocol)

#### Defined in

[assembly/structs/PairInformation.ts:19](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/structs/PairInformation.ts#L19)

___

### oracleActiveSize

• **oracleActiveSize**: `u32` = `0`

#### Defined in

[assembly/structs/PairInformation.ts:22](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/structs/PairInformation.ts#L22)

___

### oracleId

• **oracleId**: `u32` = `0`

#### Defined in

[assembly/structs/PairInformation.ts:24](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/structs/PairInformation.ts#L24)

___

### oracleLastTimestamp

• **oracleLastTimestamp**: `u64` = `0`

#### Defined in

[assembly/structs/PairInformation.ts:23](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/structs/PairInformation.ts#L23)

___

### oracleSampleLifetime

• **oracleSampleLifetime**: `u32` = `0`

#### Defined in

[assembly/structs/PairInformation.ts:20](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/structs/PairInformation.ts#L20)

___

### oracleSize

• **oracleSize**: `u32` = `0`

#### Defined in

[assembly/structs/PairInformation.ts:21](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/structs/PairInformation.ts#L21)

___

### reserveX

• **reserveX**: `u256` = `u256.Zero`

The sum of amounts of tokenX across all bins

#### Defined in

[assembly/structs/PairInformation.ts:16](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/structs/PairInformation.ts#L16)

___

### reserveY

• **reserveY**: `u256` = `u256.Zero`

The sum of amounts of tokenY across all bins

#### Defined in

[assembly/structs/PairInformation.ts:17](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/structs/PairInformation.ts#L17)

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

[assembly/structs/PairInformation.ts:46](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/structs/PairInformation.ts#L46)

___

### serialize

▸ **serialize**(): `StaticArray`<`u8`\>

#### Returns

`StaticArray`<`u8`\>

#### Implementation of

Serializable.serialize

#### Defined in

[assembly/structs/PairInformation.ts:31](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/structs/PairInformation.ts#L31)
