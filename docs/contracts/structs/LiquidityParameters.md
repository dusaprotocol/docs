# LiquidityParameters

## Implements

- `Serializable`

## Table of contents

### Constructors

- [constructor](LiquidityParameters.md#constructor)

### Properties

- [activeIdDesired](LiquidityParameters.md#activeiddesired)
- [amountX](LiquidityParameters.md#amountx)
- [amountXMin](LiquidityParameters.md#amountxmin)
- [amountY](LiquidityParameters.md#amounty)
- [amountYMin](LiquidityParameters.md#amountymin)
- [binStep](LiquidityParameters.md#binstep)
- [deadline](LiquidityParameters.md#deadline)
- [deltaIds](LiquidityParameters.md#deltaids)
- [distributionX](LiquidityParameters.md#distributionx)
- [distributionY](LiquidityParameters.md#distributiony)
- [idSlippage](LiquidityParameters.md#idslippage)
- [to](LiquidityParameters.md#to)
- [tokenX](LiquidityParameters.md#tokenx)
- [tokenY](LiquidityParameters.md#tokeny)

### Methods

- [deserialize](LiquidityParameters.md#deserialize)
- [serialize](LiquidityParameters.md#serialize)

## Constructors

### constructor

• **new LiquidityParameters**(`tokenX?`, `tokenY?`, `binStep?`, `amountX?`, `amountY?`, `amountXMin?`, `amountYMin?`, `activeIdDesired?`, `idSlippage?`, `deltaIds?`, `distributionX?`, `distributionY?`, `to?`, `deadline?`)

#### Parameters

| Name | Type | Default value | Description |
| :------ | :------ | :------ | :------ |
| `tokenX` | [`../interfaces/IERC20`](../interfaces/IERC20.md) | `undefined` | The address of token X |
| `tokenY` | [`../interfaces/IERC20`](../interfaces/IERC20.md) | `undefined` | The address of token Y |
| `binStep` | `u64` | `0` | The bin step of the pair |
| `amountX` | `u64` | `0` | The amount to send of token X |
| `amountY` | `u64` | `0` | The amount to send of token Y |
| `amountXMin` | `u64` | `0` | The min amount of token X added to liquidity |
| `amountYMin` | `u64` | `0` | The min amount of token Y added to liquidity |
| `activeIdDesired` | `u64` | `0` | The active id that user wants to add liquidity from |
| `idSlippage` | `u64` | `0` | The number of id that are allowed to slip |
| `deltaIds` | `i64`[] | `[]` | The list of delta ids to add liquidity (`deltaId = activeId - desiredId`) |
| `distributionX` | `u64`[] | `[]` | The distribution of tokenX with sum(distributionX) = 1e9 (100%) or 0 (0%) |
| `distributionY` | `u64`[] | `[]` | The distribution of tokenY with sum(distributionY) = 1e9 (100%) or 0 (0%) |
| `to` | `Address` | `undefined` | The address of the recipient |
| `deadline` | `u64` | `0` | The deadline of the tx |

#### Defined in

[assembly/structs/LiquidityParameters.ts:23](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/structs/LiquidityParameters.ts#L23)

## Properties

### activeIdDesired

• **activeIdDesired**: `u64` = `0`

The active id that user wants to add liquidity from

#### Defined in

[assembly/structs/LiquidityParameters.ts:31](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/structs/LiquidityParameters.ts#L31)

___

### amountX

• **amountX**: `u64` = `0`

The amount to send of token X

#### Defined in

[assembly/structs/LiquidityParameters.ts:27](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/structs/LiquidityParameters.ts#L27)

___

### amountXMin

• **amountXMin**: `u64` = `0`

The min amount of token X added to liquidity

#### Defined in

[assembly/structs/LiquidityParameters.ts:29](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/structs/LiquidityParameters.ts#L29)

___

### amountY

• **amountY**: `u64` = `0`

The amount to send of token Y

#### Defined in

[assembly/structs/LiquidityParameters.ts:28](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/structs/LiquidityParameters.ts#L28)

___

### amountYMin

• **amountYMin**: `u64` = `0`

The min amount of token Y added to liquidity

#### Defined in

[assembly/structs/LiquidityParameters.ts:30](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/structs/LiquidityParameters.ts#L30)

___

### binStep

• **binStep**: `u64` = `0`

The bin step of the pair

#### Defined in

[assembly/structs/LiquidityParameters.ts:26](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/structs/LiquidityParameters.ts#L26)

___

### deadline

• **deadline**: `u64` = `0`

The deadline of the tx

#### Defined in

[assembly/structs/LiquidityParameters.ts:37](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/structs/LiquidityParameters.ts#L37)

___

### deltaIds

• **deltaIds**: `i64`[] = `[]`

The list of delta ids to add liquidity (`deltaId = activeId - desiredId`)

#### Defined in

[assembly/structs/LiquidityParameters.ts:33](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/structs/LiquidityParameters.ts#L33)

___

### distributionX

• **distributionX**: `u64`[] = `[]`

The distribution of tokenX with sum(distributionX) = 1e9 (100%) or 0 (0%)

#### Defined in

[assembly/structs/LiquidityParameters.ts:34](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/structs/LiquidityParameters.ts#L34)

___

### distributionY

• **distributionY**: `u64`[] = `[]`

The distribution of tokenY with sum(distributionY) = 1e9 (100%) or 0 (0%)

#### Defined in

[assembly/structs/LiquidityParameters.ts:35](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/structs/LiquidityParameters.ts#L35)

___

### idSlippage

• **idSlippage**: `u64` = `0`

The number of id that are allowed to slip

#### Defined in

[assembly/structs/LiquidityParameters.ts:32](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/structs/LiquidityParameters.ts#L32)

___

### to

• **to**: `Address`

The address of the recipient

#### Defined in

[assembly/structs/LiquidityParameters.ts:36](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/structs/LiquidityParameters.ts#L36)

___

### tokenX

• **tokenX**: [`../interfaces/IERC20`](../interfaces/IERC20.md)

The address of token X

#### Defined in

[assembly/structs/LiquidityParameters.ts:24](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/structs/LiquidityParameters.ts#L24)

___

### tokenY

• **tokenY**: [`../interfaces/IERC20`](../interfaces/IERC20.md)

The address of token Y

#### Defined in

[assembly/structs/LiquidityParameters.ts:25](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/structs/LiquidityParameters.ts#L25)

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

[assembly/structs/LiquidityParameters.ts:63](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/structs/LiquidityParameters.ts#L63)

___

### serialize

▸ **serialize**(): `StaticArray`<`u8`\>

#### Returns

`StaticArray`<`u8`\>

#### Implementation of

Serializable.serialize

#### Defined in

[assembly/structs/LiquidityParameters.ts:44](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/structs/LiquidityParameters.ts#L44)
