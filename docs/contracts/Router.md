# Router

## Table of contents

### Functions

- [addLiquidity](Router.md#addliquidity)
- [addLiquidityMAS](Router.md#addliquiditymas)
- [constructor](Router.md#constructor)
- [createLBPair](Router.md#createlbpair)
- [getSwapIn](Router.md#getswapin)
- [getSwapOut](Router.md#getswapout)
- [removeLiquidity](Router.md#removeliquidity)
- [removeLiquidityMAS](Router.md#removeliquiditymas)
- [swapExactMASForTokens](Router.md#swapexactmasfortokens)
- [swapExactTokensForMAS](Router.md#swapexacttokensformas)
- [swapExactTokensForTokens](Router.md#swapexacttokensfortokens)
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

| Name | Type | Description |
| :------ | :------ | :------ |
| `bs` | `StaticArray`<`u8`\> | Byte string containing The liquidity parameters |

#### Returns

`StaticArray`<`u8`\>

- Byte string containing:
- liquidityMinted: Amounts of LBToken minted for each bin
- depositIds: Bin ids where the liquidity was actually deposited

#### Defined in

[assembly/contracts/Router.ts:87](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/contracts/Router.ts#L87)

___

### addLiquidityMAS

▸ **addLiquidityMAS**(`bs`): `StaticArray`<`u8`\>

Add liquidity with MAS while performing safety checks
This function is compliant with fee on transfer tokens

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `bs` | `StaticArray`<`u8`\> | Byte string containing The liquidity parameters |

#### Returns

`StaticArray`<`u8`\>

- Byte string containing:
- liquidityMinted: Amounts of LBToken minted for each bin
- depositIds: Bin ids where the liquidity was actually deposited

#### Defined in

[assembly/contracts/Router.ts:129](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/contracts/Router.ts#L129)

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

[assembly/contracts/Router.ts:36](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/contracts/Router.ts#L36)

___

### createLBPair

▸ **createLBPair**(`bs`): `StaticArray`<`u8`\>

Create a liquidity bin LBPair for _tokenX and _tokenY using the factory

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `bs` | `StaticArray`<`u8`\> | Byte string containing: - _tokenX: Address of the first token - _tokenY: Address of the second token4 - _activeId: The activeId of the pair - _binStep: The binStep of the pair |

#### Returns

`StaticArray`<`u8`\>

- Byte string containing the address of the newly created LBPair

#### Defined in

[assembly/contracts/Router.ts:66](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/contracts/Router.ts#L66)

___

### getSwapIn

▸ **getSwapIn**(`bs`): `StaticArray`<`u8`\>

Simulate a swap in

#### Parameters

| Name | Type |
| :------ | :------ |
| `bs` | `StaticArray`<`u8`\> |

#### Returns

`StaticArray`<`u8`\>

#### Defined in

[assembly/contracts/Router.ts:908](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/contracts/Router.ts#L908)

___

### getSwapOut

▸ **getSwapOut**(`bs`): `StaticArray`<`u8`\>

Simulate a swap out

#### Parameters

| Name | Type |
| :------ | :------ |
| `bs` | `StaticArray`<`u8`\> |

#### Returns

`StaticArray`<`u8`\>

#### Defined in

[assembly/contracts/Router.ts:923](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/contracts/Router.ts#L923)

___

### removeLiquidity

▸ **removeLiquidity**(`bs`): `StaticArray`<`u8`\>

Remove liquidity while performing safety checks
This function is compliant with fee on transfer tokens

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `bs` | `StaticArray`<`u8`\> | Byte string containing: - _tokenX: Address of the first token - _tokenY: Address of the second token - _binStep: The binStep of the pair - _amountXMin: The minimum amount of tokenX to receive - _amountYMin: The minimum amount of tokenY to receive - _ids: The list of bin ids - _amounts: The list of amounts to remove - _to: The address of the recipient - deadline: The deadline timestamp |

#### Returns

`StaticArray`<`u8`\>

- Byte string containing:
- amountX: The amount of tokenX received
- amountY: The amount of tokenY received

#### Defined in

[assembly/contracts/Router.ts:204](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/contracts/Router.ts#L204)

___

### removeLiquidityMAS

▸ **removeLiquidityMAS**(`bs`): `StaticArray`<`u8`\>

Remove liquidity with MAS while performing safety checks
This function is compliant with fee on transfer tokens

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `bs` | `StaticArray`<`u8`\> | Byte string containing: - _tokenX: Address of the first token - _tokenY: Address of the second token - _binStep: The binStep of the pair - _amountXMin: The minimum amount of tokenX to receive - _amountYMin: The minimum amount of tokenY to receive - _ids: The list of bin ids - _amounts: The list of amounts to remove - _to: The address of the recipient - deadline: The deadline timestamp |

#### Returns

`StaticArray`<`u8`\>

- Byte string containing:
- amountX: The amount of tokenX received
- amountY: The amount of tokenY received

#### Defined in

[assembly/contracts/Router.ts:266](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/contracts/Router.ts#L266)

___

### swapExactMASForTokens

▸ **swapExactMASForTokens**(`bs`): `StaticArray`<`u8`\>

Swaps exact MAS for tokens while performing safety checks

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `bs` | `StaticArray`<`u8`\> | Byte string containing: - amountOutMin: The minimum amount of token to receive - pairBinSteps: The bin steps of the pairs - tokenPath: The swap path using the bin steps following `_pairBinSteps` - to: The address of the recipient - deadline: The deadline timestamp |

#### Returns

`StaticArray`<`u8`\>

- Byte string containing Output amount of the swap

#### Defined in

[assembly/contracts/Router.ts:413](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/contracts/Router.ts#L413)

___

### swapExactTokensForMAS

▸ **swapExactTokensForMAS**(`bs`): `StaticArray`<`u8`\>

Swaps exact tokens for MAS while performing safety checks

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `bs` | `StaticArray`<`u8`\> | Byte string containing: - amountIn: The amount of token to swap - amountOutMinMAS: The minimum amount of MAS to receive - pairBinSteps: The bin steps of the pairs - tokenPath: The swap path using the bin steps following `_pairBinSteps` - to: The address of the recipient - deadline: The deadline timestamp |

#### Returns

`StaticArray`<`u8`\>

- Byte string containing Output amount of the swap

#### Defined in

[assembly/contracts/Router.ts:357](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/contracts/Router.ts#L357)

___

### swapExactTokensForTokens

▸ **swapExactTokensForTokens**(`bs`): `StaticArray`<`u8`\>

Swap tokens while performing safety checks

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `bs` | `StaticArray`<`u8`\> | Byte string containing: - amountIn: The amount of token to swap - amountOutMin: The minimum amount of token to receive - pairBinSteps: The bin steps of the pairs - tokenPath: The swap path using the bin steps following `_pairBinSteps` - to: The address of the recipient - deadline: The deadline timestamp |

#### Returns

`StaticArray`<`u8`\>

- Byte string containing Output amount of the swap

#### Defined in

[assembly/contracts/Router.ts:316](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/contracts/Router.ts#L316)

___

### swapMASForExactTokens

▸ **swapMASForExactTokens**(`bs`): `StaticArray`<`u8`\>

Swaps MAS for exact tokens while performing safety checks

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `bs` | `StaticArray`<`u8`\> | Byte string containing: - amountOut: The amount of token to receive - pairBinSteps: The bin steps of the pairs - tokenPath: The swap path using the bin steps following `_pairBinSteps` - to: The address of the recipient - deadline: The deadline timestamp |

#### Returns

`StaticArray`<`u8`\>

- Byte string containing Input amount of the swap

#### Defined in

[assembly/contracts/Router.ts:576](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/contracts/Router.ts#L576)

___

### swapTokensForExactMAS

▸ **swapTokensForExactMAS**(`bs`): `StaticArray`<`u8`\>

Swaps tokens for exact MAS while performing safety checks

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `bs` | `StaticArray`<`u8`\> | Byte string containing: - amountOut: The amount of MAS to receive - amountInMax: The maximum amount of token to send - pairBinSteps: The bin steps of the pairs - tokenPath: The swap path using the bin steps following `_pairBinSteps` - to: The address of the recipient - deadline: The deadline timestamp |

#### Returns

`StaticArray`<`u8`\>

- Byte string containing Input amount of the swap

#### Defined in

[assembly/contracts/Router.ts:517](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/contracts/Router.ts#L517)

___

### swapTokensForExactTokens

▸ **swapTokensForExactTokens**(`bs`): `StaticArray`<`u8`\>

Swaps tokens for exact tokens while performing safety checks

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `bs` | `StaticArray`<`u8`\> | Byte string containing: - amountOut: The amount of token to receive - amountInMax: The maximum amount of token to send - pairBinSteps: The bin steps of the pairs - tokenPath: The swap path using the bin steps following `_pairBinSteps` - to: The address of the recipient - deadline: The deadline timestamp |

#### Returns

`StaticArray`<`u8`\>

- Byte string containing Input amount of the swap

#### Defined in

[assembly/contracts/Router.ts:465](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/contracts/Router.ts#L465)

___

### sweep

▸ **sweep**(`bs`): `void`

Unstuck tokens that are sent to this contract by mistake

#### Parameters

| Name | Type |
| :------ | :------ |
| `bs` | `StaticArray`<`u8`\> |

#### Returns

`void`

**`Dev`**

Only callable by the factory owner

#### Defined in

[assembly/contracts/Router.ts:636](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/contracts/Router.ts#L636)

___

### sweepLBToken

▸ **sweepLBToken**(`bs`): `void`

Unstuck LBTokens that are sent to this contract by mistake

#### Parameters

| Name | Type |
| :------ | :------ |
| `bs` | `StaticArray`<`u8`\> |

#### Returns

`void`

**`Dev`**

Only callable by the factory owner

#### Defined in

[assembly/contracts/Router.ts:663](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/contracts/Router.ts#L663)
