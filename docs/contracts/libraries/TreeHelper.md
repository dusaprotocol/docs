# TreeHelper

## Table of contents

### Constructors

- [constructor](TreeHelper.md#constructor)

### Methods

- [\_getBottomId](TreeHelper.md#_getbottomid)
- [\_getIdsFromAbove](TreeHelper.md#_getidsfromabove)
- [addToTree](TreeHelper.md#addtotree)
- [findFirstBin](TreeHelper.md#findfirstbin)
- [removeFromTree](TreeHelper.md#removefromtree)

## Constructors

### constructor

• **new TreeHelper**(): [`TreeHelper`](TreeHelper.md)

#### Returns

[`TreeHelper`](TreeHelper.md)

## Methods

### \_getBottomId

▸ **\_getBottomId**(`_branchId`, `_leafId`): `u32`

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

[assembly/libraries/TreeHelper.ts:33](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/TreeHelper.ts#L33)

---

### \_getIdsFromAbove

▸ **\_getIdsFromAbove**(`_id`): `GetIdsFromAboveReturn`

Private pure function to return the ids from above

#### Parameters

| Name  | Type  | Description    |
| :---- | :---- | :------------- |
| `_id` | `u32` | The current id |

#### Returns

`GetIdsFromAboveReturn`

The branch id from above

The leaf id from above

#### Defined in

[assembly/libraries/TreeHelper.ts:23](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/TreeHelper.ts#L23)

---

### addToTree

▸ **addToTree**(`_id`): `void`

#### Parameters

| Name  | Type  |
| :---- | :---- |
| `_id` | `u32` |

#### Returns

`void`

#### Defined in

[assembly/libraries/TreeHelper.ts:39](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/TreeHelper.ts#L39)

---

### findFirstBin

▸ **findFirstBin**(`_binId`, `_rightSide`): `Result`<`u32`\>

Returns the first id that is non zero, corresponding to a bin with liquidity in it

#### Parameters

| Name         | Type   | Description                                                                           |
| :----------- | :----- | :------------------------------------------------------------------------------------ |
| `_binId`     | `u32`  | the binId to start searching                                                          |
| `_rightSide` | `bool` | Whether we're searching in the right side of the tree (true) or the left side (false) |

#### Returns

`Result`<`u32`\>

The closest non zero bit on the right (or left) side of the tree

#### Defined in

[assembly/libraries/TreeHelper.ts:99](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/TreeHelper.ts#L99)

---

### removeFromTree

▸ **removeFromTree**(`_id`): `void`

#### Parameters

| Name  | Type  |
| :---- | :---- |
| `_id` | `u32` |

#### Returns

`void`

#### Defined in

[assembly/libraries/TreeHelper.ts:60](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/TreeHelper.ts#L60)
