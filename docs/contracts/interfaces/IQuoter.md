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
- [legacyFactory](IQuoter.md#legacyfactory)
- [v0Factory](IQuoter.md#v0factory)

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

[assembly/interfaces/IQuoter.ts:10](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/interfaces/IQuoter.ts#L10)

## Properties

### \_origin

• **\_origin**: `Address`

#### Defined in

[assembly/interfaces/IQuoter.ts:10](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/interfaces/IQuoter.ts#L10)

## Methods

### factory

▸ **factory**(): [`IFactory`](IFactory.md)

#### Returns

[`IFactory`](IFactory.md)

#### Defined in

[assembly/interfaces/IQuoter.ts:43](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/interfaces/IQuoter.ts#L43)

___

### findBestPathFromAmountIn

▸ **findBestPathFromAmountIn**(`route`, `amountIn`, `checkLegacy`): `Quote`

#### Parameters

| Name | Type |
| :------ | :------ |
| `route` | `Address`[] |
| `amountIn` | `u256` |
| `checkLegacy` | `bool` |

#### Returns

`Quote`

#### Defined in

[assembly/interfaces/IQuoter.ts:17](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/interfaces/IQuoter.ts#L17)

___

### findBestPathFromAmountOut

▸ **findBestPathFromAmountOut**(`route`, `amountOut`, `checkLegacy`): `Quote`

#### Parameters

| Name | Type |
| :------ | :------ |
| `route` | `Address`[] |
| `amountOut` | `u256` |
| `checkLegacy` | `bool` |

#### Returns

`Quote`

#### Defined in

[assembly/interfaces/IQuoter.ts:30](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/interfaces/IQuoter.ts#L30)

___

### init

▸ **init**(`factory`, `v0Factory`, `legacyFactory`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `factory` | `Address` |
| `v0Factory` | `Address` |
| `legacyFactory` | `Address` |

#### Returns

`void`

#### Defined in

[assembly/interfaces/IQuoter.ts:12](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/interfaces/IQuoter.ts#L12)

___

### legacyFactory

▸ **legacyFactory**(): [`IV0Factory`](IV0Factory)

#### Returns

[`IV0Factory`](IV0Factory)

#### Defined in

[assembly/interfaces/IQuoter.ts:53](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/interfaces/IQuoter.ts#L53)

___

### v0Factory

▸ **v0Factory**(): [`IV0Factory`](IV0Factory)

#### Returns

[`IV0Factory`](IV0Factory)

#### Defined in

[assembly/interfaces/IQuoter.ts:48](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/interfaces/IQuoter.ts#L48)
