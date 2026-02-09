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
- [DusaV0Library](./libraries/DusaV0Library)
- [Hooks](./libraries/Hooks)
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
- [IHooks](./interfaces/IHooks)
- [IPair](./interfaces/IPair.md)
- [IQuoter](./interfaces/IQuoter.md)
- [IRouter](./interfaces/IRouter.md)
- [IV0Factory](./interfaces/IV0Factory)
- [IV0Pair](./interfaces/IV0Pair)

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
- [HooksParameters](./structs/HooksParameters)

### Variables

- [AFTER_BURN_FLAG](#after_burn_flag)
- [AFTER_FLASH_LOAN_FLAG](#after_flash_loan_flag)
- [AFTER_MINT_FLAG](#after_mint_flag)
- [AFTER_SWAP_FLAG](#after_swap_flag)
- [AFTER_TRANSFER_FLAG](#after_transfer_flag)
- [BALANCE_KEY_PREFIX_LENGTH](#balance_key_prefix_length)
- [BASIS_POINT_MAX](#basis_point_max)
- [BEFORE_BURN_FLAG](#before_burn_flag)
- [BEFORE_FLASH_LOAN_FLAG](#before_flash_loan_flag)
- [BEFORE_MINT_FLAG](#before_mint_flag)
- [BEFORE_SWAP_FLAG](#before_swap_flag)
- [BEFORE_TRANSFER_FLAG](#before_transfer_flag)
- [DELIMITER](#delimiter)
- [EVENT_DELIMITER](#event_delimiter)
- [ID_ONE](#id_one)
- [MAX](#max)
- [MAX_BIN_STEP](#max_bin_step)
- [MAX_FEE](#max_fee)
- [MAX_PROTOCOL_SHARE](#max_protocol_share)
- [MIN_BIN_STEP](#min_bin_step)
- [ONE](#one)
- [ONE_COIN](#one_coin)
- [PRECISION](#precision)
- [REAL_ID_SHIFT](#real_id_shift)
- [SCALE_OFFSET](#scale_offset)
- [STORAGE_BYTE_COST](#storage_byte_cost)
- [STORAGE_PREFIX_LENGTH](#storage_prefix_length)
- [THREE](#three)
- [TWO](#two)
- [ZERO](#zero)
- [ZERO_ADDRESS](#zero_address)
- [\_KEY_ELEMENT_SUFFIX](#_key_element_suffix)

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
- [LBQuoter_InvalidLength](#lbquoter_invalidlength)
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

### AFTER_BURN_FLAG

• `Const` **AFTER_BURN_FLAG**: `u32`

#### Defined in

[assembly/libraries/Hooks.ts:14](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Hooks.ts#L14)

---

### AFTER_FLASH_LOAN_FLAG

• `Const` **AFTER_FLASH_LOAN_FLAG**: `u32`

#### Defined in

[assembly/libraries/Hooks.ts:10](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Hooks.ts#L10)

---

### AFTER_MINT_FLAG

• `Const` **AFTER_MINT_FLAG**: `u32`

#### Defined in

[assembly/libraries/Hooks.ts:12](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Hooks.ts#L12)

---

### AFTER_SWAP_FLAG

• `Const` **AFTER_SWAP_FLAG**: `u32`

#### Defined in

[assembly/libraries/Hooks.ts:8](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Hooks.ts#L8)

---

### AFTER_TRANSFER_FLAG

• `Const` **AFTER_TRANSFER_FLAG**: `u32`

#### Defined in

[assembly/libraries/Hooks.ts:16](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Hooks.ts#L16)

---

### BALANCE_KEY_PREFIX_LENGTH

• `Const` **BALANCE_KEY_PREFIX_LENGTH**: `7`

#### Defined in

[assembly/libraries/Utils.ts:168](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Utils.ts#L168)

---

### BASIS_POINT_MAX

• `Const` **BASIS_POINT_MAX**: `u16` = `10_000`

#### Defined in

[assembly/libraries/Constants.ts:7](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Constants.ts#L7)

---

### BEFORE_BURN_FLAG

• `Const` **BEFORE_BURN_FLAG**: `u32`

#### Defined in

[assembly/libraries/Hooks.ts:13](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Hooks.ts#L13)

---

### BEFORE_FLASH_LOAN_FLAG

• `Const` **BEFORE_FLASH_LOAN_FLAG**: `u32`

#### Defined in

[assembly/libraries/Hooks.ts:9](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Hooks.ts#L9)

---

### BEFORE_MINT_FLAG

• `Const` **BEFORE_MINT_FLAG**: `u32`

#### Defined in

[assembly/libraries/Hooks.ts:11](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Hooks.ts#L11)

---

### BEFORE_SWAP_FLAG

• `Const` **BEFORE_SWAP_FLAG**: `u32`

#### Defined in

[assembly/libraries/Hooks.ts:7](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Hooks.ts#L7)

---

### BEFORE_TRANSFER_FLAG

• `Const` **BEFORE_TRANSFER_FLAG**: `u32`

#### Defined in

[assembly/libraries/Hooks.ts:15](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Hooks.ts#L15)

---

### DELIMITER

• `Const` **DELIMITER**: `":"`

#### Defined in

[assembly/libraries/Utils.ts:16](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Utils.ts#L16)

---

### EVENT_DELIMITER

• `Const` **EVENT_DELIMITER**: `";?!"`

#### Defined in

[assembly/libraries/Utils.ts:101](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Utils.ts#L101)

---

### ID_ONE

• `Const` **ID_ONE**: `u32`

#### Defined in

[assembly/libraries/Constants.ts:6](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Constants.ts#L6)

---

### MAX

• `Const` **MAX**: `u256` = `u256.Max`

#### Defined in

[assembly/libraries/Constants.ts:16](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Constants.ts#L16)

---

### MAX_BIN_STEP

• `Const` **MAX_BIN_STEP**: `100`

#### Defined in

[assembly/libraries/Constants.ts:12](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Constants.ts#L12)

---

### MAX_FEE

• `Const` **MAX_FEE**: `u64`

#### Defined in

[assembly/libraries/Constants.ts:13](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Constants.ts#L13)

---

### MAX_U128

• `Const` **MAX_U128**: `u256`

#### Defined in

[assembly/libraries/Constants.ts:20](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Constants.ts#L20)

---

### MIN_BIN_STEP

• `Const` **MIN_BIN_STEP**: `1`

#### Defined in

[assembly/libraries/Constants.ts:11](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Constants.ts#L11)

---

### ONE

• `Const` **ONE**: `u256` = `u256.One`

#### Defined in

[assembly/libraries/Constants.ts:14](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Constants.ts#L14)

---

### ONE_COIN

• `Const` **ONE_COIN**: `u64`

#### Defined in

[assembly/libraries/Constants.ts:9](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Constants.ts#L9)

---

### PRECISION

• `Const` **PRECISION**: `u256`

#### Defined in

[assembly/libraries/Constants.ts:8](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Constants.ts#L8)

---

### REAL_ID_SHIFT

• `Const` **REAL_ID_SHIFT**: `i64`

#### Defined in

[assembly/libraries/Constants.ts:5](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Constants.ts#L5)

---

### SCALE_OFFSET

• `Const` **SCALE_OFFSET**: `128`

#### Defined in

[assembly/libraries/Constants.ts:10](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Constants.ts#L10)

---

### STORAGE_BYTE_COST

• `Const` **STORAGE_BYTE_COST**: `100000`

#### Defined in

[assembly/libraries/Utils.ts:166](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Utils.ts#L166)

---

### STORAGE_PREFIX_LENGTH

• `Const` **STORAGE_PREFIX_LENGTH**: `4`

#### Defined in

[assembly/libraries/Utils.ts:167](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Utils.ts#L167)

---

### THREE

• `Const` **THREE**: `u256`

#### Defined in

[assembly/libraries/Constants.ts:18](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Constants.ts#L18)

---

### TWO

• `Const` **TWO**: `u256`

#### Defined in

[assembly/libraries/Constants.ts:17](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Constants.ts#L17)

---

### ZERO

• `Const` **ZERO**: `u256` = `u256.Zero`

#### Defined in

[assembly/libraries/Constants.ts:15](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Constants.ts#L15)

---

### ZERO_ADDRESS

• `Const` **ZERO_ADDRESS**: `Address`

#### Defined in

[assembly/libraries/Constants.ts:19](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Constants.ts#L19)

---

### \_KEY_ELEMENT_SUFFIX

• `Const` **\_KEY_ELEMENT_SUFFIX**: `"::"`

#### Defined in

[assembly/libraries/PersistentMap.ts:17](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/PersistentMap.ts#L17)

## Functions

### BinHelper\_\_BinStepOverflows

▸ **BinHelper\_\_BinStepOverflows**(`bp`): `string`

BinHelper errors

#### Parameters

| Name | Type  |
| :--- | :---- |
| `bp` | `u16` |

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:203](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Errors.ts#L203)

---

### BinHelper\_\_IdOverflows

▸ **BinHelper\_\_IdOverflows**(): `string`

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:205](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Errors.ts#L205)

---

### LBFactory\_\_BinStepHasNoPreset

▸ **LBFactory\_\_BinStepHasNoPreset**(`binStep`): `string`

#### Parameters

| Name      | Type  |
| :-------- | :---- |
| `binStep` | `u64` |

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:150](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Errors.ts#L150)

---

### LBFactory\_\_BinStepRequirementsBreached

▸ **LBFactory\_\_BinStepRequirementsBreached**(`lowerBound`, `binStep`, `higherBound`): `string`

#### Parameters

| Name          | Type  |
| :------------ | :---- |
| `lowerBound`  | `u64` |
| `binStep`     | `u32` |
| `higherBound` | `u64` |

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:134](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Errors.ts#L134)

---

### LBFactory\_\_DecreasingPeriods

▸ **LBFactory\_\_DecreasingPeriods**(`filterPeriod`, `decayPeriod`): `string`

#### Parameters

| Name           | Type  |
| :------------- | :---- |
| `filterPeriod` | `u32` |
| `decayPeriod`  | `u32` |

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:116](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Errors.ts#L116)

---

### LBFactory\_\_FactoryLockIsAlreadyInTheSameState

▸ **LBFactory\_\_FactoryLockIsAlreadyInTheSameState**(): `string`

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:146](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Errors.ts#L146)

---

### LBFactory\_\_FeesAboveMax

▸ **LBFactory\_\_FeesAboveMax**(`baseFee`, `_maxVariableFee`, `maxFees`): `string`

#### Parameters

| Name              | Type  |
| :---------------- | :---- |
| `baseFee`         | `u64` |
| `_maxVariableFee` | `u64` |
| `maxFees`         | `u64` |

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:124](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Errors.ts#L124)

---

### LBFactory\_\_FlashLoanFeeAboveMax

▸ **LBFactory\_\_FlashLoanFeeAboveMax**(`fees`, `maxFees`): `string`

#### Parameters

| Name      | Type  |
| :-------- | :---- |
| `fees`    | `u64` |
| `maxFees` | `u64` |

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:130](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Errors.ts#L130)

---

### LBFactory\_\_FunctionIsLockedForUsers

▸ **LBFactory\_\_FunctionIsLockedForUsers**(`user`): `string`

#### Parameters

| Name   | Type      |
| :----- | :-------- |
| `user` | `Address` |

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:144](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Errors.ts#L144)

---

### LBFactory\_\_IdenticalAddresses

▸ **LBFactory\_\_IdenticalAddresses**(`token`): `string`

LBFactory errors

#### Parameters

| Name    | Type      |
| :------ | :-------- |
| `token` | `Address` |

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:102](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Errors.ts#L102)

---

### LBFactory\_\_LBPairAlreadyExists

▸ **LBFactory\_\_LBPairAlreadyExists**(`tokenX`, `tokenY`, `_binStep`): `string`

#### Parameters

| Name       | Type      |
| :--------- | :-------- |
| `tokenX`   | `Address` |
| `tokenY`   | `Address` |
| `_binStep` | `u64`     |

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:110](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Errors.ts#L110)

---

### LBFactory\_\_LBPairIgnoredIsAlreadyInTheSameState

▸ **LBFactory\_\_LBPairIgnoredIsAlreadyInTheSameState**(): `string`

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:148](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Errors.ts#L148)

---

### LBFactory\_\_LBPairNotCreated

▸ **LBFactory\_\_LBPairNotCreated**(`tokenX`, `tokenY`, `binStep`): `string`

#### Parameters

| Name      | Type      |
| :-------- | :-------- |
| `tokenX`  | `Address` |
| `tokenY`  | `Address` |
| `binStep` | `u64`     |

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:156](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Errors.ts#L156)

---

### LBFactory\_\_ProtocolShareOverflows

▸ **LBFactory\_\_ProtocolShareOverflows**(`protocolShare`, `max`): `string`

#### Parameters

| Name            | Type  |
| :-------------- | :---- |
| `protocolShare` | `u32` |
| `max`           | `u64` |

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:140](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Errors.ts#L140)

---

### LBFactory\_\_QuoteAssetAlreadyWhitelisted

▸ **LBFactory\_\_QuoteAssetAlreadyWhitelisted**(`quoteAsset`): `string`

#### Parameters

| Name         | Type      |
| :----------- | :-------- |
| `quoteAsset` | `Address` |

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:107](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Errors.ts#L107)

---

### LBFactory\_\_QuoteAssetNotWhitelisted

▸ **LBFactory\_\_QuoteAssetNotWhitelisted**(`quoteAsset`): `string`

#### Parameters

| Name         | Type      |
| :----------- | :-------- |
| `quoteAsset` | `Address` |

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:104](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Errors.ts#L104)

---

### LBFactory\_\_ReductionFactorOverflows

▸ **LBFactory\_\_ReductionFactorOverflows**(`reductionFactor`, `max`): `string`

#### Parameters

| Name              | Type  |
| :---------------- | :---- |
| `reductionFactor` | `u32` |
| `max`             | `u64` |

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:120](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Errors.ts#L120)

---

### LBFactory\_\_SameFeeRecipient

▸ **LBFactory\_\_SameFeeRecipient**(`feeRecipient`): `string`

#### Parameters

| Name           | Type      |
| :------------- | :-------- |
| `feeRecipient` | `Address` |

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:152](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Errors.ts#L152)

---

### LBFactory\_\_SameFlashLoanFee

▸ **LBFactory\_\_SameFlashLoanFee**(`flashLoanFee`): `string`

#### Parameters

| Name           | Type  |
| :------------- | :---- |
| `flashLoanFee` | `u64` |

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:154](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Errors.ts#L154)

---

### LBFactory\_\_SameHooksParameters

▸ **LBFactory\_\_SameHooksParameters**(`hooksParameters`): `string`

#### Parameters

| Name              | Type                                           |
| :---------------- | :--------------------------------------------- |
| `hooksParameters` | [`HooksParameters`](./structs/HooksParameters) |

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:161](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Errors.ts#L161)

---

### LBPair\_\_AddressZero

▸ **LBPair\_\_AddressZero**(): `string`

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:170](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Errors.ts#L170)

---

### LBPair\_\_AddressZeroOrThis

▸ **LBPair\_\_AddressZeroOrThis**(): `string`

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:171](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Errors.ts#L171)

---

### LBPair\_\_BinStepNotSame

▸ **LBPair\_\_BinStepNotSame**(): `string`

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:199](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Errors.ts#L199)

---

### LBPair\_\_CompositionFactorFlawed

▸ **LBPair\_\_CompositionFactorFlawed**(`id`): `string`

#### Parameters

| Name | Type  |
| :--- | :---- |
| `id` | `u64` |

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:173](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Errors.ts#L173)

---

### LBPair\_\_DistributionsOverflow

▸ **LBPair\_\_DistributionsOverflow**(): `string`

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:183](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Errors.ts#L183)

---

### LBPair\_\_FlashLoanCallbackFailed

▸ **LBPair\_\_FlashLoanCallbackFailed**(): `string`

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:193](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Errors.ts#L193)

---

### LBPair\_\_FlashLoanInvalidBalance

▸ **LBPair\_\_FlashLoanInvalidBalance**(): `string`

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:195](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Errors.ts#L195)

---

### LBPair\_\_FlashLoanInvalidToken

▸ **LBPair\_\_FlashLoanInvalidToken**(): `string`

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:197](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Errors.ts#L197)

---

### LBPair\_\_InsufficientAmounts

▸ **LBPair\_\_InsufficientAmounts**(): `string`

LBPair errors

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:168](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Errors.ts#L168)

---

### LBPair\_\_InsufficientLiquidityBurned

▸ **LBPair\_\_InsufficientLiquidityBurned**(`id`): `string`

#### Parameters

| Name | Type  |
| :--- | :---- |
| `id` | `u64` |

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:177](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Errors.ts#L177)

---

### LBPair\_\_InsufficientLiquidityMinted

▸ **LBPair\_\_InsufficientLiquidityMinted**(`id`): `string`

#### Parameters

| Name | Type  |
| :--- | :---- |
| `id` | `u64` |

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:175](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Errors.ts#L175)

---

### LBPair\_\_OnlyFactory

▸ **LBPair\_\_OnlyFactory**(): `string`

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:182](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Errors.ts#L182)

---

### LBPair\_\_OnlyFeeRecipient

▸ **LBPair\_\_OnlyFeeRecipient**(`feeRecipient`, `sender`): `string`

#### Parameters

| Name           | Type      |
| :------------- | :-------- |
| `feeRecipient` | `Address` |
| `sender`       | `Address` |

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:185](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Errors.ts#L185)

---

### LBPair\_\_OnlyStrictlyIncreasingId

▸ **LBPair\_\_OnlyStrictlyIncreasingId**(): `string`

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:180](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Errors.ts#L180)

---

### LBPair\_\_OracleNewSizeTooSmall

▸ **LBPair\_\_OracleNewSizeTooSmall**(`newSize`, `oracleSize`): `string`

#### Parameters

| Name         | Type  |
| :----------- | :---- |
| `newSize`    | `u64` |
| `oracleSize` | `u64` |

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:189](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Errors.ts#L189)

---

### LBPair\_\_WrongLengths

▸ **LBPair\_\_WrongLengths**(): `string`

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:179](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Errors.ts#L179)

---

### LBQuoter_InvalidLength

▸ **LBQuoter_InvalidLength**(): `string`

LBQuoter errors

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:251](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Errors.ts#L251)

---

### LBRouter\_\_AmountSlippageCaught

▸ **LBRouter\_\_AmountSlippageCaught**(`amountXMin`, `amountX`, `amountYMin`, `amountY`): `string`

#### Parameters

| Name         | Type   |
| :----------- | :----- |
| `amountXMin` | `u256` |
| `amountX`    | `u256` |
| `amountYMin` | `u256` |
| `amountY`    | `u256` |

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:30](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Errors.ts#L30)

---

### LBRouter\_\_BrokenSwapSafetyCheck

▸ **LBRouter\_\_BrokenSwapSafetyCheck**(): `string`

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:12](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Errors.ts#L12)

---

### LBRouter\_\_DeadlineExceeded

▸ **LBRouter\_\_DeadlineExceeded**(`deadline`, `currentTimestamp`): `string`

#### Parameters

| Name               | Type  |
| :----------------- | :---- |
| `deadline`         | `u64` |
| `currentTimestamp` | `u64` |

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:43](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Errors.ts#L43)

---

### LBRouter\_\_IdDesiredOverflows

▸ **LBRouter\_\_IdDesiredOverflows**(`idDesired`, `idSlippage`): `string`

#### Parameters

| Name         | Type  |
| :----------- | :---- |
| `idDesired`  | `u64` |
| `idSlippage` | `u64` |

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:39](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Errors.ts#L39)

---

### LBRouter\_\_IdOverflows

▸ **LBRouter\_\_IdOverflows**(`id`): `string`

#### Parameters

| Name | Type  |
| :--- | :---- |
| `id` | `i64` |

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:18](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Errors.ts#L18)

---

### LBRouter\_\_IdSlippageCaught

▸ **LBRouter\_\_IdSlippageCaught**(`activeIdDesired`, `idSlippage`, `activeId`): `string`

#### Parameters

| Name              | Type  |
| :---------------- | :---- |
| `activeIdDesired` | `u64` |
| `idSlippage`      | `u64` |
| `activeId`        | `u64` |

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:24](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Errors.ts#L24)

---

### LBRouter\_\_InsufficientAmountOut

▸ **LBRouter\_\_InsufficientAmountOut**(`amountOutMin`, `amountOut`): `string`

#### Parameters

| Name           | Type   |
| :------------- | :----- |
| `amountOutMin` | `u256` |
| `amountOut`    | `u256` |

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:47](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Errors.ts#L47)

---

### LBRouter\_\_InvalidTokenPath

▸ **LBRouter\_\_InvalidTokenPath**(`wrongToken`): `string`

#### Parameters

| Name         | Type      |
| :----------- | :-------- |
| `wrongToken` | `Address` |

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:61](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Errors.ts#L61)

---

### LBRouter\_\_LengthsMismatch

▸ **LBRouter\_\_LengthsMismatch**(): `string`

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:20](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Errors.ts#L20)

---

### LBRouter\_\_MaxAmountInExceeded

▸ **LBRouter\_\_MaxAmountInExceeded**(`amountInMax`, `amountIn`): `string`

#### Parameters

| Name          | Type   |
| :------------ | :----- |
| `amountInMax` | `u256` |
| `amountIn`    | `u256` |

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:54](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Errors.ts#L54)

---

### LBRouter\_\_NotFactoryOwner

▸ **LBRouter\_\_NotFactoryOwner**(): `string`

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:14](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Errors.ts#L14)

---

### LBRouter\_\_SwapOverflows

▸ **LBRouter\_\_SwapOverflows**(`id`): `string`

#### Parameters

| Name | Type  |
| :--- | :---- |
| `id` | `u64` |

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:10](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Errors.ts#L10)

---

### LBRouter\_\_TooMuchTokensIn

▸ **LBRouter\_\_TooMuchTokensIn**(`excess`): `string`

#### Parameters

| Name     | Type   |
| :------- | :----- |
| `excess` | `u256` |

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:16](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Errors.ts#L16)

---

### LBRouter\_\_WrongAmounts

▸ **LBRouter\_\_WrongAmounts**(`amount`, `reserve`): `string`

LBRouter errors

#### Parameters

| Name      | Type   |
| :-------- | :----- |
| `amount`  | `u256` |
| `reserve` | `u256` |

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:8](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Errors.ts#L8)

---

### LBRouter\_\_WrongMasLiquidityParameters

▸ **LBRouter\_\_WrongMasLiquidityParameters**(`tokenX`, `tokenY`, `amountX`, `amountY`, `msgValue`): `string`

#### Parameters

| Name       | Type      |
| :--------- | :-------- |
| `tokenX`   | `Address` |
| `tokenY`   | `Address` |
| `amountX`  | `u256`    |
| `amountY`  | `u256`    |
| `msgValue` | `u64`     |

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:63](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Errors.ts#L63)

---

### LBRouter\_\_WrongTokenOrder

▸ **LBRouter\_\_WrongTokenOrder**(): `string`

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:22](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Errors.ts#L22)

---

### LBToken\_\_BurnExceedsBalance

▸ **LBToken\_\_BurnExceedsBalance**(`from`, `id`, `amount`): `string`

#### Parameters

| Name     | Type      |
| :------- | :-------- |
| `from`   | `Address` |
| `id`     | `u64`     |
| `amount` | `u256`    |

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:80](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Errors.ts#L80)

---

### LBToken\_\_LengthMismatch

▸ **LBToken\_\_LengthMismatch**(`accountsLength`, `idsLength`): `string`

#### Parameters

| Name             | Type  |
| :--------------- | :---- |
| `accountsLength` | `u64` |
| `idsLength`      | `u64` |

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:86](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Errors.ts#L86)

---

### LBToken\_\_SelfApproval

▸ **LBToken\_\_SelfApproval**(`owner`): `string`

#### Parameters

| Name    | Type      |
| :------ | :-------- |
| `owner` | `Address` |

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:90](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Errors.ts#L90)

---

### LBToken\_\_SpenderNotApproved

▸ **LBToken\_\_SpenderNotApproved**(`owner`, `spender`): `string`

LBToken errors

#### Parameters

| Name      | Type      |
| :-------- | :-------- |
| `owner`   | `Address` |
| `spender` | `Address` |

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:76](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Errors.ts#L76)

---

### LBToken\_\_TransferExceedsBalance

▸ **LBToken\_\_TransferExceedsBalance**(`from`, `id`, `amount`): `string`

#### Parameters

| Name     | Type      |
| :------- | :-------- |
| `from`   | `Address` |
| `id`     | `u64`     |
| `amount` | `u256`    |

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:92](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Errors.ts#L92)

---

### LBToken\_\_TransferToSelf

▸ **LBToken\_\_TransferToSelf**(): `string`

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:98](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Errors.ts#L98)

---

### Math128x128\_\_PowerUnderflow

▸ **Math128x128\_\_PowerUnderflow**(`x`, `y`): `string`

Math128x128 errors

#### Parameters

| Name | Type   |
| :--- | :----- |
| `x`  | `u256` |
| `y`  | `i64`  |

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:209](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Errors.ts#L209)

---

### Math512Bits\_\_MulDivOverflow

▸ **Math512Bits\_\_MulDivOverflow**(`prod1`, `denominator`): `string`

Math512Bits errors

#### Parameters

| Name          | Type   |
| :------------ | :----- |
| `prod1`       | `u256` |
| `denominator` | `u256` |

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:214](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Errors.ts#L214)

---

### Math512Bits\_\_MulShiftOverflow

▸ **Math512Bits\_\_MulShiftOverflow**(`prod1`, `offset`): `string`

#### Parameters

| Name     | Type   |
| :------- | :----- |
| `prod1`  | `u256` |
| `offset` | `u64`  |

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:221](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Errors.ts#L221)

---

### Math512Bits\_\_OffsetOverflows

▸ **Math512Bits\_\_OffsetOverflows**(`offset`): `string`

#### Parameters

| Name     | Type  |
| :------- | :---- |
| `offset` | `u64` |

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:225](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Errors.ts#L225)

---

### Oracle\_\_LookUpTimestampTooOld

▸ **Oracle\_\_LookUpTimestampTooOld**(`_minTimestamp`, `_lookUpTimestamp`): `string`

Oracle errors

#### Parameters

| Name               | Type  |
| :----------------- | :---- |
| `_minTimestamp`    | `u64` |
| `_lookUpTimestamp` | `u64` |

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:230](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Errors.ts#L230)

---

### Oracle\_\_NotInitialized

▸ **Oracle\_\_NotInitialized**(): `string`

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:235](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Errors.ts#L235)

---

### ReentrancyGuardUpgradeable\_\_AlreadyInitialized

▸ **ReentrancyGuardUpgradeable\_\_AlreadyInitialized**(): `string`

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:241](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Errors.ts#L241)

---

### ReentrancyGuardUpgradeable\_\_ReentrantCall

▸ **ReentrancyGuardUpgradeable\_\_ReentrantCall**(): `string`

ReentrancyGuardUpgradeable errors

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:239](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Errors.ts#L239)

---

### Storage\_\_NotEnoughCoinsSent

▸ **Storage\_\_NotEnoughCoinsSent**(`spent`, `sent`): `string`

Storage errors

#### Parameters

| Name    | Type  |
| :------ | :---- |
| `spent` | `u64` |
| `sent`  | `u64` |

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:255](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Errors.ts#L255)

---

### TreeMath\_\_ErrorDepthSearch

▸ **TreeMath\_\_ErrorDepthSearch**(): `string`

TreeMath errors

#### Returns

`string`

#### Defined in

[assembly/libraries/Errors.ts:246](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Errors.ts#L246)

---

### \_sortTokens

▸ **\_sortTokens**(`_tokenA`, `_tokenB`): `SortTokensReturn`

#### Parameters

| Name      | Type      | Description      |
| :-------- | :-------- | :--------------- |
| `_tokenA` | `Address` | The first token  |
| `_tokenB` | `Address` | The second token |

#### Returns

`SortTokensReturn`

SortTokensReturn: token0, token1

**`Notice`**

Private view function to sort 2 tokens in ascending order

#### Defined in

[assembly/libraries/Utils.ts:34](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Utils.ts#L34)

---

### createEvent

▸ **createEvent**(`key`, `args`): `string`

#### Parameters

| Name   | Type       | Description                 |
| :----- | :--------- | :-------------------------- |
| `key`  | `string`   | the string event key.       |
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

[assembly/libraries/Utils.ts:118](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Utils.ts#L118)

---

### createKey

▸ **createKey**(`args`): `string`

#### Parameters

| Name   | Type       |
| :----- | :--------- |
| `args` | `string`[] |

#### Returns

`string`

#### Defined in

[assembly/libraries/Utils.ts:17](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Utils.ts#L17)

---

### spreadLiquidity

▸ **spreadLiquidity**(`amountYIn`, `startId`, `numbersBins`, `gap`, `binStep`): `SpreadLiqudityReturn`

#### Parameters

| Name          | Type   |
| :------------ | :----- |
| `amountYIn`   | `u256` |
| `startId`     | `u32`  |
| `numbersBins` | `u32`  |
| `gap`         | `u32`  |
| `binStep`     | `u32`  |

#### Returns

`SpreadLiqudityReturn`

#### Defined in

[assembly/libraries/Utils.ts:54](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Utils.ts#L54)

---

### transferRemaining

▸ **transferRemaining**(`balanceInit`, `balanceFinal`, `sent`, `to`): `void`

#### Parameters

| Name           | Type      | Description                                                       |
| :------------- | :-------- | :---------------------------------------------------------------- |
| `balanceInit`  | `u64`     | Initial balance of the SC (transferred coins + balance of the SC) |
| `balanceFinal` | `u64`     | Balance of the SC at the end of the call                          |
| `sent`         | `u64`     | Number of coins sent to the SC                                    |
| `to`           | `Address` | Caller of the function to transfer the remaining coins to         |

#### Returns

`void`

**`Notice`**

Function to transfer remaining Massa coins to a recipient at the end of a call

#### Defined in

[assembly/libraries/Utils.ts:137](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Utils.ts#L137)

---

### u256ToString

▸ **u256ToString**(`u`): `string`

#### Parameters

| Name | Type   |
| :--- | :----- |
| `u`  | `u256` |

#### Returns

`string`

**`Notice`**

Function to convert a u256 to a UTF-16 bytes then to a string

**`Dev`**

u256.toString() is too expensive in as-bignum so we use this instead

#### Defined in

[assembly/libraries/Utils.ts:126](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Utils.ts#L126)
