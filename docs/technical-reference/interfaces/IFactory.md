# IFactory

## Table of contents

### Constructors

- [constructor](IFactory.md#constructor)

### Properties

- [\_origin](IFactory.md#_origin)

### Methods

- [addQuoteAsset](IFactory.md#addquoteasset)
- [createLBPair](IFactory.md#createlbpair)
- [getAllLBPairs](IFactory.md#getalllbpairs)
- [getAvailableLBPairBinSteps](IFactory.md#getavailablelbpairbinsteps)
- [getLBPairInformation](IFactory.md#getlbpairinformation)
- [getOwner](IFactory.md#getowner)
- [init](IFactory.md#init)
- [setPreset](IFactory.md#setpreset)

## Constructors

### constructor

• **new IFactory**(`at`)

Wraps a smart contract exposing standard token FFI.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `at` | `Address` | Address of the smart contract. |

#### Defined in

[assembly/interfaces/IFactory.ts:19](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/interfaces/IFactory.ts#L19)

## Properties

### \_origin

• **\_origin**: `Address`

#### Defined in

[assembly/interfaces/IFactory.ts:12](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/interfaces/IFactory.ts#L12)

## Methods

### addQuoteAsset

▸ **addQuoteAsset**(`_asset`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `_asset` | `Address` |

#### Returns

`void`

#### Defined in

[assembly/interfaces/IFactory.ts:111](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/interfaces/IFactory.ts#L111)

___

### createLBPair

▸ **createLBPair**(`_tokenA`, `_tokenB`, `_activeId`, `_binStep`): `Address`

#### Parameters

| Name | Type |
| :------ | :------ |
| `_tokenA` | `Address` |
| `_tokenB` | `Address` |
| `_activeId` | `u32` |
| `_binStep` | `u32` |

#### Returns

`Address`

#### Defined in

[assembly/interfaces/IFactory.ts:72](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/interfaces/IFactory.ts#L72)

___

### getAllLBPairs

▸ **getAllLBPairs**(`_tokenX`, `_tokenY`): [`LBPairInformation`](../structs/LBPairInformation.md)[]

#### Parameters

| Name | Type |
| :------ | :------ |
| `_tokenX` | `Address` |
| `_tokenY` | `Address` |

#### Returns

[`LBPairInformation`](../structs/LBPairInformation.md)[]

#### Defined in

[assembly/interfaces/IFactory.ts:44](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/interfaces/IFactory.ts#L44)

___

### getAvailableLBPairBinSteps

▸ **getAvailableLBPairBinSteps**(`_tokenA`, `_tokenB`): `u32`[]

#### Parameters

| Name | Type |
| :------ | :------ |
| `_tokenA` | `Address` |
| `_tokenB` | `Address` |

#### Returns

`u32`[]

#### Defined in

[assembly/interfaces/IFactory.ts:116](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/interfaces/IFactory.ts#L116)

___

### getLBPairInformation

▸ **getLBPairInformation**(`_tokenA`, `_tokenB`, `_binStep`): [`LBPairInformation`](../structs/LBPairInformation.md)

#### Parameters

| Name | Type |
| :------ | :------ |
| `_tokenA` | `Address` |
| `_tokenB` | `Address` |
| `_binStep` | `u64` |

#### Returns

[`LBPairInformation`](../structs/LBPairInformation.md)

#### Defined in

[assembly/interfaces/IFactory.ts:34](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/interfaces/IFactory.ts#L34)

___

### getOwner

▸ **getOwner**(): `Address`

#### Returns

`Address`

#### Defined in

[assembly/interfaces/IFactory.ts:122](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/interfaces/IFactory.ts#L122)

___

### init

▸ **init**(`_feeRecipient`, `_flashLoanFee?`): `void`

Initialize the factory. This function must be called before any other function.

#### Parameters

| Name | Type | Default value | Description |
| :------ | :------ | :------ | :------ |
| `_feeRecipient` | `Address` | `undefined` | The address of the fee recipient |
| `_flashLoanFee` | `u64` | `0` | The value of the fee for flash loan |

#### Returns

`void`

#### Defined in

[assembly/interfaces/IFactory.ts:29](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/interfaces/IFactory.ts#L29)

___

### setPreset

▸ **setPreset**(`_binStep`, `_baseFactor`, `_filterPeriod`, `_decayPeriod`, `_reductionFactor`, `_variableFeeControl`, `_protocolShare`, `_maxVolatilityAccumulated`, `_sampleLifeTime`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `_binStep` | `u32` |
| `_baseFactor` | `u32` |
| `_filterPeriod` | `u32` |
| `_decayPeriod` | `u32` |
| `_reductionFactor` | `u32` |
| `_variableFeeControl` | `u32` |
| `_protocolShare` | `u32` |
| `_maxVolatilityAccumulated` | `u32` |
| `_sampleLifeTime` | `u32` |

#### Returns

`void`

#### Defined in

[assembly/interfaces/IFactory.ts:87](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/interfaces/IFactory.ts#L87)
