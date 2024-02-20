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

Returns the amount of tokens of type `id` owned by `_account`

#### Parameters

| Name | Type |
| :------ | :------ |
| `bs` | `StaticArray`<`u8`\> |

#### Returns

`StaticArray`<`u8`\>

The amount of tokens of type `id` owned by `_account`

#### Defined in

[assembly/contracts/Pair.ts:1322](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/contracts/Pair.ts#L1322)

___

### balanceOfBatch

▸ **balanceOfBatch**(`bs`): `StaticArray`<`u8`\>

Return the balance of multiple (account/id) pairs

#### Parameters

| Name | Type |
| :------ | :------ |
| `bs` | `StaticArray`<`u8`\> |

#### Returns

`StaticArray`<`u8`\>

batchBalances The balance for each (account, id) pair

#### Defined in

[assembly/contracts/Pair.ts:1337](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/contracts/Pair.ts#L1337)

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

[assembly/contracts/Pair.ts:574](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/contracts/Pair.ts#L574)

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

[assembly/contracts/Pair.ts:660](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/contracts/Pair.ts#L660)

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

[assembly/contracts/Pair.ts:733](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/contracts/Pair.ts#L733)

___

### constructor

▸ **constructor**(`bs`): `void`

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `bs` | `StaticArray`<`u8`\> | Byte string |

#### Returns

`void`

**`Notice`**

Constructor

#### Defined in

[assembly/contracts/Pair.ts:91](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/contracts/Pair.ts#L91)

___

### findFirstNonEmptyBinId

▸ **findFirstNonEmptyBinId**(`bs`): `StaticArray`<`u8`\>

View function to get the first bin that isn't empty, will not be `_id` itself

#### Parameters

| Name | Type |
| :------ | :------ |
| `bs` | `StaticArray`<`u8`\> |

#### Returns

`StaticArray`<`u8`\>

#### Defined in

[assembly/contracts/Pair.ts:965](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/contracts/Pair.ts#L965)

___

### flashLoan

▸ **flashLoan**(`bs`): `void`

Perform a flashloan on one of the tokens of the pair. The flashloan will call the `_receiver` contract
to perform the desired operations. The `_receiver` contract is expected to transfer the `amount + fee` of the
token to this contract.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `bs` | `StaticArray`<`u8`\> | Byte string |

#### Returns

`void`

#### Defined in

[assembly/contracts/Pair.ts:248](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/contracts/Pair.ts#L248)

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

**`Dev`**

Only callable by the factory

#### Defined in

[assembly/contracts/Pair.ts:945](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/contracts/Pair.ts#L945)

___

### getBin

▸ **getBin**(`bs`): `StaticArray`<`u8`\>

Get the reserves of tokens for every bin. This is the amount
of tokenY if `id < _pairInformation.activeId`; of tokenX if `id > _pairInformation.activeId`
and a mix of both if `id == _pairInformation.activeId`

#### Parameters

| Name | Type |
| :------ | :------ |
| `bs` | `StaticArray`<`u8`\> |

#### Returns

`StaticArray`<`u8`\>

#### Defined in

[assembly/contracts/Pair.ts:1045](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/contracts/Pair.ts#L1045)

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

staticArray<u8\> containing :
 -feesX.total The total fees of tokenX
 -feesY.total The total fees of tokenY
 -feesX.protocol The protocol fees of tokenX
 -feesY.protocol The protocol fees of tokenY

#### Defined in

[assembly/contracts/Pair.ts:1077](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/contracts/Pair.ts#L1077)

___

### getOracleParameters

▸ **getOracleParameters**(`_`): `StaticArray`<`u8`\>

View function to get the oracle parameters

#### Parameters

| Name | Type |
| :------ | :------ |
| `_` | `StaticArray`<`u8`\> |

#### Returns

`StaticArray`<`u8`\>

#### Defined in

[assembly/contracts/Pair.ts:1155](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/contracts/Pair.ts#L1155)

___

### getOracleSampleFrom

▸ **getOracleSampleFrom**(`bs`): `StaticArray`<`u8`\>

View function to get the oracle's sample at `_timeDelta` seconds

#### Parameters

| Name | Type |
| :------ | :------ |
| `bs` | `StaticArray`<`u8`\> |

#### Returns

`StaticArray`<`u8`\>

**`Dev`**

Return a linearized sample, the weighted average of 2 neighboring samples

#### Defined in

[assembly/contracts/Pair.ts:1171](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/contracts/Pair.ts#L1171)

___

### getPairInformation

▸ **getPairInformation**(`_`): `StaticArray`<`u8`\>

Get the pair information that is used to track reserves, active ids,
fees and oracle parameters

#### Parameters

| Name | Type |
| :------ | :------ |
| `_` | `StaticArray`<`u8`\> |

#### Returns

`StaticArray`<`u8`\>

#### Defined in

[assembly/contracts/Pair.ts:1009](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/contracts/Pair.ts#L1009)

___

### getUserBins

▸ **getUserBins**(`bs`): `StaticArray`<`u8`\>

Get the deposited bins of an account

#### Parameters

| Name | Type |
| :------ | :------ |
| `bs` | `StaticArray`<`u8`\> |

#### Returns

`StaticArray`<`u8`\>

#### Defined in

[assembly/contracts/Pair.ts:985](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/contracts/Pair.ts#L985)

___

### increaseOracleLength

▸ **increaseOracleLength**(`bs`): `void`

Increases the length of the oracle to the given `_newLength` by adding empty samples to the end of the oracle.
The samples are however initialized to reduce the gas cost of the updates during a swap.

#### Parameters

| Name | Type |
| :------ | :------ |
| `bs` | `StaticArray`<`u8`\> |

#### Returns

`void`

#### Defined in

[assembly/contracts/Pair.ts:820](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/contracts/Pair.ts#L820)

___

### isApprovedForAll

▸ **isApprovedForAll**(`bs`): `StaticArray`<`u8`\>

Returns true if `spender` is approved to transfer `_account`'s tokens

#### Parameters

| Name | Type |
| :------ | :------ |
| `bs` | `StaticArray`<`u8`\> |

#### Returns

`StaticArray`<`u8`\>

True if `spender` is approved to transfer `_account`'s tokens

#### Defined in

[assembly/contracts/Pair.ts:1361](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/contracts/Pair.ts#L1361)

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

[assembly/contracts/Pair.ts:341](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/contracts/Pair.ts#L341)

___

### name

▸ **name**(`_`): `StaticArray`<`u8`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `_` | `StaticArray`<`u8`\> |

#### Returns

`StaticArray`<`u8`\>

The name of the token

#### Defined in

[assembly/contracts/Pair.ts:1292](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/contracts/Pair.ts#L1292)

___

### pendingFees

▸ **pendingFees**(`bs`): `StaticArray`<`u8`\>

View function to get the pending fees of a user
The array must be strictly increasing to ensure uniqueness

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `bs` | `StaticArray`<`u8`\> | Byte string |

#### Returns

`StaticArray`<`u8`\>

#### Defined in

[assembly/contracts/Pair.ts:784](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/contracts/Pair.ts#L784)

___

### safeBatchTransferFrom

▸ **safeBatchTransferFrom**(`bs`): `void`

Batch transfers `_amount` tokens of type `_id` from `_from` to `_to`

#### Parameters

| Name | Type |
| :------ | :------ |
| `bs` | `StaticArray`<`u8`\> |

#### Returns

`void`

#### Defined in

[assembly/contracts/Pair.ts:1425](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/contracts/Pair.ts#L1425)

___

### safeTransferFrom

▸ **safeTransferFrom**(`bs`): `void`

Transfers `_amount` token of type `_id` from `_from` to `_to`

#### Parameters

| Name | Type |
| :------ | :------ |
| `bs` | `StaticArray`<`u8`\> |

#### Returns

`void`

#### Defined in

[assembly/contracts/Pair.ts:1391](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/contracts/Pair.ts#L1391)

___

### setApprovalForAll

▸ **setApprovalForAll**(`bs`): `void`

Grants or revokes permission to `spender` to transfer the caller's tokens, according to `approved`

#### Parameters

| Name | Type |
| :------ | :------ |
| `bs` | `StaticArray`<`u8`\> |

#### Returns

`void`

#### Defined in

[assembly/contracts/Pair.ts:1375](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/contracts/Pair.ts#L1375)

___

### setFeesParameters

▸ **setFeesParameters**(`bs`): `void`

Set the fees parameters

#### Parameters

| Name | Type |
| :------ | :------ |
| `bs` | `StaticArray`<`u8`\> |

#### Returns

`void`

**`Dev`**

Needs to be called by the factory that will validate the values
The bin step will not change
Only callable by the factory

#### Defined in

[assembly/contracts/Pair.ts:1239](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/contracts/Pair.ts#L1239)

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

[assembly/contracts/Pair.ts:133](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/contracts/Pair.ts#L133)

___

### symbol

▸ **symbol**(`_`): `StaticArray`<`u8`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `_` | `StaticArray`<`u8`\> |

#### Returns

`StaticArray`<`u8`\>

The symbol of the token

#### Defined in

[assembly/contracts/Pair.ts:1299](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/contracts/Pair.ts#L1299)

___

### totalSupply

▸ **totalSupply**(`bs`): `StaticArray`<`u8`\>

Returns the total supply of token of type `id`

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `bs` | `StaticArray`<`u8`\> | the token id (serialized) |

#### Returns

`StaticArray`<`u8`\>

**`Dev`**

This is the amount of token of type `id` minted minus the amount burned

#### Defined in

[assembly/contracts/Pair.ts:1308](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/contracts/Pair.ts#L1308)
