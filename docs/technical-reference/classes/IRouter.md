[@dusalabs/core](../README.md) / [Exports](../modules.md) / IRouter

# Class: IRouter

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
- [swapExactTokensForMAS](IRouter.md#swapexacttokensformas)
- [swapExactTokensForTokens](IRouter.md#swapexacttokensfortokens)
- [swapMASForExactTokens](IRouter.md#swapmasforexacttokens)
- [swapTokensForExactMAS](IRouter.md#swaptokensforexactmas)
- [swapTokensForExactTokens](IRouter.md#swaptokensforexacttokens)

## Constructors

### constructor

• **new IRouter**(`at`)

Wraps a smart contract exposing standard token FFI.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `at` | `Address` | Address of the smart contract. |

#### Defined in

[assembly/interfaces/IRouter.ts:24](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/interfaces/IRouter.ts#L24)

## Properties

### \_origin

• **\_origin**: `Address`

#### Defined in

[assembly/interfaces/IRouter.ts:17](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/interfaces/IRouter.ts#L17)

## Methods

### addLiquidity

▸ **addLiquidity**(`liquidityParameters`): `u64`[]

Add liquidity while performing safety checks
This function is compliant with fee on transfer tokens

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `liquidityParameters` | [`LiquidityParameters`](LiquidityParameters.md) | The liquidity parameters |

#### Returns

`u64`[]

#### Defined in

[assembly/interfaces/IRouter.ts:62](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/interfaces/IRouter.ts#L62)

___

### addLiquidityMAS

▸ **addLiquidityMAS**(`liquidityParameters`, `amount`): `u64`[]

Add liquidity with MAS while performing safety checks
This function is compliant with fee on transfer tokens

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `liquidityParameters` | [`LiquidityParameters`](LiquidityParameters.md) | The liquidity parameters |
| `amount` | `u64` | The amount of MAS to deposit |

#### Returns

`u64`[]

#### Defined in

[assembly/interfaces/IRouter.ts:78](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/interfaces/IRouter.ts#L78)

___

### createLBPair

▸ **createLBPair**(`tokenX`, `tokenY`, `activeId`, `binStep`): `Address`

Create a liquidity bin LBPair for _tokenX and _tokenY using the factory

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `tokenX` | [`IERC20`](IERC20.md) | The address of the first token |
| `tokenY` | [`IERC20`](IERC20.md) | The address of the second token |
| `activeId` | `u32` | The active id of the pair |
| `binStep` | `u32` | The bin step in basis point, used to calculate log(1 + binStep) |

#### Returns

`Address`

- The address of the newly created LBPair

#### Defined in

[assembly/interfaces/IRouter.ts:50](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/interfaces/IRouter.ts#L50)

___

### getSwapIn

▸ **getSwapIn**(`_pair`, `_amountOut`, `_swapForY`): [`GetSwapInReturn`](GetSwapInReturn.md)

#### Parameters

| Name | Type |
| :------ | :------ |
| `_pair` | [`IPair`](IPair.md) |
| `_amountOut` | `u64` |
| `_swapForY` | `bool` |

#### Returns

[`GetSwapInReturn`](GetSwapInReturn.md)

#### Defined in

[assembly/interfaces/IRouter.ts:337](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/interfaces/IRouter.ts#L337)

___

### getSwapOut

▸ **getSwapOut**(`_pair`, `_amountIn`, `_swapForY`): [`GetSwapOutReturn`](GetSwapOutReturn.md)

#### Parameters

| Name | Type |
| :------ | :------ |
| `_pair` | [`IPair`](IPair.md) |
| `_amountIn` | `u64` |
| `_swapForY` | `bool` |

#### Returns

[`GetSwapOutReturn`](GetSwapOutReturn.md)

#### Defined in

[assembly/interfaces/IRouter.ts:343](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/interfaces/IRouter.ts#L343)

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

[assembly/interfaces/IRouter.ts:34](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/interfaces/IRouter.ts#L34)

___

### removeLiquidity

▸ **removeLiquidity**(`tokenX`, `tokenY`, `binStep`, `amountXMin`, `amountYMin`, `ids`, `amounts`, `to`, `deadline`): `u64`[]

Remove liquidity while performing safety checks
This function is compliant with fee on transfer tokens

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `tokenX` | `Address` | The address of token X |
| `tokenY` | `Address` | The address of token Y |
| `binStep` | `u32` | The bin step of the LBPair |
| `amountXMin` | `u64` | The min amount to receive of token X |
| `amountYMin` | `u64` | The min amount to receive of token Y |
| `ids` | `u64`[] | The list of ids to burn |
| `amounts` | `u64`[] | The list of amounts to burn of each id in `ids` |
| `to` | `Address` | The address of the recipient |
| `deadline` | `u64` | The deadline of the tx |

#### Returns

`u64`[]

#### Defined in

[assembly/interfaces/IRouter.ts:100](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/interfaces/IRouter.ts#L100)

___

### removeLiquidityMAS

▸ **removeLiquidityMAS**(`token`, `binStep`, `amountTokenMin`, `amountMasMin`, `ids`, `amounts`, `to`, `deadline`): `u64`[]

Remove liquidity with MAS while performing safety checks
This function is compliant with fee on transfer tokens

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `token` | `Address` | The address of token |
| `binStep` | `u32` | The bin step of the LBPair |
| `amountTokenMin` | `u64` | The min amount to receive of token |
| `amountMasMin` | `u64` | The min amount to receive of MAS |
| `ids` | `u64`[] | The list of ids to burn |
| `amounts` | `u64`[] | The list of amounts to burn of each id in `ids` |
| `to` | `Address` | The address of the recipient |
| `deadline` | `u64` | The deadline of the tx |

#### Returns

`u64`[]

#### Defined in

[assembly/interfaces/IRouter.ts:140](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/interfaces/IRouter.ts#L140)

___

### swapExactMASForTokens

▸ **swapExactMASForTokens**(`amountIn`, `amountOutMin`, `pairBinSteps`, `tokenPath`, `to`, `deadline`): `u64`

Swaps exact MAS for tokens while performing safety checks

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `amountIn` | `u64` | The amount of MAS to send |
| `amountOutMin` | `u64` | The min amount of token to receive |
| `pairBinSteps` | `u64`[] | The bin step of the pairs (0: V1, other values will use V2) |
| `tokenPath` | [`IERC20`](IERC20.md)[] | The swap path using the binSteps following `_pairBinSteps` |
| `to` | `Address` | The address of the recipient |
| `deadline` | `u64` | The deadline of the tx |

#### Returns

`u64`

#### Defined in

[assembly/interfaces/IRouter.ts:233](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/interfaces/IRouter.ts#L233)

___

### swapExactTokensForMAS

▸ **swapExactTokensForMAS**(`amountIn`, `amountOutMinMAS`, `pairBinSteps`, `tokenPath`, `to`, `deadline`): `u64`

Swaps exact tokens for MAS while performing safety checks

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `amountIn` | `u64` | The amount of tokens to send |
| `amountOutMinMAS` | `u64` | The min amount of MAS to receive |
| `pairBinSteps` | `u64`[] | The bin step of the pairs (0: V1, other values will use V2) |
| `tokenPath` | [`IERC20`](IERC20.md)[] | The swap path using the binSteps following `_pairBinSteps` |
| `to` | `Address` | The address of the recipient |
| `deadline` | `u64` | The deadline of the tx |

#### Returns

`u64`

#### Defined in

[assembly/interfaces/IRouter.ts:204](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/interfaces/IRouter.ts#L204)

___

### swapExactTokensForTokens

▸ **swapExactTokensForTokens**(`amountIn`, `amountOutMin`, `pairBinSteps`, `tokenPath`, `to`, `deadline`): `u64`

Swaps exact tokens for tokens while performing safety checks

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `amountIn` | `u64` | The amount of tokens to send |
| `amountOutMin` | `u64` | The min amount of tokens to receive |
| `pairBinSteps` | `u64`[] | The bin step of the pairs (0: V1, other values will use V2) |
| `tokenPath` | [`IERC20`](IERC20.md)[] | The swap path using the binSteps following `_pairBinSteps` |
| `to` | `Address` | The address of the recipient |
| `deadline` | `u64` | The deadline of the tx |

#### Returns

`u64`

#### Defined in

[assembly/interfaces/IRouter.ts:175](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/interfaces/IRouter.ts#L175)

___

### swapMASForExactTokens

▸ **swapMASForExactTokens**(`amountOut`, `amountInMax`, `pairBinSteps`, `tokenPath`, `to`, `deadline`): `u64`

Swaps MAS for exact tokens while performing safety checks

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `amountOut` | `u64` | The amount of token to receive |
| `amountInMax` | `u64` | The max amount of token to send |
| `pairBinSteps` | `u64`[] | The bin step of the pairs (0: V1, other values will use V2) |
| `tokenPath` | [`IERC20`](IERC20.md)[] | The swap path using the binSteps following `_pairBinSteps` |
| `to` | `Address` | The address of the recipient |
| `deadline` | `u64` | The deadline of the tx |

#### Returns

`u64`

#### Defined in

[assembly/interfaces/IRouter.ts:319](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/interfaces/IRouter.ts#L319)

___

### swapTokensForExactMAS

▸ **swapTokensForExactMAS**(`amountOut`, `amountInMax`, `pairBinSteps`, `tokenPath`, `to`, `deadline`): `u64`

Swaps tokens for exact MAS while performing safety checks

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `amountOut` | `u64` | The amount of MAS to receive |
| `amountInMax` | `u64` | The max amount of token to send |
| `pairBinSteps` | `u64`[] | The bin step of the pairs (0: V1, other values will use V2) |
| `tokenPath` | [`IERC20`](IERC20.md)[] | The swap path using the binSteps following `_pairBinSteps` |
| `to` | `Address` | The address of the recipient |
| `deadline` | `u64` | The deadline of the tx |

#### Returns

`u64`

#### Defined in

[assembly/interfaces/IRouter.ts:290](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/interfaces/IRouter.ts#L290)

___

### swapTokensForExactTokens

▸ **swapTokensForExactTokens**(`amountOut`, `amountInMax`, `pairBinSteps`, `tokenPath`, `to`, `deadline`): `u64`

Swaps tokens for exact tokens while performing safety checks

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `amountOut` | `u64` | The amount of token to receive |
| `amountInMax` | `u64` | The max amount of token to send |
| `pairBinSteps` | `u64`[] | The bin step of the pairs (0: V1, other values will use V2) |
| `tokenPath` | [`IERC20`](IERC20.md)[] | The swap path using the binSteps following `_pairBinSteps` |
| `to` | `Address` | The address of the recipient |
| `deadline` | `u64` | The deadline of the tx |

#### Returns

`u64`

#### Defined in

[assembly/interfaces/IRouter.ts:261](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/interfaces/IRouter.ts#L261)
