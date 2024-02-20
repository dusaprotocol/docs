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

• **new FeeParameters**(`binStep?`, `baseFactor?`, `filterPeriod?`, `decayPeriod?`, `reductionFactor?`, `variableFeeControl?`, `protocolShare?`, `maxVolatilityAccumulated?`, `volatilityAccumulated?`, `volatilityReference?`, `indexRef?`, `time?`): [`FeeParameters`](FeeParameters.md)

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

#### Returns

[`FeeParameters`](FeeParameters.md)

#### Defined in

[assembly/structs/FeeParameters.ts:28](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/structs/FeeParameters.ts#L28)

## Properties

### baseFactor

• **baseFactor**: `u32` = `0`

The base factor

#### Defined in

[assembly/structs/FeeParameters.ts:30](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/structs/FeeParameters.ts#L30)

___

### binStep

• **binStep**: `u32` = `0`

The bin step

#### Defined in

[assembly/structs/FeeParameters.ts:29](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/structs/FeeParameters.ts#L29)

___

### decayPeriod

• **decayPeriod**: `u32` = `0`

The decay period, where the fees are halved

#### Defined in

[assembly/structs/FeeParameters.ts:32](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/structs/FeeParameters.ts#L32)

___

### filterPeriod

• **filterPeriod**: `u32` = `0`

The filter period, where the fees stays constant

#### Defined in

[assembly/structs/FeeParameters.ts:31](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/structs/FeeParameters.ts#L31)

___

### indexRef

• **indexRef**: `u32` = `0`

The index reference

#### Defined in

[assembly/structs/FeeParameters.ts:39](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/structs/FeeParameters.ts#L39)

___

### maxVolatilityAccumulated

• **maxVolatilityAccumulated**: `u32` = `0`

The max value of volatility accumulated

#### Defined in

[assembly/structs/FeeParameters.ts:36](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/structs/FeeParameters.ts#L36)

___

### protocolShare

• **protocolShare**: `u32` = `0`

The share of fees sent to protocol

#### Defined in

[assembly/structs/FeeParameters.ts:35](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/structs/FeeParameters.ts#L35)

___

### reductionFactor

• **reductionFactor**: `u32` = `0`

The reduction factor, used to calculate the reduction of the accumulator

#### Defined in

[assembly/structs/FeeParameters.ts:33](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/structs/FeeParameters.ts#L33)

___

### time

• **time**: `u64`

The last time the accumulator was called

#### Defined in

[assembly/structs/FeeParameters.ts:40](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/structs/FeeParameters.ts#L40)

___

### variableFeeControl

• **variableFeeControl**: `u32` = `0`

The variable fee control, used to control the variable fee, can be 0 to disable them

#### Defined in

[assembly/structs/FeeParameters.ts:34](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/structs/FeeParameters.ts#L34)

___

### volatilityAccumulated

• **volatilityAccumulated**: `u32` = `0`

The value of volatility accumulated

#### Defined in

[assembly/structs/FeeParameters.ts:37](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/structs/FeeParameters.ts#L37)

___

### volatilityReference

• **volatilityReference**: `u32` = `0`

The value of volatility reference

#### Defined in

[assembly/structs/FeeParameters.ts:38](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/structs/FeeParameters.ts#L38)

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

[assembly/structs/FeeParameters.ts:213](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/structs/FeeParameters.ts#L213)

___

### getBaseFee

▸ **getBaseFee**(): `u256`

#### Returns

`u256`

**`Notice`**

Returns the base fee added to a swap, with 18 decimals

#### Defined in

[assembly/structs/FeeParameters.ts:124](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/structs/FeeParameters.ts#L124)

___

### getFeeAmount

▸ **getFeeAmount**(`_amount`): `u256`

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `_amount` | `u256` | The amount of token sent |

#### Returns

`u256`

The fee amount to add to the amount

**`Notice`**

Return the fees to add to an amount

**`Dev`**

Rounds amount up, follows `amountWithFees = amount + getFeeAmount(amount)`

#### Defined in

[assembly/structs/FeeParameters.ts:66](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/structs/FeeParameters.ts#L66)

___

### getFeeAmountDistribution

▸ **getFeeAmountDistribution**(`_fees`): [`FeesDistribution`](FeesDistribution.md)

Return the fees distribution added to an amount

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `_fees` | `u256` | The fee amount |

#### Returns

[`FeesDistribution`](FeesDistribution.md)

#### Defined in

[assembly/structs/FeeParameters.ts:49](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/structs/FeeParameters.ts#L49)

___

### getFeeAmountForC

▸ **getFeeAmountForC**(`_amountWithFees`): `u256`

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `_amountWithFees` | `u256` | The amount of token sent |

#### Returns

`u256`

The fee amount

**`Notice`**

Return the fees added when an user adds liquidity and change the ratio in the active bin

**`Dev`**

Rounds amount up

#### Defined in

[assembly/structs/FeeParameters.ts:97](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/structs/FeeParameters.ts#L97)

___

### getFeeAmountFrom

▸ **getFeeAmountFrom**(`_amountWithFees`): `u256`

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `_amountWithFees` | `u256` | The amount of token sent |

#### Returns

`u256`

The fee amount from the amount sent

**`Notice`**

Return the amount of fees from an amount

**`Dev`**

Rounds amount up, follows `amount = amountWithFees - getFeeAmountFrom(amountWithFees)`

#### Defined in

[assembly/structs/FeeParameters.ts:81](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/structs/FeeParameters.ts#L81)

___

### getTotalFee

▸ **getTotalFee**(): `u256`

#### Returns

`u256`

The total fee, with 18 decimals

**`Notice`**

Return the total fee, i.e. baseFee + variableFee

#### Defined in

[assembly/structs/FeeParameters.ts:116](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/structs/FeeParameters.ts#L116)

___

### getVariableFee

▸ **getVariableFee**(): `u256`

#### Returns

`u256`

**`Notice`**

Returns the variable fee added to a swap, with 18 decimals

#### Defined in

[assembly/structs/FeeParameters.ts:134](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/structs/FeeParameters.ts#L134)

___

### serialize

▸ **serialize**(): `StaticArray`<`u8`\>

#### Returns

`StaticArray`<`u8`\>

#### Implementation of

Serializable.serialize

#### Defined in

[assembly/structs/FeeParameters.ts:196](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/structs/FeeParameters.ts#L196)

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

[assembly/structs/FeeParameters.ts:156](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/structs/FeeParameters.ts#L156)

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

[assembly/structs/FeeParameters.ts:180](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/structs/FeeParameters.ts#L180)
