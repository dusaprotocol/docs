[@dusalabs/core](../README.md) / [Exports](../modules.md) / IFactory

# Class: IFactory

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

[assembly/interfaces/IFactory.ts:15](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/interfaces/IFactory.ts#L15)

## Properties

### \_origin

• **\_origin**: `Address`

#### Defined in

[assembly/interfaces/IFactory.ts:8](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/interfaces/IFactory.ts#L8)

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

[assembly/interfaces/IFactory.ts:85](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/interfaces/IFactory.ts#L85)

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

[assembly/interfaces/IFactory.ts:57](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/interfaces/IFactory.ts#L57)

___

### getAllLBPairs

▸ **getAllLBPairs**(`_tokenX`, `_tokenY`): [`LBPairInformation`](LBPairInformation.md)[]

#### Parameters

| Name | Type |
| :------ | :------ |
| `_tokenX` | `Address` |
| `_tokenY` | `Address` |

#### Returns

[`LBPairInformation`](LBPairInformation.md)[]

#### Defined in

[assembly/interfaces/IFactory.ts:36](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/interfaces/IFactory.ts#L36)

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

[assembly/interfaces/IFactory.ts:90](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/interfaces/IFactory.ts#L90)

___

### getLBPairInformation

▸ **getLBPairInformation**(`_tokenA`, `_tokenB`, `_binStep`): [`LBPairInformation`](LBPairInformation.md)

#### Parameters

| Name | Type |
| :------ | :------ |
| `_tokenA` | `Address` |
| `_tokenB` | `Address` |
| `_binStep` | `u64` |

#### Returns

[`LBPairInformation`](LBPairInformation.md)

#### Defined in

[assembly/interfaces/IFactory.ts:30](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/interfaces/IFactory.ts#L30)

___

### getOwner

▸ **getOwner**(): `Address`

#### Returns

`Address`

#### Defined in

[assembly/interfaces/IFactory.ts:96](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/interfaces/IFactory.ts#L96)

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

[assembly/interfaces/IFactory.ts:25](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/interfaces/IFactory.ts#L25)

___

### setPreset

▸ **setPreset**(`_binStep`, `_baseFactor`, `_filterPeriod`, `_decayPeriod`, `_reductionFactor`, `_variableFeeControl`, `_protocolShare`, `_maxVolatilityAccumulated`): `void`

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

#### Returns

`void`

#### Defined in

[assembly/interfaces/IFactory.ts:63](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/interfaces/IFactory.ts#L63)
