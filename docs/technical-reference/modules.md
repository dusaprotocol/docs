[@dusalabs/core](README.md) / Exports

# @dusalabs/core

## Table of contents

### Namespaces

- [ERC20](modules/ERC20.md)
- [Factory](modules/Factory.md)
- [Pair](modules/Pair.md)
- [Quoter](modules/Quoter.md)
- [Router](modules/Router.md)
- [WMAS](modules/WMAS.md)

### Classes

- [Bin](classes/Bin.md)
- [BinHelper](classes/BinHelper.md)
- [BitMath](classes/BitMath.md)
- [BurnReturn](classes/BurnReturn.md)
- [Debt](classes/Debt.md)
- [FeeParameters](classes/FeeParameters.md)
- [FeesDistribution](classes/FeesDistribution.md)
- [GetAmountsReturn](classes/GetAmountsReturn.md)
- [GetFeesReturn](classes/GetFeesReturn.md)
- [GetIdsFromAboveReturn](classes/GetIdsFromAboveReturn.md)
- [GetSwapInReturn](classes/GetSwapInReturn.md)
- [GetSwapOutReturn](classes/GetSwapOutReturn.md)
- [IERC20](classes/IERC20.md)
- [IFactory](classes/IFactory.md)
- [IFlashLoanCallback](classes/IFlashLoanCallback.md)
- [IPair](classes/IPair.md)
- [IQuoter](classes/IQuoter.md)
- [IRouter](classes/IRouter.md)
- [IWMAS](classes/IWMAS.md)
- [LBPairInformation](classes/LBPairInformation.md)
- [LiquidityParameters](classes/LiquidityParameters.md)
- [Math512Bits](classes/Math512Bits.md)
- [MintInfo](classes/MintInfo.md)
- [MintReturn](classes/MintReturn.md)
- [PairInformation](classes/PairInformation.md)
- [PersistentMap](classes/PersistentMap.md)
- [SafeMath](classes/SafeMath.md)
- [SafeMathU8](classes/SafeMathU8.md)
- [SwapHelper](classes/SwapHelper.md)
- [TreeHelper](classes/TreeHelper.md)

### Variables

- [BASIS\_POINT\_MAX](modules.md#basis_point_max)
- [CALLBACK\_SUCCESS](modules.md#callback_success)
- [MAX\_BIN\_STEP](modules.md#max_bin_step)
- [MAX\_FEE](modules.md#max_fee)
- [MAX\_PROTOCOL\_SHARE](modules.md#max_protocol_share)
- [MIN\_BIN\_STEP](modules.md#min_bin_step)
- [PRECISION](modules.md#precision)
- [REAL\_ID\_SHIFT](modules.md#real_id_shift)
- [SCALE](modules.md#scale)
- [SCALE\_OFFSET](modules.md#scale_offset)
- [\_KEY\_ELEMENT\_SUFFIX](modules.md#_key_element_suffix)

### Functions

- [\_sortTokens](modules.md#_sorttokens)
- [level0](modules.md#level0)
- [level1](modules.md#level1)
- [level2](modules.md#level2)

## Variables

### BASIS\_POINT\_MAX

• `Const` **BASIS\_POINT\_MAX**: ``10000``

#### Defined in

[assembly/libraries/Constants.ts:2](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/libraries/Constants.ts#L2)

___

### CALLBACK\_SUCCESS

• `Const` **CALLBACK\_SUCCESS**: `StaticArray`<`u8`\> = `[]`

#### Defined in

[assembly/libraries/Constants.ts:10](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/libraries/Constants.ts#L10)

___

### MAX\_BIN\_STEP

• `Const` **MAX\_BIN\_STEP**: ``100``

#### Defined in

[assembly/libraries/Constants.ts:7](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/libraries/Constants.ts#L7)

___

### MAX\_FEE

• `Const` **MAX\_FEE**: `u64`

#### Defined in

[assembly/libraries/Constants.ts:9](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/libraries/Constants.ts#L9)

___

### MAX\_PROTOCOL\_SHARE

• `Const` **MAX\_PROTOCOL\_SHARE**: ``2500``

#### Defined in

[assembly/libraries/Constants.ts:8](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/libraries/Constants.ts#L8)

___

### MIN\_BIN\_STEP

• `Const` **MIN\_BIN\_STEP**: ``1``

#### Defined in

[assembly/libraries/Constants.ts:6](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/libraries/Constants.ts#L6)

___

### PRECISION

• `Const` **PRECISION**: `u64`

#### Defined in

[assembly/libraries/Constants.ts:3](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/libraries/Constants.ts#L3)

___

### REAL\_ID\_SHIFT

• `Const` **REAL\_ID\_SHIFT**: `i64`

#### Defined in

[assembly/libraries/Constants.ts:1](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/libraries/Constants.ts#L1)

___

### SCALE

• `Const` **SCALE**: `u64`

#### Defined in

[assembly/libraries/Constants.ts:5](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/libraries/Constants.ts#L5)

___

### SCALE\_OFFSET

• `Const` **SCALE\_OFFSET**: ``32``

#### Defined in

[assembly/libraries/Constants.ts:4](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/libraries/Constants.ts#L4)

___

### \_KEY\_ELEMENT\_SUFFIX

• `Const` **\_KEY\_ELEMENT\_SUFFIX**: ``"::"``

#### Defined in

[assembly/libraries/PersistentMap.ts:15](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/libraries/PersistentMap.ts#L15)

## Functions

### \_sortTokens

▸ **_sortTokens**(`_tokenA`, `_tokenB`): `SortTokensReturn`

#### Parameters

| Name | Type |
| :------ | :------ |
| `_tokenA` | `Address` |
| `_tokenB` | `Address` |

#### Returns

`SortTokensReturn`

#### Defined in

[assembly/libraries/Utils.ts:7](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/libraries/Utils.ts#L7)

___

### level0

▸ **level0**(): `u128`

#### Returns

`u128`

#### Defined in

[assembly/libraries/TreeHelper.ts:125](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/libraries/TreeHelper.ts#L125)

___

### level1

▸ **level1**(`index`): `u128`

#### Parameters

| Name | Type |
| :------ | :------ |
| `index` | `i32` |

#### Returns

`u128`

#### Defined in

[assembly/libraries/TreeHelper.ts:129](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/libraries/TreeHelper.ts#L129)

___

### level2

▸ **level2**(`index`): `u128`

#### Parameters

| Name | Type |
| :------ | :------ |
| `index` | `i32` |

#### Returns

`u128`

#### Defined in

[assembly/libraries/TreeHelper.ts:133](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/libraries/TreeHelper.ts#L133)
