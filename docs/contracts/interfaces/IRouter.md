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

| Name | Type      | Description                    |
| :--- | :-------- | :----------------------------- |
| `at` | `Address` | Address of the smart contract. |

#### Returns

[`IRouter`](IRouter.md)

#### Defined in

[assembly/interfaces/IRouter.ts:22](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/interfaces/IRouter.ts#L22)

## Properties

### \_origin

• **\_origin**: `Address`

#### Defined in

[assembly/interfaces/IRouter.ts:15](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/interfaces/IRouter.ts#L15)

## Methods

### addLiquidity

▸ **addLiquidity**(`liquidityParameters`, `masToSend`): `AddLiquidity`

Add liquidity while performing safety checks
This function is compliant with fee on transfer tokens

#### Parameters

| Name                  | Type                                                       | Description                           |
| :-------------------- | :--------------------------------------------------------- | :------------------------------------ |
| `liquidityParameters` | [`LiquidityParameters`](../structs/LiquidityParameters.md) | The liquidity parameters              |
| `masToSend`           | `u64`                                                      | The amount of MAS to send for storage |

#### Returns

`AddLiquidity`

- The amount of tokens minted and the ids of the deposits

#### Defined in

[assembly/interfaces/IRouter.ts:82](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/interfaces/IRouter.ts#L82)

---

### addLiquidityMAS

▸ **addLiquidityMAS**(`liquidityParameters`, `amountTotal`, `masToSend`): `AddLiquidity`

Add liquidity with MAS while performing safety checks
This function is compliant with fee on transfer tokens

#### Parameters

| Name                  | Type                                                       | Description                                                          |
| :-------------------- | :--------------------------------------------------------- | :------------------------------------------------------------------- |
| `liquidityParameters` | [`LiquidityParameters`](../structs/LiquidityParameters.md) | The liquidity parameters                                             |
| `amountTotal`         | `u256`                                                     | The amount of MAS to deposit + the amount of MAS to send for storage |
| `masToSend`           | `u64`                                                      | The amount of MAS to send for storage                                |

#### Returns

`AddLiquidity`

- The amount of tokens minted and the ids of the deposits

#### Defined in

[assembly/interfaces/IRouter.ts:103](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/interfaces/IRouter.ts#L103)

---

### createLBPair

▸ **createLBPair**(`tokenX`, `tokenY`, `activeId`, `binStep`, `masToSend`): `Address`

Create a liquidity bin LBPair for \_tokenX and \_tokenY using the factory

#### Parameters

| Name        | Type                  | Description                                                     |
| :---------- | :-------------------- | :-------------------------------------------------------------- |
| `tokenX`    | [`IERC20`](IERC20.md) | The address of the first token                                  |
| `tokenY`    | [`IERC20`](IERC20.md) | The address of the second token                                 |
| `activeId`  | `u32`                 | The active id of the pair                                       |
| `binStep`   | `u32`                 | The bin step in basis point, used to calculate log(1 + binStep) |
| `masToSend` | `u64`                 | The amount of MAS to send for storage                           |

#### Returns

`Address`

- The address of the newly created LBPair

#### Defined in

[assembly/interfaces/IRouter.ts:58](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/interfaces/IRouter.ts#L58)

---

### getSwapIn

▸ **getSwapIn**(`_pair`, `_amountOut`, `_swapForY`): `GetSwapInReturn`

#### Parameters

| Name         | Type                |
| :----------- | :------------------ |
| `_pair`      | [`IPair`](IPair.md) |
| `_amountOut` | `u256`              |
| `_swapForY`  | `bool`              |

#### Returns

`GetSwapInReturn`

#### Defined in

[assembly/interfaces/IRouter.ts:543](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/interfaces/IRouter.ts#L543)

---

### getSwapOut

▸ **getSwapOut**(`_pair`, `_amountIn`, `_swapForY`): `GetSwapOutReturn`

#### Parameters

| Name        | Type                |
| :---------- | :------------------ |
| `_pair`     | [`IPair`](IPair.md) |
| `_amountIn` | `u256`              |
| `_swapForY` | `bool`              |

#### Returns

`GetSwapOutReturn`

#### Defined in

[assembly/interfaces/IRouter.ts:552](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/interfaces/IRouter.ts#L552)

---

### init

▸ **init**(`wmas`, `factory`, `v0factory`, `legacyfactory`): `void`

Calls the constructor.

#### Parameters

| Name            | Type      | Description                        |
| :-------------- | :-------- | :--------------------------------- |
| `wmas`          | `Address` | The address of WMAS                |
| `factory`       | `Address` | The address of the factory         |
| `v0factory`     | `Address` | The address of the V0 factory      |
| `legacyfactory` | `Address` | The address of the legagcy factory |

#### Returns

`void`

#### Defined in

[assembly/interfaces/IRouter.ts:34](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/interfaces/IRouter.ts#L34)

---

### removeLiquidity

▸ **removeLiquidity**(`tokenX`, `tokenY`, `binStep`, `amountXMin`, `amountYMin`, `ids`, `amounts`, `to`, `deadline`, `masToSend`): `Amounts`

Remove liquidity while performing safety checks
This function is compliant with fee on transfer tokens

#### Parameters

| Name         | Type      | Description                                     |
| :----------- | :-------- | :---------------------------------------------- |
| `tokenX`     | `Address` | The address of token X                          |
| `tokenY`     | `Address` | The address of token Y                          |
| `binStep`    | `u32`     | The bin step of the LBPair                      |
| `amountXMin` | `u256`    | The min amount to receive of token X            |
| `amountYMin` | `u256`    | The min amount to receive of token Y            |
| `ids`        | `u64`[]   | The list of ids to burn                         |
| `amounts`    | `u256`[]  | The list of amounts to burn of each id in `ids` |
| `to`         | `Address` | The address of the recipient                    |
| `deadline`   | `u64`     | The deadline of the tx                          |
| `masToSend`  | `u64`     | The amount of MAS to send for storage           |

#### Returns

`Amounts`

- The amount of tokens received

#### Defined in

[assembly/interfaces/IRouter.ts:134](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/interfaces/IRouter.ts#L134)

---

### removeLiquidityMAS

▸ **removeLiquidityMAS**(`token`, `binStep`, `amountTokenMin`, `amountMasMin`, `ids`, `amounts`, `to`, `deadline`, `masToSend`): `Amounts`

Remove liquidity with MAS while performing safety checks
This function is compliant with fee on transfer tokens

#### Parameters

| Name             | Type      | Description                                     |
| :--------------- | :-------- | :---------------------------------------------- |
| `token`          | `Address` | The address of token                            |
| `binStep`        | `u32`     | The bin step of the LBPair                      |
| `amountTokenMin` | `u256`    | The min amount to receive of token              |
| `amountMasMin`   | `u256`    | The min amount to receive of MAS                |
| `ids`            | `u64`[]   | The list of ids to burn                         |
| `amounts`        | `u256`[]  | The list of amounts to burn of each id in `ids` |
| `to`             | `Address` | The address of the recipient                    |
| `deadline`       | `u64`     | The deadline of the tx                          |
| `masToSend`      | `u64`     | The amount of MAS to send for storage           |

#### Returns

`Amounts`

- The amount of tokens received

#### Defined in

[assembly/interfaces/IRouter.ts:177](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/interfaces/IRouter.ts#L177)

---

### swapExactMASForTokens

▸ **swapExactMASForTokens**(`amountIn`, `amountOutMin`, `pairBinSteps`, `isLegacyPools`, `tokenPath`, `to`, `deadline`, `masToSend`): `u256`

Swaps exact MAS for tokens while performing safety checks

#### Parameters

| Name            | Type                    | Description                                                |
| :-------------- | :---------------------- | :--------------------------------------------------------- |
| `amountIn`      | `u256`                  | The amount of MAS to send for swap and storage             |
| `amountOutMin`  | `u256`                  | The min amount of token to receive                         |
| `pairBinSteps`  | `u64`[]                 | The bin step of the pairs                                  |
| `isLegacyPools` | `bool`[]                | If the pairs are legacy pairs                              |
| `tokenPath`     | [`IERC20`](IERC20.md)[] | The swap path using the binSteps following `_pairBinSteps` |
| `to`            | `Address`               | The address of the recipient                               |
| `deadline`      | `u64`                   | The deadline of the tx                                     |
| `masToSend`     | `u64`                   | The amount of Massa to send for storage                    |

#### Returns

`u256`

- The output amount of the swap

#### Defined in

[assembly/interfaces/IRouter.ts:286](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/interfaces/IRouter.ts#L286)

---

### swapExactMASForTokensSupportingFeeOnTransferTokens

▸ **swapExactMASForTokensSupportingFeeOnTransferTokens**(`amountIn`, `amountOutMin`, `pairBinSteps`, `isLegacyPools`, `tokenPath`, `to`, `deadline`, `masToSend`): `u256`

Swaps exact MAS for tokens while performing safety checks supporting for fee on transfer tokens

#### Parameters

| Name            | Type                    | Description                                                |
| :-------------- | :---------------------- | :--------------------------------------------------------- |
| `amountIn`      | `u256`                  | The amount of MAS to send for swap and storage             |
| `amountOutMin`  | `u256`                  | The min amount of token to receive                         |
| `pairBinSteps`  | `u64`[]                 | The bin step of the pairs                                  |
| `isLegacyPools` | `bool`[]                | If the pairs are legacy pairs                              |
| `tokenPath`     | [`IERC20`](IERC20.md)[] | The swap path using the binSteps following `_pairBinSteps` |
| `to`            | `Address`               | The address of the recipient                               |
| `deadline`      | `u64`                   | The deadline of the tx                                     |
| `masToSend`     | `u64`                   | The amount of Massa to send for storage                    |

#### Returns

`u256`

- The output amount of the swap

#### Defined in

[assembly/interfaces/IRouter.ts:516](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/interfaces/IRouter.ts#L516)

---

### swapExactTokensForMAS

▸ **swapExactTokensForMAS**(`amountIn`, `amountOutMinMAS`, `pairBinSteps`, `isLegacyPools`, `tokenPath`, `to`, `deadline`, `masToSend`): `u256`

Swaps exact tokens for MAS while performing safety checks

#### Parameters

| Name              | Type                    | Description                                                |
| :---------------- | :---------------------- | :--------------------------------------------------------- |
| `amountIn`        | `u256`                  | The amount of tokens to send                               |
| `amountOutMinMAS` | `u256`                  | The min amount of MAS to receive                           |
| `pairBinSteps`    | `u64`[]                 | The bin step of the pairs                                  |
| `isLegacyPools`   | `bool`[]                | If the pairs are legacy pairs                              |
| `tokenPath`       | [`IERC20`](IERC20.md)[] | The swap path using the binSteps following `_pairBinSteps` |
| `to`              | `Address`               | The address of the recipient                               |
| `deadline`        | `u64`                   | The deadline of the tx                                     |
| `masToSend`       | `u64`                   | The amount of Massa to send for storage                    |

#### Returns

`u256`

- The output amount of the swap

#### Defined in

[assembly/interfaces/IRouter.ts:251](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/interfaces/IRouter.ts#L251)

---

### swapExactTokensForMASSupportingFeeOnTransferTokens

▸ **swapExactTokensForMASSupportingFeeOnTransferTokens**(`amountIn`, `amountOutMinMAS`, `pairBinSteps`, `isLegacyPools`, `tokenPath`, `to`, `deadline`, `masToSend`): `u256`

Swaps exact tokens for MAS while performing safety checks supporting for fee on transfer tokens

#### Parameters

| Name              | Type                    | Description                                                |
| :---------------- | :---------------------- | :--------------------------------------------------------- |
| `amountIn`        | `u256`                  | The amount of token to send                                |
| `amountOutMinMAS` | `u256`                  | The min amount of MAS to receive                           |
| `pairBinSteps`    | `u64`[]                 | The bin step of the pairs                                  |
| `isLegacyPools`   | `bool`[]                | If the pairs are legacy pairs                              |
| `tokenPath`       | [`IERC20`](IERC20.md)[] | The swap path using the binSteps following `_pairBinSteps` |
| `to`              | `Address`               | The address of the recipient                               |
| `deadline`        | `u64`                   | The deadline of the tx                                     |
| `masToSend`       | `u64`                   | The amount of Massa to send for storage                    |

#### Returns

`u256`

- The output amount of the swap

#### Defined in

[assembly/interfaces/IRouter.ts:476](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/interfaces/IRouter.ts#L476)

---

### swapExactTokensForTokens

▸ **swapExactTokensForTokens**(`amountIn`, `amountOutMin`, `pairBinSteps`, `isLegacyPools`, `tokenPath`, `to`, `deadline`, `masToSend`): `u256`

Swaps exact tokens for tokens while performing safety checks

#### Parameters

| Name            | Type                    | Description                                                |
| :-------------- | :---------------------- | :--------------------------------------------------------- |
| `amountIn`      | `u256`                  | The amount of tokens to send                               |
| `amountOutMin`  | `u256`                  | The min amount of tokens to receive                        |
| `pairBinSteps`  | `u64`[]                 | The bin step of the pairs                                  |
| `isLegacyPools` | `bool`[]                | If the pairs are legacy pairs                              |
| `tokenPath`     | [`IERC20`](IERC20.md)[] | The swap path using the binSteps following `_pairBinSteps` |
| `to`            | `Address`               | The address of the recipient                               |
| `deadline`      | `u64`                   | The deadline of the tx                                     |
| `masToSend`     | `u64`                   | The amount of Massa to send for storage                    |

#### Returns

`u256`

- The output amount of the swap

#### Defined in

[assembly/interfaces/IRouter.ts:216](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/interfaces/IRouter.ts#L216)

---

### swapExactTokensForTokensSupportingFeeOnTransferTokens

▸ **swapExactTokensForTokensSupportingFeeOnTransferTokens**(`amountIn`, `amountOutMin`, `pairBinSteps`, `isLegacyPools`, `tokenPath`, `to`, `deadline`, `masToSend`): `u256`

Swaps exact tokens for tokens while performing safety checks supporting for fee on transfer tokens

#### Parameters

| Name            | Type                    | Description                                                |
| :-------------- | :---------------------- | :--------------------------------------------------------- |
| `amountIn`      | `u256`                  | The amount of token to send                                |
| `amountOutMin`  | `u256`                  | The min amount of token to receive                         |
| `pairBinSteps`  | `u64`[]                 | The bin step of the pairs                                  |
| `isLegacyPools` | `bool`[]                | If the pairs are legacy pairs                              |
| `tokenPath`     | [`IERC20`](IERC20.md)[] | The swap path using the binSteps following `_pairBinSteps` |
| `to`            | `Address`               | The address of the recipient                               |
| `deadline`      | `u64`                   | The deadline of the tx                                     |
| `masToSend`     | `u64`                   | The amount of Massa to send for storage                    |

#### Returns

`u256`

- The output amount of the swap

#### Defined in

[assembly/interfaces/IRouter.ts:436](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/interfaces/IRouter.ts#L436)

---

### swapMASForExactTokens

▸ **swapMASForExactTokens**(`amountOut`, `amountInMax`, `pairBinSteps`, `isLegacyPools`, `tokenPath`, `to`, `deadline`, `masToSend`): `u256`

Swaps MAS for exact tokens while performing safety checks

#### Parameters

| Name            | Type                    | Description                                                |
| :-------------- | :---------------------- | :--------------------------------------------------------- |
| `amountOut`     | `u256`                  | The amount of token to receive                             |
| `amountInMax`   | `u256`                  | The max amount of Mas to send                              |
| `pairBinSteps`  | `u64`[]                 | The bin step of the pairs                                  |
| `isLegacyPools` | `bool`[]                | If the pairs are legacy pairs                              |
| `tokenPath`     | [`IERC20`](IERC20.md)[] | The swap path using the binSteps following `_pairBinSteps` |
| `to`            | `Address`               | The address of the recipient                               |
| `deadline`      | `u64`                   | The deadline of the tx                                     |
| `masToSend`     | `u64`                   | The amount of Massa to send for storage                    |

#### Returns

`u256`

- The output amount of the swap

#### Defined in

[assembly/interfaces/IRouter.ts:396](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/interfaces/IRouter.ts#L396)

---

### swapTokensForExactMAS

▸ **swapTokensForExactMAS**(`amountOut`, `amountInMax`, `pairBinSteps`, `isLegacyPools`, `tokenPath`, `to`, `deadline`, `masToSend`): `u256`

Swaps tokens for exact MAS while performing safety checks

#### Parameters

| Name            | Type                    | Description                                                |
| :-------------- | :---------------------- | :--------------------------------------------------------- |
| `amountOut`     | `u256`                  | The amount of MAS to receive                               |
| `amountInMax`   | `u256`                  | The max amount of token to send                            |
| `pairBinSteps`  | `u64`[]                 | The bin step of the pairs                                  |
| `isLegacyPools` | `bool`[]                | If the pairs are legacy pairs                              |
| `tokenPath`     | [`IERC20`](IERC20.md)[] | The swap path using the binSteps following `_pairBinSteps` |
| `to`            | `Address`               | The address of the recipient                               |
| `deadline`      | `u64`                   | The deadline of the tx                                     |
| `masToSend`     | `u64`                   | The amount of Massa to send for storage                    |

#### Returns

`u256`

- The output amount of the swap

#### Defined in

[assembly/interfaces/IRouter.ts:361](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/interfaces/IRouter.ts#L361)

---

### swapTokensForExactTokens

▸ **swapTokensForExactTokens**(`amountOut`, `amountInMax`, `pairBinSteps`, `isLegacyPools`, `tokenPath`, `to`, `deadline`, `masToSend`): `u256`

Swaps tokens for exact tokens while performing safety checks

#### Parameters

| Name            | Type                    | Description                                                |
| :-------------- | :---------------------- | :--------------------------------------------------------- |
| `amountOut`     | `u256`                  | The amount of token to receive                             |
| `amountInMax`   | `u256`                  | The max amount of token to send                            |
| `pairBinSteps`  | `u64`[]                 | The bin step of the pairs                                  |
| `isLegacyPools` | `bool`[]                | If the pairs are legacy pairs                              |
| `tokenPath`     | [`IERC20`](IERC20.md)[] | The swap path using the binSteps following `_pairBinSteps` |
| `to`            | `Address`               | The address of the recipient                               |
| `deadline`      | `u64`                   | The deadline of the tx                                     |
| `masToSend`     | `u64`                   | The amount of Massa to send for storage                    |

#### Returns

`u256`

- The output amount of the swap

#### Defined in

[assembly/interfaces/IRouter.ts:326](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/interfaces/IRouter.ts#L326)
