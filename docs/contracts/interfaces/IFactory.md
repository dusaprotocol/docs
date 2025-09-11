# IFactory

## Table of contents

### Constructors

- [constructor](IFactory.md#constructor)

### Properties

- [\_origin](IFactory.md#_origin)

### Methods

- [acceptOwnership](IFactory.md#acceptownership)
- [addQuoteAsset](IFactory.md#addquoteasset)
- [createLBPair](IFactory.md#createlbpair)
- [forceDecay](IFactory.md#forcedecay)
- [getAllLBPairs](IFactory.md#getalllbpairs)
- [getAvailableLBPairBinSteps](IFactory.md#getavailablelbpairbinsteps)
- [getLBPairInformation](IFactory.md#getlbpairinformation)
- [getOwner](IFactory.md#getowner)
- [getPreset](IFactory.md#getpreset)
- [init](IFactory.md#init)
- [proposeNewOwner](IFactory.md#proposenewowner)
- [removeLBHooksOnPair](IFactory.md#removelbhooksonpair)
- [removePreset](IFactory.md#removepreset)
- [removeQuoteAsset](IFactory.md#removequoteasset)
- [setFactoryLockedState](IFactory.md#setfactorylockedstate)
- [setFeeRecipient](IFactory.md#setfeerecipient)
- [setFeesParametersOnPair](IFactory.md#setfeesparametersonpair)
- [setFlashLoanFee](IFactory.md#setflashloanfee)
- [setLBHooksParametersOnPair](IFactory.md#setlbhooksparametersonpair)
- [setLBPairIgnored](IFactory.md#setlbpairignored)
- [setPreset](IFactory.md#setpreset)

## Constructors

### constructor

• **new IFactory**(`at`): [`IFactory`](IFactory.md)

Wraps a smart contract exposing standard token FFI.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `at` | `Address` | Address of the smart contract. |

#### Returns

[`IFactory`](IFactory.md)

#### Defined in

[assembly/interfaces/IFactory.ts:28](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/interfaces/IFactory.ts#L28)

## Properties

### \_origin

• **\_origin**: `Address`

#### Defined in

[assembly/interfaces/IFactory.ts:21](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/interfaces/IFactory.ts#L21)

## Methods

### acceptOwnership

▸ **acceptOwnership**(): `void`

#### Returns

`void`

#### Defined in

[assembly/interfaces/IFactory.ts:237](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/interfaces/IFactory.ts#L237)

___

### addQuoteAsset

▸ **addQuoteAsset**(`_asset`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `_asset` | `Address` |

#### Returns

`void`

#### Defined in

[assembly/interfaces/IFactory.ts:221](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/interfaces/IFactory.ts#L221)

___

### createLBPair

▸ **createLBPair**(`_tokenA`, `_tokenB`, `_activeId`, `_binStep`, `_masToSend`): `Address`

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `_tokenA` | `Address` | address of the first token |
| `_tokenB` | `Address` | address of the second token |
| `_activeId` | `u32` | active id disired |
| `_binStep` | `u32` | bin step disired |
| `_masToSend` | `u64` | Massa to send for storage |

#### Returns

`Address`

the address of the new LBPair

**`Dev`**

Create a new LBPair

#### Defined in

[assembly/interfaces/IFactory.ts:99](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/interfaces/IFactory.ts#L99)

___

### forceDecay

▸ **forceDecay**(`_pair`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `_pair` | `Address` |

#### Returns

`void`

#### Defined in

[assembly/interfaces/IFactory.ts:229](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/interfaces/IFactory.ts#L229)

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

[assembly/interfaces/IFactory.ts:60](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/interfaces/IFactory.ts#L60)

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

[assembly/interfaces/IFactory.ts:241](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/interfaces/IFactory.ts#L241)

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

[assembly/interfaces/IFactory.ts:50](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/interfaces/IFactory.ts#L50)

___

### getOwner

▸ **getOwner**(): `Address`

#### Returns

`Address`

#### Defined in

[assembly/interfaces/IFactory.ts:247](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/interfaces/IFactory.ts#L247)

___

### getPreset

▸ **getPreset**(`binstep`): [`Preset`](../structs/Preset.md)

#### Parameters

| Name | Type |
| :------ | :------ |
| `binstep` | `u32` |

#### Returns

[`Preset`](../structs/Preset.md)

#### Defined in

[assembly/interfaces/IFactory.ts:251](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/interfaces/IFactory.ts#L251)

___

### init

▸ **init**(`_feeRecipient`, `_quoteAssets`, `_flashLoanFee?`): `void`

Initialize the factory. This function must be called before any other function.

#### Parameters

| Name | Type | Default value | Description |
| :------ | :------ | :------ | :------ |
| `_feeRecipient` | `Address` | `undefined` | The address of the fee recipient |
| `_quoteAssets` | `Address`[] | `undefined` | - |
| `_flashLoanFee` | `u256` | `ZERO` | The value of the fee for flash loan |

#### Returns

`void`

#### Defined in

[assembly/interfaces/IFactory.ts:38](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/interfaces/IFactory.ts#L38)

___

### proposeNewOwner

▸ **proposeNewOwner**(`_newOwner`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `_newOwner` | `Address` |

#### Returns

`void`

#### Defined in

[assembly/interfaces/IFactory.ts:233](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/interfaces/IFactory.ts#L233)

___

### removeLBHooksOnPair

▸ **removeLBHooksOnPair**(`_tokenA`, `_tokenB`, `_binStep`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `_tokenA` | `Address` |
| `_tokenB` | `Address` |
| `_binStep` | `u32` |

#### Returns

`void`

#### Defined in

[assembly/interfaces/IFactory.ts:199](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/interfaces/IFactory.ts#L199)

___

### removePreset

▸ **removePreset**(`_binStep`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `_binStep` | `u32` |

#### Returns

`void`

#### Defined in

[assembly/interfaces/IFactory.ts:153](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/interfaces/IFactory.ts#L153)

___

### removeQuoteAsset

▸ **removeQuoteAsset**(`_asset`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `_asset` | `Address` |

#### Returns

`void`

#### Defined in

[assembly/interfaces/IFactory.ts:225](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/interfaces/IFactory.ts#L225)

___

### setFactoryLockedState

▸ **setFactoryLockedState**(`_factoryLockedState`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `_factoryLockedState` | `bool` |

#### Returns

`void`

#### Defined in

[assembly/interfaces/IFactory.ts:212](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/interfaces/IFactory.ts#L212)

___

### setFeeRecipient

▸ **setFeeRecipient**(`_feeRecipient`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `_feeRecipient` | `Address` |

#### Returns

`void`

#### Defined in

[assembly/interfaces/IFactory.ts:204](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/interfaces/IFactory.ts#L204)

___

### setFeesParametersOnPair

▸ **setFeesParametersOnPair**(`_tokenA`, `_tokenB`, `_binStep`, `_baseFactor`, `_filterPeriod`, `_decayPeriod`, `_reductionFactor`, `_variableFeeControl`, `_protocolShare`, `_maxVolatilityAccumulated`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `_tokenA` | `Address` |
| `_tokenB` | `Address` |
| `_binStep` | `u32` |
| `_baseFactor` | `u32` |
| `_filterPeriod` | `u32` |
| `_decayPeriod` | `u32` |
| `_reductionFactor` | `u32` |
| `_variableFeeControl` | `u32` |
| `_protocolShare` | `u32` |
| `_maxVolatilityAccumulated` | `u32` |

#### Returns

`void`

#### Defined in

[assembly/interfaces/IFactory.ts:157](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/interfaces/IFactory.ts#L157)

___

### setFlashLoanFee

▸ **setFlashLoanFee**(`_flashLoanFee`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `_flashLoanFee` | `u64` |

#### Returns

`void`

#### Defined in

[assembly/interfaces/IFactory.ts:208](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/interfaces/IFactory.ts#L208)

___

### setLBHooksParametersOnPair

▸ **setLBHooksParametersOnPair**(`_tokenA`, `_tokenB`, `_binStep`, `_hooksParameters`, `_onHooksSetData`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `_tokenA` | `Address` |
| `_tokenB` | `Address` |
| `_binStep` | `u32` |
| `_hooksParameters` | [`HooksParameters`](../structs/HooksParameters) |
| `_onHooksSetData` | `StaticArray`<`u8`\> |

#### Returns

`void`

#### Defined in

[assembly/interfaces/IFactory.ts:183](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/interfaces/IFactory.ts#L183)

___

### setLBPairIgnored

▸ **setLBPairIgnored**(`_tokenA`, `_tokenB`, `_binStep`, `_ignored`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `_tokenA` | `Address` |
| `_tokenB` | `Address` |
| `_binStep` | `u32` |
| `_ignored` | `bool` |

#### Returns

`void`

#### Defined in

[assembly/interfaces/IFactory.ts:115](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/interfaces/IFactory.ts#L115)

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

[assembly/interfaces/IFactory.ts:129](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/interfaces/IFactory.ts#L129)
