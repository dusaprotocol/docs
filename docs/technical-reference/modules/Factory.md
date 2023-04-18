[@dusalabs/core](../README.md) / [Exports](../modules.md) / Factory

# Namespace: Factory

## Table of contents

### Functions

- [addQuoteAsset](Factory.md#addquoteasset)
- [constructor](Factory.md#constructor)
- [createLBPair](Factory.md#createlbpair)
- [forceDecay](Factory.md#forcedecay)
- [getAllBinSteps](Factory.md#getallbinsteps)
- [getAvailableLBPairBinSteps](Factory.md#getavailablelbpairbinsteps)
- [getLBPairInformation](Factory.md#getlbpairinformation)
- [removePreset](Factory.md#removepreset)
- [removeQuoteAsset](Factory.md#removequoteasset)
- [setFactoryLockedState](Factory.md#setfactorylockedstate)
- [setFeeRecipient](Factory.md#setfeerecipient)
- [setFeesParametersOnPair](Factory.md#setfeesparametersonpair)
- [setFlashLoanFee](Factory.md#setflashloanfee)
- [setLBPairIgnored](Factory.md#setlbpairignored)
- [setLBPairInformation](Factory.md#setlbpairinformation)
- [setPreset](Factory.md#setpreset)
- [transferOwnership](Factory.md#transferownership)

## Functions

### addQuoteAsset

▸ **addQuoteAsset**(`bs`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `bs` | `StaticArray`<`u8`\> |

#### Returns

`void`

#### Defined in

[assembly/contracts/Factory.ts:413](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/contracts/Factory.ts#L413)

___

### constructor

▸ **constructor**(`bs`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `bs` | `StaticArray`<`u8`\> |

#### Returns

`void`

#### Defined in

[assembly/contracts/Factory.ts:34](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/contracts/Factory.ts#L34)

___

### createLBPair

▸ **createLBPair**(`bs`): `StaticArray`<`u8`\>

Create a liquidity bin LBPair for _tokenX and _tokenY

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `bs` | `StaticArray`<`u8`\> | The serialized arguments |

#### Returns

`StaticArray`<`u8`\>

The address of the newly created LBPair

#### Defined in

[assembly/contracts/Factory.ts:156](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/contracts/Factory.ts#L156)

___

### forceDecay

▸ **forceDecay**(`bs`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `bs` | `StaticArray`<`u8`\> |

#### Returns

`void`

#### Defined in

[assembly/contracts/Factory.ts:447](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/contracts/Factory.ts#L447)

___

### getAllBinSteps

▸ **getAllBinSteps**(`_`): `StaticArray`<`u8`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `_` | `StaticArray`<`u8`\> |

#### Returns

`StaticArray`<`u8`\>

#### Defined in

[assembly/contracts/Factory.ts:89](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/contracts/Factory.ts#L89)

___

### getAvailableLBPairBinSteps

▸ **getAvailableLBPairBinSteps**(`bs`): `StaticArray`<`u8`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `bs` | `StaticArray`<`u8`\> |

#### Returns

`StaticArray`<`u8`\>

#### Defined in

[assembly/contracts/Factory.ts:104](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/contracts/Factory.ts#L104)

___

### getLBPairInformation

▸ **getLBPairInformation**(`bs`): `StaticArray`<`u8`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `bs` | `StaticArray`<`u8`\> |

#### Returns

`StaticArray`<`u8`\>

#### Defined in

[assembly/contracts/Factory.ts:66](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/contracts/Factory.ts#L66)

___

### removePreset

▸ **removePreset**(`bs`): `void`

Remove the preset linked to a binStep

#### Parameters

| Name | Type |
| :------ | :------ |
| `bs` | `StaticArray`<`u8`\> |

#### Returns

`void`

#### Defined in

[assembly/contracts/Factory.ts:314](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/contracts/Factory.ts#L314)

___

### removeQuoteAsset

▸ **removeQuoteAsset**(`bs`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `bs` | `StaticArray`<`u8`\> |

#### Returns

`void`

#### Defined in

[assembly/contracts/Factory.ts:426](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/contracts/Factory.ts#L426)

___

### setFactoryLockedState

▸ **setFactoryLockedState**(`bs`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `bs` | `StaticArray`<`u8`\> |

#### Returns

`void`

#### Defined in

[assembly/contracts/Factory.ts:401](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/contracts/Factory.ts#L401)

___

### setFeeRecipient

▸ **setFeeRecipient**(`bs`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `bs` | `StaticArray`<`u8`\> |

#### Returns

`void`

#### Defined in

[assembly/contracts/Factory.ts:381](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/contracts/Factory.ts#L381)

___

### setFeesParametersOnPair

▸ **setFeesParametersOnPair**(`bs`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `bs` | `StaticArray`<`u8`\> |

#### Returns

`void`

#### Defined in

[assembly/contracts/Factory.ts:328](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/contracts/Factory.ts#L328)

___

### setFlashLoanFee

▸ **setFlashLoanFee**(`bs`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `bs` | `StaticArray`<`u8`\> |

#### Returns

`void`

#### Defined in

[assembly/contracts/Factory.ts:388](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/contracts/Factory.ts#L388)

___

### setLBPairIgnored

▸ **setLBPairIgnored**(`bs`): `void`

Function to set whether the pair is ignored or not for routing, it will make the pair unusable by the router

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `bs` | `StaticArray`<`u8`\> | The serialized arguments |

#### Returns

`void`

#### Defined in

[assembly/contracts/Factory.ts:228](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/contracts/Factory.ts#L228)

___

### setLBPairInformation

▸ **setLBPairInformation**(`bs`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `bs` | `StaticArray`<`u8`\> |

#### Returns

`void`

#### Defined in

[assembly/contracts/Factory.ts:127](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/contracts/Factory.ts#L127)

___

### setPreset

▸ **setPreset**(`bs`): `void`

Sets the preset parameters of a bin step

#### Parameters

| Name | Type |
| :------ | :------ |
| `bs` | `StaticArray`<`u8`\> |

#### Returns

`void`

#### Defined in

[assembly/contracts/Factory.ts:260](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/contracts/Factory.ts#L260)

___

### transferOwnership

▸ **transferOwnership**(`bs`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `bs` | `StaticArray`<`u8`\> |

#### Returns

`void`

#### Defined in

[assembly/contracts/Factory.ts:454](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/contracts/Factory.ts#L454)
