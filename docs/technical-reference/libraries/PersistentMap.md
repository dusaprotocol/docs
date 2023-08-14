# PersistentMap

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

## Type parameters

| Name | Description |
| :------ | :------ |
| `K` | The generic type parameter `K` can be any [valid AssemblyScript type](https://docs.assemblyscript.org/basics/types). |
| `V` | The generic type parameter `V` can be any [valid AssemblyScript type](https://docs.assemblyscript.org/basics/types). |

## Table of contents

### Constructors

- [constructor](PersistentMap.md#constructor)

### Properties

- [\_elementPrefix](PersistentMap.md#_elementprefix)
- [\_size](PersistentMap.md#_size)

### Methods

- [\_decreaseSize](PersistentMap.md#_decreasesize)
- [\_increaseSize](PersistentMap.md#_increasesize)
- [\_key](PersistentMap.md#_key)
- [contains](PersistentMap.md#contains)
- [delete](PersistentMap.md#delete)
- [get](PersistentMap.md#get)
- [getSome](PersistentMap.md#getsome)
- [set](PersistentMap.md#set)
- [size](PersistentMap.md#size)

## Constructors

### constructor

• **new PersistentMap**<`K`, `V`\>(`prefix`)

Creates or restores a persistent map with a given storage prefix.
Always use a unique storage prefix for different collections.

Example

```ts
let map = new PersistentMap<string, string>("m") // note the prefix must be unique (per NEAR account)
```

#### Type parameters

| Name |
| :------ |
| `K` |
| `V` |

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `prefix` | `string` | A prefix to use for every key of this map. |

#### Defined in

[assembly/libraries/PersistentMap.ts:59](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/libraries/PersistentMap.ts#L59)

## Properties

### \_elementPrefix

• `Private` **\_elementPrefix**: `string`

#### Defined in

[assembly/libraries/PersistentMap.ts:45](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/libraries/PersistentMap.ts#L45)

___

### \_size

• `Private` **\_size**: `usize`

#### Defined in

[assembly/libraries/PersistentMap.ts:46](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/libraries/PersistentMap.ts#L46)

## Methods

### \_decreaseSize

▸ **_decreaseSize**(): `void`

Decreases the internal map size counter

#### Returns

`void`

#### Defined in

[assembly/libraries/PersistentMap.ts:138](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/libraries/PersistentMap.ts#L138)

___

### \_increaseSize

▸ **_increaseSize**(`key`): `void`

Increases the internal map size counter

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `key` | `K` | Key to remove. |

#### Returns

`void`

#### Defined in

[assembly/libraries/PersistentMap.ts:129](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/libraries/PersistentMap.ts#L129)

___

### \_key

▸ `Private` **_key**(`key`): `StaticArray`<`u8`\>

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `key` | `K` | Search key. |

#### Returns

`StaticArray`<`u8`\>

An internal string key for a given key of type K.

#### Defined in

[assembly/libraries/PersistentMap.ts:68](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/libraries/PersistentMap.ts#L68)

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
| `key` | `K` | Key to check. |

#### Returns

`bool`

True if the given key present in the map.

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
| `key` | `K` | Key to remove. |

#### Returns

`void`

#### Defined in

[assembly/libraries/PersistentMap.ts:120](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/libraries/PersistentMap.ts#L120)

___

### get

▸ **get**(`key`, `defaultValue`): `V`

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
| `key` | `K` | Key of the element. |
| `defaultValue` | `V` | The default value if the key is not present. |

#### Returns

`V`

Value for the given key or the default value.

#### Defined in

[assembly/libraries/PersistentMap.ts:162](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/libraries/PersistentMap.ts#L162)

___

### getSome

▸ **getSome**(`key`, `msg?`): `V`

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
| `key` | `K` | `undefined` | Key of the element. |
| `msg` | `string` | `'key not found'` | - |

#### Returns

`V`

Value for the given key or the default value.

#### Defined in

[assembly/libraries/PersistentMap.ts:218](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/libraries/PersistentMap.ts#L218)

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
| `key` | `K` | Key of the element. |
| `value` | `V` | The new value of the element. |

#### Returns

`void`

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

#### Defined in

[assembly/libraries/PersistentMap.ts:103](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/libraries/PersistentMap.ts#L103)
