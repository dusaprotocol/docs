# SwapHelper

## Table of contents

### Constructors

- [constructor](SwapHelper.md#constructor)

### Methods

- [getAmounts](SwapHelper.md#getamounts)
- [getSwapIn](SwapHelper.md#getswapin)
- [getSwapOut](SwapHelper.md#getswapout)

## Constructors

### constructor

• **new SwapHelper**()

## Methods

### getAmounts

▸ `Static` **getAmounts**(`_bin`, `_fp`, `_activeId`, `_swapForY`, `_amountIn`): `GetAmountsReturn`

#### Parameters

| Name | Type |
| :------ | :------ |
| `_bin` | [`Bin`](../structs/Bin.md) |
| `_fp` | [`FeeParameters`](../structs/FeeParameters.md) |
| `_activeId` | `u64` |
| `_swapForY` | `bool` |
| `_amountIn` | `u64` |

#### Returns

`GetAmountsReturn`

#### Defined in

[assembly/libraries/SwapHelper.ts:21](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/libraries/SwapHelper.ts#L21)

___

### getSwapIn

▸ `Static` **getSwapIn**(`_pair`, `_amountOut`, `_swapForY`, `isQuote?`): `Result`<`GetSwapInReturn`\>

#### Parameters

| Name | Type | Default value |
| :------ | :------ | :------ |
| `_pair` | [`IPair`](../interfaces/IPair.md) | `undefined` |
| `_amountOut` | `u64` | `undefined` |
| `_swapForY` | `bool` | `undefined` |
| `isQuote` | `bool` | `false` |

#### Returns

`Result`<`GetSwapInReturn`\>

#### Defined in

[assembly/libraries/SwapHelper.ts:78](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/libraries/SwapHelper.ts#L78)

___

### getSwapOut

▸ `Static` **getSwapOut**(`_pair`, `_amountIn`, `_swapForY`, `isQuote?`): `Result`<`GetSwapOutReturn`\>

#### Parameters

| Name | Type | Default value |
| :------ | :------ | :------ |
| `_pair` | [`IPair`](../interfaces/IPair.md) | `undefined` |
| `_amountIn` | `u64` | `undefined` |
| `_swapForY` | `bool` | `undefined` |
| `isQuote` | `bool` | `false` |

#### Returns

`Result`<`GetSwapOutReturn`\>

#### Defined in

[assembly/libraries/SwapHelper.ts:157](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/libraries/SwapHelper.ts#L157)
