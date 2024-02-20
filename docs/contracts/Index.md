# Index

## Table of contents

### Contracts

- [Factory](./Factory.md)
- [Pair](./Pair.md)
- [Quoter](./Quoter.md)
- [Router](./Router.md)

### Libraries

- [BinHelper](./libraries/BinHelper.md)
- [BitMath](./libraries/BitMath.md)
- [Math512Bits](./libraries/Math512Bits.md)
- [PersistentMap](./libraries/PersistentMap.md)
- [ReentrancyGuardUpgradeable](./libraries/ReentrancyGuardUpgradeable)
- [SafeMath](./libraries/SafeMath.md)
- [SafeMath256](./libraries/SafeMath256.md)
- [SafeMathU8](./libraries/SafeMathU8.md)
- [SwapHelper](./libraries/SwapHelper.md)
- [TreeHelper](./libraries/TreeHelper.md)

### Interfaces

- [IERC20](./interfaces/IERC20.md)
- [IFactory](./interfaces/IFactory.md)
- [IFlashLoanCallback](./interfaces/IFlashLoanCallback.md)
- [IPair](./interfaces/IPair.md)
- [IQuoter](./interfaces/IQuoter.md)
- [IRouter](./interfaces/IRouter.md)

### Structs

- [Bin](./structs/Bin.md)
- [Debt](./structs/Debt.md)
- [FeeParameters](./structs/FeeParameters.md)
- [FeesDistribution](./structs/FeesDistribution.md)
- [LBPairInformation](./structs/LBPairInformation.md)
- [LiquidityParameters](./structs/LiquidityParameters.md)
- [MintInfo](./structs/MintInfo.md)
- [Oracle](./structs/Oracle.md)
- [OracleParameters](./structs/OracleParameters.md)
- [PairInformation](./structs/PairInformation.md)
- [Preset](./structs/Preset.md)
- [Sample](./structs/Sample.md)

### Variables

- [BASIS\_POINT\_MAX](#basis_point_max)
- [ID\_ONE](#id_one)
- [MAX\_BIN\_STEP](#max_bin_step)
- [MAX\_FEE](#max_fee)
- [MAX\_PROTOCOL\_SHARE](#max_protocol_share)
- [MIN\_BIN\_STEP](#min_bin_step)
- [ONE\_COIN](#one_coin)
- [PRECISION](#precision)
- [REAL\_ID\_SHIFT](#real_id_shift)
- [SCALE\_OFFSET](#scale_offset)
- [\_KEY\_ELEMENT\_SUFFIX](#_key_element_suffix)

### Functions

- [\_sortTokens](#_sorttokens)
- [createEvent](#createevent)
- [spreadLiqudity](#spreadliqudity)
- [u256ToString](#u256tostring)

## Variables

### BASIS\_POINT\_MAX

• `Const` **BASIS\_POINT\_MAX**: ``10000``

#### Defined in

[assembly/libraries/Constants.ts:5](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/libraries/Constants.ts#L5)

___

### ID\_ONE

• `Const` **ID\_ONE**: `u32`

#### Defined in

[assembly/libraries/Constants.ts:4](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/libraries/Constants.ts#L4)

___

### MAX\_BIN\_STEP

• `Const` **MAX\_BIN\_STEP**: ``100``

#### Defined in

[assembly/libraries/Constants.ts:10](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/libraries/Constants.ts#L10)

___

### MAX\_FEE

• `Const` **MAX\_FEE**: `u64`

#### Defined in

[assembly/libraries/Constants.ts:12](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/libraries/Constants.ts#L12)

___

### MAX\_PROTOCOL\_SHARE

• `Const` **MAX\_PROTOCOL\_SHARE**: ``2500``

#### Defined in

[assembly/libraries/Constants.ts:11](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/libraries/Constants.ts#L11)

___

### MIN\_BIN\_STEP

• `Const` **MIN\_BIN\_STEP**: ``1``

#### Defined in

[assembly/libraries/Constants.ts:9](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/libraries/Constants.ts#L9)

___

### ONE\_COIN

• `Const` **ONE\_COIN**: `u64`

#### Defined in

[assembly/libraries/Constants.ts:7](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/libraries/Constants.ts#L7)

___

### PRECISION

• `Const` **PRECISION**: `u256`

#### Defined in

[assembly/libraries/Constants.ts:6](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/libraries/Constants.ts#L6)

___

### REAL\_ID\_SHIFT

• `Const` **REAL\_ID\_SHIFT**: `i64`

#### Defined in

[assembly/libraries/Constants.ts:3](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/libraries/Constants.ts#L3)

___

### SCALE\_OFFSET

• `Const` **SCALE\_OFFSET**: ``128``

#### Defined in

[assembly/libraries/Constants.ts:8](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/libraries/Constants.ts#L8)

___

### \_KEY\_ELEMENT\_SUFFIX

• `Const` **\_KEY\_ELEMENT\_SUFFIX**: ``"::"``

#### Defined in

[assembly/libraries/PersistentMap.ts:17](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/libraries/PersistentMap.ts#L17)

## Functions

### \_sortTokens

▸ **_sortTokens**(`_tokenA`, `_tokenB`): `SortTokensReturn`

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `_tokenA` | `Address` | The first token |
| `_tokenB` | `Address` | The second token |

#### Returns

`SortTokensReturn`

SortTokensReturn: token0, token1

**`Notice`**

Private view function to sort 2 tokens in ascending order

#### Defined in

[assembly/libraries/Utils.ts:20](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/libraries/Utils.ts#L20)

___

### createEvent

▸ **createEvent**(`key`, `args`): `string`

#### Parameters

| Name | Type |
| :------ | :------ |
| `key` | `string` |
| `args` | `string`[] |

#### Returns

`string`

#### Defined in

[assembly/libraries/Utils.ts:87](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/libraries/Utils.ts#L87)

___

### spreadLiqudity

▸ **spreadLiqudity**(`amountYIn`, `startId`, `numbersBins`, `gap`, `binStep`): `SpreadLiqudityReturn`

#### Parameters

| Name | Type |
| :------ | :------ |
| `amountYIn` | `u256` |
| `startId` | `u32` |
| `numbersBins` | `u32` |
| `gap` | `u32` |
| `binStep` | `u32` |

#### Returns

`SpreadLiqudityReturn`

#### Defined in

[assembly/libraries/Utils.ts:40](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/libraries/Utils.ts#L40)

___

### u256ToString

▸ **u256ToString**(`u`): `string`

#### Parameters

| Name | Type |
| :------ | :------ |
| `u` | `u256` |

#### Returns

`string`

**`Notice`**

Function to convert a u256 to a UTF-16 bytes then to a string

**`Dev`**

u256.toString() is too expensive in as-bignum so we use this instead

#### Defined in

[assembly/libraries/Utils.ts:95](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/libraries/Utils.ts#L95)
