# TreeHelper

## Table of contents

### Constructors

- [constructor](TreeHelper.md#constructor)

### Methods

- [\_getBottomId](TreeHelper.md#_getbottomid)
- [\_getIdsFromAbove](TreeHelper.md#_getidsfromabove)
- [addToTree](TreeHelper.md#addtotree)
- [findFirstBin](TreeHelper.md#findfirstbin)
- [level0](TreeHelper.md#level0)
- [level1](TreeHelper.md#level1)
- [level2](TreeHelper.md#level2)
- [removeFromTree](TreeHelper.md#removefromtree)
- [setLevel0](TreeHelper.md#setlevel0)
- [setLevel1](TreeHelper.md#setlevel1)
- [setLevel2](TreeHelper.md#setlevel2)

## Constructors

### constructor

• **new TreeHelper**(): [`TreeHelper`](TreeHelper.md)

#### Returns

[`TreeHelper`](TreeHelper.md)

## Methods

### \_getBottomId

▸ **_getBottomId**(`_branchId`, `_leafId`): `u32`

Private pure function to return the bottom id

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `_branchId` | `u32` | The branch id |
| `_leafId` | `u32` | The leaf id |

#### Returns

`u32`

The bottom branchId

#### Defined in

[assembly/libraries/TreeHelper.ts:29](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/libraries/TreeHelper.ts#L29)

___

### \_getIdsFromAbove

▸ **_getIdsFromAbove**(`_id`): `GetIdsFromAboveReturn`

Private pure function to return the ids from above

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `_id` | `u32` | The current id |

#### Returns

`GetIdsFromAboveReturn`

The branch id from above

The leaf id from above

#### Defined in

[assembly/libraries/TreeHelper.ts:19](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/libraries/TreeHelper.ts#L19)

___

### addToTree

▸ **addToTree**(`_id`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `_id` | `u64` |

#### Returns

`void`

#### Defined in

[assembly/libraries/TreeHelper.ts:35](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/libraries/TreeHelper.ts#L35)

___

### findFirstBin

▸ **findFirstBin**(`_binId`, `_rightSide`): `Result`<`u32`\>

Returns the first id that is non zero, corresponding to a bin with liquidity in it

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `_binId` | `u32` | the binId to start searching |
| `_rightSide` | `bool` | Whether we're searching in the right side of the tree (true) or the left side (false) |

#### Returns

`Result`<`u32`\>

The closest non zero bit on the right (or left) side of the tree

#### Defined in

[assembly/libraries/TreeHelper.ts:85](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/libraries/TreeHelper.ts#L85)

___

### level0

▸ **level0**(): `u256`

#### Returns

`u256`

#### Defined in

[assembly/libraries/TreeHelper.ts:145](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/libraries/TreeHelper.ts#L145)

___

### level1

▸ **level1**(`index`): `u256`

#### Parameters

| Name | Type |
| :------ | :------ |
| `index` | `i32` |

#### Returns

`u256`

#### Defined in

[assembly/libraries/TreeHelper.ts:148](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/libraries/TreeHelper.ts#L148)

___

### level2

▸ **level2**(`index`): `u256`

#### Parameters

| Name | Type |
| :------ | :------ |
| `index` | `i32` |

#### Returns

`u256`

#### Defined in

[assembly/libraries/TreeHelper.ts:151](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/libraries/TreeHelper.ts#L151)

___

### removeFromTree

▸ **removeFromTree**(`_id`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `_id` | `u64` |

#### Returns

`void`

#### Defined in

[assembly/libraries/TreeHelper.ts:53](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/libraries/TreeHelper.ts#L53)

___

### setLevel0

▸ **setLevel0**(`value`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `value` | `u256` |

#### Returns

`void`

#### Defined in

[assembly/libraries/TreeHelper.ts:154](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/libraries/TreeHelper.ts#L154)

___

### setLevel1

▸ **setLevel1**(`index`, `value`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `index` | `i32` |
| `value` | `u256` |

#### Returns

`void`

#### Defined in

[assembly/libraries/TreeHelper.ts:157](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/libraries/TreeHelper.ts#L157)

___

### setLevel2

▸ **setLevel2**(`index`, `value`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `index` | `i32` |
| `value` | `u256` |

#### Returns

`void`

#### Defined in

[assembly/libraries/TreeHelper.ts:160](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/libraries/TreeHelper.ts#L160)
