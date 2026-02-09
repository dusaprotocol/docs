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

▸ **getAmounts**(`bin`, `fp`, `activeId`, `swapForY`, `amountIn`): `GetAmountsReturn`

Returns the swap amounts in the current bin

#### Parameters

| Name       | Type                                           | Description                                                                       |
| :--------- | :--------------------------------------------- | :-------------------------------------------------------------------------------- |
| `bin`      | [`Bin`](../structs/Bin.md)                     | The bin information                                                               |
| `fp`       | [`FeeParameters`](../structs/FeeParameters.md) | The fee parameters                                                                |
| `activeId` | `u32`                                          | The active id of the pair                                                         |
| `swapForY` | `bool`                                         | Whether you've swapping token X for token Y (true) or token Y for token X (false) |
| `amountIn` | `u256`                                         | The amount sent by the user                                                       |

#### Returns

`GetAmountsReturn`

GetAmountsReturn: amountInToBin (u256), amountOutOfBin (u256), fees (FeesDistribution)

#### Defined in

[assembly/libraries/SwapHelper.ts:30](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/SwapHelper.ts#L30)

---

### getSwapIn

▸ **getSwapIn**(`pair`, `amountOut`, `swapForY`, `isQuote?`): `Result`<`GetSwapInReturn`\>

Simulate a swap in

#### Parameters

| Name        | Type                              | Default value | Description                                         |
| :---------- | :-------------------------------- | :------------ | :-------------------------------------------------- |
| `pair`      | [`IPair`](../interfaces/IPair.md) | `undefined`   | -                                                   |
| `amountOut` | `u256`                            | `undefined`   | The amount of token to receive                      |
| `swapForY`  | `bool`                            | `undefined`   | Whether you swap X for Y (true), or Y for X (false) |
| `isQuote`   | `bool`                            | `false`       | -                                                   |

#### Returns

`Result`<`GetSwapInReturn`\>

GetSwapInReturn: amountIn, feesIn

#### Defined in

[assembly/libraries/SwapHelper.ts:78](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/SwapHelper.ts#L78)

---

### getSwapOut

▸ **getSwapOut**(`pair`, `amountIn`, `swapForY`, `isQuote?`): `Result`<`GetSwapOutReturn`\>

Simulate a swap out

#### Parameters

| Name       | Type                              | Default value | Description                                                    |
| :--------- | :-------------------------------- | :------------ | :------------------------------------------------------------- |
| `pair`     | [`IPair`](../interfaces/IPair.md) | `undefined`   | -                                                              |
| `amountIn` | `u256`                            | `undefined`   | The amount of token sent                                       |
| `swapForY` | `bool`                            | `undefined`   | Whether you swap X for Y (true), or Y for X (false)            |
| `isQuote`  | `bool`                            | `false`       | Whether this is a quote or not (will throw or return an error) |

#### Returns

`Result`<`GetSwapOutReturn`\>

GetSwapOutReturn: amountOut, feesIn

#### Defined in

[assembly/libraries/SwapHelper.ts:158](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/SwapHelper.ts#L158)
