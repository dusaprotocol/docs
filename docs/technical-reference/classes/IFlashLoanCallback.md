[@dusalabs/core](../README.md) / [Exports](../modules.md) / IFlashLoanCallback

# Class: IFlashLoanCallback

## Table of contents

### Constructors

- [constructor](IFlashLoanCallback.md#constructor)

### Properties

- [\_origin](IFlashLoanCallback.md#_origin)

### Methods

- [flashLoanCallback](IFlashLoanCallback.md#flashloancallback)

## Constructors

### constructor

• **new IFlashLoanCallback**(`at`)

Wraps a smart contract exposing standard token FFI.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `at` | `Address` | Address of the smart contract. |

#### Defined in

[assembly/interfaces/IFlashLoanCallback.ts:13](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/interfaces/IFlashLoanCallback.ts#L13)

## Properties

### \_origin

• **\_origin**: `Address`

#### Defined in

[assembly/interfaces/IFlashLoanCallback.ts:6](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/interfaces/IFlashLoanCallback.ts#L6)

## Methods

### flashLoanCallback

▸ **flashLoanCallback**(`sender`, `token`, `amount`, `fee`): `StaticArray`<`u8`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `sender` | `Address` |
| `token` | [`IERC20`](IERC20.md) |
| `amount` | `u64` |
| `fee` | `u64` |

#### Returns

`StaticArray`<`u8`\>

#### Defined in

[assembly/interfaces/IFlashLoanCallback.ts:17](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/interfaces/IFlashLoanCallback.ts#L17)
