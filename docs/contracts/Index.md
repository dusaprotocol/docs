# Index

## Table of contents

### Contracts

- [BaseHooks](BaseHooks)
- [Factory](Factory)
- [Pair](Pair)
- [Quoter](Quoter)
- [Router](Router)

### Libraries

- [BinHelper](./libraries/BinHelper.md)
- [BitMath](./libraries/BitMath.md)
- [DusaV0Library](classes/DusaV0Library)
- [Hooks](classes/Hooks)
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
- [IHooks](classes/IHooks)
- [IPair](./interfaces/IPair.md)
- [IQuoter](./interfaces/IQuoter.md)
- [IRouter](./interfaces/IRouter.md)
- [IV0Factory](classes/IV0Factory)
- [IV0Pair](classes/IV0Pair)

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
- [HooksParameters](classes/HooksParameters)

### Variables

- [AFTER\_BURN\_FLAG](#after_burn_flag)
- [AFTER\_FLASH\_LOAN\_FLAG](#after_flash_loan_flag)
- [AFTER\_MINT\_FLAG](#after_mint_flag)
- [AFTER\_SWAP\_FLAG](#after_swap_flag)
- [AFTER\_TRANSFER\_FLAG](#after_transfer_flag)
- [BALANCE\_KEY\_PREFIX\_LENGTH](#balance_key_prefix_length)
- [BASIS\_POINT\_MAX](#basis_point_max)
- [BEFORE\_BURN\_FLAG](#before_burn_flag)
- [BEFORE\_FLASH\_LOAN\_FLAG](#before_flash_loan_flag)
- [BEFORE\_MINT\_FLAG](#before_mint_flag)
- [BEFORE\_SWAP\_FLAG](#before_swap_flag)
- [BEFORE\_TRANSFER\_FLAG](#before_transfer_flag)
- [DELIMITER](#delimiter)
- [EVENT\_DELIMITER](#event_delimiter)
- [ID\_ONE](#id_one)
- [MAX](#max)
- [MAX\_BIN\_STEP](#max_bin_step)
- [MAX\_FEE](#max_fee)
- [MAX\_PROTOCOL\_SHARE](#max_protocol_share)
- [MIN\_BIN\_STEP](#min_bin_step)
- [ONE](#one)
- [ONE\_COIN](#one_coin)
- [PRECISION](#precision)
- [REAL\_ID\_SHIFT](#real_id_shift)
- [SCALE\_OFFSET](#scale_offset)
- [STORAGE\_BYTE\_COST](#storage_byte_cost)
- [STORAGE\_PREFIX\_LENGTH](#storage_prefix_length)
- [THREE](#three)
- [TWO](#two)
- [ZERO](#zero)
- [ZERO\_ADDRESS](#zero_address)
- [\_KEY\_ELEMENT\_SUFFIX](#_key_element_suffix)

### Functions

- [BinHelper\_\_BinStepOverflows](#binhelper__binstepoverflows)
- [BinHelper\_\_IdOverflows](#binhelper__idoverflows)
- [LBFactory\_\_BinStepHasNoPreset](#lbfactory__binstephasnopreset)
- [LBFactory\_\_BinStepRequirementsBreached](#lbfactory__binsteprequirementsbreached)
- [LBFactory\_\_DecreasingPeriods](#lbfactory__decreasingperiods)
- [LBFactory\_\_FactoryLockIsAlreadyInTheSameState](#lbfactory__factorylockisalreadyinthesamestate)
- [LBFactory\_\_FeesAboveMax](#lbfactory__feesabovemax)
- [LBFactory\_\_FlashLoanFeeAboveMax](#lbfactory__flashloanfeeabovemax)
- [LBFactory\_\_FunctionIsLockedForUsers](#lbfactory__functionislockedforusers)
- [LBFactory\_\_IdenticalAddresses](#lbfactory__identicaladdresses)
- [LBFactory\_\_LBPairAlreadyExists](#lbfactory__lbpairalreadyexists)
- [LBFactory\_\_LBPairIgnoredIsAlreadyInTheSameState](#lbfactory__lbpairignoredisalreadyinthesamestate)
- [LBFactory\_\_LBPairNotCreated](#lbfactory__lbpairnotcreated)
- [LBFactory\_\_ProtocolShareOverflows](#lbfactory__protocolshareoverflows)
- [LBFactory\_\_QuoteAssetAlreadyWhitelisted](#lbfactory__quoteassetalreadywhitelisted)
- [LBFactory\_\_QuoteAssetNotWhitelisted](#lbfactory__quoteassetnotwhitelisted)
- [LBFactory\_\_ReductionFactorOverflows](#lbfactory__reductionfactoroverflows)
- [LBFactory\_\_SameFeeRecipient](#lbfactory__samefeerecipient)
- [LBFactory\_\_SameFlashLoanFee](#lbfactory__sameflashloanfee)
- [LBFactory\_\_SameHooksParameters](#lbfactory__samehooksparameters)
- [LBPair\_\_AddressZero](#lbpair__addresszero)
- [LBPair\_\_AddressZeroOrThis](#lbpair__addresszeroorthis)
- [LBPair\_\_BinStepNotSame](#lbpair__binstepnotsame)
- [LBPair\_\_CompositionFactorFlawed](#lbpair__compositionfactorflawed)
- [LBPair\_\_DistributionsOverflow](#lbpair__distributionsoverflow)
- [LBPair\_\_FlashLoanCallbackFailed](#lbpair__flashloancallbackfailed)
- [LBPair\_\_FlashLoanInvalidBalance](#lbpair__flashloaninvalidbalance)
- [LBPair\_\_FlashLoanInvalidToken](#lbpair__flashloaninvalidtoken)
- [LBPair\_\_InsufficientAmounts](#lbpair__insufficientamounts)
- [LBPair\_\_InsufficientLiquidityBurned](#lbpair__insufficientliquidityburned)
- [LBPair\_\_InsufficientLiquidityMinted](#lbpair__insufficientliquidityminted)
- [LBPair\_\_OnlyFactory](#lbpair__onlyfactory)
- [LBPair\_\_OnlyFeeRecipient](#lbpair__onlyfeerecipient)
- [LBPair\_\_OnlyStrictlyIncreasingId](#lbpair__onlystrictlyincreasingid)
- [LBPair\_\_OracleNewSizeTooSmall](#lbpair__oraclenewsizetoosmall)
- [LBPair\_\_WrongLengths](#lbpair__wronglengths)
- [LBQuoter\_InvalidLength](#lbquoter_invalidlength)
- [LBRouter\_\_AmountSlippageCaught](#lbrouter__amountslippagecaught)
- [LBRouter\_\_BrokenSwapSafetyCheck](#lbrouter__brokenswapsafetycheck)
- [LBRouter\_\_DeadlineExceeded](#lbrouter__deadlineexceeded)
- [LBRouter\_\_IdDesiredOverflows](#lbrouter__iddesiredoverflows)
- [LBRouter\_\_IdOverflows](#lbrouter__idoverflows)
- [LBRouter\_\_IdSlippageCaught](#lbrouter__idslippagecaught)
- [LBRouter\_\_InsufficientAmountOut](#lbrouter__insufficientamountout)
- [LBRouter\_\_InvalidTokenPath](#lbrouter__invalidtokenpath)
- [LBRouter\_\_LengthsMismatch](#lbrouter__lengthsmismatch)
- [LBRouter\_\_MaxAmountInExceeded](#lbrouter__maxamountinexceeded)
- [LBRouter\_\_NotFactoryOwner](#lbrouter__notfactoryowner)
- [LBRouter\_\_SwapOverflows](#lbrouter__swapoverflows)
- [LBRouter\_\_TooMuchTokensIn](#lbrouter__toomuchtokensin)
- [LBRouter\_\_WrongAmounts](#lbrouter__wrongamounts)
- [LBRouter\_\_WrongMasLiquidityParameters](#lbrouter__wrongmasliquidityparameters)
- [LBRouter\_\_WrongTokenOrder](#lbrouter__wrongtokenorder)
- [LBToken\_\_BurnExceedsBalance](#lbtoken__burnexceedsbalance)
- [LBToken\_\_LengthMismatch](#lbtoken__lengthmismatch)
- [LBToken\_\_SelfApproval](#lbtoken__selfapproval)
- [LBToken\_\_SpenderNotApproved](#lbtoken__spendernotapproved)
- [LBToken\_\_TransferExceedsBalance](#lbtoken__transferexceedsbalance)
- [LBToken\_\_TransferToSelf](#lbtoken__transfertoself)
- [Math128x128\_\_PowerUnderflow](#math128x128__powerunderflow)
- [Math512Bits\_\_MulDivOverflow](#math512bits__muldivoverflow)
- [Math512Bits\_\_MulShiftOverflow](#math512bits__mulshiftoverflow)
- [Math512Bits\_\_OffsetOverflows](#math512bits__offsetoverflows)
- [Oracle\_\_LookUpTimestampTooOld](#oracle__lookuptimestamptooold)
- [Oracle\_\_NotInitialized](#oracle__notinitialized)
- [ReentrancyGuardUpgradeable\_\_AlreadyInitialized](#reentrancyguardupgradeable__alreadyinitialized)
- [ReentrancyGuardUpgradeable\_\_ReentrantCall](#reentrancyguardupgradeable__reentrantcall)
- [Storage\_\_NotEnoughCoinsSent](#storage__notenoughcoinssent)
- [TreeMath\_\_ErrorDepthSearch](#treemath__errordepthsearch)
- [\_sortTokens](#_sorttokens)
- [createEvent](#createevent)
- [createKey](#createkey)
- [spreadLiqudity](#spreadliqudity)
- [transferRemaining](#transferremaining)
- [u256ToString](#u256tostring)

## Variables

### AFTER\_BURN\_FLAG

• `Const` **AFTER\_BURN\_FLAG**: `u32`

#### Defined in

[assembly/libraries/Hooks.ts:14](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Hooks.ts#L14)

___

### AFTER\_FLASH\_LOAN\_FLAG

• `Const` **AFTER\_FLASH\_LOAN\_FLAG**: `u32`

#### Defined in

[assembly/libraries/Hooks.ts:10](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Hooks.ts#L10)

___

### AFTER\_MINT\_FLAG

• `Const` **AFTER\_MINT\_FLAG**: `u32`

#### Defined in

[assembly/libraries/Hooks.ts:12](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Hooks.ts#L12)

___

### AFTER\_SWAP\_FLAG

• `Const` **AFTER\_SWAP\_FLAG**: `u32`

#### Defined in

[assembly/libraries/Hooks.ts:8](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Hooks.ts#L8)

___

### AFTER\_TRANSFER\_FLAG

• `Const` **AFTER\_TRANSFER\_FLAG**: `u32`

#### Defined in

[assembly/libraries/Hooks.ts:16](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Hooks.ts#L16)

___

### BALANCE\_KEY\_PREFIX\_LENGTH

• `Const` **BALANCE\_KEY\_PREFIX\_LENGTH**: ``7``

#### Defined in

[assembly/libraries/Utils.ts:168](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Utils.ts#L168)

___

### BASIS\_POINT\_MAX

• `Const` **BASIS\_POINT\_MAX**: `u16` = `10_000`

#### Defined in

[assembly/libraries/Constants.ts:7](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Constants.ts#L7)

___

### BEFORE\_BURN\_FLAG

• `Const` **BEFORE\_BURN\_FLAG**: `u32`

#### Defined in

[assembly/libraries/Hooks.ts:13](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Hooks.ts#L13)

___

### BEFORE\_FLASH\_LOAN\_FLAG

• `Const` **BEFORE\_FLASH\_LOAN\_FLAG**: `u32`

#### Defined in

[assembly/libraries/Hooks.ts:9](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Hooks.ts#L9)

___

### BEFORE\_MINT\_FLAG

• `Const` **BEFORE\_MINT\_FLAG**: `u32`

#### Defined in

[assembly/libraries/Hooks.ts:11](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Hooks.ts#L11)

___

### BEFORE\_SWAP\_FLAG

• `Const` **BEFORE\_SWAP\_FLAG**: `u32`

#### Defined in

[assembly/libraries/Hooks.ts:7](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Hooks.ts#L7)

___

### BEFORE\_TRANSFER\_FLAG

• `Const` **BEFORE\_TRANSFER\_FLAG**: `u32`

#### Defined in

[assembly/libraries/Hooks.ts:15](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Hooks.ts#L15)

___

### DELIMITER

• `Const` **DELIMITER**: ``":"``

#### Defined in

[assembly/libraries/Utils.ts:16](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Utils.ts#L16)

___

### EVENT\_DELIMITER

• `Const` **EVENT\_DELIMITER**: ``";?!"``

#### Defined in

[assembly/libraries/Utils.ts:101](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Utils.ts#L101)

___

### ID\_ONE

• `Const` **ID\_ONE**: `u32`

#### Defined in

[assembly/libraries/Constants.ts:6](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Constants.ts#L6)

___

### MAX

• `Const` **MAX**: `u256` = `u256.Max`

#### Defined in

[assembly/libraries/Constants.ts:16](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Constants.ts#L16)

___

### MAX\_BIN\_STEP

• `Const` **MAX\_BIN\_STEP**: ``100``

#### Defined in

[assembly/libraries/Constants.ts:12](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Constants.ts#L12)

___

### MAX\_FEE

• `Const` **MAX\_FEE**: `u64`

#### Defined in

[assembly/libraries/Constants.ts:13](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Constants.ts#L13)

___

### MAX\_U128

• `Const` **MAX\_U128**: `u256`

#### Defined in

[assembly/libraries/Constants.ts:20](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Constants.ts#L20)

___

### MIN\_BIN\_STEP

• `Const` **MIN\_BIN\_STEP**: ``1``

#### Defined in

[assembly/libraries/Constants.ts:11](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Constants.ts#L11)

___

### ONE

• `Const` **ONE**: `u256` = `u256.One`

#### Defined in

[assembly/libraries/Constants.ts:14](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Constants.ts#L14)

___

### ONE\_COIN

• `Const` **ONE\_COIN**: `u64`

#### Defined in

[assembly/libraries/Constants.ts:9](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Constants.ts#L9)

___

### PRECISION

• `Const` **PRECISION**: `u256`

#### Defined in

[assembly/libraries/Constants.ts:8](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Constants.ts#L8)

___

### REAL\_ID\_SHIFT

• `Const` **REAL\_ID\_SHIFT**: `i64`

#### Defined in

[assembly/libraries/Constants.ts:5](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Constants.ts#L5)

___

### SCALE\_OFFSET

• `Const` **SCALE\_OFFSET**: ``128``

#### Defined in

[assembly/libraries/Constants.ts:10](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Constants.ts#L10)

___

### STORAGE\_BYTE\_COST

• `Const` **STORAGE\_BYTE\_COST**: ``100000``

#### Defined in

[assembly/libraries/Utils.ts:166](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Utils.ts#L166)

___

### STORAGE\_PREFIX\_LENGTH

• `Const` **STORAGE\_PREFIX\_LENGTH**: ``4``

#### Defined in

[assembly/libraries/Utils.ts:167](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Utils.ts#L167)

___

### THREE

• `Const` **THREE**: `u256`

#### Defined in

[assembly/libraries/Constants.ts:18](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Constants.ts#L18)

___

### TWO

• `Const` **TWO**: `u256`

#### Defined in

[assembly/libraries/Constants.ts:17](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Constants.ts#L17)

___

### ZERO

• `Const` **ZERO**: `u256` = `u256.Zero`

#### Defined in

[assembly/libraries/Constants.ts:15](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Constants.ts#L15)

___

### ZERO\_ADDRESS

• `Const` **ZERO\_ADDRESS**: `Address`

#### Defined in

[assembly/libraries/Constants.ts:19](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Constants.ts#L19)

___

### \_KEY\_ELEMENT\_SUFFIX

• `Const` **\_KEY\_ELEMENT\_SUFFIX**: ``"::"``

#### Defined in

[assembly/libraries/PersistentMap.ts:17](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/PersistentMap.ts#L17)

## Functions

### BinHelper\_\_BinStepOverflows

▸ **BinHelper__BinStepOverflows**(`bp`): `string`

BinHelper errors

#### Parameters

| Name | Type |
| :------ | :------ |
| `bp` | `u16` |

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:203](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Errors.ts#L203)

___

### BinHelper\_\_IdOverflows

▸ **BinHelper__IdOverflows**(): `string`

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:205](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Errors.ts#L205)

___

### LBFactory\_\_BinStepHasNoPreset

▸ **LBFactory__BinStepHasNoPreset**(`binStep`): `string`

#### Parameters

| Name | Type |
| :------ | :------ |
| `binStep` | `u64` |

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:150](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Errors.ts#L150)

___

### LBFactory\_\_BinStepRequirementsBreached

▸ **LBFactory__BinStepRequirementsBreached**(`lowerBound`, `binStep`, `higherBound`): `string`

#### Parameters

| Name | Type |
| :------ | :------ |
| `lowerBound` | `u64` |
| `binStep` | `u32` |
| `higherBound` | `u64` |

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:134](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Errors.ts#L134)

___

### LBFactory\_\_DecreasingPeriods

▸ **LBFactory__DecreasingPeriods**(`filterPeriod`, `decayPeriod`): `string`

#### Parameters

| Name | Type |
| :------ | :------ |
| `filterPeriod` | `u32` |
| `decayPeriod` | `u32` |

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:116](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Errors.ts#L116)

___

### LBFactory\_\_FactoryLockIsAlreadyInTheSameState

▸ **LBFactory__FactoryLockIsAlreadyInTheSameState**(): `string`

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:146](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Errors.ts#L146)

___

### LBFactory\_\_FeesAboveMax

▸ **LBFactory__FeesAboveMax**(`baseFee`, `_maxVariableFee`, `maxFees`): `string`

#### Parameters

| Name | Type |
| :------ | :------ |
| `baseFee` | `u64` |
| `_maxVariableFee` | `u64` |
| `maxFees` | `u64` |

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:124](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Errors.ts#L124)

___

### LBFactory\_\_FlashLoanFeeAboveMax

▸ **LBFactory__FlashLoanFeeAboveMax**(`fees`, `maxFees`): `string`

#### Parameters

| Name | Type |
| :------ | :------ |
| `fees` | `u64` |
| `maxFees` | `u64` |

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:130](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Errors.ts#L130)

___

### LBFactory\_\_FunctionIsLockedForUsers

▸ **LBFactory__FunctionIsLockedForUsers**(`user`): `string`

#### Parameters

| Name | Type |
| :------ | :------ |
| `user` | `Address` |

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:144](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Errors.ts#L144)

___

### LBFactory\_\_IdenticalAddresses

▸ **LBFactory__IdenticalAddresses**(`token`): `string`

LBFactory errors

#### Parameters

| Name | Type |
| :------ | :------ |
| `token` | `Address` |

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:102](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Errors.ts#L102)

___

### LBFactory\_\_LBPairAlreadyExists

▸ **LBFactory__LBPairAlreadyExists**(`tokenX`, `tokenY`, `_binStep`): `string`

#### Parameters

| Name | Type |
| :------ | :------ |
| `tokenX` | `Address` |
| `tokenY` | `Address` |
| `_binStep` | `u64` |

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:110](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Errors.ts#L110)

___

### LBFactory\_\_LBPairIgnoredIsAlreadyInTheSameState

▸ **LBFactory__LBPairIgnoredIsAlreadyInTheSameState**(): `string`

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:148](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Errors.ts#L148)

___

### LBFactory\_\_LBPairNotCreated

▸ **LBFactory__LBPairNotCreated**(`tokenX`, `tokenY`, `binStep`): `string`

#### Parameters

| Name | Type |
| :------ | :------ |
| `tokenX` | `Address` |
| `tokenY` | `Address` |
| `binStep` | `u64` |

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:156](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Errors.ts#L156)

___

### LBFactory\_\_ProtocolShareOverflows

▸ **LBFactory__ProtocolShareOverflows**(`protocolShare`, `max`): `string`

#### Parameters

| Name | Type |
| :------ | :------ |
| `protocolShare` | `u32` |
| `max` | `u64` |

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:140](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Errors.ts#L140)

___

### LBFactory\_\_QuoteAssetAlreadyWhitelisted

▸ **LBFactory__QuoteAssetAlreadyWhitelisted**(`quoteAsset`): `string`

#### Parameters

| Name | Type |
| :------ | :------ |
| `quoteAsset` | `Address` |

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:107](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Errors.ts#L107)

___

### LBFactory\_\_QuoteAssetNotWhitelisted

▸ **LBFactory__QuoteAssetNotWhitelisted**(`quoteAsset`): `string`

#### Parameters

| Name | Type |
| :------ | :------ |
| `quoteAsset` | `Address` |

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:104](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Errors.ts#L104)

___

### LBFactory\_\_ReductionFactorOverflows

▸ **LBFactory__ReductionFactorOverflows**(`reductionFactor`, `max`): `string`

#### Parameters

| Name | Type |
| :------ | :------ |
| `reductionFactor` | `u32` |
| `max` | `u64` |

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:120](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Errors.ts#L120)

___

### LBFactory\_\_SameFeeRecipient

▸ **LBFactory__SameFeeRecipient**(`feeRecipient`): `string`

#### Parameters

| Name | Type |
| :------ | :------ |
| `feeRecipient` | `Address` |

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:152](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Errors.ts#L152)

___

### LBFactory\_\_SameFlashLoanFee

▸ **LBFactory__SameFlashLoanFee**(`flashLoanFee`): `string`

#### Parameters

| Name | Type |
| :------ | :------ |
| `flashLoanFee` | `u64` |

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:154](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Errors.ts#L154)

___

### LBFactory\_\_SameHooksParameters

▸ **LBFactory__SameHooksParameters**(`hooksParameters`): `string`

#### Parameters

| Name | Type |
| :------ | :------ |
| `hooksParameters` | [`HooksParameters`](classes/HooksParameters) |

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:161](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Errors.ts#L161)

___

### LBPair\_\_AddressZero

▸ **LBPair__AddressZero**(): `string`

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:170](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Errors.ts#L170)

___

### LBPair\_\_AddressZeroOrThis

▸ **LBPair__AddressZeroOrThis**(): `string`

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:171](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Errors.ts#L171)

___

### LBPair\_\_BinStepNotSame

▸ **LBPair__BinStepNotSame**(): `string`

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:199](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Errors.ts#L199)

___

### LBPair\_\_CompositionFactorFlawed

▸ **LBPair__CompositionFactorFlawed**(`id`): `string`

#### Parameters

| Name | Type |
| :------ | :------ |
| `id` | `u64` |

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:173](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Errors.ts#L173)

___

### LBPair\_\_DistributionsOverflow

▸ **LBPair__DistributionsOverflow**(): `string`

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:183](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Errors.ts#L183)

___

### LBPair\_\_FlashLoanCallbackFailed

▸ **LBPair__FlashLoanCallbackFailed**(): `string`

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:193](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Errors.ts#L193)

___

### LBPair\_\_FlashLoanInvalidBalance

▸ **LBPair__FlashLoanInvalidBalance**(): `string`

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:195](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Errors.ts#L195)

___

### LBPair\_\_FlashLoanInvalidToken

▸ **LBPair__FlashLoanInvalidToken**(): `string`

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:197](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Errors.ts#L197)

___

### LBPair\_\_InsufficientAmounts

▸ **LBPair__InsufficientAmounts**(): `string`

LBPair errors

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:168](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Errors.ts#L168)

___

### LBPair\_\_InsufficientLiquidityBurned

▸ **LBPair__InsufficientLiquidityBurned**(`id`): `string`

#### Parameters

| Name | Type |
| :------ | :------ |
| `id` | `u64` |

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:177](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Errors.ts#L177)

___

### LBPair\_\_InsufficientLiquidityMinted

▸ **LBPair__InsufficientLiquidityMinted**(`id`): `string`

#### Parameters

| Name | Type |
| :------ | :------ |
| `id` | `u64` |

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:175](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Errors.ts#L175)

___

### LBPair\_\_OnlyFactory

▸ **LBPair__OnlyFactory**(): `string`

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:182](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Errors.ts#L182)

___

### LBPair\_\_OnlyFeeRecipient

▸ **LBPair__OnlyFeeRecipient**(`feeRecipient`, `sender`): `string`

#### Parameters

| Name | Type |
| :------ | :------ |
| `feeRecipient` | `Address` |
| `sender` | `Address` |

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:185](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Errors.ts#L185)

___

### LBPair\_\_OnlyStrictlyIncreasingId

▸ **LBPair__OnlyStrictlyIncreasingId**(): `string`

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:180](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Errors.ts#L180)

___

### LBPair\_\_OracleNewSizeTooSmall

▸ **LBPair__OracleNewSizeTooSmall**(`newSize`, `oracleSize`): `string`

#### Parameters

| Name | Type |
| :------ | :------ |
| `newSize` | `u64` |
| `oracleSize` | `u64` |

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:189](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Errors.ts#L189)

___

### LBPair\_\_WrongLengths

▸ **LBPair__WrongLengths**(): `string`

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:179](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Errors.ts#L179)

___

### LBQuoter\_InvalidLength

▸ **LBQuoter_InvalidLength**(): `string`

LBQuoter errors

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:251](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Errors.ts#L251)

___

### LBRouter\_\_AmountSlippageCaught

▸ **LBRouter__AmountSlippageCaught**(`amountXMin`, `amountX`, `amountYMin`, `amountY`): `string`

#### Parameters

| Name | Type |
| :------ | :------ |
| `amountXMin` | `u256` |
| `amountX` | `u256` |
| `amountYMin` | `u256` |
| `amountY` | `u256` |

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:30](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Errors.ts#L30)

___

### LBRouter\_\_BrokenSwapSafetyCheck

▸ **LBRouter__BrokenSwapSafetyCheck**(): `string`

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:12](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Errors.ts#L12)

___

### LBRouter\_\_DeadlineExceeded

▸ **LBRouter__DeadlineExceeded**(`deadline`, `currentTimestamp`): `string`

#### Parameters

| Name | Type |
| :------ | :------ |
| `deadline` | `u64` |
| `currentTimestamp` | `u64` |

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:43](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Errors.ts#L43)

___

### LBRouter\_\_IdDesiredOverflows

▸ **LBRouter__IdDesiredOverflows**(`idDesired`, `idSlippage`): `string`

#### Parameters

| Name | Type |
| :------ | :------ |
| `idDesired` | `u64` |
| `idSlippage` | `u64` |

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:39](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Errors.ts#L39)

___

### LBRouter\_\_IdOverflows

▸ **LBRouter__IdOverflows**(`id`): `string`

#### Parameters

| Name | Type |
| :------ | :------ |
| `id` | `i64` |

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:18](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Errors.ts#L18)

___

### LBRouter\_\_IdSlippageCaught

▸ **LBRouter__IdSlippageCaught**(`activeIdDesired`, `idSlippage`, `activeId`): `string`

#### Parameters

| Name | Type |
| :------ | :------ |
| `activeIdDesired` | `u64` |
| `idSlippage` | `u64` |
| `activeId` | `u64` |

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:24](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Errors.ts#L24)

___

### LBRouter\_\_InsufficientAmountOut

▸ **LBRouter__InsufficientAmountOut**(`amountOutMin`, `amountOut`): `string`

#### Parameters

| Name | Type |
| :------ | :------ |
| `amountOutMin` | `u256` |
| `amountOut` | `u256` |

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:47](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Errors.ts#L47)

___

### LBRouter\_\_InvalidTokenPath

▸ **LBRouter__InvalidTokenPath**(`wrongToken`): `string`

#### Parameters

| Name | Type |
| :------ | :------ |
| `wrongToken` | `Address` |

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:61](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Errors.ts#L61)

___

### LBRouter\_\_LengthsMismatch

▸ **LBRouter__LengthsMismatch**(): `string`

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:20](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Errors.ts#L20)

___

### LBRouter\_\_MaxAmountInExceeded

▸ **LBRouter__MaxAmountInExceeded**(`amountInMax`, `amountIn`): `string`

#### Parameters

| Name | Type |
| :------ | :------ |
| `amountInMax` | `u256` |
| `amountIn` | `u256` |

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:54](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Errors.ts#L54)

___

### LBRouter\_\_NotFactoryOwner

▸ **LBRouter__NotFactoryOwner**(): `string`

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:14](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Errors.ts#L14)

___

### LBRouter\_\_SwapOverflows

▸ **LBRouter__SwapOverflows**(`id`): `string`

#### Parameters

| Name | Type |
| :------ | :------ |
| `id` | `u64` |

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:10](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Errors.ts#L10)

___

### LBRouter\_\_TooMuchTokensIn

▸ **LBRouter__TooMuchTokensIn**(`excess`): `string`

#### Parameters

| Name | Type |
| :------ | :------ |
| `excess` | `u256` |

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:16](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Errors.ts#L16)

___

### LBRouter\_\_WrongAmounts

▸ **LBRouter__WrongAmounts**(`amount`, `reserve`): `string`

LBRouter errors

#### Parameters

| Name | Type |
| :------ | :------ |
| `amount` | `u256` |
| `reserve` | `u256` |

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:8](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Errors.ts#L8)

___

### LBRouter\_\_WrongMasLiquidityParameters

▸ **LBRouter__WrongMasLiquidityParameters**(`tokenX`, `tokenY`, `amountX`, `amountY`, `msgValue`): `string`

#### Parameters

| Name | Type |
| :------ | :------ |
| `tokenX` | `Address` |
| `tokenY` | `Address` |
| `amountX` | `u256` |
| `amountY` | `u256` |
| `msgValue` | `u64` |

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:63](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Errors.ts#L63)

___

### LBRouter\_\_WrongTokenOrder

▸ **LBRouter__WrongTokenOrder**(): `string`

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:22](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Errors.ts#L22)

___

### LBToken\_\_BurnExceedsBalance

▸ **LBToken__BurnExceedsBalance**(`from`, `id`, `amount`): `string`

#### Parameters

| Name | Type |
| :------ | :------ |
| `from` | `Address` |
| `id` | `u64` |
| `amount` | `u256` |

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:80](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Errors.ts#L80)

___

### LBToken\_\_LengthMismatch

▸ **LBToken__LengthMismatch**(`accountsLength`, `idsLength`): `string`

#### Parameters

| Name | Type |
| :------ | :------ |
| `accountsLength` | `u64` |
| `idsLength` | `u64` |

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:86](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Errors.ts#L86)

___

### LBToken\_\_SelfApproval

▸ **LBToken__SelfApproval**(`owner`): `string`

#### Parameters

| Name | Type |
| :------ | :------ |
| `owner` | `Address` |

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:90](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Errors.ts#L90)

___

### LBToken\_\_SpenderNotApproved

▸ **LBToken__SpenderNotApproved**(`owner`, `spender`): `string`

LBToken errors

#### Parameters

| Name | Type |
| :------ | :------ |
| `owner` | `Address` |
| `spender` | `Address` |

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:76](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Errors.ts#L76)

___

### LBToken\_\_TransferExceedsBalance

▸ **LBToken__TransferExceedsBalance**(`from`, `id`, `amount`): `string`

#### Parameters

| Name | Type |
| :------ | :------ |
| `from` | `Address` |
| `id` | `u64` |
| `amount` | `u256` |

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:92](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Errors.ts#L92)

___

### LBToken\_\_TransferToSelf

▸ **LBToken__TransferToSelf**(): `string`

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:98](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Errors.ts#L98)

___

### Math128x128\_\_PowerUnderflow

▸ **Math128x128__PowerUnderflow**(`x`, `y`): `string`

Math128x128 errors

#### Parameters

| Name | Type |
| :------ | :------ |
| `x` | `u256` |
| `y` | `i64` |

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:209](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Errors.ts#L209)

___

### Math512Bits\_\_MulDivOverflow

▸ **Math512Bits__MulDivOverflow**(`prod1`, `denominator`): `string`

Math512Bits errors

#### Parameters

| Name | Type |
| :------ | :------ |
| `prod1` | `u256` |
| `denominator` | `u256` |

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:214](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Errors.ts#L214)

___

### Math512Bits\_\_MulShiftOverflow

▸ **Math512Bits__MulShiftOverflow**(`prod1`, `offset`): `string`

#### Parameters

| Name | Type |
| :------ | :------ |
| `prod1` | `u256` |
| `offset` | `u64` |

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:221](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Errors.ts#L221)

___

### Math512Bits\_\_OffsetOverflows

▸ **Math512Bits__OffsetOverflows**(`offset`): `string`

#### Parameters

| Name | Type |
| :------ | :------ |
| `offset` | `u64` |

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:225](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Errors.ts#L225)

___

### Oracle\_\_LookUpTimestampTooOld

▸ **Oracle__LookUpTimestampTooOld**(`_minTimestamp`, `_lookUpTimestamp`): `string`

Oracle errors

#### Parameters

| Name | Type |
| :------ | :------ |
| `_minTimestamp` | `u64` |
| `_lookUpTimestamp` | `u64` |

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:230](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Errors.ts#L230)

___

### Oracle\_\_NotInitialized

▸ **Oracle__NotInitialized**(): `string`

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:235](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Errors.ts#L235)

___

### ReentrancyGuardUpgradeable\_\_AlreadyInitialized

▸ **ReentrancyGuardUpgradeable__AlreadyInitialized**(): `string`

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:241](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Errors.ts#L241)

___

### ReentrancyGuardUpgradeable\_\_ReentrantCall

▸ **ReentrancyGuardUpgradeable__ReentrantCall**(): `string`

ReentrancyGuardUpgradeable errors

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:239](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Errors.ts#L239)

___

### Storage\_\_NotEnoughCoinsSent

▸ **Storage__NotEnoughCoinsSent**(`spent`, `sent`): `string`

Storage errors

#### Parameters

| Name | Type |
| :------ | :------ |
| `spent` | `u64` |
| `sent` | `u64` |

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:255](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Errors.ts#L255)

___

### TreeMath\_\_ErrorDepthSearch

▸ **TreeMath__ErrorDepthSearch**(): `string`

TreeMath errors

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:246](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Errors.ts#L246)

___

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

[assembly/libraries/Utils.ts:34](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Utils.ts#L34)

___

### createEvent

▸ **createEvent**(`key`, `args`): `string`

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `key` | `string` | the string event key. |
| `args` | `string`[] | the string array arguments. |

#### Returns

`string`

the stringified event.

**`Notice`**

Overrides Massa default createEvent function (use a custom delimiter to avoid collisions)

Constructs a pretty formatted event with given key and arguments.

**`Remarks`**

The result is meant to be used with the generateEvent function.
It is useful to generate events from an array.

#### Defined in

[assembly/libraries/Utils.ts:118](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Utils.ts#L118)

___

### createKey

▸ **createKey**(`args`): `string`

#### Parameters

| Name | Type |
| :------ | :------ |
| `args` | `string`[] |

#### Returns

`string`

#### Defined in

[assembly/libraries/Utils.ts:17](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Utils.ts#L17)

___

### spreadLiquidity

▸ **spreadLiquidity**(`amountYIn`, `startId`, `numbersBins`, `gap`, `binStep`): `SpreadLiqudityReturn`

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

[assembly/libraries/Utils.ts:54](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Utils.ts#L54)

___

### transferRemaining

▸ **transferRemaining**(`balanceInit`, `balanceFinal`, `sent`, `to`): `void`

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `balanceInit` | `u64` | Initial balance of the SC (transferred coins + balance of the SC) |
| `balanceFinal` | `u64` | Balance of the SC at the end of the call |
| `sent` | `u64` | Number of coins sent to the SC |
| `to` | `Address` | Caller of the function to transfer the remaining coins to |

#### Returns

`void`

**`Notice`**

Function to transfer remaining Massa coins to a recipient at the end of a call

#### Defined in

[assembly/libraries/Utils.ts:137](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Utils.ts#L137)

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

[assembly/libraries/Utils.ts:126](https://github.com/dusaprotocol/v1-core-confidencial/blob/327ce5d/assembly/libraries/Utils.ts#L126)
