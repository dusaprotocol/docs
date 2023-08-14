# Pair

## Table of contents

### Functions

- [balanceOf](Pair.md#balanceof)
- [balanceOfBatch](Pair.md#balanceofbatch)
- [burn](Pair.md#burn)
- [collectFees](Pair.md#collectfees)
- [collectProtocolFees](Pair.md#collectprotocolfees)
- [constructor](Pair.md#constructor)
- [findFirstNonEmptyBinId](Pair.md#findfirstnonemptybinid)
- [flashLoan](Pair.md#flashloan)
- [forceDecay](Pair.md#forcedecay)
- [getBin](Pair.md#getbin)
- [getGlobalFees](Pair.md#getglobalfees)
- [getOracleParameters](Pair.md#getoracleparameters)
- [getOracleSampleFrom](Pair.md#getoraclesamplefrom)
- [getPairInformation](Pair.md#getpairinformation)
- [getUserBins](Pair.md#getuserbins)
- [increaseOracleLength](Pair.md#increaseoraclelength)
- [isApprovedForAll](Pair.md#isapprovedforall)
- [mint](Pair.md#mint)
- [name](Pair.md#name)
- [pendingFees](Pair.md#pendingfees)
- [safeBatchTransferFrom](Pair.md#safebatchtransferfrom)
- [safeTransferFrom](Pair.md#safetransferfrom)
- [setApprovalForAll](Pair.md#setapprovalforall)
- [setFeesParameters](Pair.md#setfeesparameters)
- [swap](Pair.md#swap)
- [symbol](Pair.md#symbol)
- [totalSupply](Pair.md#totalsupply)

## Functions

### balanceOf

▸ **balanceOf**(`bs`): `StaticArray`<`u8`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `bs` | `StaticArray`<`u8`\> |

#### Returns

`StaticArray`<`u8`\>

#### Defined in

[assembly/contracts/Pair.ts:993](https://github.com/dusaprotocol/v2.1/blob/0058e1c/assembly/contracts/Pair.ts#L993)

___

### balanceOfBatch

▸ **balanceOfBatch**(`bs`): `StaticArray`<`u8`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `bs` | `StaticArray`<`u8`\> |

#### Returns

`StaticArray`<`u8`\>

#### Defined in

[assembly/contracts/Pair.ts:1006](https://github.com/dusaprotocol/v2.1/blob/0058e1c/assembly/contracts/Pair.ts#L1006)

___

### burn

▸ **burn**(`bs`): `StaticArray`<`u8`\>

Burns LB tokens and sends the corresponding amounts of tokens to `_to`. The amount of tokens sent is
determined by the ratio of the amount of LB tokens burned to the total supply of LB tokens in the bin.
This function will not transfer the LB Tokens from the caller, it is expected that the tokens have already been
transferred to this contract through another contract.
That is why this function shouldn't be called directly, but through one of the remove liquidity functions of the router
that will also perform safety checks.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `bs` | `StaticArray`<`u8`\> | Byte string |

#### Returns

`StaticArray`<`u8`\>

#### Defined in

[assembly/contracts/Pair.ts:446](https://github.com/dusaprotocol/v2.1/blob/0058e1c/assembly/contracts/Pair.ts#L446)

___

### collectFees

▸ **collectFees**(`bs`): `StaticArray`<`u8`\>

Collect the fees accumulated by a user.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `bs` | `StaticArray`<`u8`\> | Byte string |

#### Returns

`StaticArray`<`u8`\>

#### Defined in

[assembly/contracts/Pair.ts:543](https://github.com/dusaprotocol/v2.1/blob/0058e1c/assembly/contracts/Pair.ts#L543)

___

### collectProtocolFees

▸ **collectProtocolFees**(`_`): `StaticArray`<`u8`\>

Collect the protocol fees and send them to the fee recipient.
The protocol fees are not set to zero to save gas by not resetting the storage slot.

#### Parameters

| Name | Type |
| :------ | :------ |
| `_` | `StaticArray`<`u8`\> |

#### Returns

`StaticArray`<`u8`\>

#### Defined in

[assembly/contracts/Pair.ts:599](https://github.com/dusaprotocol/v2.1/blob/0058e1c/assembly/contracts/Pair.ts#L599)

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

[assembly/contracts/Pair.ts:64](https://github.com/dusaprotocol/v2.1/blob/0058e1c/assembly/contracts/Pair.ts#L64)

___

### findFirstNonEmptyBinId

▸ **findFirstNonEmptyBinId**(`bs`): `StaticArray`<`u8`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `bs` | `StaticArray`<`u8`\> |

#### Returns

`StaticArray`<`u8`\>

#### Defined in

[assembly/contracts/Pair.ts:943](https://github.com/dusaprotocol/v2.1/blob/0058e1c/assembly/contracts/Pair.ts#L943)

___

### flashLoan

▸ **flashLoan**(`bs`): `StaticArray`<`u8`\>

Perform a flashloan on one of the tokens of the pair. The flashloan will call the `_receiver` contract
to perform the desired operations. The `_receiver` contract is expected to transfer the `amount + fee` of the
token to this contract.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `bs` | `StaticArray`<`u8`\> | Byte string |

#### Returns

`StaticArray`<`u8`\>

#### Defined in

[assembly/contracts/Pair.ts:198](https://github.com/dusaprotocol/v2.1/blob/0058e1c/assembly/contracts/Pair.ts#L198)

___

### forceDecay

▸ **forceDecay**(`_`): `void`

Force the decaying of the references for volatility and index

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `_` | `StaticArray`<`u8`\> | unused |

#### Returns

`void`

#### Defined in

[assembly/contracts/Pair.ts:932](https://github.com/dusaprotocol/v2.1/blob/0058e1c/assembly/contracts/Pair.ts#L932)

___

### getBin

▸ **getBin**(`bs`): `StaticArray`<`u8`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `bs` | `StaticArray`<`u8`\> |

#### Returns

`StaticArray`<`u8`\>

#### Defined in

[assembly/contracts/Pair.ts:720](https://github.com/dusaprotocol/v2.1/blob/0058e1c/assembly/contracts/Pair.ts#L720)

___

### getGlobalFees

▸ **getGlobalFees**(`_`): `StaticArray`<`u8`\>

View function to get the total fees and the protocol fees of each tokens

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `_` | `StaticArray`<`u8`\> | unused |

#### Returns

`StaticArray`<`u8`\>

 -feesX.total The total fees of tokenX
 -feesY.total The total fees of tokenY
 -feesX.protocol The protocol fees of tokenX
 -feesY.protocol The protocol fees of tokenY

#### Defined in

[assembly/contracts/Pair.ts:745](https://github.com/dusaprotocol/v2.1/blob/0058e1c/assembly/contracts/Pair.ts#L745)

___

### getOracleParameters

▸ **getOracleParameters**(`_`): `StaticArray`<`u8`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `_` | `StaticArray`<`u8`\> |

#### Returns

`StaticArray`<`u8`\>

#### Defined in

[assembly/contracts/Pair.ts:790](https://github.com/dusaprotocol/v2.1/blob/0058e1c/assembly/contracts/Pair.ts#L790)

___

### getOracleSampleFrom

▸ **getOracleSampleFrom**(`bs`): `StaticArray`<`u8`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `bs` | `StaticArray`<`u8`\> |

#### Returns

`StaticArray`<`u8`\>

#### Defined in

[assembly/contracts/Pair.ts:798](https://github.com/dusaprotocol/v2.1/blob/0058e1c/assembly/contracts/Pair.ts#L798)

___

### getPairInformation

▸ **getPairInformation**(`_`): `StaticArray`<`u8`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `_` | `StaticArray`<`u8`\> |

#### Returns

`StaticArray`<`u8`\>

#### Defined in

[assembly/contracts/Pair.ts:698](https://github.com/dusaprotocol/v2.1/blob/0058e1c/assembly/contracts/Pair.ts#L698)

___

### getUserBins

▸ **getUserBins**(`bs`): `StaticArray`<`u8`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `bs` | `StaticArray`<`u8`\> |

#### Returns

`StaticArray`<`u8`\>

#### Defined in

[assembly/contracts/Pair.ts:679](https://github.com/dusaprotocol/v2.1/blob/0058e1c/assembly/contracts/Pair.ts#L679)

___

### increaseOracleLength

▸ **increaseOracleLength**(`bs`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `bs` | `StaticArray`<`u8`\> |

#### Returns

`void`

#### Defined in

[assembly/contracts/Pair.ts:827](https://github.com/dusaprotocol/v2.1/blob/0058e1c/assembly/contracts/Pair.ts#L827)

___

### isApprovedForAll

▸ **isApprovedForAll**(`bs`): `StaticArray`<`u8`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `bs` | `StaticArray`<`u8`\> |

#### Returns

`StaticArray`<`u8`\>

#### Defined in

[assembly/contracts/Pair.ts:1027](https://github.com/dusaprotocol/v2.1/blob/0058e1c/assembly/contracts/Pair.ts#L1027)

___

### mint

▸ **mint**(`bs`): `StaticArray`<`u8`\>

Mint new LB tokens for each bins where the user adds liquidity.
This function will not transfer the tokens from the caller, it is expected that the tokens have already been
transferred to this contract through another contract.
That is why this function shouldn't be called directly, but through one of the add liquidity functions of the
router that will also perform safety checks.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `bs` | `StaticArray`<`u8`\> | Byte string |

#### Returns

`StaticArray`<`u8`\>

#### Defined in

[assembly/contracts/Pair.ts:270](https://github.com/dusaprotocol/v2.1/blob/0058e1c/assembly/contracts/Pair.ts#L270)

___

### name

▸ **name**(`_`): `StaticArray`<`u8`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `_` | `StaticArray`<`u8`\> |

#### Returns

`StaticArray`<`u8`\>

#### Defined in

[assembly/contracts/Pair.ts:969](https://github.com/dusaprotocol/v2.1/blob/0058e1c/assembly/contracts/Pair.ts#L969)

___

### pendingFees

▸ **pendingFees**(`bs`): `StaticArray`<`u8`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `bs` | `StaticArray`<`u8`\> |

#### Returns

`StaticArray`<`u8`\>

#### Defined in

[assembly/contracts/Pair.ts:643](https://github.com/dusaprotocol/v2.1/blob/0058e1c/assembly/contracts/Pair.ts#L643)

___

### safeBatchTransferFrom

▸ **safeBatchTransferFrom**(`bs`): `StaticArray`<`u8`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `bs` | `StaticArray`<`u8`\> |

#### Returns

`StaticArray`<`u8`\>

#### Defined in

[assembly/contracts/Pair.ts:1081](https://github.com/dusaprotocol/v2.1/blob/0058e1c/assembly/contracts/Pair.ts#L1081)

___

### safeTransferFrom

▸ **safeTransferFrom**(`bs`): `StaticArray`<`u8`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `bs` | `StaticArray`<`u8`\> |

#### Returns

`StaticArray`<`u8`\>

#### Defined in

[assembly/contracts/Pair.ts:1055](https://github.com/dusaprotocol/v2.1/blob/0058e1c/assembly/contracts/Pair.ts#L1055)

___

### setApprovalForAll

▸ **setApprovalForAll**(`bs`): `StaticArray`<`u8`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `bs` | `StaticArray`<`u8`\> |

#### Returns

`StaticArray`<`u8`\>

#### Defined in

[assembly/contracts/Pair.ts:1039](https://github.com/dusaprotocol/v2.1/blob/0058e1c/assembly/contracts/Pair.ts#L1039)

___

### setFeesParameters

▸ **setFeesParameters**(`bs`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `bs` | `StaticArray`<`u8`\> |

#### Returns

`void`

#### Defined in

[assembly/contracts/Pair.ts:868](https://github.com/dusaprotocol/v2.1/blob/0058e1c/assembly/contracts/Pair.ts#L868)

___

### swap

▸ **swap**(`bs`): `StaticArray`<`u8`\>

Swap tokens iterating over the bins until the entire amount is swapped.
Will swap token X for token Y if `_swapForY` is true, and token Y for token X if `_swapForY` is false.
This function will not transfer the tokens from the caller, it is expected that the tokens have already been
transferred to this contract through another contract.
That is why this function shouldn't be called directly, but through one of the swap functions of the router
that will also perform safety checks.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `bs` | `StaticArray`<`u8`\> | Byte string |

#### Returns

`StaticArray`<`u8`\>

#### Defined in

[assembly/contracts/Pair.ts:100](https://github.com/dusaprotocol/v2.1/blob/0058e1c/assembly/contracts/Pair.ts#L100)

___

### symbol

▸ **symbol**(`_`): `StaticArray`<`u8`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `_` | `StaticArray`<`u8`\> |

#### Returns

`StaticArray`<`u8`\>

#### Defined in

[assembly/contracts/Pair.ts:973](https://github.com/dusaprotocol/v2.1/blob/0058e1c/assembly/contracts/Pair.ts#L973)

___

### totalSupply

▸ **totalSupply**(`bs`): `StaticArray`<`u8`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `bs` | `StaticArray`<`u8`\> |

#### Returns

`StaticArray`<`u8`\>

#### Defined in

[assembly/contracts/Pair.ts:981](https://github.com/dusaprotocol/v2.1/blob/0058e1c/assembly/contracts/Pair.ts#L981)
