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
| `V` | The generic type parameter `V` can be any [valid AssemblyScript type](https://docs.assemblyscript.org/basics/types). MISC: Original code from Near (https://github.com/near/near-sdk-as/blob/master/sdk-core/assembly/collections/persistentMap.ts) |

## Hierarchy

- **`PersistentMap`**

  ↳ [`Oracle`](../structs/Oracle.md)

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

• **new PersistentMap**<`K`, `V`\>(`prefix`): [`PersistentMap`](PersistentMap.md)<`K`, `V`\>

Creates or restores a persistent map with a given storage prefix.
Always use a unique storage prefix for different collections.

Example

```ts
let map = new PersistentMap<string, string>("m") // note the prefix must be unique (per MASSA account)
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

#### Returns

[`PersistentMap`](PersistentMap.md)<`K`, `V`\>

#### Defined in

[assembly/libraries/PersistentMap.ts:65](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/libraries/PersistentMap.ts#L65)

## Properties

### \_elementPrefix

• `Private` **\_elementPrefix**: `string`

#### Defined in

[assembly/libraries/PersistentMap.ts:51](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/libraries/PersistentMap.ts#L51)

___

### \_size

• `Private` **\_size**: `usize`

#### Defined in

[assembly/libraries/PersistentMap.ts:52](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/libraries/PersistentMap.ts#L52)

## Methods

### \_decreaseSize

▸ **_decreaseSize**(): `void`

Decreases the internal map size counter

#### Returns

`void`

#### Defined in

[assembly/libraries/PersistentMap.ts:144](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/libraries/PersistentMap.ts#L144)

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

[assembly/libraries/PersistentMap.ts:135](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/libraries/PersistentMap.ts#L135)

___

### \_key

▸ **_key**(`key`): `StaticArray`<`u8`\>

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `key` | `K` | Search key. |

#### Returns

`StaticArray`<`u8`\>

An internal string key for a given key of type K.

#### Defined in

[assembly/libraries/PersistentMap.ts:74](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/libraries/PersistentMap.ts#L74)

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
| `key` | `K` | Key to remove. |

#### Returns

`void`

#### Defined in

[assembly/libraries/PersistentMap.ts:126](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/libraries/PersistentMap.ts#L126)

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

[assembly/libraries/PersistentMap.ts:168](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/libraries/PersistentMap.ts#L168)

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

[assembly/libraries/PersistentMap.ts:230](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/libraries/PersistentMap.ts#L230)

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

#### Defined in

[assembly/libraries/PersistentMap.ts:109](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/libraries/PersistentMap.ts#L109)
