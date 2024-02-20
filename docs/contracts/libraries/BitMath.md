# BitMath

## Table of contents

### Constructors

- [constructor](BitMath.md#constructor)

### Methods

- [closestBit](BitMath.md#closestbit)
- [closestBitLeft](BitMath.md#closestbitleft)
- [closestBitRight](BitMath.md#closestbitright)
- [leastSignificantBit](BitMath.md#leastsignificantbit)
- [mostSignificantBit](BitMath.md#mostsignificantbit)
- [significantBit](BitMath.md#significantbit)

## Constructors

### constructor

• **new BitMath**(): [`BitMath`](BitMath.md)

#### Returns

[`BitMath`](BitMath.md)

## Methods

### closestBit

▸ **closestBit**(`_integer`, `_bit`, `_rightSide`): `Result`<`u8`\>

Returns the closest non-zero bit of `integer` to the right (of left) of the `bit` bits that is not `bit`

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `_integer` | `u256` | The integer as a u256 |
| `_bit` | `u8` | The bit index |
| `_rightSide` | `bool` | Whether we're searching in the right side of the tree (true) or the left side (false) |

#### Returns

`Result`<`u8`\>

The index of the closest non-zero bit.

#### Defined in

[assembly/libraries/BitMath.ts:14](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/libraries/BitMath.ts#L14)

___

### closestBitLeft

▸ **closestBitLeft**(`x`, `bit`): `Result`<`u8`\>

Returns the index of the closest bit on the left of x that is non null

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `x` | `u256` | The value as a u256 |
| `bit` | `i32` | The index of the bit to start searching at |

#### Returns

`Result`<`u8`\>

The index of the closest non null bit on the left of x.

#### Defined in

[assembly/libraries/BitMath.ts:41](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/libraries/BitMath.ts#L41)

___

### closestBitRight

▸ **closestBitRight**(`x`, `bit`): `Result`<`u8`\>

Returns the index of the closest bit on the right of x that is non null

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `x` | `u256` | The value as a u256 |
| `bit` | `i32` | The index of the bit to start searching at |

#### Returns

`Result`<`u8`\>

The index of the closest non null bit on the right of x.

#### Defined in

[assembly/libraries/BitMath.ts:26](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/libraries/BitMath.ts#L26)

___

### leastSignificantBit

▸ **leastSignificantBit**(`x`): `u8`

Returns the index of the least significant bit of x

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `x` | `u256` | The value as a u256 |

#### Returns

`u8`

The index of the least significant bit of x

#### Defined in

[assembly/libraries/BitMath.ts:96](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/libraries/BitMath.ts#L96)

___

### mostSignificantBit

▸ **mostSignificantBit**(`x`): `u8`

Returns the index of the most significant bit of x

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `x` | `u256` | The value as a u256 |

#### Returns

`u8`

The index of the most significant bit of x

#### Defined in

[assembly/libraries/BitMath.ts:54](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/libraries/BitMath.ts#L54)

___

### significantBit

▸ **significantBit**(`_integer`, `_isMostSignificant`): `u8`

Returns the most (or least) significant bit of `_integer`

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `_integer` | `u256` | The integer |
| `_isMostSignificant` | `bool` | Whether we want the most (true) or the least (false) significant bit |

#### Returns

`u8`

The index of the most (or least) significant bit

#### Defined in

[assembly/libraries/BitMath.ts:139](https://github.com/dusaprotocol/v2.1/blob/34784b1/assembly/libraries/BitMath.ts#L139)
