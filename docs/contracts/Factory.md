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
- [grantRole](Factory.md#grantrole)
- [hasRole](Factory.md#hasrole)
- [members](Factory.md#members)
- [onlyRole](Factory.md#onlyrole)
- [proposeNewOwner](Factory.md#proposenewowner)
- [receiveCoins](Factory.md#receivecoins)
- [removeLBHooksOnPair](Factory.md#removelbhooksonpair)
- [removePreset](Factory.md#removepreset)
- [removeQuoteAsset](Factory.md#removequoteasset)
- [revokeRole](Factory.md#revokerole)
- [setFactoryLockedState](Factory.md#setfactorylockedstate)
- [setFeeRecipient](Factory.md#setfeerecipient)
- [setFeesParametersOnPair](Factory.md#setfeesparametersonpair)
- [setFlashLoanFee](Factory.md#setflashloanfee)
- [setLBHooksParametersOnPair](Factory.md#setlbhooksparametersonpair)
- [setLBPairIgnored](Factory.md#setlbpairignored)
- [setPreset](Factory.md#setpreset)

## Functions

### acceptOwnership

▸ **acceptOwnership**(`_`): `void`

Accept the ownership of the contract.

#### Parameters

| Name | Type                 | Description |
| :--- | :------------------- | :---------- |
| `_`  | `StaticArray`<`u8`\> | unused      |

#### Returns

`void`

#### Defined in

[assembly/contracts/Factory.ts:855](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/contracts/Factory.ts#L855)

---

### addQuoteAsset

▸ **addQuoteAsset**(`bs`): `void`

Function to add an asset to the whitelist of quote assets

#### Parameters

| Name | Type                 | Description              |
| :--- | :------------------- | :----------------------- |
| `bs` | `StaticArray`<`u8`\> | The serialized arguments |

#### Returns

`void`

#### Defined in

[assembly/contracts/Factory.ts:776](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/contracts/Factory.ts#L776)

---

### constructor

▸ **constructor**(`bs`): `void`

#### Parameters

| Name | Type                 | Description                                                                                                                                 |
| :--- | :------------------- | :------------------------------------------------------------------------------------------------------------------------------------------ |
| `bs` | `StaticArray`<`u8`\> | The serialized arguments containing: - \_feeRecipient The address of the fee recipient - \_flashLoanFee The value of the fee for flash loan |

#### Returns

`void`

**`Notice`**

Constructor

#### Defined in

[assembly/contracts/Factory.ts:95](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/contracts/Factory.ts#L95)

---

### createLBPair

▸ **createLBPair**(`bs`): `StaticArray`<`u8`\>

Create a liquidity bin LBPair for \_tokenX and \_tokenY

#### Parameters

| Name | Type                 | Description                                                                                                                                                                            |
| :--- | :------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `bs` | `StaticArray`<`u8`\> | The serialized arguments -\_tokenX The address of the first token -\_tokenY The address of the second token -\_activeId The id of the active bin -\_binStep The bin step of the LBPair |

#### Returns

`StaticArray`<`u8`\>

The address of the newly created LBPair

#### Defined in

[assembly/contracts/Factory.ts:360](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/contracts/Factory.ts#L360)

---

### forceDecay

▸ **forceDecay**(`bs`): `void`

#### Parameters

| Name | Type                 |
| :--- | :------------------- |
| `bs` | `StaticArray`<`u8`\> |

#### Returns

`void`

#### Defined in

[assembly/contracts/Factory.ts:826](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/contracts/Factory.ts#L826)

---

### getAllBinSteps

▸ **getAllBinSteps**(`_`): `StaticArray`<`u8`\>

#### Parameters

| Name | Type                 |
| :--- | :------------------- |
| `_`  | `StaticArray`<`u8`\> |

#### Returns

`StaticArray`<`u8`\>

#### Defined in

[assembly/contracts/Factory.ts:196](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/contracts/Factory.ts#L196)

---

### getAllLBPairs

▸ **getAllLBPairs**(`bs`): `StaticArray`<`u8`\>

View function to return all the LBPair of a pair of tokens

#### Parameters

| Name | Type                 | Description              |
| :--- | :------------------- | :----------------------- |
| `bs` | `StaticArray`<`u8`\> | The serialized arguments |

#### Returns

`StaticArray`<`u8`\>

#### Defined in

[assembly/contracts/Factory.ts:244](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/contracts/Factory.ts#L244)

---

### getAvailableLBPairBinSteps

▸ **getAvailableLBPairBinSteps**(`bs`): `StaticArray`<`u8`\>

View function to return the list of available binStep for a pair of tokens

#### Parameters

| Name | Type                 | Description                                                                                                                                       |
| :--- | :------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------ |
| `bs` | `StaticArray`<`u8`\> | the serialized arguments containing: - \_tokenA The address of the first token of the pair - \_tokenB The address of the second token of the pair |

#### Returns

`StaticArray`<`u8`\>

Available bin steps for a pair of tokens

#### Defined in

[assembly/contracts/Factory.ts:218](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/contracts/Factory.ts#L218)

---

### getLBPairInformation

▸ **getLBPairInformation**(`bs`): `StaticArray`<`u8`\>

Returns the LBPairInformation if it exists

#### Parameters

| Name | Type                 |
| :--- | :------------------- |
| `bs` | `StaticArray`<`u8`\> |

#### Returns

`StaticArray`<`u8`\>

#### Defined in

[assembly/contracts/Factory.ts:145](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/contracts/Factory.ts#L145)

---

### getPreset

▸ **getPreset**(`bs`): `StaticArray`<`u8`\>

View function to return the different parameters of the preset

#### Parameters

| Name | Type                 |
| :--- | :------------------- |
| `bs` | `StaticArray`<`u8`\> |

#### Returns

`StaticArray`<`u8`\>

#### Defined in

[assembly/contracts/Factory.ts:179](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/contracts/Factory.ts#L179)

---

### grantRole

▸ **grantRole**(`binaryArgs`): `void`

Set the role for account

#### Parameters

| Name         | Type                 |
| :----------- | :------------------- |
| `binaryArgs` | `StaticArray`<`u8`\> |

#### Returns

`void`

#### Defined in

node_modules/@massalabs/sc-standards/assembly/contracts/utils/accessControl.ts:17

---

### hasRole

▸ **hasRole**(`binaryArgs`): `StaticArray`<`u8`\>

Returns true if the account has the role.

#### Parameters

| Name         | Type                 |
| :----------- | :------------------- |
| `binaryArgs` | `StaticArray`<`u8`\> |

#### Returns

`StaticArray`<`u8`\>

boolean

#### Defined in

node_modules/@massalabs/sc-standards/assembly/contracts/utils/accessControl.ts:49

---

### members

▸ **members**(`binaryArgs`): `StaticArray`<`u8`\>

get the members for a role

#### Parameters

| Name         | Type                 |
| :----------- | :------------------- |
| `binaryArgs` | `StaticArray`<`u8`\> |

#### Returns

`StaticArray`<`u8`\>

#### Defined in

node_modules/@massalabs/sc-standards/assembly/contracts/utils/accessControl.ts:36

---

### onlyRole

▸ **onlyRole**(`binaryArgs`): `void`

Assert that caller has the role.

#### Parameters

| Name         | Type                 |
| :----------- | :------------------- |
| `binaryArgs` | `StaticArray`<`u8`\> |

#### Returns

`void`

boolean

#### Defined in

node_modules/@massalabs/sc-standards/assembly/contracts/utils/accessControl.ts:85

---

### proposeNewOwner

▸ **proposeNewOwner**(`bs`): `void`

Propose to transfer the ownership of the contract to a new account (`newOwner`).

#### Parameters

| Name | Type                 | Description                                               |
| :--- | :------------------- | :-------------------------------------------------------- |
| `bs` | `StaticArray`<`u8`\> | The serialized arguments containing the new owner address |

#### Returns

`void`

#### Defined in

[assembly/contracts/Factory.ts:839](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/contracts/Factory.ts#L839)

---

### receiveCoins

▸ **receiveCoins**(`_`): `void`

#### Parameters

| Name | Type                 | Description |
| :--- | :------------------- | :---------- |
| `_`  | `StaticArray`<`u8`\> | unused      |

#### Returns

`void`

**`Notice`**

Function used by an SC to receive Massa coins

#### Defined in

[assembly/contracts/Factory.ts:967](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/contracts/Factory.ts#L967)

---

### removeLBHooksOnPair

▸ **removeLBHooksOnPair**(`bs`): `void`

Function to remove the hooks contract from the pair

#### Parameters

| Name | Type                 |
| :--- | :------------------- |
| `bs` | `StaticArray`<`u8`\> |

#### Returns

`void`

**`Dev`**

Needs to be called by an address with the HOOKS_MANAGER role
fail if:

- The pair doesn't exist

#### Defined in

[assembly/contracts/Factory.ts:667](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/contracts/Factory.ts#L667)

---

### removePreset

▸ **removePreset**(`bs`): `void`

Remove the preset linked to a binStep

#### Parameters

| Name | Type                 | Description              |
| :--- | :------------------- | :----------------------- |
| `bs` | `StaticArray`<`u8`\> | The serialized arguments |

#### Returns

`void`

#### Defined in

[assembly/contracts/Factory.ts:536](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/contracts/Factory.ts#L536)

---

### removeQuoteAsset

▸ **removeQuoteAsset**(`bs`): `void`

Function to remove an asset from the whitelist of quote assets

#### Parameters

| Name | Type                 | Description              |
| :--- | :------------------- | :----------------------- |
| `bs` | `StaticArray`<`u8`\> | The serialized arguments |

#### Returns

`void`

#### Defined in

[assembly/contracts/Factory.ts:798](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/contracts/Factory.ts#L798)

---

### revokeRole

▸ **revokeRole**(`binaryArgs`): `void`

Revoke role for account. Must be called by the role owner or the contract admin.

#### Parameters

| Name         | Type                 |
| :----------- | :------------------- |
| `binaryArgs` | `StaticArray`<`u8`\> |

#### Returns

`void`

#### Defined in

node_modules/@massalabs/sc-standards/assembly/contracts/utils/accessControl.ts:66

---

### setFactoryLockedState

▸ **setFactoryLockedState**(`bs`): `void`

Function to set the creation restriction of the Factory

#### Parameters

| Name | Type                 | Description              |
| :--- | :------------------- | :----------------------- |
| `bs` | `StaticArray`<`u8`\> | The serialized arguments |

#### Returns

`void`

#### Defined in

[assembly/contracts/Factory.ts:757](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/contracts/Factory.ts#L757)

---

### setFeeRecipient

▸ **setFeeRecipient**(`bs`): `void`

Function to set the recipient of the fees. This address needs to be able to receive ERC20s

#### Parameters

| Name | Type                 | Description              |
| :--- | :------------------- | :----------------------- |
| `bs` | `StaticArray`<`u8`\> | The serialized arguments |

#### Returns

`void`

#### Defined in

[assembly/contracts/Factory.ts:719](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/contracts/Factory.ts#L719)

---

### setFeesParametersOnPair

▸ **setFeesParametersOnPair**(`bs`): `void`

Function to set the fee parameter of a LBPair

#### Parameters

| Name | Type                 | Description              |
| :--- | :------------------- | :----------------------- |
| `bs` | `StaticArray`<`u8`\> | The serialized arguments |

#### Returns

`void`

#### Defined in

[assembly/contracts/Factory.ts:557](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/contracts/Factory.ts#L557)

---

### setFlashLoanFee

▸ **setFlashLoanFee**(`bs`): `void`

Function to set the flash loan fee

#### Parameters

| Name | Type                 | Description              |
| :--- | :------------------- | :----------------------- |
| `bs` | `StaticArray`<`u8`\> | The serialized arguments |

#### Returns

`void`

#### Defined in

[assembly/contracts/Factory.ts:732](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/contracts/Factory.ts#L732)

---

### setLBHooksParametersOnPair

▸ **setLBHooksParametersOnPair**(`bs`): `void`

Function to set the hooks parameters of a pair

#### Parameters

| Name | Type                 |
| :--- | :------------------- |
| `bs` | `StaticArray`<`u8`\> |

#### Returns

`void`

**`Dev`**

Needs to be called by an address with the HOOKS_MANAGER role
fail if:

- The pair doesn't exist
- The hooks address is not valid or the hooks flags are all false

#### Defined in

[assembly/contracts/Factory.ts:630](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/contracts/Factory.ts#L630)

---

### setLBPairIgnored

▸ **setLBPairIgnored**(`bs`): `void`

Function to set whether the pair is ignored or not for routing, it will make the pair unusable by the quoter

#### Parameters

| Name | Type                 | Description                                                                                                                                                                                                                |
| :--- | :------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `bs` | `StaticArray`<`u8`\> | The serialized arguments -\_tokenA The address of the first token -\_tokenB The address of the second token -\_binStep The bin step of the LBPair -\_ignored: Whether to ignore (true) or not (false) the pair for routing |

#### Returns

`void`

#### Defined in

[assembly/contracts/Factory.ts:436](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/contracts/Factory.ts#L436)

---

### setPreset

▸ **setPreset**(`bs`): `void`

Sets the preset parameters of a bin step

#### Parameters

| Name | Type                 | Description              |
| :--- | :------------------- | :----------------------- |
| `bs` | `StaticArray`<`u8`\> | The serialized arguments |

#### Returns

`void`

#### Defined in

[assembly/contracts/Factory.ts:475](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/contracts/Factory.ts#L475)
