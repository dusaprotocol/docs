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

• **new TreeHelper**()

## Methods

### \_getBottomId

▸ `Static` **_getBottomId**(`_branchId`, `_leafId`): `u32`

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

[assembly/libraries/TreeHelper.ts:27](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/libraries/TreeHelper.ts#L27)

___

### \_getIdsFromAbove

▸ `Static` **_getIdsFromAbove**(`_id`): `GetIdsFromAboveReturn`

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

[assembly/libraries/TreeHelper.ts:17](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/libraries/TreeHelper.ts#L17)

___

### addToTree

▸ `Static` **addToTree**(`_id`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `_id` | `u64` |

#### Returns

`void`

#### Defined in

[assembly/libraries/TreeHelper.ts:33](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/libraries/TreeHelper.ts#L33)

___

### findFirstBin

▸ `Static` **findFirstBin**(`_binId`, `_rightSide`): `u32`

Returns the first id that is non zero, corresponding to a bin with liquidity in it

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `_binId` | `u32` | the binId to start searching |
| `_rightSide` | `bool` | Whether we're searching in the right side of the tree (true) or the left side (false) |

#### Returns

`u32`

The closest non zero bit

#### Defined in

[assembly/libraries/TreeHelper.ts:81](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/libraries/TreeHelper.ts#L81)

___

### level0

▸ `Static` **level0**(): `u128`

#### Returns

`u128`

#### Defined in

[assembly/libraries/TreeHelper.ts:137](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/libraries/TreeHelper.ts#L137)

___

### level1

▸ `Static` **level1**(`index`): `u128`

#### Parameters

| Name | Type |
| :------ | :------ |
| `index` | `i32` |

#### Returns

`u128`

#### Defined in

[assembly/libraries/TreeHelper.ts:141](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/libraries/TreeHelper.ts#L141)

___

### level2

▸ `Static` **level2**(`index`): `u128`

#### Parameters

| Name | Type |
| :------ | :------ |
| `index` | `i32` |

#### Returns

`u128`

#### Defined in

[assembly/libraries/TreeHelper.ts:145](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/libraries/TreeHelper.ts#L145)

___

### removeFromTree

▸ `Static` **removeFromTree**(`_id`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `_id` | `u64` |

#### Returns

`void`

#### Defined in

[assembly/libraries/TreeHelper.ts:50](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/libraries/TreeHelper.ts#L50)

___

### setLevel0

▸ `Static` **setLevel0**(`value`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `value` | `u128` |

#### Returns

`void`

#### Defined in

[assembly/libraries/TreeHelper.ts:149](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/libraries/TreeHelper.ts#L149)

___

### setLevel1

▸ `Static` **setLevel1**(`index`, `value`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `index` | `i32` |
| `value` | `u128` |

#### Returns

`void`

#### Defined in

[assembly/libraries/TreeHelper.ts:152](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/libraries/TreeHelper.ts#L152)

___

### setLevel2

▸ `Static` **setLevel2**(`index`, `value`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `index` | `i32` |
| `value` | `u128` |

#### Returns

`void`

#### Defined in

[assembly/libraries/TreeHelper.ts:155](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/libraries/TreeHelper.ts#L155)
