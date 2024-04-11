# IQuoter

## Table of contents

### Constructors

- [constructor](IQuoter.md#constructor)

### Properties

- [\_origin](IQuoter.md#_origin)

### Methods

- [factory](IQuoter.md#factory)
- [findBestPathFromAmountIn](IQuoter.md#findbestpathfromamountin)
- [findBestPathFromAmountOut](IQuoter.md#findbestpathfromamountout)
- [init](IQuoter.md#init)

## Constructors

### constructor

• **new IQuoter**(`_origin`): [`IQuoter`](IQuoter.md)

#### Parameters

| Name | Type |
| :------ | :------ |
| `_origin` | `Address` |

#### Returns

[`IQuoter`](IQuoter.md)

#### Defined in

[assembly/interfaces/IQuoter.ts:9](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/interfaces/IQuoter.ts#L9)

## Properties

### \_origin

• **\_origin**: `Address`

#### Defined in

[assembly/interfaces/IQuoter.ts:9](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/interfaces/IQuoter.ts#L9)

## Methods

### factory

▸ **factory**(): [`IFactory`](IFactory.md)

#### Returns

[`IFactory`](IFactory.md)

#### Defined in

[assembly/interfaces/IQuoter.ts:28](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/interfaces/IQuoter.ts#L28)

___

### findBestPathFromAmountIn

▸ **findBestPathFromAmountIn**(`route`, `amountIn`): `Quote`

#### Parameters

| Name | Type |
| :------ | :------ |
| `route` | `Address`[] |
| `amountIn` | `u256` |

#### Returns

`Quote`

#### Defined in

[assembly/interfaces/IQuoter.ts:16](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/interfaces/IQuoter.ts#L16)

___

### findBestPathFromAmountOut

▸ **findBestPathFromAmountOut**(`route`, `amountOut`): `Quote`

#### Parameters

| Name | Type |
| :------ | :------ |
| `route` | `Address`[] |
| `amountOut` | `u256` |

#### Returns

`Quote`

#### Defined in

[assembly/interfaces/IQuoter.ts:22](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/interfaces/IQuoter.ts#L22)

___

### init

▸ **init**(`factory`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `factory` | `Address` |

#### Returns

`void`

#### Defined in

[assembly/interfaces/IQuoter.ts:11](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/interfaces/IQuoter.ts#L11)
