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
| `reserveX` | `u256` | `ZERO` | The current reserve of tokenX of the bin |
| `reserveY` | `u256` | `ZERO` | The current reserve of tokenY of the bin |
| `accTokenXPerShare` | `u256` | `ZERO` | - |
| `accTokenYPerShare` | `u256` | `ZERO` | - |

#### Returns

[`Bin`](Bin.md)

#### Defined in

[assembly/structs/Bin.ts:13](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/structs/Bin.ts#L13)

## Properties

### accTokenXPerShare

• **accTokenXPerShare**: `u256` = `ZERO`

#### Defined in

[assembly/structs/Bin.ts:16](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/structs/Bin.ts#L16)

___

### accTokenYPerShare

• **accTokenYPerShare**: `u256` = `ZERO`

#### Defined in

[assembly/structs/Bin.ts:17](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/structs/Bin.ts#L17)

___

### reserveX

• **reserveX**: `u256` = `ZERO`

The current reserve of tokenX of the bin

#### Defined in

[assembly/structs/Bin.ts:14](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/structs/Bin.ts#L14)

___

### reserveY

• **reserveY**: `u256` = `ZERO`

The current reserve of tokenY of the bin

#### Defined in

[assembly/structs/Bin.ts:15](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/structs/Bin.ts#L15)

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

[assembly/structs/Bin.ts:97](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/structs/Bin.ts#L97)

___

### serialize

▸ **serialize**(): `StaticArray`<`u8`\>

#### Returns

`StaticArray`<`u8`\>

#### Implementation of

Serializable.serialize

#### Defined in

[assembly/structs/Bin.ts:88](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/structs/Bin.ts#L88)

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

[assembly/structs/Bin.ts:28](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/structs/Bin.ts#L28)

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

[assembly/structs/Bin.ts:61](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/structs/Bin.ts#L61)
