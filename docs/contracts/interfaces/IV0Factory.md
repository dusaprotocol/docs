# IV0Factory

## Table of contents

### Constructors

- [constructor](IV0Factory#constructor)

### Properties

- [\_origin](IV0Factory#_origin)

### Methods

- [allPairsLength](IV0Factory#allpairslength)
- [createPair](IV0Factory#createpair)
- [feeTo](IV0Factory#feeto)
- [getPair](IV0Factory#getpair)
- [init](IV0Factory#init)

## Constructors

### constructor

• **new IV0Factory**(`_origin`): [`IV0Factory`](IV0Factory)

#### Parameters

| Name | Type |
| :------ | :------ |
| `_origin` | `Address` |

#### Returns

[`IV0Factory`](IV0Factory)

#### Defined in

[assembly/interfaces/IV0Factory.ts:14](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/interfaces/IV0Factory.ts#L14)

## Properties

### \_origin

• **\_origin**: `Address`

#### Defined in

[assembly/interfaces/IV0Factory.ts:12](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/interfaces/IV0Factory.ts#L12)

## Methods

### allPairsLength

▸ **allPairsLength**(): `u32`

Returns the length of the allPairs array.

#### Returns

`u32`

- The number of pairs.

#### Defined in

[assembly/interfaces/IV0Factory.ts:42](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/interfaces/IV0Factory.ts#L42)

___

### createPair

▸ **createPair**(`_tokenA`, `_tokenB`, `amount`): `Address`

Creates a new pair for tokenA and tokenB.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `_tokenA` | `Address` | - |
| `_tokenB` | `Address` | - |
| `amount` | `u64` | The amount of coins to transfer to the pair for storage fee. |

#### Returns

`Address`

- The address of the created pair.

#### Defined in

[assembly/interfaces/IV0Factory.ts:31](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/interfaces/IV0Factory.ts#L31)

___

### feeTo

▸ **feeTo**(): `Address`

Returns the feeTo address.

#### Returns

`Address`

- The feeTo address.

#### Defined in

[assembly/interfaces/IV0Factory.ts:54](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/interfaces/IV0Factory.ts#L54)

___

### getPair

▸ **getPair**(`tokenA`, `tokenB`): [`IV0Pair`](IV0Pair)

#### Parameters

| Name | Type |
| :------ | :------ |
| `tokenA` | `Address` |
| `tokenB` | `Address` |

#### Returns

[`IV0Pair`](IV0Pair)

#### Defined in

[assembly/interfaces/IV0Factory.ts:58](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/interfaces/IV0Factory.ts#L58)

___

### init

▸ **init**(`_feeToSetter`): `StaticArray`<`u8`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `_feeToSetter` | `Address` |

#### Returns

`StaticArray`<`u8`\>

#### Defined in

[assembly/interfaces/IV0Factory.ts:18](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/interfaces/IV0Factory.ts#L18)
