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
- [swapExactTokensForMAS](IRouter.md#swapexacttokensformas)
- [swapExactTokensForTokens](IRouter.md#swapexacttokensfortokens)
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

[assembly/interfaces/IRouter.ts:22](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/interfaces/IRouter.ts#L22)

## Properties

### \_origin

• **\_origin**: `Address`

#### Defined in

[assembly/interfaces/IRouter.ts:15](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/interfaces/IRouter.ts#L15)

## Methods

### addLiquidity

▸ **addLiquidity**(`liquidityParameters`): `AddLiquidity`

Add liquidity while performing safety checks
This function is compliant with fee on transfer tokens

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `liquidityParameters` | [`LiquidityParameters`](LiquidityParameters.md) | The liquidity parameters |

#### Returns

`AddLiquidity`

- The amount of tokens minted and the ids of the deposits

#### Defined in

[assembly/interfaces/IRouter.ts:70](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/interfaces/IRouter.ts#L70)

___

### addLiquidityMAS

▸ **addLiquidityMAS**(`liquidityParameters`, `amount`): `AddLiquidity`

Add liquidity with MAS while performing safety checks
This function is compliant with fee on transfer tokens

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `liquidityParameters` | [`LiquidityParameters`](LiquidityParameters.md) | The liquidity parameters |
| `amount` | `u256` | The amount of MAS to deposit |

#### Returns

`AddLiquidity`

- The amount of tokens minted and the ids of the deposits

#### Defined in

[assembly/interfaces/IRouter.ts:87](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/interfaces/IRouter.ts#L87)

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

[assembly/interfaces/IRouter.ts:48](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/interfaces/IRouter.ts#L48)

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

[assembly/interfaces/IRouter.ts:360](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/interfaces/IRouter.ts#L360)

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

[assembly/interfaces/IRouter.ts:369](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/interfaces/IRouter.ts#L369)

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

[assembly/interfaces/IRouter.ts:32](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/interfaces/IRouter.ts#L32)

___

### removeLiquidity

▸ **removeLiquidity**(`tokenX`, `tokenY`, `binStep`, `amountXMin`, `amountYMin`, `ids`, `amounts`, `to`, `deadline`): `Amounts`

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

#### Returns

`Amounts`

- The amount of tokens received

#### Defined in

[assembly/interfaces/IRouter.ts:116](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/interfaces/IRouter.ts#L116)

___

### removeLiquidityMAS

▸ **removeLiquidityMAS**(`token`, `binStep`, `amountTokenMin`, `amountMasMin`, `ids`, `amounts`, `to`, `deadline`): `Amounts`

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

#### Returns

`Amounts`

#### Defined in

[assembly/interfaces/IRouter.ts:154](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/interfaces/IRouter.ts#L154)

___

### swapExactMASForTokens

▸ **swapExactMASForTokens**(`amountIn`, `amountOutMin`, `pairBinSteps`, `tokenPath`, `to`, `deadline`): `u256`

Swaps exact MAS for tokens while performing safety checks

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `amountIn` | `u256` | The amount of MAS to send |
| `amountOutMin` | `u256` | The min amount of token to receive |
| `pairBinSteps` | `u64`[] | The bin step of the pairs (0: V1, other values will use V2) |
| `tokenPath` | [`IERC20`](IERC20.md)[] | The swap path using the binSteps following `_pairBinSteps` |
| `to` | `Address` | The address of the recipient |
| `deadline` | `u64` | The deadline of the tx |

#### Returns

`u256`

#### Defined in

[assembly/interfaces/IRouter.ts:245](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/interfaces/IRouter.ts#L245)

___

### swapExactTokensForMAS

▸ **swapExactTokensForMAS**(`amountIn`, `amountOutMinMAS`, `pairBinSteps`, `tokenPath`, `to`, `deadline`): `u256`

Swaps exact tokens for MAS while performing safety checks

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `amountIn` | `u256` | The amount of tokens to send |
| `amountOutMinMAS` | `u256` | The min amount of MAS to receive |
| `pairBinSteps` | `u64`[] | The bin step of the pairs (0: V1, other values will use V2) |
| `tokenPath` | [`IERC20`](IERC20.md)[] | The swap path using the binSteps following `_pairBinSteps` |
| `to` | `Address` | The address of the recipient |
| `deadline` | `u64` | The deadline of the tx |

#### Returns

`u256`

#### Defined in

[assembly/interfaces/IRouter.ts:216](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/interfaces/IRouter.ts#L216)

___

### swapExactTokensForTokens

▸ **swapExactTokensForTokens**(`amountIn`, `amountOutMin`, `pairBinSteps`, `tokenPath`, `to`, `deadline`): `u256`

Swaps exact tokens for tokens while performing safety checks

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `amountIn` | `u256` | The amount of tokens to send |
| `amountOutMin` | `u256` | The min amount of tokens to receive |
| `pairBinSteps` | `u64`[] | The bin step of the pairs (0: V1, other values will use V2) |
| `tokenPath` | [`IERC20`](IERC20.md)[] | The swap path using the binSteps following `_pairBinSteps` |
| `to` | `Address` | The address of the recipient |
| `deadline` | `u64` | The deadline of the tx |

#### Returns

`u256`

#### Defined in

[assembly/interfaces/IRouter.ts:187](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/interfaces/IRouter.ts#L187)

___

### swapMASForExactTokens

▸ **swapMASForExactTokens**(`amountOut`, `amountInMax`, `pairBinSteps`, `tokenPath`, `to`, `deadline`): `u256`

Swaps MAS for exact tokens while performing safety checks

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `amountOut` | `u256` | The amount of token to receive |
| `amountInMax` | `u256` | The max amount of token to send |
| `pairBinSteps` | `u64`[] | The bin step of the pairs (0: V1, other values will use V2) |
| `tokenPath` | [`IERC20`](IERC20.md)[] | The swap path using the binSteps following `_pairBinSteps` |
| `to` | `Address` | The address of the recipient |
| `deadline` | `u64` | The deadline of the tx |

#### Returns

`u256`

- The amount of MAS sent

#### Defined in

[assembly/interfaces/IRouter.ts:337](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/interfaces/IRouter.ts#L337)

___

### swapTokensForExactMAS

▸ **swapTokensForExactMAS**(`amountOut`, `amountInMax`, `pairBinSteps`, `tokenPath`, `to`, `deadline`): `u256`

Swaps tokens for exact MAS while performing safety checks

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `amountOut` | `u256` | The amount of MAS to receive |
| `amountInMax` | `u256` | The max amount of token to send |
| `pairBinSteps` | `u64`[] | The bin step of the pairs (0: V1, other values will use V2) |
| `tokenPath` | [`IERC20`](IERC20.md)[] | The swap path using the binSteps following `_pairBinSteps` |
| `to` | `Address` | The address of the recipient |
| `deadline` | `u64` | The deadline of the tx |

#### Returns

`u256`

#### Defined in

[assembly/interfaces/IRouter.ts:307](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/interfaces/IRouter.ts#L307)

___

### swapTokensForExactTokens

▸ **swapTokensForExactTokens**(`amountOut`, `amountInMax`, `pairBinSteps`, `tokenPath`, `to`, `deadline`): `u256`

Swaps tokens for exact tokens while performing safety checks

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `amountOut` | `u256` | The amount of token to receive |
| `amountInMax` | `u256` | The max amount of token to send |
| `pairBinSteps` | `u64`[] | The bin step of the pairs (0: V1, other values will use V2) |
| `tokenPath` | [`IERC20`](IERC20.md)[] | The swap path using the binSteps following `_pairBinSteps` |
| `to` | `Address` | The address of the recipient |
| `deadline` | `u64` | The deadline of the tx |

#### Returns

`u256`

#### Defined in

[assembly/interfaces/IRouter.ts:278](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/interfaces/IRouter.ts#L278)
