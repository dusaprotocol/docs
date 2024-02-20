# Oracle

This class is one of several convenience collections built on top of the `Storage` class
It implements a map -- a persistent unordered map.

To create a map

```ts
let map = new PersistentMap<string, string>("m")  // choose a unique prefix per account
```

To use the map

```ts
map.set(key, value)
map.get(key)
```

IMPORTANT NOTES:

(1) The Map doesn't store keys, so if you need to retrieve them, include keys in the values.

(2) Since all data stored on the blockchain is kept in a single key-value store under the contract account,
you must always use a *unique storage prefix* for different collections to avoid data collision.

## Hierarchy

- [`PersistentMap`](../libraries/PersistentMap.md)<`u64`, [`Sample`](Sample.md)\>

  ↳ **`Oracle`**

## Table of contents

### Constructors

- [constructor](Oracle.md#constructor)

### Methods

- [\_decreaseSize](Oracle.md#_decreasesize)
- [\_increaseSize](Oracle.md#_increasesize)
- [before](Oracle.md#before)
- [binarySearch](Oracle.md#binarysearch)
- [contains](Oracle.md#contains)
- [delete](Oracle.md#delete)
- [get](Oracle.md#get)
- [getSampleAt](Oracle.md#getsampleat)
- [getSome](Oracle.md#getsome)
- [initialize](Oracle.md#initialize)
- [set](Oracle.md#set)
- [size](Oracle.md#size)
- [update](Oracle.md#update)

## Constructors

### constructor

• **new Oracle**(`prefix`): [`Oracle`](Oracle.md)

Creates or restores a persistent map with a given storage prefix.
Always use a unique storage prefix for different collections.

Example

```ts
let map = new PersistentMap<string, string>("m") // note the prefix must be unique (per MASSA account)
```

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `prefix` | `string` | A prefix to use for every key of this map. |

#### Returns

[`Oracle`](Oracle.md)

#### Inherited from

[PersistentMap](PersistentMap.md).[constructor](PersistentMap.md#constructor)

#### Defined in

[assembly/libraries/PersistentMap.ts:65](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/libraries/PersistentMap.ts#L65)

## Methods

### \_decreaseSize

▸ **_decreaseSize**(): `void`

Decreases the internal map size counter

#### Returns

`void`

#### Inherited from

[PersistentMap](PersistentMap.md).[_decreaseSize](PersistentMap.md#_decreasesize)

#### Defined in

[assembly/libraries/PersistentMap.ts:144](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/libraries/PersistentMap.ts#L144)

___

### \_increaseSize

▸ **_increaseSize**(`key`): `void`

Increases the internal map size counter

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `key` | `u64` | Key to remove. |

#### Returns

`void`

#### Inherited from

[PersistentMap](PersistentMap.md).[_increaseSize](PersistentMap.md#_increasesize)

#### Defined in

[assembly/libraries/PersistentMap.ts:135](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/libraries/PersistentMap.ts#L135)

___

### before

▸ **before**(`x`, `n`): `u64`

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `x` | `u64` | The value |
| `n` | `u64` | The modulo value |

#### Returns

`u64`

result The result

**`Notice`**

Internal function to do positive (x - 1) % n

**`Dev`**

This function is used to get the previous index of the oracle

#### Defined in

[assembly/structs/Oracle.ts:207](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/structs/Oracle.ts#L207)

___

### binarySearch

▸ **binarySearch**(`_index`, `_activeSize`, `_lookUpTimestamp`): [`Sample`](Sample.md)[]

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `_index` | `u64` | The current index of the oracle |
| `_activeSize` | `u64` | The size of the oracle (without empty data) |
| `_lookUpTimestamp` | `u64` | The looked up timestamp |

#### Returns

[`Sample`](Sample.md)[]

Sample[] The last sample with a timestamp lower than the lookUpTimestamp and the first sample with a timestamp greater than the lookUpTimestamp

**`Notice`**

Binary search on oracle samples and return the 2 samples (as bytes32) that surrounds the `lookUpTimestamp`

**`Dev`**

The oracle needs to be in increasing order `{_index + 1, _index + 2 ..., _index + _activeSize} % _activeSize`.
The sample that aren't initialized yet will be skipped as _activeSize only contains the samples that are initialized.
This function works only if `timestamp(_oracle[_index + 1 % _activeSize] <= _lookUpTimestamp <= timestamp(_oracle[_index]`.
The edge cases needs to be handled before

#### Defined in

[assembly/structs/Oracle.ts:169](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/structs/Oracle.ts#L169)

___

### contains

▸ **contains**(`key`): `bool`

Checks whether the map contains a given key

```ts
let map = new PersistentMap<string, string>("m")

map.contains("hello")      // false
map.set("hello", "world")
map.contains("hello")      // true
```

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `key` | `u64` | Key to check. |

#### Returns

`bool`

True if the given key present in the map.

#### Inherited from

[PersistentMap](PersistentMap.md).[contains](PersistentMap.md#contains)

#### Defined in

[assembly/libraries/PersistentMap.ts:94](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/libraries/PersistentMap.ts#L94)

___

### delete

▸ **delete**(`key`): `void`

Removes the given key and related value from the map

```ts
let map = new PersistentMap<string, string>("m")

map.set("hello", "world")
map.delete("hello")
```

Removes value and the key from the map.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `key` | `u64` | Key to remove. |

#### Returns

`void`

#### Inherited from

[PersistentMap](PersistentMap.md).[delete](PersistentMap.md#delete)

#### Defined in

[assembly/libraries/PersistentMap.ts:126](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/libraries/PersistentMap.ts#L126)

___

### get

▸ **get**(`key`, `defaultValue`): [`Sample`](Sample.md)

Retrieves the related value for a given key, or uses the `defaultValue` if not key is found

```ts
let map = new PersistentMap<string, string>("m")

map.set("hello", "world")
let found = map.get("hello")
let notFound = map.get("goodbye", "cruel world")

assert(found == "world")
assert(notFound == "cruel world")
```

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `key` | `u64` | Key of the element. |
| `defaultValue` | [`Sample`](Sample.md) | The default value if the key is not present. |

#### Returns

[`Sample`](Sample.md)

Value for the given key or the default value.

#### Inherited from

[PersistentMap](PersistentMap.md).[get](PersistentMap.md#get)

#### Defined in

[assembly/libraries/PersistentMap.ts:168](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/libraries/PersistentMap.ts#L168)

___

### getSampleAt

▸ **getSampleAt**(`_activeSize`, `_activeId`, `_lookUpTimestamp`): `GetSampleAtReturn`

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `_activeSize` | `u64` | The size of the oracle (without empty data) |
| `_activeId` | `u64` | The active index of the oracle |
| `_lookUpTimestamp` | `u64` | The looked up date |

#### Returns

`GetSampleAtReturn`

GetSampleAtReturn: timestamp, cumulativeId, cumulativeVolatilityAccumulated, cumulativeBinCrossed

**`Notice`**

View function to get the oracle's sample at `_ago` seconds

**`Dev`**

Return a linearized sample, the weighted average of 2 neighboring samples

#### Defined in

[assembly/structs/Oracle.ts:22](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/structs/Oracle.ts#L22)

___

### getSome

▸ **getSome**(`key`, `msg?`): [`Sample`](Sample.md)

Retrieves a related value for a given key or fails assertion with "key not found"

```ts
let map = new PersistentMap<string, string>("m")

map.set("hello", "world")
let result = map.getSome("hello")
// map.getSome("goodbye")  // will throw with failed assertion

assert(result == "world")
```

#### Parameters

| Name | Type | Default value | Description |
| :------ | :------ | :------ | :------ |
| `key` | `u64` | `undefined` | Key of the element. |
| `msg` | `string` | `'key not found'` | - |

#### Returns

[`Sample`](Sample.md)

Value for the given key or the default value.

#### Inherited from

[PersistentMap](PersistentMap.md).[getSome](PersistentMap.md#getsome)

#### Defined in

[assembly/libraries/PersistentMap.ts:230](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/libraries/PersistentMap.ts#L230)

___

### initialize

▸ **initialize**(`_id`): `void`

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `_id` | `u64` | The index to initialize |

#### Returns

`void`

**`Notice`**

Initialize the sample

#### Defined in

[assembly/structs/Oracle.ts:154](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/structs/Oracle.ts#L154)

___

### set

▸ **set**(`key`, `value`): `void`

```ts
let map = new PersistentMap<string, string>("m")

map.set("hello", "world")
```

Sets the new value for the given key.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `key` | `u64` | Key of the element. |
| `value` | [`Sample`](Sample.md) | The new value of the element. |

#### Returns

`void`

#### Inherited from

[PersistentMap](PersistentMap.md).[set](PersistentMap.md#set)

#### Defined in

[assembly/libraries/PersistentMap.ts:273](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/libraries/PersistentMap.ts#L273)

___

### size

▸ **size**(): `usize`

Returns the map size

#### Returns

`usize`

the map size

**`Example`**

```ts
let map = new PersistentMap<string, string> ("m")

map.size()
```

#### Inherited from

[PersistentMap](PersistentMap.md).[size](PersistentMap.md#size)

#### Defined in

[assembly/libraries/PersistentMap.ts:109](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/libraries/PersistentMap.ts#L109)

___

### update

▸ **update**(`_size`, `_sampleLifetime`, `_lastTimestamp`, `_lastIndex`, `_activeId`, `_volatilityAccumulated`, `_binCrossed`): `u64`

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `_size` | `u64` | The size of the oracle (last ids can be empty) |
| `_sampleLifetime` | `u64` | The lifetime of a sample, it accumulates information for up to this timestamp |
| `_lastTimestamp` | `u64` | The timestamp of the creation of the oracle's latest sample |
| `_lastIndex` | `u64` | The index of the oracle's latest sample |
| `_activeId` | `u64` | The active index of the pair during the latest swap |
| `_volatilityAccumulated` | `u64` | The volatility accumulated of the pair during the latest swap |
| `_binCrossed` | `u64` | The bin crossed during the latest swap |

#### Returns

`u64`

updatedIndex The oracle updated index, it is either the same as before, or the next one

**`Notice`**

Function to update a sample

#### Defined in

[assembly/structs/Oracle.ts:125](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/structs/Oracle.ts#L125)
