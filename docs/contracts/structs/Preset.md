# Preset

## Implements

- `Serializable`

## Table of contents

### Constructors

- [constructor](Preset.md#constructor)

### Properties

- [baseFactor](Preset.md#basefactor)
- [binStep](Preset.md#binstep)
- [decayPeriod](Preset.md#decayperiod)
- [filterPeriod](Preset.md#filterperiod)
- [maxVolatilityAccumulated](Preset.md#maxvolatilityaccumulated)
- [protocolShare](Preset.md#protocolshare)
- [reductionFactor](Preset.md#reductionfactor)
- [sampleLifetime](Preset.md#samplelifetime)
- [variableFeeControl](Preset.md#variablefeecontrol)

### Methods

- [deserialize](Preset.md#deserialize)
- [serialize](Preset.md#serialize)

## Constructors

### constructor

• **new Preset**(`binStep?`, `baseFactor?`, `filterPeriod?`, `decayPeriod?`, `reductionFactor?`, `variableFeeControl?`, `protocolShare?`, `maxVolatilityAccumulated?`, `sampleLifetime?`): [`Preset`](Preset.md)

#### Parameters

| Name                       | Type  | Default value | Description                                                                          |
| :------------------------- | :---- | :------------ | :----------------------------------------------------------------------------------- |
| `binStep`                  | `u32` | `0`           | The bin step                                                                         |
| `baseFactor`               | `u32` | `0`           | The base factor                                                                      |
| `filterPeriod`             | `u32` | `0`           | The filter period, where the fees stays constant                                     |
| `decayPeriod`              | `u32` | `0`           | The decay period, where the fees are halved                                          |
| `reductionFactor`          | `u32` | `0`           | The reduction factor, used to calculate the reduction of the accumulator             |
| `variableFeeControl`       | `u32` | `0`           | The variable fee control, used to control the variable fee, can be 0 to disable them |
| `protocolShare`            | `u32` | `0`           | The share of fees sent to protocol                                                   |
| `maxVolatilityAccumulated` | `u32` | `0`           | The max value of volatility accumulated                                              |
| `sampleLifetime`           | `u32` | `0`           | The value of volatility accumulated                                                  |

#### Returns

[`Preset`](Preset.md)

#### Defined in

[assembly/structs/Preset.ts:16](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/structs/Preset.ts#L16)

## Properties

### baseFactor

• **baseFactor**: `u32` = `0`

The base factor

#### Defined in

[assembly/structs/Preset.ts:18](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/structs/Preset.ts#L18)

---

### binStep

• **binStep**: `u32` = `0`

The bin step

#### Defined in

[assembly/structs/Preset.ts:17](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/structs/Preset.ts#L17)

---

### decayPeriod

• **decayPeriod**: `u32` = `0`

The decay period, where the fees are halved

#### Defined in

[assembly/structs/Preset.ts:20](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/structs/Preset.ts#L20)

---

### filterPeriod

• **filterPeriod**: `u32` = `0`

The filter period, where the fees stays constant

#### Defined in

[assembly/structs/Preset.ts:19](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/structs/Preset.ts#L19)

---

### maxVolatilityAccumulated

• **maxVolatilityAccumulated**: `u32` = `0`

The max value of volatility accumulated

#### Defined in

[assembly/structs/Preset.ts:24](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/structs/Preset.ts#L24)

---

### protocolShare

• **protocolShare**: `u32` = `0`

The share of fees sent to protocol

#### Defined in

[assembly/structs/Preset.ts:23](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/structs/Preset.ts#L23)

---

### reductionFactor

• **reductionFactor**: `u32` = `0`

The reduction factor, used to calculate the reduction of the accumulator

#### Defined in

[assembly/structs/Preset.ts:21](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/structs/Preset.ts#L21)

---

### sampleLifetime

• **sampleLifetime**: `u32` = `0`

The value of volatility accumulated

#### Defined in

[assembly/structs/Preset.ts:25](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/structs/Preset.ts#L25)

---

### variableFeeControl

• **variableFeeControl**: `u32` = `0`

The variable fee control, used to control the variable fee, can be 0 to disable them

#### Defined in

[assembly/structs/Preset.ts:22](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/structs/Preset.ts#L22)

## Methods

### deserialize

▸ **deserialize**(`data`, `offset`): `Result`<`i32`\>

#### Parameters

| Name     | Type                 |
| :------- | :------------------- |
| `data`   | `StaticArray`<`u8`\> |
| `offset` | `i32`                |

#### Returns

`Result`<`i32`\>

#### Implementation of

Serializable.deserialize

#### Defined in

[assembly/structs/Preset.ts:46](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/structs/Preset.ts#L46)

---

### serialize

▸ **serialize**(): `StaticArray`<`u8`\>

#### Returns

`StaticArray`<`u8`\>

#### Implementation of

Serializable.serialize

#### Defined in

[assembly/structs/Preset.ts:32](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/structs/Preset.ts#L32)
