# Debt

**`Dev`**

Structure to store the debts of users

**`Param`**

The tokenX's debt

**`Param`**

The tokenY's debt

## Implements

- `Serializable`

## Table of contents

### Constructors

- [constructor](Debt.md#constructor)

### Properties

- [debtX](Debt.md#debtx)
- [debtY](Debt.md#debty)

### Methods

- [deserialize](Debt.md#deserialize)
- [serialize](Debt.md#serialize)

## Constructors

### constructor

• **new Debt**(`debtX?`, `debtY?`): [`Debt`](Debt.md)

#### Parameters

| Name | Type | Default value |
| :------ | :------ | :------ |
| `debtX` | `u256` | `ZERO` |
| `debtY` | `u256` | `ZERO` |

#### Returns

[`Debt`](Debt.md)

#### Defined in

[assembly/structs/Debt.ts:11](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/structs/Debt.ts#L11)

## Properties

### debtX

• **debtX**: `u256` = `ZERO`

#### Defined in

[assembly/structs/Debt.ts:12](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/structs/Debt.ts#L12)

___

### debtY

• **debtY**: `u256` = `ZERO`

#### Defined in

[assembly/structs/Debt.ts:13](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/structs/Debt.ts#L13)

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

[assembly/structs/Debt.ts:20](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/structs/Debt.ts#L20)

___

### serialize

▸ **serialize**(): `StaticArray`<`u8`\>

#### Returns

`StaticArray`<`u8`\>

#### Implementation of

Serializable.serialize

#### Defined in

[assembly/structs/Debt.ts:16](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/structs/Debt.ts#L16)
