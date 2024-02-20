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

• **new SwapHelper**(): [`SwapHelper`](SwapHelper.md)

#### Returns

[`SwapHelper`](SwapHelper.md)

## Methods

### getAmounts

▸ **getAmounts**(`_bin`, `_fp`, `_activeId`, `_swapForY`, `_amountIn`): `GetAmountsReturn`

Returns the swap amounts in the current bin

#### Parameters

| Name | Type |
| :------ | :------ |
| `_bin` | [`Bin`](Bin.md) |
| `_fp` | [`FeeParameters`](FeeParameters.md) |
| `_activeId` | `u64` |
| `_swapForY` | `bool` |
| `_amountIn` | `u256` |

#### Returns

`GetAmountsReturn`

GetAmountsReturn: amountInToBin (u256), amountOutOfBin (u256), fees (FeesDistribution)

#### Defined in

[assembly/libraries/SwapHelper.ts:31](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/libraries/SwapHelper.ts#L31)

___

### getSwapIn

▸ **getSwapIn**(`_pair`, `_amountOut`, `_swapForY`, `isQuote?`): `Result`<`GetSwapInReturn`\>

Simulate a swap in

#### Parameters

| Name | Type | Default value | Description |
| :------ | :------ | :------ | :------ |
| `_pair` | [`IPair`](IPair.md) | `undefined` | - |
| `_amountOut` | `u256` | `undefined` | The amount of token to receive |
| `_swapForY` | `bool` | `undefined` | Whether you swap X for Y (true), or Y for X (false) |
| `isQuote` | `bool` | `false` | - |

#### Returns

`Result`<`GetSwapInReturn`\>

GetSwapInReturn: amountIn, feesIn

#### Defined in

[assembly/libraries/SwapHelper.ts:87](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/libraries/SwapHelper.ts#L87)

___

### getSwapOut

▸ **getSwapOut**(`_pair`, `_amountIn`, `_swapForY`, `isQuote?`): `Result`<`GetSwapOutReturn`\>

Simulate a swap out

#### Parameters

| Name | Type | Default value | Description |
| :------ | :------ | :------ | :------ |
| `_pair` | [`IPair`](IPair.md) | `undefined` | - |
| `_amountIn` | `u256` | `undefined` | The amount of token sent |
| `_swapForY` | `bool` | `undefined` | Whether you swap X for Y (true), or Y for X (false) |
| `isQuote` | `bool` | `false` | Whether this is a quote or not (will throw or return an error) |

#### Returns

`Result`<`GetSwapOutReturn`\>

GetSwapOutReturn: amountOut, feesIn

#### Defined in

[assembly/libraries/SwapHelper.ts:176](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/libraries/SwapHelper.ts#L176)
