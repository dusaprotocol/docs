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
| `bs` | `StaticArray`<`u8`\> | Byte string |

#### Returns

`StaticArray`<`u8`\>

#### Defined in

[assembly/contracts/Router.ts:85](https://github.com/dusaprotocol/v2.1/blob/0058e1c/assembly/contracts/Router.ts#L85)

___

### addLiquidityMAS

▸ **addLiquidityMAS**(`bs`): `StaticArray`<`u8`\>

Add liquidity with MAS while performing safety checks
This function is compliant with fee on transfer tokens

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `bs` | `StaticArray`<`u8`\> | Byte string |

#### Returns

`StaticArray`<`u8`\>

#### Defined in

[assembly/contracts/Router.ts:109](https://github.com/dusaprotocol/v2.1/blob/0058e1c/assembly/contracts/Router.ts#L109)

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

[assembly/contracts/Router.ts:33](https://github.com/dusaprotocol/v2.1/blob/0058e1c/assembly/contracts/Router.ts#L33)

___

### createLBPair

▸ **createLBPair**(`bs`): `StaticArray`<`u8`\>

Create a liquidity book Pair for _tokenX and _tokenY using the factory

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `bs` | `StaticArray`<`u8`\> | Byte string |

#### Returns

`StaticArray`<`u8`\>

- Byte string

#### Defined in

[assembly/contracts/Router.ts:57](https://github.com/dusaprotocol/v2.1/blob/0058e1c/assembly/contracts/Router.ts#L57)

___

### getSwapIn

▸ **getSwapIn**(`bs`): `StaticArray`<`u8`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `bs` | `StaticArray`<`u8`\> |

#### Returns

`StaticArray`<`u8`\>

#### Defined in

[assembly/contracts/Router.ts:646](https://github.com/dusaprotocol/v2.1/blob/0058e1c/assembly/contracts/Router.ts#L646)

___

### getSwapOut

▸ **getSwapOut**(`bs`): `StaticArray`<`u8`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `bs` | `StaticArray`<`u8`\> |

#### Returns

`StaticArray`<`u8`\>

#### Defined in

[assembly/contracts/Router.ts:656](https://github.com/dusaprotocol/v2.1/blob/0058e1c/assembly/contracts/Router.ts#L656)

___

### removeLiquidity

▸ **removeLiquidity**(`bs`): `StaticArray`<`u8`\>

Remove liquidity while performing safety checks
This function is compliant with fee on transfer tokens

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `bs` | `StaticArray`<`u8`\> | Byte string |

#### Returns

`StaticArray`<`u8`\>

#### Defined in

[assembly/contracts/Router.ts:151](https://github.com/dusaprotocol/v2.1/blob/0058e1c/assembly/contracts/Router.ts#L151)

___

### removeLiquidityMAS

▸ **removeLiquidityMAS**(`bs`): `StaticArray`<`u8`\>

Remove liquidity with MAS while performing safety checks
This function is compliant with fee on transfer tokens

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `bs` | `StaticArray`<`u8`\> | Byte string |

#### Returns

`StaticArray`<`u8`\>

#### Defined in

[assembly/contracts/Router.ts:188](https://github.com/dusaprotocol/v2.1/blob/0058e1c/assembly/contracts/Router.ts#L188)

___

### swapExactMASForTokens

▸ **swapExactMASForTokens**(`bs`): `StaticArray`<`u8`\>

Swaps exact MAS for tokens while performing safety checks

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `bs` | `StaticArray`<`u8`\> | Byte string |

#### Returns

`StaticArray`<`u8`\>

#### Defined in

[assembly/contracts/Router.ts:290](https://github.com/dusaprotocol/v2.1/blob/0058e1c/assembly/contracts/Router.ts#L290)

___

### swapExactTokensForMAS

▸ **swapExactTokensForMAS**(`bs`): `StaticArray`<`u8`\>

Swaps exact tokens for MAS while performing safety checks

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `bs` | `StaticArray`<`u8`\> | Byte string |

#### Returns

`StaticArray`<`u8`\>

#### Defined in

[assembly/contracts/Router.ts:254](https://github.com/dusaprotocol/v2.1/blob/0058e1c/assembly/contracts/Router.ts#L254)

___

### swapExactTokensForTokens

▸ **swapExactTokensForTokens**(`bs`): `StaticArray`<`u8`\>

Swap tokens while performing safety checks

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `bs` | `StaticArray`<`u8`\> | Byte string |

#### Returns

`StaticArray`<`u8`\>

#### Defined in

[assembly/contracts/Router.ts:227](https://github.com/dusaprotocol/v2.1/blob/0058e1c/assembly/contracts/Router.ts#L227)

___

### swapMASForExactTokens

▸ **swapMASForExactTokens**(`bs`): `StaticArray`<`u8`\>

Swaps MAS for exact tokens while performing safety checks

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `bs` | `StaticArray`<`u8`\> | Byte string |

#### Returns

`StaticArray`<`u8`\>

#### Defined in

[assembly/contracts/Router.ts:389](https://github.com/dusaprotocol/v2.1/blob/0058e1c/assembly/contracts/Router.ts#L389)

___

### swapTokensForExactMAS

▸ **swapTokensForExactMAS**(`bs`): `StaticArray`<`u8`\>

Swaps tokens for exact MAS while performing safety checks

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `bs` | `StaticArray`<`u8`\> | Byte string |

#### Returns

`StaticArray`<`u8`\>

#### Defined in

[assembly/contracts/Router.ts:350](https://github.com/dusaprotocol/v2.1/blob/0058e1c/assembly/contracts/Router.ts#L350)

___

### swapTokensForExactTokens

▸ **swapTokensForExactTokens**(`bs`): `StaticArray`<`u8`\>

Swaps tokens for exact tokens while performing safety checks

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `bs` | `StaticArray`<`u8`\> | Byte string |

#### Returns

`StaticArray`<`u8`\>

#### Defined in

[assembly/contracts/Router.ts:320](https://github.com/dusaprotocol/v2.1/blob/0058e1c/assembly/contracts/Router.ts#L320)

___

### sweep

▸ **sweep**(`bs`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `bs` | `StaticArray`<`u8`\> |

#### Returns

`void`

#### Defined in

[assembly/contracts/Router.ts:430](https://github.com/dusaprotocol/v2.1/blob/0058e1c/assembly/contracts/Router.ts#L430)

___

### sweepLBToken

▸ **sweepLBToken**(`bs`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `bs` | `StaticArray`<`u8`\> |

#### Returns

`void`

#### Defined in

[assembly/contracts/Router.ts:453](https://github.com/dusaprotocol/v2.1/blob/0058e1c/assembly/contracts/Router.ts#L453)
