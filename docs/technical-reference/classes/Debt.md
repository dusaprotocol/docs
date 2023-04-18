Debt

# Class: Debt

## Implements

-   `Serializable`

## Table of contents

### Constructors

-   [constructor](Debt.md#constructor)

### Properties

-   [debtX](Debt.md#debtx)
-   [debtY](Debt.md#debty)

### Methods

-   [deserialize](Debt.md#deserialize)
-   [serialize](Debt.md#serialize)

## Constructors

### constructor

• **new Debt**(`debtX?`, `debtY?`)

#### Parameters

| Name    | Type  | Default value |
| :------ | :---- | :------------ |
| `debtX` | `u64` | `0`           |
| `debtY` | `u64` | `0`           |

#### Defined in

[assembly/structs/Debt.ts:4](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/structs/Debt.ts#L4)

## Properties

### debtX

• **debtX**: `u64` = `0`

#### Defined in

[assembly/structs/Debt.ts:4](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/structs/Debt.ts#L4)

---

### debtY

• **debtY**: `u64` = `0`

#### Defined in

[assembly/structs/Debt.ts:4](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/structs/Debt.ts#L4)

## Methods

### deserialize

▸ **deserialize**(`data`, `offset`): `Result`<`i32`\>

#### Parameters

| Name     | Type                 |
| :------- | :------------------- |
| `data`   | `StaticArray`<`u8`\> |
| `offset` | `i32`                |

#### Returns

`Result`<`i32`\>

#### Implementation of

Serializable.deserialize

#### Defined in

[assembly/structs/Debt.ts:10](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/structs/Debt.ts#L10)

---

### serialize

▸ **serialize**(): `StaticArray`<`u8`\>

#### Returns

`StaticArray`<`u8`\>

#### Implementation of

Serializable.serialize

#### Defined in

[assembly/structs/Debt.ts:6](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/structs/Debt.ts#L6)
