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
- [router](IQuoter.md#router)

## Constructors

### constructor

• **new IQuoter**(`_origin`)

#### Parameters

| Name | Type |
| :------ | :------ |
| `_origin` | `Address` |

#### Defined in

[assembly/interfaces/IQuoter.ts:9](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/interfaces/IQuoter.ts#L9)

## Properties

### \_origin

• **\_origin**: `Address`

#### Defined in

[assembly/interfaces/IQuoter.ts:9](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/interfaces/IQuoter.ts#L9)

## Methods

### factory

▸ **factory**(): [`IFactory`](IFactory.md)

#### Returns

[`IFactory`](IFactory.md)

#### Defined in

[assembly/interfaces/IQuoter.ts:33](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/interfaces/IQuoter.ts#L33)

___

### findBestPathFromAmountIn

▸ **findBestPathFromAmountIn**(`route`, `amountIn`): `Quote`

#### Parameters

| Name | Type |
| :------ | :------ |
| `route` | `Address`[] |
| `amountIn` | `u64` |

#### Returns

`Quote`

#### Defined in

[assembly/interfaces/IQuoter.ts:16](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/interfaces/IQuoter.ts#L16)

___

### findBestPathFromAmountOut

▸ **findBestPathFromAmountOut**(`route`, `amountOut`): `Quote`

#### Parameters

| Name | Type |
| :------ | :------ |
| `route` | `Address`[] |
| `amountOut` | `u64` |

#### Returns

`Quote`

#### Defined in

[assembly/interfaces/IQuoter.ts:22](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/interfaces/IQuoter.ts#L22)

___

### init

▸ **init**(`router`, `factory`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `router` | `Address` |
| `factory` | `Address` |

#### Returns

`void`

#### Defined in

[assembly/interfaces/IQuoter.ts:11](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/interfaces/IQuoter.ts#L11)

___

### router

▸ **router**(): [`IRouter`](IRouter.md)

#### Returns

[`IRouter`](IRouter.md)

#### Defined in

[assembly/interfaces/IQuoter.ts:28](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/interfaces/IQuoter.ts#L28)
