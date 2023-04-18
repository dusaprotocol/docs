Pair

# Namespace: Pair

## Table of contents

### Classes

-   [GetFeesReturn](../classes/Pair.GetFeesReturn.md)

### Functions

-   [balanceOf](Pair.md#balanceof)
-   [balanceOfBatch](Pair.md#balanceofbatch)
-   [burn](Pair.md#burn)
-   [collectFees](Pair.md#collectfees)
-   [collectProtocolFees](Pair.md#collectprotocolfees)
-   [constructor](Pair.md#constructor)
-   [findFirstNonEmptyBinId](Pair.md#findfirstnonemptybinid)
-   [flashLoan](Pair.md#flashloan)
-   [forceDecay](Pair.md#forcedecay)
-   [getBin](Pair.md#getbin)
-   [getGlobalFees](Pair.md#getglobalfees)
-   [getPairInformation](Pair.md#getpairinformation)
-   [getUserBins](Pair.md#getuserbins)
-   [isApprovedForAll](Pair.md#isapprovedforall)
-   [mint](Pair.md#mint)
-   [name](Pair.md#name)
-   [pendingFees](Pair.md#pendingfees)
-   [safeBatchTransferFrom](Pair.md#safebatchtransferfrom)
-   [safeTransferFrom](Pair.md#safetransferfrom)
-   [setApprovalForAll](Pair.md#setapprovalforall)
-   [setFeesParameters](Pair.md#setfeesparameters)
-   [swap](Pair.md#swap)
-   [symbol](Pair.md#symbol)
-   [totalSupply](Pair.md#totalsupply)

## Functions

### balanceOf

▸ **balanceOf**(`bs`): `StaticArray`<`u8`\>

#### Parameters

| Name | Type                 |
| :--- | :------------------- |
| `bs` | `StaticArray`<`u8`\> |

#### Returns

`StaticArray`<`u8`\>

#### Defined in

[assembly/contracts/Pair.ts:871](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/contracts/Pair.ts#L871)

---

### balanceOfBatch

▸ **balanceOfBatch**(`bs`): `StaticArray`<`u8`\>

#### Parameters

| Name | Type                 |
| :--- | :------------------- |
| `bs` | `StaticArray`<`u8`\> |

#### Returns

`StaticArray`<`u8`\>

#### Defined in

[assembly/contracts/Pair.ts:884](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/contracts/Pair.ts#L884)

---

### burn

▸ **burn**(`bs`): `StaticArray`<`u8`\>

Burns LB tokens and sends the corresponding amounts of tokens to `_to`. The amount of tokens sent is
determined by the ratio of the amount of LB tokens burned to the total supply of LB tokens in the bin.
This function will not transfer the LB Tokens from the caller, it is expected that the tokens have already been
transferred to this contract through another contract.
That is why this function shouldn't be called directly, but through one of the remove liquidity functions of the router
that will also perform safety checks.

#### Parameters

| Name | Type                 | Description |
| :--- | :------------------- | :---------- |
| `bs` | `StaticArray`<`u8`\> | Byte string |

#### Returns

`StaticArray`<`u8`\>

#### Defined in

[assembly/contracts/Pair.ts:400](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/contracts/Pair.ts#L400)

---

### collectFees

▸ **collectFees**(`bs`): `StaticArray`<`u8`\>

Collect the fees accumulated by a user.

#### Parameters

| Name | Type                 | Description |
| :--- | :------------------- | :---------- |
| `bs` | `StaticArray`<`u8`\> | Byte string |

#### Returns

`StaticArray`<`u8`\>

#### Defined in

[assembly/contracts/Pair.ts:488](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/contracts/Pair.ts#L488)

---

### collectProtocolFees

▸ **collectProtocolFees**(`_`): `StaticArray`<`u8`\>

Collect the protocol fees and send them to the fee recipient.
The protocol fees are not set to zero to save gas by not resetting the storage slot.

#### Parameters

| Name | Type                 |
| :--- | :------------------- |
| `_`  | `StaticArray`<`u8`\> |

#### Returns

`StaticArray`<`u8`\>

#### Defined in

[assembly/contracts/Pair.ts:544](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/contracts/Pair.ts#L544)

---

### constructor

▸ **constructor**(`bs`): `void`

#### Parameters

| Name | Type                 |
| :--- | :------------------- |
| `bs` | `StaticArray`<`u8`\> |

#### Returns

`void`

#### Defined in

[assembly/contracts/Pair.ts:42](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/contracts/Pair.ts#L42)

---

### findFirstNonEmptyBinId

▸ **findFirstNonEmptyBinId**(`bs`): `StaticArray`<`u8`\>

#### Parameters

| Name | Type                 |
| :--- | :------------------- |
| `bs` | `StaticArray`<`u8`\> |

#### Returns

`StaticArray`<`u8`\>

#### Defined in

[assembly/contracts/Pair.ts:821](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/contracts/Pair.ts#L821)

---

### flashLoan

▸ **flashLoan**(`bs`): `StaticArray`<`u8`\>

Perform a flashloan on one of the tokens of the pair. The flashloan will call the `_receiver` contract
to perform the desired operations. The `_receiver` contract is expected to transfer the `amount + fee` of the
token to this contract.

#### Parameters

| Name | Type                 | Description |
| :--- | :------------------- | :---------- |
| `bs` | `StaticArray`<`u8`\> | Byte string |

#### Returns

`StaticArray`<`u8`\>

#### Defined in

[assembly/contracts/Pair.ts:152](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/contracts/Pair.ts#L152)

---

### forceDecay

▸ **forceDecay**(`_`): `void`

Force the decaying of the references for volatility and index

#### Parameters

| Name | Type                 | Description |
| :--- | :------------------- | :---------- |
| `_`  | `StaticArray`<`u8`\> | unused      |

#### Returns

`void`

#### Defined in

[assembly/contracts/Pair.ts:810](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/contracts/Pair.ts#L810)

---

### getBin

▸ **getBin**(`bs`): `StaticArray`<`u8`\>

#### Parameters

| Name | Type                 |
| :--- | :------------------- |
| `bs` | `StaticArray`<`u8`\> |

#### Returns

`StaticArray`<`u8`\>

#### Defined in

[assembly/contracts/Pair.ts:667](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/contracts/Pair.ts#L667)

---

### getGlobalFees

▸ **getGlobalFees**(`_`): `StaticArray`<`u8`\>

View function to get the total fees and the protocol fees of each tokens

#### Parameters

| Name | Type                 | Description |
| :--- | :------------------- | :---------- |
| `_`  | `StaticArray`<`u8`\> | unused      |

#### Returns

`StaticArray`<`u8`\>

bs containing :
-feesXTotal The total fees of tokenX
-feesYTotal The total fees of tokenY
-feesXProtocol The protocol fees of tokenX
-feesYProtocol The protocol fees of tokenY

#### Defined in

[assembly/contracts/Pair.ts:692](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/contracts/Pair.ts#L692)

---

### getPairInformation

▸ **getPairInformation**(`_`): `StaticArray`<`u8`\>

#### Parameters

| Name | Type                 |
| :--- | :------------------- |
| `_`  | `StaticArray`<`u8`\> |

#### Returns

`StaticArray`<`u8`\>

#### Defined in

[assembly/contracts/Pair.ts:645](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/contracts/Pair.ts#L645)

---

### getUserBins

▸ **getUserBins**(`bs`): `StaticArray`<`u8`\>

#### Parameters

| Name | Type                 |
| :--- | :------------------- |
| `bs` | `StaticArray`<`u8`\> |

#### Returns

`StaticArray`<`u8`\>

#### Defined in

[assembly/contracts/Pair.ts:626](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/contracts/Pair.ts#L626)

---

### isApprovedForAll

▸ **isApprovedForAll**(`bs`): `StaticArray`<`u8`\>

#### Parameters

| Name | Type                 |
| :--- | :------------------- |
| `bs` | `StaticArray`<`u8`\> |

#### Returns

`StaticArray`<`u8`\>

#### Defined in

[assembly/contracts/Pair.ts:905](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/contracts/Pair.ts#L905)

---

### mint

▸ **mint**(`bs`): `StaticArray`<`u8`\>

Mint new LB tokens for each bins where the user adds liquidity.
This function will not transfer the tokens from the caller, it is expected that the tokens have already been
transferred to this contract through another contract.
That is why this function shouldn't be called directly, but through one of the add liquidity functions of the
router that will also perform safety checks.

#### Parameters

| Name | Type                 | Description |
| :--- | :------------------- | :---------- |
| `bs` | `StaticArray`<`u8`\> | Byte string |

#### Returns

`StaticArray`<`u8`\>

#### Defined in

[assembly/contracts/Pair.ts:224](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/contracts/Pair.ts#L224)

---

### name

▸ **name**(`_`): `StaticArray`<`u8`\>

#### Parameters

| Name | Type                 |
| :--- | :------------------- |
| `_`  | `StaticArray`<`u8`\> |

#### Returns

`StaticArray`<`u8`\>

#### Defined in

[assembly/contracts/Pair.ts:847](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/contracts/Pair.ts#L847)

---

### pendingFees

▸ **pendingFees**(`bs`): `StaticArray`<`u8`\>

#### Parameters

| Name | Type                 |
| :--- | :------------------- |
| `bs` | `StaticArray`<`u8`\> |

#### Returns

`StaticArray`<`u8`\>

#### Defined in

[assembly/contracts/Pair.ts:590](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/contracts/Pair.ts#L590)

---

### safeBatchTransferFrom

▸ **safeBatchTransferFrom**(`bs`): `StaticArray`<`u8`\>

#### Parameters

| Name | Type                 |
| :--- | :------------------- |
| `bs` | `StaticArray`<`u8`\> |

#### Returns

`StaticArray`<`u8`\>

#### Defined in

[assembly/contracts/Pair.ts:959](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/contracts/Pair.ts#L959)

---

### safeTransferFrom

▸ **safeTransferFrom**(`bs`): `StaticArray`<`u8`\>

#### Parameters

| Name | Type                 |
| :--- | :------------------- |
| `bs` | `StaticArray`<`u8`\> |

#### Returns

`StaticArray`<`u8`\>

#### Defined in

[assembly/contracts/Pair.ts:933](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/contracts/Pair.ts#L933)

---

### setApprovalForAll

▸ **setApprovalForAll**(`bs`): `StaticArray`<`u8`\>

#### Parameters

| Name | Type                 |
| :--- | :------------------- |
| `bs` | `StaticArray`<`u8`\> |

#### Returns

`StaticArray`<`u8`\>

#### Defined in

[assembly/contracts/Pair.ts:917](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/contracts/Pair.ts#L917)

---

### setFeesParameters

▸ **setFeesParameters**(`bs`): `void`

#### Parameters

| Name | Type                 |
| :--- | :------------------- |
| `bs` | `StaticArray`<`u8`\> |

#### Returns

`void`

#### Defined in

[assembly/contracts/Pair.ts:746](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/contracts/Pair.ts#L746)

---

### swap

▸ **swap**(`bs`): `StaticArray`<`u8`\>

Swap tokens iterating over the bins until the entire amount is swapped.
Will swap token X for token Y if `_swapForY` is true, and token Y for token X if `_swapForY` is false.
This function will not transfer the tokens from the caller, it is expected that the tokens have already been
transferred to this contract through another contract.
That is why this function shouldn't be called directly, but through one of the swap functions of the router
that will also perform safety checks.

#### Parameters

| Name | Type                 | Description |
| :--- | :------------------- | :---------- |
| `bs` | `StaticArray`<`u8`\> | Byte string |

#### Returns

`StaticArray`<`u8`\>

#### Defined in

[assembly/contracts/Pair.ts:74](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/contracts/Pair.ts#L74)

---

### symbol

▸ **symbol**(`_`): `StaticArray`<`u8`\>

#### Parameters

| Name | Type                 |
| :--- | :------------------- |
| `_`  | `StaticArray`<`u8`\> |

#### Returns

`StaticArray`<`u8`\>

#### Defined in

[assembly/contracts/Pair.ts:851](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/contracts/Pair.ts#L851)

---

### totalSupply

▸ **totalSupply**(`bs`): `StaticArray`<`u8`\>

#### Parameters

| Name | Type                 |
| :--- | :------------------- |
| `bs` | `StaticArray`<`u8`\> |

#### Returns

`StaticArray`<`u8`\>

#### Defined in

[assembly/contracts/Pair.ts:859](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/contracts/Pair.ts#L859)
