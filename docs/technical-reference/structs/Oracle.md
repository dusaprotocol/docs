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

- [`PersistentMap`](PersistentMap.md)<`u64`, [`Sample`](Sample.md)\>

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

• **new Oracle**(`prefix`)

Creates or restores a persistent map with a given storage prefix.
Always use a unique storage prefix for different collections.

Example

```ts
let map = new PersistentMap<string, string>("m") // note the prefix must be unique (per NEAR account)
```

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `prefix` | `string` | A prefix to use for every key of this map. |

#### Inherited from

[PersistentMap](PersistentMap.md).[constructor](PersistentMap.md#constructor)

#### Defined in

[assembly/libraries/PersistentMap.ts:59](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/libraries/PersistentMap.ts#L59)

## Methods

### \_decreaseSize

▸ **_decreaseSize**(): `void`

Decreases the internal map size counter

#### Returns

`void`

#### Inherited from

[PersistentMap](PersistentMap.md).[_decreaseSize](PersistentMap.md#_decreasesize)

#### Defined in

[assembly/libraries/PersistentMap.ts:138](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/libraries/PersistentMap.ts#L138)

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

[assembly/libraries/PersistentMap.ts:129](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/libraries/PersistentMap.ts#L129)

___

### before

▸ **before**(`x`, `n`): `u64`

#### Parameters

| Name | Type |
| :------ | :------ |
| `x` | `u64` |
| `n` | `u64` |

#### Returns

`u64`

#### Defined in

[assembly/structs/Oracle.ts:163](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/structs/Oracle.ts#L163)

___

### binarySearch

▸ **binarySearch**(`_index`, `_activeSize`, `_lookUpTimestamp`): [`Sample`](Sample.md)[]

#### Parameters

| Name | Type |
| :------ | :------ |
| `_index` | `u64` |
| `_activeSize` | `u64` |
| `_lookUpTimestamp` | `u64` |

#### Returns

[`Sample`](Sample.md)[]

#### Defined in

[assembly/structs/Oracle.ts:132](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/structs/Oracle.ts#L132)

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

[assembly/libraries/PersistentMap.ts:88](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/libraries/PersistentMap.ts#L88)

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

[assembly/libraries/PersistentMap.ts:120](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/libraries/PersistentMap.ts#L120)

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

[assembly/libraries/PersistentMap.ts:162](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/libraries/PersistentMap.ts#L162)

___

### getSampleAt

▸ **getSampleAt**(`_activeSize`, `_activeId`, `_lookUpTimestamp`): `GetSampleAtReturn`

#### Parameters

| Name | Type |
| :------ | :------ |
| `_activeSize` | `u64` |
| `_activeId` | `u64` |
| `_lookUpTimestamp` | `u64` |

#### Returns

`GetSampleAtReturn`

#### Defined in

[assembly/structs/Oracle.ts:12](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/structs/Oracle.ts#L12)

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

[assembly/libraries/PersistentMap.ts:218](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/libraries/PersistentMap.ts#L218)

___

### initialize

▸ **initialize**(`_id`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `_id` | `u64` |

#### Returns

`void`

#### Defined in

[assembly/structs/Oracle.ts:128](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/structs/Oracle.ts#L128)

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

[assembly/libraries/PersistentMap.ts:257](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/libraries/PersistentMap.ts#L257)

___

### size

▸ **size**(): `usize`

Returns the map size

**`Example`**

```ts
let map = new PersistentMap<string, string> ("m")

map.size()
```

#### Returns

`usize`

the map size

#### Inherited from

[PersistentMap](PersistentMap.md).[size](PersistentMap.md#size)

#### Defined in

[assembly/libraries/PersistentMap.ts:103](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/libraries/PersistentMap.ts#L103)

___

### update

▸ **update**(`_size`, `_sampleLifetime`, `_lastTimestamp`, `_lastIndex`, `_activeId`, `_volatilityAccumulated`, `_binCrossed`): `u64`

#### Parameters

| Name | Type |
| :------ | :------ |
| `_size` | `u64` |
| `_sampleLifetime` | `u64` |
| `_lastTimestamp` | `u64` |
| `_lastIndex` | `u64` |
| `_activeId` | `u64` |
| `_volatilityAccumulated` | `u64` |
| `_binCrossed` | `u64` |

#### Returns

`u64`

#### Defined in

[assembly/structs/Oracle.ts:103](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/structs/Oracle.ts#L103)
