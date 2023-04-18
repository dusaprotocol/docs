[@dusalabs/core](../README.md) / [Exports](../modules.md) / Router

# Namespace: Router

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

[assembly/contracts/Router.ts:72](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/contracts/Router.ts#L72)

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

[assembly/contracts/Router.ts:94](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/contracts/Router.ts#L94)

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

[assembly/contracts/Router.ts:20](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/contracts/Router.ts#L20)

___

### createLBPair

▸ **createLBPair**(`bs`): `StaticArray`<`u8`\>

Create a liquidity bin LBPair for _tokenX and _tokenY using the factory

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `bs` | `StaticArray`<`u8`\> | Byte string |

#### Returns

`StaticArray`<`u8`\>

- Byte string

#### Defined in

[assembly/contracts/Router.ts:44](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/contracts/Router.ts#L44)

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

[assembly/contracts/Router.ts:609](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/contracts/Router.ts#L609)

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

[assembly/contracts/Router.ts:666](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/contracts/Router.ts#L666)

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

[assembly/contracts/Router.ts:124](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/contracts/Router.ts#L124)

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

[assembly/contracts/Router.ts:161](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/contracts/Router.ts#L161)

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

[assembly/contracts/Router.ts:260](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/contracts/Router.ts#L260)

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

[assembly/contracts/Router.ts:227](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/contracts/Router.ts#L227)

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

[assembly/contracts/Router.ts:200](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/contracts/Router.ts#L200)

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

[assembly/contracts/Router.ts:356](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/contracts/Router.ts#L356)

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

[assembly/contracts/Router.ts:320](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/contracts/Router.ts#L320)

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

[assembly/contracts/Router.ts:290](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/contracts/Router.ts#L290)

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

[assembly/contracts/Router.ts:397](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/contracts/Router.ts#L397)

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

[assembly/contracts/Router.ts:420](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/contracts/Router.ts#L420)
