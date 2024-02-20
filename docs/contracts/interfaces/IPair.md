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

• **new IPair**(`at`): [`IPair`](IPair.md)

Wraps a smart contract exposing standard token FFI.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `at` | `Address` | Address of the smart contract. |

#### Returns

[`IPair`](IPair.md)

#### Defined in

[assembly/interfaces/IPair.ts:31](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/interfaces/IPair.ts#L31)

## Properties

### \_origin

• **\_origin**: `Address`

#### Defined in

[assembly/interfaces/IPair.ts:24](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/interfaces/IPair.ts#L24)

## Methods

### balanceOf

▸ **balanceOf**(`_account`, `_id`): `u256`

#### Parameters

| Name | Type |
| :------ | :------ |
| `_account` | `Address` |
| `_id` | `u64` |

#### Returns

`u256`

#### Defined in

[assembly/interfaces/IPair.ts:201](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/interfaces/IPair.ts#L201)

___

### balanceOfBatch

▸ **balanceOfBatch**(`_accounts`, `_ids`): `u256`[]

#### Parameters

| Name | Type |
| :------ | :------ |
| `_accounts` | `Address`[] |
| `_ids` | `u64`[] |

#### Returns

`u256`[]

#### Defined in

[assembly/interfaces/IPair.ts:211](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/interfaces/IPair.ts#L211)

___

### burn

▸ **burn**(`_ids`, `_amounts`, `_to`): `Amounts`

#### Parameters

| Name | Type |
| :------ | :------ |
| `_ids` | `u64`[] |
| `_amounts` | `u256`[] |
| `_to` | `Address` |

#### Returns

`Amounts`

#### Defined in

[assembly/interfaces/IPair.ts:129](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/interfaces/IPair.ts#L129)

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

[assembly/interfaces/IPair.ts:261](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/interfaces/IPair.ts#L261)

___

### feeParameters

▸ **feeParameters**(): [`FeeParameters`](../structs/FeeParameters.md)

#### Returns

[`FeeParameters`](../structs/FeeParameters.md)

#### Defined in

[assembly/interfaces/IPair.ts:68](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/interfaces/IPair.ts#L68)

___

### findFirstNonEmptyBinId

▸ **findFirstNonEmptyBinId**(`id`, `sentTokenY`): `Result`<`u32`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `id` | `u32` |
| `sentTokenY` | `bool` |

#### Returns

`Result`<`u32`\>

#### Defined in

[assembly/interfaces/IPair.ts:158](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/interfaces/IPair.ts#L158)

___

### flashLoan

▸ **flashLoan**(`token`, `amount`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `token` | [`IERC20`](IERC20.md) |
| `amount` | `u256` |

#### Returns

`void`

#### Defined in

[assembly/interfaces/IPair.ts:135](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/interfaces/IPair.ts#L135)

___

### forceDecay

▸ **forceDecay**(): `void`

#### Returns

`void`

#### Defined in

[assembly/interfaces/IPair.ts:182](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/interfaces/IPair.ts#L182)

___

### getBin

▸ **getBin**(`_id`): [`Bin`](../structs/Bin.md)

#### Parameters

| Name | Type |
| :------ | :------ |
| `_id` | `u32` |

#### Returns

[`Bin`](../structs/Bin.md)

#### Defined in

[assembly/interfaces/IPair.ts:73](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/interfaces/IPair.ts#L73)

___

### getFactory

▸ **getFactory**(): `Address`

#### Returns

`Address`

#### Defined in

[assembly/interfaces/IPair.ts:173](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/interfaces/IPair.ts#L173)

___

### getOracleParameters

▸ **getOracleParameters**(): [`OracleParameters`](../structs/OracleParameters.md)

#### Returns

[`OracleParameters`](../structs/OracleParameters.md)

#### Defined in

[assembly/interfaces/IPair.ts:267](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/interfaces/IPair.ts#L267)

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

[assembly/interfaces/IPair.ts:272](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/interfaces/IPair.ts#L272)

___

### getPairInformation

▸ **getPairInformation**(): [`PairInformation`](../structs/PairInformation.md)

#### Returns

[`PairInformation`](../structs/PairInformation.md)

#### Defined in

[assembly/interfaces/IPair.ts:148](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/interfaces/IPair.ts#L148)

___

### getTokenX

▸ **getTokenX**(): [`IERC20`](IERC20.md)

#### Returns

[`IERC20`](IERC20.md)

#### Defined in

[assembly/interfaces/IPair.ts:140](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/interfaces/IPair.ts#L140)

___

### getTokenY

▸ **getTokenY**(): [`IERC20`](IERC20.md)

#### Returns

[`IERC20`](IERC20.md)

#### Defined in

[assembly/interfaces/IPair.ts:144](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/interfaces/IPair.ts#L144)

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

[assembly/interfaces/IPair.ts:153](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/interfaces/IPair.ts#L153)

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

[assembly/interfaces/IPair.ts:283](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/interfaces/IPair.ts#L283)

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
| `preset` | [`Preset`](../structs/Preset.md) |

#### Returns

`void`

#### Defined in

[assembly/interfaces/IPair.ts:40](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/interfaces/IPair.ts#L40)

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

[assembly/interfaces/IPair.ts:217](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/interfaces/IPair.ts#L217)

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
| `_distributionX` | `u256`[] | The percentage of token X to add to each bin. The sum of all the values must not exceed 100%, that is 1e9. |
| `_distributionY` | `u256`[] | The percentage of token Y to add to each bin. The sum of all the values must not exceed 100%, that is 1e9. |
| `_to` | `Address` | The address that will receive the LB tokens and the excess amount of tokens. |

#### Returns

`MintReturn`

#### Defined in

[assembly/interfaces/IPair.ts:110](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/interfaces/IPair.ts#L110)

___

### name

▸ **name**(): `string`

#### Returns

`string`

#### Defined in

[assembly/interfaces/IPair.ts:186](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/interfaces/IPair.ts#L186)

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

[assembly/interfaces/IPair.ts:255](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/interfaces/IPair.ts#L255)

___

### safeBatchTransferFrom

▸ **safeBatchTransferFrom**(`_from`, `_to`, `_ids`, `_amounts`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `_from` | `Address` |
| `_to` | `Address` |
| `_ids` | `u64`[] |
| `_amounts` | `u256`[] |

#### Returns

`void`

#### Defined in

[assembly/interfaces/IPair.ts:245](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/interfaces/IPair.ts#L245)

___

### safeTransferFrom

▸ **safeTransferFrom**(`_from`, `_to`, `_id`, `amount`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `_from` | `Address` |
| `_to` | `Address` |
| `_id` | `u64` |
| `amount` | `u256` |

#### Returns

`void`

#### Defined in

[assembly/interfaces/IPair.ts:236](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/interfaces/IPair.ts#L236)

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

[assembly/interfaces/IPair.ts:227](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/interfaces/IPair.ts#L227)

___

### setFeesParameters

▸ **setFeesParameters**(`fp`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `fp` | [`FeeParameters`](../structs/FeeParameters.md) |

#### Returns

`void`

#### Defined in

[assembly/interfaces/IPair.ts:177](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/interfaces/IPair.ts#L177)

___

### swap

▸ **swap**(`swapForY`, `to`): `u256`

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

`u256`

#### Defined in

[assembly/interfaces/IPair.ts:90](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/interfaces/IPair.ts#L90)

___

### symbol

▸ **symbol**(): `string`

#### Returns

`string`

#### Defined in

[assembly/interfaces/IPair.ts:191](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/interfaces/IPair.ts#L191)

___

### totalSupply

▸ **totalSupply**(`_id`): `u256`

#### Parameters

| Name | Type |
| :------ | :------ |
| `_id` | `u64` |

#### Returns

`u256`

#### Defined in

[assembly/interfaces/IPair.ts:196](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/interfaces/IPair.ts#L196)
