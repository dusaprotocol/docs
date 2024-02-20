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
| `debtX` | `u256` | `u256.Zero` |
| `debtY` | `u256` | `u256.Zero` |

#### Returns

[`Debt`](Debt.md)

#### Defined in

[assembly/structs/Debt.ts:10](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/structs/Debt.ts#L10)

## Properties

### debtX

• **debtX**: `u256` = `u256.Zero`

#### Defined in

[assembly/structs/Debt.ts:11](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/structs/Debt.ts#L11)

___

### debtY

• **debtY**: `u256` = `u256.Zero`

#### Defined in

[assembly/structs/Debt.ts:12](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/structs/Debt.ts#L12)

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

[assembly/structs/Debt.ts:19](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/structs/Debt.ts#L19)

___

### serialize

▸ **serialize**(): `StaticArray`<`u8`\>

#### Returns

`StaticArray`<`u8`\>

#### Implementation of

Serializable.serialize

#### Defined in

[assembly/structs/Debt.ts:15](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/structs/Debt.ts#L15)
