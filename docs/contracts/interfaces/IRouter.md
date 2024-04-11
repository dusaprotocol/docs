# IRouter

## Table of contents

### Constructors

- [constructor](IRouter.md#constructor)

### Properties

- [\_origin](IRouter.md#_origin)

### Methods

- [addLiquidity](IRouter.md#addliquidity)
- [addLiquidityMAS](IRouter.md#addliquiditymas)
- [createLBPair](IRouter.md#createlbpair)
- [getSwapIn](IRouter.md#getswapin)
- [getSwapOut](IRouter.md#getswapout)
- [init](IRouter.md#init)
- [removeLiquidity](IRouter.md#removeliquidity)
- [removeLiquidityMAS](IRouter.md#removeliquiditymas)
- [swapExactMASForTokens](IRouter.md#swapexactmasfortokens)
- [swapExactMASForTokensSupportingFeeOnTransferTokens](IRouter.md#swapexactmasfortokenssupportingfeeontransfertokens)
- [swapExactTokensForMAS](IRouter.md#swapexacttokensformas)
- [swapExactTokensForMASSupportingFeeOnTransferTokens](IRouter.md#swapexacttokensformassupportingfeeontransfertokens)
- [swapExactTokensForTokens](IRouter.md#swapexacttokensfortokens)
- [swapExactTokensForTokensSupportingFeeOnTransferTokens](IRouter.md#swapexacttokensfortokenssupportingfeeontransfertokens)
- [swapMASForExactTokens](IRouter.md#swapmasforexacttokens)
- [swapTokensForExactMAS](IRouter.md#swaptokensforexactmas)
- [swapTokensForExactTokens](IRouter.md#swaptokensforexacttokens)

## Constructors

### constructor

• **new IRouter**(`at`): [`IRouter`](IRouter.md)

Wraps a smart contract exposing standard token FFI.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `at` | `Address` | Address of the smart contract. |

#### Returns

[`IRouter`](IRouter.md)

#### Defined in

[assembly/interfaces/IRouter.ts:22](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/interfaces/IRouter.ts#L22)

## Properties

### \_origin

• **\_origin**: `Address`

#### Defined in

[assembly/interfaces/IRouter.ts:15](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/interfaces/IRouter.ts#L15)

## Methods

### addLiquidity

▸ **addLiquidity**(`liquidityParameters`, `masToSend`): `AddLiquidity`

Add liquidity while performing safety checks
This function is compliant with fee on transfer tokens

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `liquidityParameters` | [`LiquidityParameters`](../structs/LiquidityParameters.md) | The liquidity parameters |
| `masToSend` | `u64` | The amount of MAS to send for storage |

#### Returns

`AddLiquidity`

- The amount of tokens minted and the ids of the deposits

#### Defined in

[assembly/interfaces/IRouter.ts:73](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/interfaces/IRouter.ts#L73)

___

### addLiquidityMAS

▸ **addLiquidityMAS**(`liquidityParameters`, `amountTotal`, `masToSend`): `AddLiquidity`

Add liquidity with MAS while performing safety checks
This function is compliant with fee on transfer tokens

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `liquidityParameters` | [`LiquidityParameters`](../structs/LiquidityParameters.md) | The liquidity parameters |
| `amountTotal` | `u256` | The amount of MAS to deposit + the amount of MAS to send for storage |
| `masToSend` | `u64` | The amount of MAS to send for storage |

#### Returns

`AddLiquidity`

- The amount of tokens minted and the ids of the deposits

#### Defined in

[assembly/interfaces/IRouter.ts:94](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/interfaces/IRouter.ts#L94)

___

### createLBPair

▸ **createLBPair**(`tokenX`, `tokenY`, `activeId`, `binStep`, `masToSend`): `Address`

Create a liquidity bin LBPair for _tokenX and _tokenY using the factory

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `tokenX` | [`IERC20`](IERC20.md) | The address of the first token |
| `tokenY` | [`IERC20`](IERC20.md) | The address of the second token |
| `activeId` | `u32` | The active id of the pair |
| `binStep` | `u32` | The bin step in basis point, used to calculate log(1 + binStep) |
| `masToSend` | `u64` | The amount of MAS to send for storage |

#### Returns

`Address`

- The address of the newly created LBPair

#### Defined in

[assembly/interfaces/IRouter.ts:49](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/interfaces/IRouter.ts#L49)

___

### getSwapIn

▸ **getSwapIn**(`_pair`, `_amountOut`, `_swapForY`): `GetSwapInReturn`

#### Parameters

| Name | Type |
| :------ | :------ |
| `_pair` | [`IPair`](IPair.md) |
| `_amountOut` | `u256` |
| `_swapForY` | `bool` |

#### Returns

`GetSwapInReturn`

#### Defined in

[assembly/interfaces/IRouter.ts:506](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/interfaces/IRouter.ts#L506)

___

### getSwapOut

▸ **getSwapOut**(`_pair`, `_amountIn`, `_swapForY`): `GetSwapOutReturn`

#### Parameters

| Name | Type |
| :------ | :------ |
| `_pair` | [`IPair`](IPair.md) |
| `_amountIn` | `u256` |
| `_swapForY` | `bool` |

#### Returns

`GetSwapOutReturn`

#### Defined in

[assembly/interfaces/IRouter.ts:515](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/interfaces/IRouter.ts#L515)

___

### init

▸ **init**(`wmas`, `factory`): `void`

Calls the constructor.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `wmas` | `Address` | The address of WMAS |
| `factory` | `Address` | The address of the factory |

#### Returns

`void`

#### Defined in

[assembly/interfaces/IRouter.ts:32](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/interfaces/IRouter.ts#L32)

___

### removeLiquidity

▸ **removeLiquidity**(`tokenX`, `tokenY`, `binStep`, `amountXMin`, `amountYMin`, `ids`, `amounts`, `to`, `deadline`, `masToSend`): `Amounts`

Remove liquidity while performing safety checks
This function is compliant with fee on transfer tokens

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `tokenX` | `Address` | The address of token X |
| `tokenY` | `Address` | The address of token Y |
| `binStep` | `u32` | The bin step of the LBPair |
| `amountXMin` | `u256` | The min amount to receive of token X |
| `amountYMin` | `u256` | The min amount to receive of token Y |
| `ids` | `u64`[] | The list of ids to burn |
| `amounts` | `u256`[] | The list of amounts to burn of each id in `ids` |
| `to` | `Address` | The address of the recipient |
| `deadline` | `u64` | The deadline of the tx |
| `masToSend` | `u64` | The amount of MAS to send for storage |

#### Returns

`Amounts`

- The amount of tokens received

#### Defined in

[assembly/interfaces/IRouter.ts:125](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/interfaces/IRouter.ts#L125)

___

### removeLiquidityMAS

▸ **removeLiquidityMAS**(`token`, `binStep`, `amountTokenMin`, `amountMasMin`, `ids`, `amounts`, `to`, `deadline`, `masToSend`): `Amounts`

Remove liquidity with MAS while performing safety checks
This function is compliant with fee on transfer tokens

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `token` | `Address` | The address of token |
| `binStep` | `u32` | The bin step of the LBPair |
| `amountTokenMin` | `u256` | The min amount to receive of token |
| `amountMasMin` | `u256` | The min amount to receive of MAS |
| `ids` | `u64`[] | The list of ids to burn |
| `amounts` | `u256`[] | The list of amounts to burn of each id in `ids` |
| `to` | `Address` | The address of the recipient |
| `deadline` | `u64` | The deadline of the tx |
| `masToSend` | `u64` | The amount of MAS to send for storage |

#### Returns

`Amounts`

#### Defined in

[assembly/interfaces/IRouter.ts:167](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/interfaces/IRouter.ts#L167)

___

### swapExactMASForTokens

▸ **swapExactMASForTokens**(`amountIn`, `amountOutMin`, `pairBinSteps`, `tokenPath`, `to`, `deadline`, `masToSend`): `u256`

Swaps exact MAS for tokens while performing safety checks

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `amountIn` | `u256` | The amount of MAS to send for swap and storage |
| `amountOutMin` | `u256` | The min amount of token to receive |
| `pairBinSteps` | `u64`[] | The bin step of the pairs |
| `tokenPath` | [`IERC20`](IERC20.md)[] | The swap path using the binSteps following `_pairBinSteps` |
| `to` | `Address` | The address of the recipient |
| `deadline` | `u64` | The deadline of the tx |
| `masToSend` | `u64` | The amount of Massa to send for storage |

#### Returns

`u256`

- The output amount of the swap

#### Defined in

[assembly/interfaces/IRouter.ts:269](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/interfaces/IRouter.ts#L269)

___

### swapExactMASForTokensSupportingFeeOnTransferTokens

▸ **swapExactMASForTokensSupportingFeeOnTransferTokens**(`amountIn`, `amountOutMin`, `pairBinSteps`, `tokenPath`, `to`, `deadline`, `masToSend`): `u256`

Swaps exact MAS for tokens while performing safety checks supporting for fee on transfer tokens

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `amountIn` | `u256` | The amount of MAS to send for swap and storage |
| `amountOutMin` | `u256` | The min amount of token to receive |
| `pairBinSteps` | `u64`[] | The bin step of the pairs |
| `tokenPath` | [`IERC20`](IERC20.md)[] | The swap path using the binSteps following `_pairBinSteps` |
| `to` | `Address` | The address of the recipient |
| `deadline` | `u64` | The deadline of the tx |
| `masToSend` | `u64` | The amount of Massa to send for storage |

#### Returns

`u256`

- The output amount of the swap

#### Defined in

[assembly/interfaces/IRouter.ts:481](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/interfaces/IRouter.ts#L481)

___

### swapExactTokensForMAS

▸ **swapExactTokensForMAS**(`amountIn`, `amountOutMinMAS`, `pairBinSteps`, `tokenPath`, `to`, `deadline`, `masToSend`): `u256`

Swaps exact tokens for MAS while performing safety checks

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `amountIn` | `u256` | The amount of tokens to send |
| `amountOutMinMAS` | `u256` | The min amount of MAS to receive |
| `pairBinSteps` | `u64`[] | The bin step of the pairs |
| `tokenPath` | [`IERC20`](IERC20.md)[] | The swap path using the binSteps following `_pairBinSteps` |
| `to` | `Address` | The address of the recipient |
| `deadline` | `u64` | The deadline of the tx |
| `masToSend` | `u64` | The amount of Massa to send for storage |

#### Returns

`u256`

- The output amount of the swap

#### Defined in

[assembly/interfaces/IRouter.ts:237](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/interfaces/IRouter.ts#L237)

___

### swapExactTokensForMASSupportingFeeOnTransferTokens

▸ **swapExactTokensForMASSupportingFeeOnTransferTokens**(`amountIn`, `amountOutMinMAS`, `pairBinSteps`, `tokenPath`, `to`, `deadline`, `masToSend`): `u256`

Swaps exact tokens for MAS while performing safety checks supporting for fee on transfer tokens

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `amountIn` | `u256` | The amount of token to send |
| `amountOutMinMAS` | `u256` | The min amount of MAS to receive |
| `pairBinSteps` | `u64`[] | The bin step of the pairs |
| `tokenPath` | [`IERC20`](IERC20.md)[] | The swap path using the binSteps following `_pairBinSteps` |
| `to` | `Address` | The address of the recipient |
| `deadline` | `u64` | The deadline of the tx |
| `masToSend` | `u64` | The amount of Massa to send for storage |

#### Returns

`u256`

- The output amount of the swap

#### Defined in

[assembly/interfaces/IRouter.ts:444](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/interfaces/IRouter.ts#L444)

___

### swapExactTokensForTokens

▸ **swapExactTokensForTokens**(`amountIn`, `amountOutMin`, `pairBinSteps`, `tokenPath`, `to`, `deadline`, `masToSend`): `u256`

Swaps exact tokens for tokens while performing safety checks

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `amountIn` | `u256` | The amount of tokens to send |
| `amountOutMin` | `u256` | The min amount of tokens to receive |
| `pairBinSteps` | `u64`[] | The bin step of the pairs |
| `tokenPath` | [`IERC20`](IERC20.md)[] | The swap path using the binSteps following `_pairBinSteps` |
| `to` | `Address` | The address of the recipient |
| `deadline` | `u64` | The deadline of the tx |
| `masToSend` | `u64` | The amount of Massa to send for storage |

#### Returns

`u256`

- The output amount of the swap

#### Defined in

[assembly/interfaces/IRouter.ts:205](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/interfaces/IRouter.ts#L205)

___

### swapExactTokensForTokensSupportingFeeOnTransferTokens

▸ **swapExactTokensForTokensSupportingFeeOnTransferTokens**(`amountIn`, `amountOutMin`, `pairBinSteps`, `tokenPath`, `to`, `deadline`, `masToSend`): `u256`

Swaps exact tokens for tokens while performing safety checks supporting for fee on transfer tokens

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `amountIn` | `u256` | The amount of token to send |
| `amountOutMin` | `u256` | The min amount of token to receive |
| `pairBinSteps` | `u64`[] | The bin step of the pairs |
| `tokenPath` | [`IERC20`](IERC20.md)[] | The swap path using the binSteps following `_pairBinSteps` |
| `to` | `Address` | The address of the recipient |
| `deadline` | `u64` | The deadline of the tx |
| `masToSend` | `u64` | The amount of Massa to send for storage |

#### Returns

`u256`

- The output amount of the swap

#### Defined in

[assembly/interfaces/IRouter.ts:407](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/interfaces/IRouter.ts#L407)

___

### swapMASForExactTokens

▸ **swapMASForExactTokens**(`amountOut`, `amountInMax`, `pairBinSteps`, `tokenPath`, `to`, `deadline`, `masToSend`): `u256`

Swaps MAS for exact tokens while performing safety checks

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `amountOut` | `u256` | The amount of token to receive |
| `amountInMax` | `u256` | The max amount of Mas to send |
| `pairBinSteps` | `u64`[] | The bin step of the pairs |
| `tokenPath` | [`IERC20`](IERC20.md)[] | The swap path using the binSteps following `_pairBinSteps` |
| `to` | `Address` | The address of the recipient |
| `deadline` | `u64` | The deadline of the tx |
| `masToSend` | `u64` | The amount of Massa to send for storage |

#### Returns

`u256`

- The output amount of the swap

#### Defined in

[assembly/interfaces/IRouter.ts:370](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/interfaces/IRouter.ts#L370)

___

### swapTokensForExactMAS

▸ **swapTokensForExactMAS**(`amountOut`, `amountInMax`, `pairBinSteps`, `tokenPath`, `to`, `deadline`, `masToSend`): `u256`

Swaps tokens for exact MAS while performing safety checks

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `amountOut` | `u256` | The amount of MAS to receive |
| `amountInMax` | `u256` | The max amount of token to send |
| `pairBinSteps` | `u64`[] | The bin step of the pairs |
| `tokenPath` | [`IERC20`](IERC20.md)[] | The swap path using the binSteps following `_pairBinSteps` |
| `to` | `Address` | The address of the recipient |
| `deadline` | `u64` | The deadline of the tx |
| `masToSend` | `u64` | The amount of Massa to send for storage |

#### Returns

`u256`

- The output amount of the swap

#### Defined in

[assembly/interfaces/IRouter.ts:338](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/interfaces/IRouter.ts#L338)

___

### swapTokensForExactTokens

▸ **swapTokensForExactTokens**(`amountOut`, `amountInMax`, `pairBinSteps`, `tokenPath`, `to`, `deadline`, `masToSend`): `u256`

Swaps tokens for exact tokens while performing safety checks

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `amountOut` | `u256` | The amount of token to receive |
| `amountInMax` | `u256` | The max amount of token to send |
| `pairBinSteps` | `u64`[] | The bin step of the pairs |
| `tokenPath` | [`IERC20`](IERC20.md)[] | The swap path using the binSteps following `_pairBinSteps` |
| `to` | `Address` | The address of the recipient |
| `deadline` | `u64` | The deadline of the tx |
| `masToSend` | `u64` | The amount of Massa to send for storage |

#### Returns

`u256`

- The output amount of the swap

#### Defined in

[assembly/interfaces/IRouter.ts:306](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/interfaces/IRouter.ts#L306)
