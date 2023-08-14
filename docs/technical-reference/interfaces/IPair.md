# IPair

## Table of contents

### Constructors

- [constructor](IPair.md#constructor)

### Properties

- [\_origin](IPair.md#_origin)

### Methods

- [balanceOf](IPair.md#balanceof)
- [balanceOfBatch](IPair.md#balanceofbatch)
- [burn](IPair.md#burn)
- [collectFees](IPair.md#collectfees)
- [feeParameters](IPair.md#feeparameters)
- [findFirstNonEmptyBinId](IPair.md#findfirstnonemptybinid)
- [flashLoan](IPair.md#flashloan)
- [forceDecay](IPair.md#forcedecay)
- [getBin](IPair.md#getbin)
- [getFactory](IPair.md#getfactory)
- [getOracleParameters](IPair.md#getoracleparameters)
- [getOracleSampleFrom](IPair.md#getoraclesamplefrom)
- [getPairInformation](IPair.md#getpairinformation)
- [getTokenX](IPair.md#gettokenx)
- [getTokenY](IPair.md#gettokeny)
- [getUserBins](IPair.md#getuserbins)
- [increaseOracleLength](IPair.md#increaseoraclelength)
- [init](IPair.md#init)
- [isApprovedForAll](IPair.md#isapprovedforall)
- [mint](IPair.md#mint)
- [name](IPair.md#name)
- [pendingFees](IPair.md#pendingfees)
- [safeBatchTransferFrom](IPair.md#safebatchtransferfrom)
- [safeTransferFrom](IPair.md#safetransferfrom)
- [setApprovalForAll](IPair.md#setapprovalforall)
- [setFeesParameters](IPair.md#setfeesparameters)
- [swap](IPair.md#swap)
- [symbol](IPair.md#symbol)
- [totalSupply](IPair.md#totalsupply)

## Constructors

### constructor

• **new IPair**(`at`)

Wraps a smart contract exposing standard token FFI.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `at` | `Address` | Address of the smart contract. |

#### Defined in

[assembly/interfaces/IPair.ts:29](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/interfaces/IPair.ts#L29)

## Properties

### \_origin

• **\_origin**: `Address`

#### Defined in

[assembly/interfaces/IPair.ts:22](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/interfaces/IPair.ts#L22)

## Methods

### balanceOf

▸ **balanceOf**(`_account`, `_id`): `u64`

#### Parameters

| Name | Type |
| :------ | :------ |
| `_account` | `Address` |
| `_id` | `u64` |

#### Returns

`u64`

#### Defined in

[assembly/interfaces/IPair.ts:194](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/interfaces/IPair.ts#L194)

___

### balanceOfBatch

▸ **balanceOfBatch**(`_accounts`, `_ids`): `u64`[]

#### Parameters

| Name | Type |
| :------ | :------ |
| `_accounts` | `Address`[] |
| `_ids` | `u64`[] |

#### Returns

`u64`[]

#### Defined in

[assembly/interfaces/IPair.ts:204](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/interfaces/IPair.ts#L204)

___

### burn

▸ **burn**(`_ids`, `_amounts`, `_to`): `Amounts`

#### Parameters

| Name | Type |
| :------ | :------ |
| `_ids` | `u64`[] |
| `_amounts` | `u64`[] |
| `_to` | `Address` |

#### Returns

`Amounts`

#### Defined in

[assembly/interfaces/IPair.ts:127](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/interfaces/IPair.ts#L127)

___

### collectFees

▸ **collectFees**(`account`, `ids`): `Amounts`

#### Parameters

| Name | Type |
| :------ | :------ |
| `account` | `Address` |
| `ids` | `u64`[] |

#### Returns

`Amounts`

#### Defined in

[assembly/interfaces/IPair.ts:254](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/interfaces/IPair.ts#L254)

___

### feeParameters

▸ **feeParameters**(): [`FeeParameters`](FeeParameters.md)

#### Returns

[`FeeParameters`](FeeParameters.md)

#### Defined in

[assembly/interfaces/IPair.ts:66](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/interfaces/IPair.ts#L66)

___

### findFirstNonEmptyBinId

▸ **findFirstNonEmptyBinId**(`id`, `sentTokenY`): `u32`

#### Parameters

| Name | Type |
| :------ | :------ |
| `id` | `u32` |
| `sentTokenY` | `bool` |

#### Returns

`u32`

#### Defined in

[assembly/interfaces/IPair.ts:156](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/interfaces/IPair.ts#L156)

___

### flashLoan

▸ **flashLoan**(`token`, `amount`, `data?`): `void`

#### Parameters

| Name | Type | Default value |
| :------ | :------ | :------ |
| `token` | [`IERC20`](IERC20.md) | `undefined` |
| `amount` | `u64` | `undefined` |
| `data` | `StaticArray`<`u8`\> | `[]` |

#### Returns

`void`

#### Defined in

[assembly/interfaces/IPair.ts:133](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/interfaces/IPair.ts#L133)

___

### forceDecay

▸ **forceDecay**(): `void`

#### Returns

`void`

#### Defined in

[assembly/interfaces/IPair.ts:175](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/interfaces/IPair.ts#L175)

___

### getBin

▸ **getBin**(`_id`): [`Bin`](Bin.md)

#### Parameters

| Name | Type |
| :------ | :------ |
| `_id` | `u32` |

#### Returns

[`Bin`](Bin.md)

#### Defined in

[assembly/interfaces/IPair.ts:71](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/interfaces/IPair.ts#L71)

___

### getFactory

▸ **getFactory**(): `Address`

#### Returns

`Address`

#### Defined in

[assembly/interfaces/IPair.ts:166](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/interfaces/IPair.ts#L166)

___

### getOracleParameters

▸ **getOracleParameters**(): [`OracleParameters`](OracleParameters.md)

#### Returns

[`OracleParameters`](OracleParameters.md)

#### Defined in

[assembly/interfaces/IPair.ts:260](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/interfaces/IPair.ts#L260)

___

### getOracleSampleFrom

▸ **getOracleSampleFrom**(`timeDelta`): `OracleSampleReturn`

#### Parameters

| Name | Type |
| :------ | :------ |
| `timeDelta` | `u64` |

#### Returns

`OracleSampleReturn`

#### Defined in

[assembly/interfaces/IPair.ts:265](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/interfaces/IPair.ts#L265)

___

### getPairInformation

▸ **getPairInformation**(): [`PairInformation`](PairInformation.md)

#### Returns

[`PairInformation`](PairInformation.md)

#### Defined in

[assembly/interfaces/IPair.ts:146](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/interfaces/IPair.ts#L146)

___

### getTokenX

▸ **getTokenX**(): [`IERC20`](IERC20.md)

#### Returns

[`IERC20`](IERC20.md)

#### Defined in

[assembly/interfaces/IPair.ts:138](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/interfaces/IPair.ts#L138)

___

### getTokenY

▸ **getTokenY**(): [`IERC20`](IERC20.md)

#### Returns

[`IERC20`](IERC20.md)

#### Defined in

[assembly/interfaces/IPair.ts:142](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/interfaces/IPair.ts#L142)

___

### getUserBins

▸ **getUserBins**(`account`): `u32`[]

#### Parameters

| Name | Type |
| :------ | :------ |
| `account` | `Address` |

#### Returns

`u32`[]

#### Defined in

[assembly/interfaces/IPair.ts:151](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/interfaces/IPair.ts#L151)

___

### increaseOracleLength

▸ **increaseOracleLength**(`newSize`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `newSize` | `u64` |

#### Returns

`void`

#### Defined in

[assembly/interfaces/IPair.ts:276](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/interfaces/IPair.ts#L276)

___

### init

▸ **init**(`factory`, `tokenX`, `tokenY`, `activeId`, `preset`): `void`

Calls the constructor

#### Parameters

| Name | Type |
| :------ | :------ |
| `factory` | `Address` |
| `tokenX` | `Address` |
| `tokenY` | `Address` |
| `activeId` | `u32` |
| `preset` | [`Preset`](Preset.md) |

#### Returns

`void`

#### Defined in

[assembly/interfaces/IPair.ts:38](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/interfaces/IPair.ts#L38)

___

### isApprovedForAll

▸ **isApprovedForAll**(`_owner`, `_spender`): `bool`

#### Parameters

| Name | Type |
| :------ | :------ |
| `_owner` | `Address` |
| `_spender` | `Address` |

#### Returns

`bool`

#### Defined in

[assembly/interfaces/IPair.ts:210](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/interfaces/IPair.ts#L210)

___

### mint

▸ **mint**(`_ids`, `_distributionX`, `_distributionY`, `_to`): `MintReturn`

Mint new LB tokens for each bins where the user adds liquidity.
This function will not transfer the tokens from the caller, it is expected that the tokens have already been
transferred to this contract through another contract.
That is why this function shouldn't be called directly, but through one of the add liquidity functions of the
router that will also perform safety checks.
Any excess amount of token will be sent to the `to` address. The lengths of the arrays must be the same.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `_ids` | `u64`[] | The ids of the bins where the liquidity will be added. It will mint LB tokens for each of these bins. |
| `_distributionX` | `u64`[] | The percentage of token X to add to each bin. The sum of all the values must not exceed 100%, that is 1e9. |
| `_distributionY` | `u64`[] | The percentage of token Y to add to each bin. The sum of all the values must not exceed 100%, that is 1e9. |
| `_to` | `Address` | The address that will receive the LB tokens and the excess amount of tokens. |

#### Returns

`MintReturn`

#### Defined in

[assembly/interfaces/IPair.ts:108](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/interfaces/IPair.ts#L108)

___

### name

▸ **name**(): `string`

#### Returns

`string`

#### Defined in

[assembly/interfaces/IPair.ts:179](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/interfaces/IPair.ts#L179)

___

### pendingFees

▸ **pendingFees**(`account`, `ids`): `Amounts`

#### Parameters

| Name | Type |
| :------ | :------ |
| `account` | `Address` |
| `ids` | `u64`[] |

#### Returns

`Amounts`

#### Defined in

[assembly/interfaces/IPair.ts:248](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/interfaces/IPair.ts#L248)

___

### safeBatchTransferFrom

▸ **safeBatchTransferFrom**(`_from`, `_to`, `_ids`, `_amounts`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `_from` | `Address` |
| `_to` | `Address` |
| `_ids` | `u64`[] |
| `_amounts` | `u64`[] |

#### Returns

`void`

#### Defined in

[assembly/interfaces/IPair.ts:238](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/interfaces/IPair.ts#L238)

___

### safeTransferFrom

▸ **safeTransferFrom**(`_from`, `_to`, `_id`, `amount`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `_from` | `Address` |
| `_to` | `Address` |
| `_id` | `u64` |
| `amount` | `u64` |

#### Returns

`void`

#### Defined in

[assembly/interfaces/IPair.ts:229](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/interfaces/IPair.ts#L229)

___

### setApprovalForAll

▸ **setApprovalForAll**(`_approved`, `_sender`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `_approved` | `bool` |
| `_sender` | `Address` |

#### Returns

`void`

#### Defined in

[assembly/interfaces/IPair.ts:220](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/interfaces/IPair.ts#L220)

___

### setFeesParameters

▸ **setFeesParameters**(`fp`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `fp` | [`FeeParameters`](FeeParameters.md) |

#### Returns

`void`

#### Defined in

[assembly/interfaces/IPair.ts:170](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/interfaces/IPair.ts#L170)

___

### swap

▸ **swap**(`swapForY`, `to`): `u64`

Swap tokens iterating over the bins until the entire amount is swapped.
Will swap token X for token Y if `_swapForY` is true, and token Y for token X if `_swapForY` is false.
This function will not transfer the tokens from the caller, it is expected that the tokens have already been
transferred to this contract through another contract.
That is why this function shouldn't be called directly, but through one of the swap functions of the router
that will also perform safety checks.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `swapForY` | `bool` | Whether you've swapping token X for token Y (true) or token Y for token X (false) |
| `to` | `Address` | The address to send the tokens to |

#### Returns

`u64`

#### Defined in

[assembly/interfaces/IPair.ts:88](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/interfaces/IPair.ts#L88)

___

### symbol

▸ **symbol**(): `string`

#### Returns

`string`

#### Defined in

[assembly/interfaces/IPair.ts:184](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/interfaces/IPair.ts#L184)

___

### totalSupply

▸ **totalSupply**(`_id`): `u64`

#### Parameters

| Name | Type |
| :------ | :------ |
| `_id` | `u64` |

#### Returns

`u64`

#### Defined in

[assembly/interfaces/IPair.ts:189](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/interfaces/IPair.ts#L189)
