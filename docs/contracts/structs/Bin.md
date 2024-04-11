# Bin

## Implements

- `Serializable`

## Table of contents

### Constructors

- [constructor](Bin.md#constructor)

### Properties

- [accTokenXPerShare](Bin.md#acctokenxpershare)
- [accTokenYPerShare](Bin.md#acctokenypershare)
- [reserveX](Bin.md#reservex)
- [reserveY](Bin.md#reservey)

### Methods

- [deserialize](Bin.md#deserialize)
- [serialize](Bin.md#serialize)
- [updateFees](Bin.md#updatefees)
- [updateReserves](Bin.md#updatereserves)

## Constructors

### constructor

• **new Bin**(`reserveX?`, `reserveY?`, `accTokenXPerShare?`, `accTokenYPerShare?`): [`Bin`](Bin.md)

#### Parameters

| Name | Type | Default value | Description |
| :------ | :------ | :------ | :------ |
| `reserveX` | `u256` | `u256.Zero` | The current reserve of tokenX of the bin |
| `reserveY` | `u256` | `u256.Zero` | The current reserve of tokenY of the bin |
| `accTokenXPerShare` | `u256` | `u256.Zero` | - |
| `accTokenYPerShare` | `u256` | `u256.Zero` | - |

#### Returns

[`Bin`](Bin.md)

#### Defined in

[assembly/structs/Bin.ts:12](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/structs/Bin.ts#L12)

## Properties

### accTokenXPerShare

• **accTokenXPerShare**: `u256` = `u256.Zero`

#### Defined in

[assembly/structs/Bin.ts:15](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/structs/Bin.ts#L15)

___

### accTokenYPerShare

• **accTokenYPerShare**: `u256` = `u256.Zero`

#### Defined in

[assembly/structs/Bin.ts:16](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/structs/Bin.ts#L16)

___

### reserveX

• **reserveX**: `u256` = `u256.Zero`

The current reserve of tokenX of the bin

#### Defined in

[assembly/structs/Bin.ts:13](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/structs/Bin.ts#L13)

___

### reserveY

• **reserveY**: `u256` = `u256.Zero`

The current reserve of tokenY of the bin

#### Defined in

[assembly/structs/Bin.ts:14](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/structs/Bin.ts#L14)

## Methods

### deserialize

▸ **deserialize**(`data`, `offset`): `Result`<`i32`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `data` | `StaticArray`<`u8`\> |
| `offset` | `i32` |

#### Returns

`Result`<`i32`\>

#### Implementation of

Serializable.deserialize

#### Defined in

[assembly/structs/Bin.ts:96](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/structs/Bin.ts#L96)

___

### serialize

▸ **serialize**(): `StaticArray`<`u8`\>

#### Returns

`StaticArray`<`u8`\>

#### Implementation of

Serializable.serialize

#### Defined in

[assembly/structs/Bin.ts:87](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/structs/Bin.ts#L87)

___

### updateFees

▸ **updateFees**(`pair`, `fees`, `swapForY`, `totalSupply`): `void`

Update the fees of the pair and accumulated token per share of the bin

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `pair` | [`PairInformation`](PairInformation.md) | - |
| `fees` | [`FeesDistribution`](FeesDistribution.md) | The fees amounts added to the pairFees |
| `swapForY` | `bool` | whether the token sent was Y (true) or X (false) |
| `totalSupply` | `u256` | The total supply of the token id |

#### Returns

`void`

#### Defined in

[assembly/structs/Bin.ts:27](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/structs/Bin.ts#L27)

___

### updateReserves

▸ **updateReserves**(`pair`, `swapForY`, `amountInToBin`, `amountOutOfBin`): `void`

Update reserves

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `pair` | [`PairInformation`](PairInformation.md) | The pair information |
| `swapForY` | `bool` | whether the token sent was Y (true) or X (false) |
| `amountInToBin` | `u256` | The amount of token that is added to the bin without fees |
| `amountOutOfBin` | `u256` | The amount of token that is removed from the bin |

#### Returns

`void`

#### Defined in

[assembly/structs/Bin.ts:60](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/structs/Bin.ts#L60)
