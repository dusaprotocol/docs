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
- [receiveCoins](Factory.md#receivecoins)
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

[assembly/contracts/Factory.ts:753](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/contracts/Factory.ts#L753)

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

[assembly/contracts/Factory.ts:683](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/contracts/Factory.ts#L683)

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

[assembly/contracts/Factory.ts:89](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/contracts/Factory.ts#L89)

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

[assembly/contracts/Factory.ts:351](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/contracts/Factory.ts#L351)

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

[assembly/contracts/Factory.ts:724](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/contracts/Factory.ts#L724)

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

[assembly/contracts/Factory.ts:188](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/contracts/Factory.ts#L188)

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

[assembly/contracts/Factory.ts:236](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/contracts/Factory.ts#L236)

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

[assembly/contracts/Factory.ts:210](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/contracts/Factory.ts#L210)

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

[assembly/contracts/Factory.ts:137](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/contracts/Factory.ts#L137)

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

[assembly/contracts/Factory.ts:171](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/contracts/Factory.ts#L171)

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

[assembly/contracts/Factory.ts:737](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/contracts/Factory.ts#L737)

___

### receiveCoins

▸ **receiveCoins**(`_`): `void`

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `_` | `StaticArray`<`u8`\> | unused |

#### Returns

`void`

**`Notice`**

Function used by an SC to receive Massa coins

#### Defined in

[assembly/contracts/Factory.ts:865](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/contracts/Factory.ts#L865)

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

[assembly/contracts/Factory.ts:540](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/contracts/Factory.ts#L540)

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

[assembly/contracts/Factory.ts:705](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/contracts/Factory.ts#L705)

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

[assembly/contracts/Factory.ts:664](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/contracts/Factory.ts#L664)

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

[assembly/contracts/Factory.ts:626](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/contracts/Factory.ts#L626)

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

[assembly/contracts/Factory.ts:561](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/contracts/Factory.ts#L561)

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

[assembly/contracts/Factory.ts:639](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/contracts/Factory.ts#L639)

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

[assembly/contracts/Factory.ts:440](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/contracts/Factory.ts#L440)

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

[assembly/contracts/Factory.ts:479](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/contracts/Factory.ts#L479)
