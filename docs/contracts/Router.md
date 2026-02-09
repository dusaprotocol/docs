# Router

## Table of contents

### Functions

- [addLiquidity](Router.md#addliquidity)
- [addLiquidityMAS](Router.md#addliquiditymas)
- [constructor](Router.md#constructor)
- [createLBPair](Router.md#createlbpair)
- [getSwapIn](Router.md#getswapin)
- [getSwapOut](Router.md#getswapout)
- [receiveCoins](Router.md#receivecoins)
- [removeLiquidity](Router.md#removeliquidity)
- [removeLiquidityMAS](Router.md#removeliquiditymas)
- [swapExactMASForTokens](Router.md#swapexactmasfortokens)
- [swapExactMASForTokensSupportingFeeOnTransferTokens](Router.md#swapexactmasfortokenssupportingfeeontransfertokens)
- [swapExactTokensForMAS](Router.md#swapexacttokensformas)
- [swapExactTokensForMASSupportingFeeOnTransferTokens](Router.md#swapexacttokensformassupportingfeeontransfertokens)
- [swapExactTokensForTokens](Router.md#swapexacttokensfortokens)
- [swapExactTokensForTokensSupportingFeeOnTransferTokens](Router.md#swapexacttokensfortokenssupportingfeeontransfertokens)
- [swapMASForExactTokens](Router.md#swapmasforexacttokens)
- [swapTokensForExactMAS](Router.md#swaptokensforexactmas)
- [swapTokensForExactTokens](Router.md#swaptokensforexacttokens)
- [sweep](Router.md#sweep)
- [sweepLBToken](Router.md#sweeplbtoken)

## Functions

### addLiquidity

▸ **addLiquidity**(`bs`): `StaticArray`<`u8`\>

Add liquidity while performing safety checks
This function is compliant with fee on transfer tokens

#### Parameters

| Name | Type                 | Description                                     |
| :--- | :------------------- | :---------------------------------------------- |
| `bs` | `StaticArray`<`u8`\> | Byte string containing The liquidity parameters |

#### Returns

`StaticArray`<`u8`\>

- Byte string containing:
- liquidityMinted: Amounts of LBToken minted for each bin
- depositIds: Bin ids where the liquidity was actually deposited

#### Defined in

[assembly/contracts/Router.ts:116](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/contracts/Router.ts#L116)

---

### addLiquidityMAS

▸ **addLiquidityMAS**(`bs`): `StaticArray`<`u8`\>

Add liquidity with MAS while performing safety checks
This function is compliant with fee on transfer tokens

#### Parameters

| Name | Type                 | Description                                                                                    |
| :--- | :------------------- | :--------------------------------------------------------------------------------------------- |
| `bs` | `StaticArray`<`u8`\> | Byte string containing - The liquidity parameters - The amount of MAS to send for storage fees |

#### Returns

`StaticArray`<`u8`\>

- Byte string containing:
- liquidityMinted: Amounts of LBToken minted for each bin
- depositIds: Bin ids where the liquidity was actually deposited

#### Defined in

[assembly/contracts/Router.ts:168](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/contracts/Router.ts#L168)

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

[assembly/contracts/Router.ts:51](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/contracts/Router.ts#L51)

---

### createLBPair

▸ **createLBPair**(`bs`): `StaticArray`<`u8`\>

Create a liquidity bin LBPair for \_tokenX and \_tokenY using the factory

#### Parameters

| Name | Type                 | Description                                                                                                                                                                         |
| :--- | :------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `bs` | `StaticArray`<`u8`\> | Byte string containing: - \_tokenX: Address of the first token - \_tokenY: Address of the second token4 - \_activeId: The activeId of the pair - \_binStep: The binStep of the pair |

#### Returns

`StaticArray`<`u8`\>

- Byte string containing the address of the newly created LBPair

#### Defined in

[assembly/contracts/Router.ts:89](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/contracts/Router.ts#L89)

---

### getSwapIn

▸ **getSwapIn**(`bs`): `StaticArray`<`u8`\>

Simulate a swap in

#### Parameters

| Name | Type                 |
| :--- | :------------------- |
| `bs` | `StaticArray`<`u8`\> |

#### Returns

`StaticArray`<`u8`\>

#### Defined in

[assembly/contracts/Router.ts:1381](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/contracts/Router.ts#L1381)

---

### getSwapOut

▸ **getSwapOut**(`bs`): `StaticArray`<`u8`\>

Simulate a swap out

#### Parameters

| Name | Type                 |
| :--- | :------------------- |
| `bs` | `StaticArray`<`u8`\> |

#### Returns

`StaticArray`<`u8`\>

#### Defined in

[assembly/contracts/Router.ts:1396](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/contracts/Router.ts#L1396)

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

[assembly/contracts/Router.ts:1535](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/contracts/Router.ts#L1535)

---

### removeLiquidity

▸ **removeLiquidity**(`bs`): `StaticArray`<`u8`\>

Remove liquidity while performing safety checks
This function is compliant with fee on transfer tokens

#### Parameters

| Name | Type                 | Description                                                                                                                                                                                                                                                                                                                                                                                                 |
| :--- | :------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `bs` | `StaticArray`<`u8`\> | Byte string containing: - \_tokenX: Address of the first token - \_tokenY: Address of the second token - \_binStep: The binStep of the pair - \_amountXMin: The minimum amount of tokenX to receive - \_amountYMin: The minimum amount of tokenY to receive - \_ids: The list of bin ids - \_amounts: The list of amounts to remove - \_to: The address of the recipient - deadline: The deadline timestamp |

#### Returns

`StaticArray`<`u8`\>

- Byte string containing:
- amountX: The amount of tokenX received
- amountY: The amount of tokenY received

#### Defined in

[assembly/contracts/Router.ts:254](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/contracts/Router.ts#L254)

---

### removeLiquidityMAS

▸ **removeLiquidityMAS**(`bs`): `StaticArray`<`u8`\>

Remove liquidity with MAS while performing safety checks
This function is compliant with fee on transfer tokens

#### Parameters

| Name | Type                 | Description                                                                                                                                                                                                                                                                                                                                                                                                 |
| :--- | :------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `bs` | `StaticArray`<`u8`\> | Byte string containing: - \_tokenX: Address of the first token - \_tokenY: Address of the second token - \_binStep: The binStep of the pair - \_amountXMin: The minimum amount of tokenX to receive - \_amountYMin: The minimum amount of tokenY to receive - \_ids: The list of bin ids - \_amounts: The list of amounts to remove - \_to: The address of the recipient - deadline: The deadline timestamp |

#### Returns

`StaticArray`<`u8`\>

- Byte string containing:
- amountX: The amount of tokenX received
- amountY: The amount of tokenY received

#### Defined in

[assembly/contracts/Router.ts:321](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/contracts/Router.ts#L321)

---

### swapExactMASForTokens

▸ **swapExactMASForTokens**(`bs`): `StaticArray`<`u8`\>

Swaps exact MAS for tokens while performing safety checks

#### Parameters

| Name | Type                 | Description                                                                                                                                                                                                                                                                                                                                                                     |
| :--- | :------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `bs` | `StaticArray`<`u8`\> | Byte string containing: - amountOutMin: The minimum amount of token to receive - pairBinSteps: The bin steps of the pairs - isLegacyPools: If the pairs are legacy pairs - tokenPath: The swap path using the bin steps following `_pairBinSteps` - to: The address of the recipient - deadline: The deadline timestamp - masToSend: The amount of MAS to send for storage fees |

#### Returns

`StaticArray`<`u8`\>

- Byte string containing Output amount of the swap

#### Defined in

[assembly/contracts/Router.ts:503](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/contracts/Router.ts#L503)

---

### swapExactMASForTokensSupportingFeeOnTransferTokens

▸ **swapExactMASForTokensSupportingFeeOnTransferTokens**(`bs`): `StaticArray`<`u8`\>

Swaps exact MAS for tokens while performing safety checks supporting for fee on transfer tokens

#### Parameters

| Name | Type                 | Description                                                                                                                                                                                                                                                                                                                                                                 |
| :--- | :------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `bs` | `StaticArray`<`u8`\> | Byte string containing: - amountOutMin: The min amount of token to receive - pairBinSteps: The bin steps of the pairs - isLegacyPools: If the pairs are legacy pairs - tokenPath: The swap path using the bin steps following `_pairBinSteps` - to: The address of the recipient - deadline: The deadline timestamp - masToSend: The amount of MAS to send for storage fees |

#### Returns

`StaticArray`<`u8`\>

- Byte string containing the output amount of the swap

#### Defined in

[assembly/contracts/Router.ts:908](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/contracts/Router.ts#L908)

---

### swapExactTokensForMAS

▸ **swapExactTokensForMAS**(`bs`): `StaticArray`<`u8`\>

Swaps exact tokens for MAS while performing safety checks

#### Parameters

| Name | Type                 | Description                                                                                                                                                                                                                                                                                                                                                      |
| :--- | :------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `bs` | `StaticArray`<`u8`\> | Byte string containing: - amountIn: The amount of token to swap - amountOutMinMAS: The minimum amount of MAS to receive - pairBinSteps: The bin steps of the pairs - isLegacyPools: If the pairs are legacy pairs - tokenPath: The swap path using the bin steps following `_pairBinSteps` - to: The address of the recipient - deadline: The deadline timestamp |

#### Returns

`StaticArray`<`u8`\>

- Byte string containing Output amount of the swap

#### Defined in

[assembly/contracts/Router.ts:437](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/contracts/Router.ts#L437)

---

### swapExactTokensForMASSupportingFeeOnTransferTokens

▸ **swapExactTokensForMASSupportingFeeOnTransferTokens**(`bs`): `StaticArray`<`u8`\>

Swaps exact tokens for MAS while performing safety checks supporting for fee on transfer tokens

#### Parameters

| Name | Type                 | Description                                                                                                                                                                                                                                                                                                                                                  |
| :--- | :------------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `bs` | `StaticArray`<`u8`\> | Byte string containing: - amountIn: The amount of token to send - amountOutMinMAS: The min amount of MAS to receive - pairBinSteps: The bin steps of the pairs - isLegacyPools: If the pairs are legacy pairs - tokenPath: The swap path using the bin steps following `_pairBinSteps` - to: The address of the recipient - deadline: The deadline timestamp |

#### Returns

`StaticArray`<`u8`\>

- Byte string containing the output amount of the swap

#### Defined in

[assembly/contracts/Router.ts:835](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/contracts/Router.ts#L835)

---

### swapExactTokensForTokens

▸ **swapExactTokensForTokens**(`bs`): `StaticArray`<`u8`\>

Swap tokens while performing safety checks

#### Parameters

| Name | Type                 | Description                                                                                                                                                                                                                                                                                                                                                     |
| :--- | :------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `bs` | `StaticArray`<`u8`\> | Byte string containing: - amountIn: The amount of token to swap - amountOutMin: The minimum amount of token to receive - pairBinSteps: The bin steps of the pairs - isLegacyPools: If the pairs are legacy pairs - tokenPath: The swap path using the bin steps following `_pairBinSteps` - to: The address of the recipient - deadline: The deadline timestamp |

#### Returns

`StaticArray`<`u8`\>

- Byte string containing Output amount of the swap

#### Defined in

[assembly/contracts/Router.ts:382](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/contracts/Router.ts#L382)

---

### swapExactTokensForTokensSupportingFeeOnTransferTokens

▸ **swapExactTokensForTokensSupportingFeeOnTransferTokens**(`bs`): `StaticArray`<`u8`\>

Swaps exact tokens for tokens while performing safety checks supporting for fee on transfer tokens

#### Parameters

| Name | Type                 | Description                                                                                                                                                                                                                                                                                                                                                 |
| :--- | :------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `bs` | `StaticArray`<`u8`\> | Byte string containing: - amountIn: The amount of token to send - amountOutMin: The min amount of token to receive - pairBinSteps: The bin steps of the pairs - isLegacyPools: If the pairs are legacy pairs - tokenPath: The swap path using the bin steps following `_pairBinSteps` - to: The address of the recipient - deadline: The deadline timestamp |

#### Returns

`StaticArray`<`u8`\>

- Byte string containing the output amount of the swap

#### Defined in

[assembly/contracts/Router.ts:776](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/contracts/Router.ts#L776)

---

### swapMASForExactTokens

▸ **swapMASForExactTokens**(`bs`): `StaticArray`<`u8`\>

Swaps MAS for exact tokens while performing safety checks

#### Parameters

| Name | Type                 | Description                                                                                                                                                                                                                                                                                                                                                          |
| :--- | :------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `bs` | `StaticArray`<`u8`\> | Byte string containing: - amountOut: The amount of token to receive - pairBinSteps: The bin steps of the pairs - isLegacyPools: If the pairs are legacy pairs - tokenPath: The swap path using the bin steps following `_pairBinSteps` - to: The address of the recipient - deadline: The deadline timestamp - masToSend: The amount of MAS to send for storage fees |

#### Returns

`StaticArray`<`u8`\>

- Byte string containing the output amount of the swap

#### Defined in

[assembly/contracts/Router.ts:702](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/contracts/Router.ts#L702)

---

### swapTokensForExactMAS

▸ **swapTokensForExactMAS**(`bs`): `StaticArray`<`u8`\>

Swaps tokens for exact MAS while performing safety checks

#### Parameters

| Name | Type                 | Description                                                                                                                                                                                                                                                                                                                                                   |
| :--- | :------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `bs` | `StaticArray`<`u8`\> | Byte string containing: - amountOut: The amount of MAS to receive - amountInMax: The maximum amount of token to send - pairBinSteps: The bin steps of the pairs - isLegacyPools: If the pairs are legacy pairs - tokenPath: The swap path using the bin steps following `_pairBinSteps` - to: The address of the recipient - deadline: The deadline timestamp |

#### Returns

`StaticArray`<`u8`\>

- Byte string containing the output amount of the swap

#### Defined in

[assembly/contracts/Router.ts:627](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/contracts/Router.ts#L627)

---

### swapTokensForExactTokens

▸ **swapTokensForExactTokens**(`bs`): `StaticArray`<`u8`\>

Swaps tokens for exact tokens while performing safety checks

#### Parameters

| Name | Type                 | Description                                                                                                                                                                                                                                                                                                                                                     |
| :--- | :------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `bs` | `StaticArray`<`u8`\> | Byte string containing: - amountOut: The amount of token to receive - amountInMax: The maximum amount of token to send - pairBinSteps: The bin steps of the pairs - isLegacyPools: If the pairs are legacy pairs - tokenPath: The swap path using the bin steps following `_pairBinSteps` - to: The address of the recipient - deadline: The deadline timestamp |

#### Returns

`StaticArray`<`u8`\>

- Byte string containing the output amount of the swap

#### Defined in

[assembly/contracts/Router.ts:566](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/contracts/Router.ts#L566)

---

### sweep

▸ **sweep**(`bs`): `void`

Unstuck tokens that are sent to this contract by mistake

#### Parameters

| Name | Type                 |
| :--- | :------------------- |
| `bs` | `StaticArray`<`u8`\> |

#### Returns

`void`

**`Dev`**

Only callable by the factory owner

#### Defined in

[assembly/contracts/Router.ts:971](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/contracts/Router.ts#L971)

---

### sweepLBToken

▸ **sweepLBToken**(`bs`): `void`

Unstuck LBTokens that are sent to this contract by mistake

#### Parameters

| Name | Type                 |
| :--- | :------------------- |
| `bs` | `StaticArray`<`u8`\> |

#### Returns

`void`

**`Dev`**

Only callable by the factory owner

#### Defined in

[assembly/contracts/Router.ts:998](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/contracts/Router.ts#L998)
