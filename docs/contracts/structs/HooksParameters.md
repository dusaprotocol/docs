# HooksParameters

## Implements

- `Serializable`

## Table of contents

### Constructors

- [constructor](HooksParameters#constructor)

### Properties

- [flags](HooksParameters#flags)
- [hooks](HooksParameters#hooks)

### Methods

- [deserialize](HooksParameters#deserialize)
- [serialize](HooksParameters#serialize)

## Constructors

### constructor

• **new HooksParameters**(`hooks?`, `flags?`): [`HooksParameters`](HooksParameters)

#### Parameters

| Name | Type | Default value |
| :------ | :------ | :------ |
| `hooks` | `Address` | `undefined` |
| `flags` | `u32` | `0` |

#### Returns

[`HooksParameters`](HooksParameters)

#### Defined in

[assembly/libraries/Hooks.ts:19](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Hooks.ts#L19)

## Properties

### flags

• **flags**: `u32` = `0`

#### Defined in

[assembly/libraries/Hooks.ts:21](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Hooks.ts#L21)

___

### hooks

• **hooks**: `Address`

#### Defined in

[assembly/libraries/Hooks.ts:20](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Hooks.ts#L20)

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

[assembly/libraries/Hooks.ts:28](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Hooks.ts#L28)

___

### serialize

▸ **serialize**(): `StaticArray`<`u8`\>

#### Returns

`StaticArray`<`u8`\>

#### Implementation of

Serializable.serialize

#### Defined in

[assembly/libraries/Hooks.ts:24](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Hooks.ts#L24)
