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

| Name         | Type   | Description                                                                           |
| :----------- | :----- | :------------------------------------------------------------------------------------ |
| `_integer`   | `u256` | The integer as a u256                                                                 |
| `_bit`       | `u8`   | The bit index                                                                         |
| `_rightSide` | `bool` | Whether we're searching in the right side of the tree (true) or the left side (false) |

#### Returns

`Result`<`u8`\>

The index of the closest non-zero bit.

#### Defined in

[assembly/libraries/BitMath.ts:35](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/BitMath.ts#L35)

---

### closestBitLeft

▸ **closestBitLeft**(`x`, `bit`): `Result`<`u8`\>

Returns the index of the closest bit on the left of x that is non null

#### Parameters

| Name  | Type   | Description                                |
| :---- | :----- | :----------------------------------------- |
| `x`   | `u256` | The value as a u256                        |
| `bit` | `i32`  | The index of the bit to start searching at |

#### Returns

`Result`<`u8`\>

The index of the closest non null bit on the left of x.

#### Defined in

[assembly/libraries/BitMath.ts:62](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/BitMath.ts#L62)

---

### closestBitRight

▸ **closestBitRight**(`x`, `bit`): `Result`<`u8`\>

Returns the index of the closest bit on the right of x that is non null

#### Parameters

| Name  | Type   | Description                                |
| :---- | :----- | :----------------------------------------- |
| `x`   | `u256` | The value as a u256                        |
| `bit` | `i32`  | The index of the bit to start searching at |

#### Returns

`Result`<`u8`\>

The index of the closest non null bit on the right of x.

#### Defined in

[assembly/libraries/BitMath.ts:47](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/BitMath.ts#L47)

---

### leastSignificantBit

▸ **leastSignificantBit**(`x`): `u8`

Returns the index of the least significant set bit

#### Parameters

| Name | Type   |
| :--- | :----- |
| `x`  | `u256` |

#### Returns

`u8`

The index of the least significant bit of x

#### Defined in

[assembly/libraries/BitMath.ts:81](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/BitMath.ts#L81)

---

### mostSignificantBit

▸ **mostSignificantBit**(`x`): `u8`

Returns the index of the most significant set bit

#### Parameters

| Name | Type   |
| :--- | :----- |
| `x`  | `u256` |

#### Returns

`u8`

The index of the most significant bit of x

#### Defined in

[assembly/libraries/BitMath.ts:74](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/BitMath.ts#L74)

---

### significantBit

▸ **significantBit**(`x`, `most`): `u8`

Returns the most (true) or least (false) significant bit index

#### Parameters

| Name   | Type   |
| :----- | :----- |
| `x`    | `u256` |
| `most` | `bool` |

#### Returns

`u8`

The index of the most (or least) significant bit

#### Defined in

[assembly/libraries/BitMath.ts:90](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/BitMath.ts#L90)
