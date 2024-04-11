# IFlashLoanCallback

## Table of contents

### Constructors

- [constructor](IFlashLoanCallback.md#constructor)

### Properties

- [\_origin](IFlashLoanCallback.md#_origin)

### Methods

- [flashLoanCallback](IFlashLoanCallback.md#flashloancallback)

## Constructors

### constructor

• **new IFlashLoanCallback**(`at`): [`IFlashLoanCallback`](IFlashLoanCallback.md)

Wraps a smart contract exposing standard token FFI.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `at` | `Address` | Address of the smart contract. |

#### Returns

[`IFlashLoanCallback`](IFlashLoanCallback.md)

#### Defined in

[assembly/interfaces/IFlashLoanCallback.ts:14](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/interfaces/IFlashLoanCallback.ts#L14)

## Properties

### \_origin

• **\_origin**: `Address`

#### Defined in

[assembly/interfaces/IFlashLoanCallback.ts:7](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/interfaces/IFlashLoanCallback.ts#L7)

## Methods

### flashLoanCallback

▸ **flashLoanCallback**(`sender`, `token`, `amount`, `fee`): `bool`

#### Parameters

| Name | Type |
| :------ | :------ |
| `sender` | `Address` |
| `token` | [`IERC20`](IERC20.md) |
| `amount` | `u256` |
| `fee` | `u256` |

#### Returns

`bool`

#### Defined in

[assembly/interfaces/IFlashLoanCallback.ts:18](https://github.com/dusaprotocol/v1-core-confidencial/blob/b44ea92/assembly/interfaces/IFlashLoanCallback.ts#L18)
