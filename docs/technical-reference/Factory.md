# Factory

## Table of contents

### Functions

- [addQuoteAsset](Factory.md#addquoteasset)
- [constructor](Factory.md#constructor)
- [createLBPair](Factory.md#createlbpair)
- [forceDecay](Factory.md#forcedecay)
- [getAllBinSteps](Factory.md#getallbinsteps)
- [getAvailableLBPairBinSteps](Factory.md#getavailablelbpairbinsteps)
- [getLBPairInformation](Factory.md#getlbpairinformation)
- [getPreset](Factory.md#getpreset)
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

[assembly/contracts/Factory.ts:441](https://github.com/dusaprotocol/v2.1/blob/0058e1c/assembly/contracts/Factory.ts#L441)

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

[assembly/contracts/Factory.ts:52](https://github.com/dusaprotocol/v2.1/blob/0058e1c/assembly/contracts/Factory.ts#L52)

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

[assembly/contracts/Factory.ts:182](https://github.com/dusaprotocol/v2.1/blob/0058e1c/assembly/contracts/Factory.ts#L182)

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

[assembly/contracts/Factory.ts:475](https://github.com/dusaprotocol/v2.1/blob/0058e1c/assembly/contracts/Factory.ts#L475)

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

[assembly/contracts/Factory.ts:115](https://github.com/dusaprotocol/v2.1/blob/0058e1c/assembly/contracts/Factory.ts#L115)

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

[assembly/contracts/Factory.ts:130](https://github.com/dusaprotocol/v2.1/blob/0058e1c/assembly/contracts/Factory.ts#L130)

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

[assembly/contracts/Factory.ts:85](https://github.com/dusaprotocol/v2.1/blob/0058e1c/assembly/contracts/Factory.ts#L85)

___

### getPreset

▸ **getPreset**(`bs`): `StaticArray`<`u8`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `bs` | `StaticArray`<`u8`\> |

#### Returns

`StaticArray`<`u8`\>

#### Defined in

[assembly/contracts/Factory.ts:101](https://github.com/dusaprotocol/v2.1/blob/0058e1c/assembly/contracts/Factory.ts#L101)

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

[assembly/contracts/Factory.ts:342](https://github.com/dusaprotocol/v2.1/blob/0058e1c/assembly/contracts/Factory.ts#L342)

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

[assembly/contracts/Factory.ts:454](https://github.com/dusaprotocol/v2.1/blob/0058e1c/assembly/contracts/Factory.ts#L454)

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

[assembly/contracts/Factory.ts:429](https://github.com/dusaprotocol/v2.1/blob/0058e1c/assembly/contracts/Factory.ts#L429)

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

[assembly/contracts/Factory.ts:409](https://github.com/dusaprotocol/v2.1/blob/0058e1c/assembly/contracts/Factory.ts#L409)

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

[assembly/contracts/Factory.ts:356](https://github.com/dusaprotocol/v2.1/blob/0058e1c/assembly/contracts/Factory.ts#L356)

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

[assembly/contracts/Factory.ts:416](https://github.com/dusaprotocol/v2.1/blob/0058e1c/assembly/contracts/Factory.ts#L416)

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

[assembly/contracts/Factory.ts:253](https://github.com/dusaprotocol/v2.1/blob/0058e1c/assembly/contracts/Factory.ts#L253)

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

[assembly/contracts/Factory.ts:153](https://github.com/dusaprotocol/v2.1/blob/0058e1c/assembly/contracts/Factory.ts#L153)

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

[assembly/contracts/Factory.ts:285](https://github.com/dusaprotocol/v2.1/blob/0058e1c/assembly/contracts/Factory.ts#L285)

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

[assembly/contracts/Factory.ts:482](https://github.com/dusaprotocol/v2.1/blob/0058e1c/assembly/contracts/Factory.ts#L482)
