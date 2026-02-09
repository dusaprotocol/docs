# Hooks

## Table of contents

### Constructors

- [constructor](Hooks#constructor)

### Methods

- [\_safeCall](Hooks#_safecall)
- [afterBatchTransferFrom](Hooks#afterbatchtransferfrom)
- [afterBurn](Hooks#afterburn)
- [afterFlashLoan](Hooks#afterflashloan)
- [afterMint](Hooks#aftermint)
- [afterSwap](Hooks#afterswap)
- [beforeBatchTransferFrom](Hooks#beforebatchtransferfrom)
- [beforeBurn](Hooks#beforeburn)
- [beforeFlashLoan](Hooks#beforeflashloan)
- [beforeMint](Hooks#beforemint)
- [beforeSwap](Hooks#beforeswap)
- [getFlags](Hooks#getflags)
- [onHooksSet](Hooks#onhooksset)
- [setHooks](Hooks#sethooks)

## Constructors

### constructor

• **new Hooks**(): [`Hooks`](Hooks)

#### Returns

[`Hooks`](Hooks)

## Methods

### \_safeCall

▸ **\_safeCall**(`encoded`, `method`, `args`): `void`

Helper function call the hook contract.

#### Parameters

| Name      | Type                                            |
| :-------- | :---------------------------------------------- |
| `encoded` | [`HooksParameters`](../structs/HooksParameters) |
| `method`  | `string`                                        |
| `args`    | `Args`                                          |

#### Returns

`void`

#### Defined in

[assembly/libraries/Hooks.ts:63](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Hooks.ts#L63)

---

### afterBatchTransferFrom

▸ **afterBatchTransferFrom**(`encoded`, `sender`, `from`, `to`, `ids`, `amounts`): `void`

Calls afterBatchTransferFrom on the hooks contract if the AFTER_TRANSFER_FLAG is set.

#### Parameters

| Name      | Type                                            |
| :-------- | :---------------------------------------------- |
| `encoded` | [`HooksParameters`](../structs/HooksParameters) |
| `sender`  | `Address`                                       |
| `from`    | `Address`                                       |
| `to`      | `Address`                                       |
| `ids`     | `u64`[]                                         |
| `amounts` | `u256`[]                                        |

#### Returns

`void`

#### Defined in

[assembly/libraries/Hooks.ts:275](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Hooks.ts#L275)

---

### afterBurn

▸ **afterBurn**(`encoded`, `sender`, `to`, `ids`, `amountsToBurn`): `void`

Calls afterBurn on the hooks contract if the AFTER_BURN_FLAG is set.

#### Parameters

| Name            | Type                                            |
| :-------------- | :---------------------------------------------- |
| `encoded`       | [`HooksParameters`](../structs/HooksParameters) |
| `sender`        | `Address`                                       |
| `to`            | `Address`                                       |
| `ids`           | `u64`[]                                         |
| `amountsToBurn` | `u256`[]                                        |

#### Returns

`void`

#### Defined in

[assembly/libraries/Hooks.ts:236](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Hooks.ts#L236)

---

### afterFlashLoan

▸ **afterFlashLoan**(`encoded`, `sender`, `to`, `fees`, `feesReceived`): `void`

Calls afterFlashLoan on the hooks contract if the AFTER_FLASH_LOAN_FLAG is set.

#### Parameters

| Name           | Type                                            |
| :------------- | :---------------------------------------------- |
| `encoded`      | [`HooksParameters`](../structs/HooksParameters) |
| `sender`       | `Address`                                       |
| `to`           | `Address`                                       |
| `fees`         | `u256`                                          |
| `feesReceived` | `u256`                                          |

#### Returns

`void`

#### Defined in

[assembly/libraries/Hooks.ts:144](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Hooks.ts#L144)

---

### afterMint

▸ **afterMint**(`encoded`, `sender`, `to`, `ids`, `distributionX`, `distributionY`, `amountsIn`): `void`

Calls afterMint on the hooks contract if the AFTER_MINT_FLAG is set.

#### Parameters

| Name            | Type                                            |
| :-------------- | :---------------------------------------------- |
| `encoded`       | [`HooksParameters`](../structs/HooksParameters) |
| `sender`        | `Address`                                       |
| `to`            | `Address`                                       |
| `ids`           | `u64`[]                                         |
| `distributionX` | `u256`[]                                        |
| `distributionY` | `u256`[]                                        |
| `amountsIn`     | `u256`[]                                        |

#### Returns

`void`

#### Defined in

[assembly/libraries/Hooks.ts:190](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Hooks.ts#L190)

---

### afterSwap

▸ **afterSwap**(`encoded`, `sender`, `to`, `swapForY`, `amountOut`): `void`

Calls afterSwap on the hooks contract if the AFTER_SWAP_FLAG is set.

#### Parameters

| Name        | Type                                            |
| :---------- | :---------------------------------------------- |
| `encoded`   | [`HooksParameters`](../structs/HooksParameters) |
| `sender`    | `Address`                                       |
| `to`        | `Address`                                       |
| `swapForY`  | `bool`                                          |
| `amountOut` | `u256`                                          |

#### Returns

`void`

#### Defined in

[assembly/libraries/Hooks.ts:107](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Hooks.ts#L107)

---

### beforeBatchTransferFrom

▸ **beforeBatchTransferFrom**(`encoded`, `sender`, `from`, `to`, `ids`, `amounts`): `void`

Calls beforeBatchTransferFrom on the hooks contract if the BEFORE_TRANSFER_FLAG is set.

#### Parameters

| Name      | Type                                            |
| :-------- | :---------------------------------------------- |
| `encoded` | [`HooksParameters`](../structs/HooksParameters) |
| `sender`  | `Address`                                       |
| `from`    | `Address`                                       |
| `to`      | `Address`                                       |
| `ids`     | `u64`[]                                         |
| `amounts` | `u256`[]                                        |

#### Returns

`void`

#### Defined in

[assembly/libraries/Hooks.ts:255](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Hooks.ts#L255)

---

### beforeBurn

▸ **beforeBurn**(`encoded`, `sender`, `to`, `ids`, `amountsToBurn`): `void`

Calls beforeBurn on the hooks contract if the BEFORE_BURN_FLAG is set.

#### Parameters

| Name            | Type                                            |
| :-------------- | :---------------------------------------------- |
| `encoded`       | [`HooksParameters`](../structs/HooksParameters) |
| `sender`        | `Address`                                       |
| `to`            | `Address`                                       |
| `ids`           | `u64`[]                                         |
| `amountsToBurn` | `u256`[]                                        |

#### Returns

`void`

#### Defined in

[assembly/libraries/Hooks.ts:217](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Hooks.ts#L217)

---

### beforeFlashLoan

▸ **beforeFlashLoan**(`encoded`, `sender`, `to`, `amount`): `void`

Calls beforeFlashLoan on the hooks contract if the BEFORE_FLASH_LOAN_FLAG is set.

#### Parameters

| Name      | Type                                            |
| :-------- | :---------------------------------------------- |
| `encoded` | [`HooksParameters`](../structs/HooksParameters) |
| `sender`  | `Address`                                       |
| `to`      | `Address`                                       |
| `amount`  | `u256`                                          |

#### Returns

`void`

#### Defined in

[assembly/libraries/Hooks.ts:126](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Hooks.ts#L126)

---

### beforeMint

▸ **beforeMint**(`encoded`, `sender`, `to`, `ids`, `distributionX`, `distributionY`, `amountsReceived`): `void`

Calls beforeMint on the hooks contract if the BEFORE_MINT_FLAG is set.

#### Parameters

| Name              | Type                                            |
| :---------------- | :---------------------------------------------- |
| `encoded`         | [`HooksParameters`](../structs/HooksParameters) |
| `sender`          | `Address`                                       |
| `to`              | `Address`                                       |
| `ids`             | `u64`[]                                         |
| `distributionX`   | `u256`[]                                        |
| `distributionY`   | `u256`[]                                        |
| `amountsReceived` | `u256`[]                                        |

#### Returns

`void`

#### Defined in

[assembly/libraries/Hooks.ts:163](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Hooks.ts#L163)

---

### beforeSwap

▸ **beforeSwap**(`encoded`, `sender`, `to`, `swapForY`, `amountIn`): `void`

Calls beforeSwap on the hooks contract if the BEFORE_SWAP_FLAG is set.

#### Parameters

| Name       | Type                                            |
| :--------- | :---------------------------------------------- |
| `encoded`  | [`HooksParameters`](../structs/HooksParameters) |
| `sender`   | `Address`                                       |
| `to`       | `Address`                                       |
| `swapForY` | `bool`                                          |
| `amountIn` | `u256`                                          |

#### Returns

`void`

#### Defined in

[assembly/libraries/Hooks.ts:88](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Hooks.ts#L88)

---

### getFlags

▸ **getFlags**(`encoded`): `u32`

Returns the flags stored in the encoded parameters.

#### Parameters

| Name      | Type                                            |
| :-------- | :---------------------------------------------- |
| `encoded` | [`HooksParameters`](../structs/HooksParameters) |

#### Returns

`u32`

#### Defined in

[assembly/libraries/Hooks.ts:56](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Hooks.ts#L56)

---

### onHooksSet

▸ **onHooksSet**(`encoded`, `onHooksSetData`): `void`

Calls the onHooksSet hook on the hooks contract if the hooks address is set.

#### Parameters

| Name             | Type                                            |
| :--------------- | :---------------------------------------------- |
| `encoded`        | [`HooksParameters`](../structs/HooksParameters) |
| `onHooksSetData` | `StaticArray`<`u8`\>                            |

#### Returns

`void`

#### Defined in

[assembly/libraries/Hooks.ts:72](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Hooks.ts#L72)

---

### setHooks

▸ **setHooks**(`encoded`, `newHooks`): [`HooksParameters`](../structs/HooksParameters)

Returns a new encoded parameter with the hooks address replaced.

#### Parameters

| Name       | Type                                            |
| :--------- | :---------------------------------------------- |
| `encoded`  | [`HooksParameters`](../structs/HooksParameters) |
| `newHooks` | `Address`                                       |

#### Returns

[`HooksParameters`](../structs/HooksParameters)

#### Defined in

[assembly/libraries/Hooks.ts:43](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/Hooks.ts#L43)
