TreeHelper

# Class: TreeHelper

## Table of contents

### Constructors

-   [constructor](TreeHelper.md#constructor)

### Methods

-   [\_getBottomId](TreeHelper.md#_getbottomid)
-   [\_getIdsFromAbove](TreeHelper.md#_getidsfromabove)
-   [addToTree](TreeHelper.md#addtotree)
-   [findFirstBin](TreeHelper.md#findfirstbin)
-   [removeFromTree](TreeHelper.md#removefromtree)

## Constructors

### constructor

• **new TreeHelper**()

## Methods

### \_getBottomId

▸ `Static` **\_getBottomId**(`_branchId`, `_leafId`): `u32`

Private pure function to return the bottom id

#### Parameters

| Name        | Type  | Description   |
| :---------- | :---- | :------------ |
| `_branchId` | `u32` | The branch id |
| `_leafId`   | `u32` | The leaf id   |

#### Returns

`u32`

The bottom branchId

#### Defined in

[assembly/libraries/TreeHelper.ts:30](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/libraries/TreeHelper.ts#L30)

---

### \_getIdsFromAbove

▸ `Static` **\_getIdsFromAbove**(`_id`): [`GetIdsFromAboveReturn`](GetIdsFromAboveReturn.md)

Private pure function to return the ids from above

#### Parameters

| Name  | Type  | Description    |
| :---- | :---- | :------------- |
| `_id` | `u32` | The current id |

#### Returns

[`GetIdsFromAboveReturn`](GetIdsFromAboveReturn.md)

The branch id from above

The leaf id from above

#### Defined in

[assembly/libraries/TreeHelper.ts:20](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/libraries/TreeHelper.ts#L20)

---

### addToTree

▸ `Static` **addToTree**(`_id`): `void`

#### Parameters

| Name  | Type  |
| :---- | :---- |
| `_id` | `u64` |

#### Returns

`void`

#### Defined in

[assembly/libraries/TreeHelper.ts:36](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/libraries/TreeHelper.ts#L36)

---

### findFirstBin

▸ `Static` **findFirstBin**(`_binId`, `_rightSide`): `u32`

Returns the first id that is non zero, corresponding to a bin with liquidity in it

#### Parameters

| Name         | Type   | Description                                                                           |
| :----------- | :----- | :------------------------------------------------------------------------------------ |
| `_binId`     | `u32`  | the binId to start searching                                                          |
| `_rightSide` | `bool` | Whether we're searching in the right side of the tree (true) or the left side (false) |

#### Returns

`u32`

The closest non zero bit

#### Defined in

[assembly/libraries/TreeHelper.ts:78](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/libraries/TreeHelper.ts#L78)

---

### removeFromTree

▸ `Static` **removeFromTree**(`_id`): `void`

#### Parameters

| Name  | Type  |
| :---- | :---- |
| `_id` | `u64` |

#### Returns

`void`

#### Defined in

[assembly/libraries/TreeHelper.ts:53](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/libraries/TreeHelper.ts#L53)
