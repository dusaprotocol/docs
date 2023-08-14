# FeeParameters

## Implements

- `Serializable`

## Table of contents

### Constructors

- [constructor](FeeParameters.md#constructor)

### Properties

- [baseFactor](FeeParameters.md#basefactor)
- [binStep](FeeParameters.md#binstep)
- [decayPeriod](FeeParameters.md#decayperiod)
- [filterPeriod](FeeParameters.md#filterperiod)
- [indexRef](FeeParameters.md#indexref)
- [maxVolatilityAccumulated](FeeParameters.md#maxvolatilityaccumulated)
- [protocolShare](FeeParameters.md#protocolshare)
- [reductionFactor](FeeParameters.md#reductionfactor)
- [time](FeeParameters.md#time)
- [variableFeeControl](FeeParameters.md#variablefeecontrol)
- [volatilityAccumulated](FeeParameters.md#volatilityaccumulated)
- [volatilityReference](FeeParameters.md#volatilityreference)

### Methods

- [deserialize](FeeParameters.md#deserialize)
- [getBaseFee](FeeParameters.md#getbasefee)
- [getFeeAmount](FeeParameters.md#getfeeamount)
- [getFeeAmountDistribution](FeeParameters.md#getfeeamountdistribution)
- [getFeeAmountForC](FeeParameters.md#getfeeamountforc)
- [getFeeAmountFrom](FeeParameters.md#getfeeamountfrom)
- [getTotalFee](FeeParameters.md#gettotalfee)
- [getVariableFee](FeeParameters.md#getvariablefee)
- [serialize](FeeParameters.md#serialize)
- [updateVariableFeeParameters](FeeParameters.md#updatevariablefeeparameters)
- [updateVolatilityAccumulated](FeeParameters.md#updatevolatilityaccumulated)

## Constructors

### constructor

• **new FeeParameters**(`binStep?`, `baseFactor?`, `filterPeriod?`, `decayPeriod?`, `reductionFactor?`, `variableFeeControl?`, `protocolShare?`, `maxVolatilityAccumulated?`, `volatilityAccumulated?`, `volatilityReference?`, `indexRef?`, `time?`)

#### Parameters

| Name | Type | Default value | Description |
| :------ | :------ | :------ | :------ |
| `binStep` | `u32` | `0` | The bin step |
| `baseFactor` | `u32` | `0` | The base factor |
| `filterPeriod` | `u32` | `0` | The filter period, where the fees stays constant |
| `decayPeriod` | `u32` | `0` | The decay period, where the fees are halved |
| `reductionFactor` | `u32` | `0` | The reduction factor, used to calculate the reduction of the accumulator |
| `variableFeeControl` | `u32` | `0` | The variable fee control, used to control the variable fee, can be 0 to disable them |
| `protocolShare` | `u32` | `0` | The share of fees sent to protocol |
| `maxVolatilityAccumulated` | `u32` | `0` | The max value of volatility accumulated |
| `volatilityAccumulated` | `u32` | `0` | The value of volatility accumulated |
| `volatilityReference` | `u32` | `0` | The value of volatility reference |
| `indexRef` | `u32` | `0` | The index reference |
| `time` | `u64` | `undefined` | The last time the accumulator was called |

#### Defined in

[assembly/structs/FeeParameters.ts:23](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/structs/FeeParameters.ts#L23)

## Properties

### baseFactor

• **baseFactor**: `u32` = `0`

The base factor

#### Defined in

[assembly/structs/FeeParameters.ts:25](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/structs/FeeParameters.ts#L25)

___

### binStep

• **binStep**: `u32` = `0`

The bin step

#### Defined in

[assembly/structs/FeeParameters.ts:24](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/structs/FeeParameters.ts#L24)

___

### decayPeriod

• **decayPeriod**: `u32` = `0`

The decay period, where the fees are halved

#### Defined in

[assembly/structs/FeeParameters.ts:27](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/structs/FeeParameters.ts#L27)

___

### filterPeriod

• **filterPeriod**: `u32` = `0`

The filter period, where the fees stays constant

#### Defined in

[assembly/structs/FeeParameters.ts:26](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/structs/FeeParameters.ts#L26)

___

### indexRef

• **indexRef**: `u32` = `0`

The index reference

#### Defined in

[assembly/structs/FeeParameters.ts:34](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/structs/FeeParameters.ts#L34)

___

### maxVolatilityAccumulated

• **maxVolatilityAccumulated**: `u32` = `0`

The max value of volatility accumulated

#### Defined in

[assembly/structs/FeeParameters.ts:31](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/structs/FeeParameters.ts#L31)

___

### protocolShare

• **protocolShare**: `u32` = `0`

The share of fees sent to protocol

#### Defined in

[assembly/structs/FeeParameters.ts:30](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/structs/FeeParameters.ts#L30)

___

### reductionFactor

• **reductionFactor**: `u32` = `0`

The reduction factor, used to calculate the reduction of the accumulator

#### Defined in

[assembly/structs/FeeParameters.ts:28](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/structs/FeeParameters.ts#L28)

___

### time

• **time**: `u64`

The last time the accumulator was called

#### Defined in

[assembly/structs/FeeParameters.ts:35](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/structs/FeeParameters.ts#L35)

___

### variableFeeControl

• **variableFeeControl**: `u32` = `0`

The variable fee control, used to control the variable fee, can be 0 to disable them

#### Defined in

[assembly/structs/FeeParameters.ts:29](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/structs/FeeParameters.ts#L29)

___

### volatilityAccumulated

• **volatilityAccumulated**: `u32` = `0`

The value of volatility accumulated

#### Defined in

[assembly/structs/FeeParameters.ts:32](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/structs/FeeParameters.ts#L32)

___

### volatilityReference

• **volatilityReference**: `u32` = `0`

The value of volatility reference

#### Defined in

[assembly/structs/FeeParameters.ts:33](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/structs/FeeParameters.ts#L33)

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

[assembly/structs/FeeParameters.ts:164](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/structs/FeeParameters.ts#L164)

___

### getBaseFee

▸ **getBaseFee**(): `u64`

#### Returns

`u64`

#### Defined in

[assembly/structs/FeeParameters.ts:87](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/structs/FeeParameters.ts#L87)

___

### getFeeAmount

▸ **getFeeAmount**(`_amount`): `u64`

#### Parameters

| Name | Type |
| :------ | :------ |
| `_amount` | `u64` |

#### Returns

`u64`

#### Defined in

[assembly/structs/FeeParameters.ts:52](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/structs/FeeParameters.ts#L52)

___

### getFeeAmountDistribution

▸ **getFeeAmountDistribution**(`_fees`): [`FeesDistribution`](FeesDistribution.md)

Return the fees distribution added to an amount

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `_fees` | `u64` | The fee amount |

#### Returns

[`FeesDistribution`](FeesDistribution.md)

#### Defined in

[assembly/structs/FeeParameters.ts:44](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/structs/FeeParameters.ts#L44)

___

### getFeeAmountForC

▸ **getFeeAmountForC**(`_amountWithFees`): `u64`

#### Parameters

| Name | Type |
| :------ | :------ |
| `_amountWithFees` | `u128` |

#### Returns

`u64`

#### Defined in

[assembly/structs/FeeParameters.ts:65](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/structs/FeeParameters.ts#L65)

___

### getFeeAmountFrom

▸ **getFeeAmountFrom**(`_amountWithFees`): `u64`

#### Parameters

| Name | Type |
| :------ | :------ |
| `_amountWithFees` | `u64` |

#### Returns

`u64`

#### Defined in

[assembly/structs/FeeParameters.ts:61](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/structs/FeeParameters.ts#L61)

___

### getTotalFee

▸ **getTotalFee**(): `u64`

#### Returns

`u64`

#### Defined in

[assembly/structs/FeeParameters.ts:82](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/structs/FeeParameters.ts#L82)

___

### getVariableFee

▸ **getVariableFee**(): `u64`

#### Returns

`u64`

#### Defined in

[assembly/structs/FeeParameters.ts:91](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/structs/FeeParameters.ts#L91)

___

### serialize

▸ **serialize**(): `StaticArray`<`u8`\>

#### Returns

`StaticArray`<`u8`\>

#### Implementation of

Serializable.serialize

#### Defined in

[assembly/structs/FeeParameters.ts:147](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/structs/FeeParameters.ts#L147)

___

### updateVariableFeeParameters

▸ **updateVariableFeeParameters**(`_activeId`): `void`

Update the value of the volatility accumulated

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `_activeId` | `u64` | The current active id |

#### Returns

`void`

#### Defined in

[assembly/structs/FeeParameters.ts:107](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/structs/FeeParameters.ts#L107)

___

### updateVolatilityAccumulated

▸ **updateVolatilityAccumulated**(`_activeId`): `void`

Update the volatility accumulated

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `_activeId` | `u64` | The current active id |

#### Returns

`void`

#### Defined in

[assembly/structs/FeeParameters.ts:131](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/structs/FeeParameters.ts#L131)
