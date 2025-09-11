# MintInfo

## Implements

- `Serializable`

## Table of contents

### Constructors

- [constructor](MintInfo.md#constructor)

### Properties

- [activeFeeX](MintInfo.md#activefeex)
- [activeFeeY](MintInfo.md#activefeey)
- [amountX](MintInfo.md#amountx)
- [amountXAddedToPair](MintInfo.md#amountxaddedtopair)
- [amountXIn](MintInfo.md#amountxin)
- [amountY](MintInfo.md#amounty)
- [amountYAddedToPair](MintInfo.md#amountyaddedtopair)
- [amountYIn](MintInfo.md#amountyin)
- [distributionX](MintInfo.md#distributionx)
- [distributionY](MintInfo.md#distributiony)
- [id](MintInfo.md#id)
- [totalDistributionX](MintInfo.md#totaldistributionx)
- [totalDistributionY](MintInfo.md#totaldistributiony)

### Methods

- [deserialize](MintInfo.md#deserialize)
- [serialize](MintInfo.md#serialize)

## Constructors

### constructor

• **new MintInfo**(`amountXIn?`, `amountYIn?`, `amountXAddedToPair?`, `amountYAddedToPair?`, `activeFeeX?`, `activeFeeY?`, `totalDistributionX?`, `totalDistributionY?`, `id?`, `amountX?`, `amountY?`, `distributionX?`, `distributionY?`): [`MintInfo`](MintInfo.md)

#### Parameters

| Name | Type | Default value | Description |
| :------ | :------ | :------ | :------ |
| `amountXIn` | `u256` | `ZERO` | The amount of token X sent |
| `amountYIn` | `u256` | `ZERO` | The amount of token Y sent |
| `amountXAddedToPair` | `u256` | `ZERO` | The amount of token X that have been actually added to the pair |
| `amountYAddedToPair` | `u256` | `ZERO` | The amount of token Y that have been actually added to the pair |
| `activeFeeX` | `u256` | `ZERO` | Fees X currently generated |
| `activeFeeY` | `u256` | `ZERO` | Fees Y currently generated |
| `totalDistributionX` | `u256` | `ZERO` | Total distribution of token X. Should be 1e18 (100%) or 0 (0%) |
| `totalDistributionY` | `u256` | `ZERO` | Total distribution of token Y. Should be 1e18 (100%) or 0 (0%) |
| `id` | `u32` | `0` | Id of the current working bin when looping on the distribution array |
| `amountX` | `u256` | `ZERO` | The amount of token X deposited in the current bin |
| `amountY` | `u256` | `ZERO` | The amount of token Y deposited in the current bin |
| `distributionX` | `u256` | `ZERO` | Distribution of token X for the current working bin |
| `distributionY` | `u256` | `ZERO` | Distribution of token Y for the current working bin |

#### Returns

[`MintInfo`](MintInfo.md)

#### Defined in

[assembly/structs/MintInfo.ts:23](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/structs/MintInfo.ts#L23)

## Properties

### activeFeeX

• **activeFeeX**: `u256` = `ZERO`

Fees X currently generated

#### Defined in

[assembly/structs/MintInfo.ts:28](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/structs/MintInfo.ts#L28)

___

### activeFeeY

• **activeFeeY**: `u256` = `ZERO`

Fees Y currently generated

#### Defined in

[assembly/structs/MintInfo.ts:29](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/structs/MintInfo.ts#L29)

___

### amountX

• **amountX**: `u256` = `ZERO`

The amount of token X deposited in the current bin

#### Defined in

[assembly/structs/MintInfo.ts:33](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/structs/MintInfo.ts#L33)

___

### amountXAddedToPair

• **amountXAddedToPair**: `u256` = `ZERO`

The amount of token X that have been actually added to the pair

#### Defined in

[assembly/structs/MintInfo.ts:26](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/structs/MintInfo.ts#L26)

___

### amountXIn

• **amountXIn**: `u256` = `ZERO`

The amount of token X sent

#### Defined in

[assembly/structs/MintInfo.ts:24](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/structs/MintInfo.ts#L24)

___

### amountY

• **amountY**: `u256` = `ZERO`

The amount of token Y deposited in the current bin

#### Defined in

[assembly/structs/MintInfo.ts:34](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/structs/MintInfo.ts#L34)

___

### amountYAddedToPair

• **amountYAddedToPair**: `u256` = `ZERO`

The amount of token Y that have been actually added to the pair

#### Defined in

[assembly/structs/MintInfo.ts:27](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/structs/MintInfo.ts#L27)

___

### amountYIn

• **amountYIn**: `u256` = `ZERO`

The amount of token Y sent

#### Defined in

[assembly/structs/MintInfo.ts:25](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/structs/MintInfo.ts#L25)

___

### distributionX

• **distributionX**: `u256` = `ZERO`

Distribution of token X for the current working bin

#### Defined in

[assembly/structs/MintInfo.ts:35](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/structs/MintInfo.ts#L35)

___

### distributionY

• **distributionY**: `u256` = `ZERO`

Distribution of token Y for the current working bin

#### Defined in

[assembly/structs/MintInfo.ts:36](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/structs/MintInfo.ts#L36)

___

### id

• **id**: `u32` = `0`

Id of the current working bin when looping on the distribution array

#### Defined in

[assembly/structs/MintInfo.ts:32](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/structs/MintInfo.ts#L32)

___

### totalDistributionX

• **totalDistributionX**: `u256` = `ZERO`

Total distribution of token X. Should be 1e18 (100%) or 0 (0%)

#### Defined in

[assembly/structs/MintInfo.ts:30](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/structs/MintInfo.ts#L30)

___

### totalDistributionY

• **totalDistributionY**: `u256` = `ZERO`

Total distribution of token Y. Should be 1e18 (100%) or 0 (0%)

#### Defined in

[assembly/structs/MintInfo.ts:31](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/structs/MintInfo.ts#L31)

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

[assembly/structs/MintInfo.ts:61](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/structs/MintInfo.ts#L61)

___

### serialize

▸ **serialize**(): `StaticArray`<`u8`\>

#### Returns

`StaticArray`<`u8`\>

#### Implementation of

Serializable.serialize

#### Defined in

[assembly/structs/MintInfo.ts:43](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/structs/MintInfo.ts#L43)
