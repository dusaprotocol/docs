# Factory

## Table of contents

### Functions

- [acceptOwnership](Factory.md#acceptownership)
- [addQuoteAsset](Factory.md#addquoteasset)
- [constructor](Factory.md#constructor)
- [createLBPair](Factory.md#createlbpair)
- [forceDecay](Factory.md#forcedecay)
- [getAllBinSteps](Factory.md#getallbinsteps)
- [getAllLBPairs](Factory.md#getalllbpairs)
- [getAvailableLBPairBinSteps](Factory.md#getavailablelbpairbinsteps)
- [getLBPairInformation](Factory.md#getlbpairinformation)
- [getPreset](Factory.md#getpreset)
- [proposeNewOwner](Factory.md#proposenewowner)
- [removePreset](Factory.md#removepreset)
- [removeQuoteAsset](Factory.md#removequoteasset)
- [setFactoryLockedState](Factory.md#setfactorylockedstate)
- [setFeeRecipient](Factory.md#setfeerecipient)
- [setFeesParametersOnPair](Factory.md#setfeesparametersonpair)
- [setFlashLoanFee](Factory.md#setflashloanfee)
- [setLBPairIgnored](Factory.md#setlbpairignored)
- [setPreset](Factory.md#setpreset)

## Functions

### acceptOwnership

▸ **acceptOwnership**(`_`): `void`

Accept the ownership of the contract.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `_` | `StaticArray`<`u8`\> | unused |

#### Returns

`void`

#### Defined in

[assembly/contracts/Factory.ts:737](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/contracts/Factory.ts#L737)

___

### addQuoteAsset

▸ **addQuoteAsset**(`bs`): `void`

Function to add an asset to the whitelist of quote assets

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `bs` | `StaticArray`<`u8`\> | The serialized arguments |

#### Returns

`void`

#### Defined in

[assembly/contracts/Factory.ts:667](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/contracts/Factory.ts#L667)

___

### constructor

▸ **constructor**(`bs`): `void`

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `bs` | `StaticArray`<`u8`\> | The serialized arguments containing: - _feeRecipient The address of the fee recipient - _flashLoanFee The value of the fee for flash loan |

#### Returns

`void`

**`Notice`**

Constructor

#### Defined in

[assembly/contracts/Factory.ts:79](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/contracts/Factory.ts#L79)

___

### createLBPair

▸ **createLBPair**(`bs`): `StaticArray`<`u8`\>

Create a liquidity bin LBPair for _tokenX and _tokenY

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `bs` | `StaticArray`<`u8`\> | The serialized arguments -_tokenX The address of the first token -_tokenY The address of the second token -_activeId The id of the active bin -_binStep The bin step of the LBPair |

#### Returns

`StaticArray`<`u8`\>

The address of the newly created LBPair

#### Defined in

[assembly/contracts/Factory.ts:340](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/contracts/Factory.ts#L340)

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

[assembly/contracts/Factory.ts:708](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/contracts/Factory.ts#L708)

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

[assembly/contracts/Factory.ts:178](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/contracts/Factory.ts#L178)

___

### getAllLBPairs

▸ **getAllLBPairs**(`bs`): `StaticArray`<`u8`\>

View function to return all the LBPair of a pair of tokens

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `bs` | `StaticArray`<`u8`\> | The serialized arguments |

#### Returns

`StaticArray`<`u8`\>

#### Defined in

[assembly/contracts/Factory.ts:226](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/contracts/Factory.ts#L226)

___

### getAvailableLBPairBinSteps

▸ **getAvailableLBPairBinSteps**(`bs`): `StaticArray`<`u8`\>

View function to return the list of available binStep for a pair of tokens

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `bs` | `StaticArray`<`u8`\> | the serialized arguments containing: - _tokenA The address of the first token of the pair - _tokenB The address of the second token of the pair |

#### Returns

`StaticArray`<`u8`\>

Available bin steps for a pair of tokens

#### Defined in

[assembly/contracts/Factory.ts:200](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/contracts/Factory.ts#L200)

___

### getLBPairInformation

▸ **getLBPairInformation**(`bs`): `StaticArray`<`u8`\>

Returns the LBPairInformation if it exists

#### Parameters

| Name | Type |
| :------ | :------ |
| `bs` | `StaticArray`<`u8`\> |

#### Returns

`StaticArray`<`u8`\>

#### Defined in

[assembly/contracts/Factory.ts:127](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/contracts/Factory.ts#L127)

___

### getPreset

▸ **getPreset**(`bs`): `StaticArray`<`u8`\>

View function to return the different parameters of the preset

#### Parameters

| Name | Type |
| :------ | :------ |
| `bs` | `StaticArray`<`u8`\> |

#### Returns

`StaticArray`<`u8`\>

#### Defined in

[assembly/contracts/Factory.ts:161](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/contracts/Factory.ts#L161)

___

### proposeNewOwner

▸ **proposeNewOwner**(`bs`): `void`

Propose to transfer the ownership of the contract to a new account (`newOwner`).

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `bs` | `StaticArray`<`u8`\> | The serialized arguments containing the new owner address |

#### Returns

`void`

#### Defined in

[assembly/contracts/Factory.ts:721](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/contracts/Factory.ts#L721)

___

### removePreset

▸ **removePreset**(`bs`): `void`

Remove the preset linked to a binStep

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `bs` | `StaticArray`<`u8`\> | The serialized arguments |

#### Returns

`void`

#### Defined in

[assembly/contracts/Factory.ts:524](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/contracts/Factory.ts#L524)

___

### removeQuoteAsset

▸ **removeQuoteAsset**(`bs`): `void`

Function to remove an asset from the whitelist of quote assets

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `bs` | `StaticArray`<`u8`\> | The serialized arguments |

#### Returns

`void`

#### Defined in

[assembly/contracts/Factory.ts:689](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/contracts/Factory.ts#L689)

___

### setFactoryLockedState

▸ **setFactoryLockedState**(`bs`): `void`

Function to set the creation restriction of the Factory

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `bs` | `StaticArray`<`u8`\> | The serialized arguments |

#### Returns

`void`

#### Defined in

[assembly/contracts/Factory.ts:648](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/contracts/Factory.ts#L648)

___

### setFeeRecipient

▸ **setFeeRecipient**(`bs`): `void`

Function to set the recipient of the fees. This address needs to be able to receive ERC20s

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `bs` | `StaticArray`<`u8`\> | The serialized arguments |

#### Returns

`void`

#### Defined in

[assembly/contracts/Factory.ts:610](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/contracts/Factory.ts#L610)

___

### setFeesParametersOnPair

▸ **setFeesParametersOnPair**(`bs`): `void`

Function to set the fee parameter of a LBPair

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `bs` | `StaticArray`<`u8`\> | The serialized arguments |

#### Returns

`void`

#### Defined in

[assembly/contracts/Factory.ts:545](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/contracts/Factory.ts#L545)

___

### setFlashLoanFee

▸ **setFlashLoanFee**(`bs`): `void`

Function to set the flash loan fee

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `bs` | `StaticArray`<`u8`\> | The serialized arguments |

#### Returns

`void`

#### Defined in

[assembly/contracts/Factory.ts:623](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/contracts/Factory.ts#L623)

___

### setLBPairIgnored

▸ **setLBPairIgnored**(`bs`): `void`

Function to set whether the pair is ignored or not for routing, it will make the pair unusable by the router

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `bs` | `StaticArray`<`u8`\> | The serialized arguments -_tokenA The address of the first token -_tokenB The address of the second token -_binStep The bin step of the LBPair -Whether to ignore (true) or not (false) the pair for routing |

#### Returns

`void`

#### Defined in

[assembly/contracts/Factory.ts:424](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/contracts/Factory.ts#L424)

___

### setPreset

▸ **setPreset**(`bs`): `void`

Sets the preset parameters of a bin step

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `bs` | `StaticArray`<`u8`\> | The serialized arguments |

#### Returns

`void`

#### Defined in

[assembly/contracts/Factory.ts:463](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/contracts/Factory.ts#L463)
