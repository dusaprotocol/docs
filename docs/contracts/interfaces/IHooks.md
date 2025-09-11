# IHooks

## Table of contents

### Constructors

- [constructor](IHooks#constructor)

### Properties

- [\_origin](IHooks#_origin)

### Methods

- [afterBatchTransferFrom](IHooks#afterbatchtransferfrom)
- [afterBurn](IHooks#afterburn)
- [afterFlashLoan](IHooks#afterflashloan)
- [afterMint](IHooks#aftermint)
- [afterSwap](IHooks#afterswap)
- [beforeBatchTransferFrom](IHooks#beforebatchtransferfrom)
- [beforeBurn](IHooks#beforeburn)
- [beforeFlashLoan](IHooks#beforeflashloan)
- [beforeMint](IHooks#beforemint)
- [beforeSwap](IHooks#beforeswap)
- [getPair](IHooks#getpair)
- [init](IHooks#init)
- [isLinked](IHooks#islinked)
- [onHooksSet](IHooks#onhooksset)

## Constructors

### constructor

• **new IHooks**(`at`): [`IHooks`](IHooks)

Wraps a smart contract exposing standard token FFI.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `at` | `Address` | Address of the smart contract. |

#### Returns

[`IHooks`](IHooks)

#### Defined in

[assembly/interfaces/IHooks.ts:16](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/interfaces/IHooks.ts#L16)

## Properties

### \_origin

• **\_origin**: `Address`

#### Defined in

[assembly/interfaces/IHooks.ts:9](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/interfaces/IHooks.ts#L9)

## Methods

### afterBatchTransferFrom

▸ **afterBatchTransferFrom**(`sender`, `from`, `to`, `ids`, `amounts`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `sender` | `Address` |
| `from` | `Address` |
| `to` | `Address` |
| `ids` | `u64`[] |
| `amounts` | `u256`[] |

#### Returns

`void`

#### Defined in

[assembly/interfaces/IHooks.ts:149](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/interfaces/IHooks.ts#L149)

___

### afterBurn

▸ **afterBurn**(`sender`, `to`, `ids`, `amountsToBurn`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `sender` | `Address` |
| `to` | `Address` |
| `ids` | `u64`[] |
| `amountsToBurn` | `u256`[] |

#### Returns

`void`

#### Defined in

[assembly/interfaces/IHooks.ts:128](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/interfaces/IHooks.ts#L128)

___

### afterFlashLoan

▸ **afterFlashLoan**(`sender`, `to`, `fees`, `feesReceived`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `sender` | `Address` |
| `to` | `Address` |
| `fees` | `u256` |
| `feesReceived` | `u256` |

#### Returns

`void`

#### Defined in

[assembly/interfaces/IHooks.ts:72](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/interfaces/IHooks.ts#L72)

___

### afterMint

▸ **afterMint**(`sender`, `to`, `ids`, `distributionX`, `distributionY`, `amountsIn`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `sender` | `Address` |
| `to` | `Address` |
| `ids` | `u64`[] |
| `distributionX` | `u256`[] |
| `distributionY` | `u256`[] |
| `amountsIn` | `u256`[] |

#### Returns

`void`

#### Defined in

[assembly/interfaces/IHooks.ts:100](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/interfaces/IHooks.ts#L100)

___

### afterSwap

▸ **afterSwap**(`sender`, `to`, `swapForY`, `amountOut`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `sender` | `Address` |
| `to` | `Address` |
| `swapForY` | `bool` |
| `amountOut` | `u256` |

#### Returns

`void`

#### Defined in

[assembly/interfaces/IHooks.ts:57](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/interfaces/IHooks.ts#L57)

___

### beforeBatchTransferFrom

▸ **beforeBatchTransferFrom**(`sender`, `from`, `to`, `ids`, `amounts`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `sender` | `Address` |
| `from` | `Address` |
| `to` | `Address` |
| `ids` | `u64`[] |
| `amounts` | `u256`[] |

#### Returns

`void`

#### Defined in

[assembly/interfaces/IHooks.ts:138](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/interfaces/IHooks.ts#L138)

___

### beforeBurn

▸ **beforeBurn**(`sender`, `to`, `ids`, `amountsToBurn`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `sender` | `Address` |
| `to` | `Address` |
| `ids` | `u64`[] |
| `amountsToBurn` | `u256`[] |

#### Returns

`void`

#### Defined in

[assembly/interfaces/IHooks.ts:118](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/interfaces/IHooks.ts#L118)

___

### beforeFlashLoan

▸ **beforeFlashLoan**(`sender`, `to`, `amount`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `sender` | `Address` |
| `to` | `Address` |
| `amount` | `u256` |

#### Returns

`void`

#### Defined in

[assembly/interfaces/IHooks.ts:67](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/interfaces/IHooks.ts#L67)

___

### beforeMint

▸ **beforeMint**(`sender`, `to`, `ids`, `distributionX`, `distributionY`, `amountsReceived`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `sender` | `Address` |
| `to` | `Address` |
| `ids` | `u64`[] |
| `distributionX` | `u256`[] |
| `distributionY` | `u256`[] |
| `amountsReceived` | `u256`[] |

#### Returns

`void`

#### Defined in

[assembly/interfaces/IHooks.ts:82](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/interfaces/IHooks.ts#L82)

___

### beforeSwap

▸ **beforeSwap**(`sender`, `to`, `swapForY`, `amountIn`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `sender` | `Address` |
| `to` | `Address` |
| `swapForY` | `bool` |
| `amountIn` | `u256` |

#### Returns

`void`

#### Defined in

[assembly/interfaces/IHooks.ts:47](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/interfaces/IHooks.ts#L47)

___

### getPair

▸ **getPair**(): [`IPair`](IPair.md)

#### Returns

[`IPair`](IPair.md)

#### Defined in

[assembly/interfaces/IHooks.ts:30](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/interfaces/IHooks.ts#L30)

___

### init

▸ **init**(`pair`, `masToSend`): `void`

Calls the constructor

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `pair` | `Address` | The pair associated to this hook |
| `masToSend` | `u64` | - |

#### Returns

`void`

#### Defined in

[assembly/interfaces/IHooks.ts:25](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/interfaces/IHooks.ts#L25)

___

### isLinked

▸ **isLinked**(): `bool`

#### Returns

`bool`

#### Defined in

[assembly/interfaces/IHooks.ts:34](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/interfaces/IHooks.ts#L34)

___

### onHooksSet

▸ **onHooksSet**(`hooksParameters`, `onHooksSetData`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `hooksParameters` | [`HooksParameters`](../structs/HooksParameters) |
| `onHooksSetData` | `StaticArray`<`u8`\> |

#### Returns

`void`

#### Defined in

[assembly/interfaces/IHooks.ts:39](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/interfaces/IHooks.ts#L39)
