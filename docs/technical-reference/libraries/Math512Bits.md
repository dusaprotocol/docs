# Math512Bits

## Table of contents

### Constructors

- [constructor](Math512Bits.md#constructor)

### Methods

- [mulDivRoundDown](Math512Bits.md#muldivrounddown)
- [mulShiftRoundDown](Math512Bits.md#mulshiftrounddown)
- [mulShiftRoundUp](Math512Bits.md#mulshiftroundup)
- [shiftDivRoundDown](Math512Bits.md#shiftdivrounddown)
- [shiftDivRoundUp](Math512Bits.md#shiftdivroundup)

## Constructors

### constructor

• **new Math512Bits**()

## Methods

### mulDivRoundDown

▸ `Static` **mulDivRoundDown**(`x`, `y`, `denominator`): `u64`

Calculates floor(x*y÷denominator) with full precision
The result will be rounded down

Credit to Remco Bloemen under MIT license https://xn--2-umb.com/21/muldiv

Requirements:
- The denominator cannot be zero
- The result must fit within u64

Caveats:
- This function does not work with fixed-point numbers

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `x` | `u128` | The multiplicand as an u64 |
| `y` | `u128` | The multiplier as an u64 |
| `denominator` | `u128` | The divisor as an u64 |

#### Returns

`u64`

The result as an u64

#### Defined in

[assembly/libraries/Math512Bits.ts:29](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/libraries/Math512Bits.ts#L29)

___

### mulShiftRoundDown

▸ `Static` **mulShiftRoundDown**(`x`, `y`, `offset`): `u64`

Calculates x * y >> offset with full precision
The result will be rounded down

Credit to Remco Bloemen under MIT license https://xn--2-umb.com/21/muldiv

Requirements:
- The offset needs to be strictly lower than 128
- The result must fit within u64

Caveats:
- This function does not work with fixed-point numbers

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `x` | `u128` | The multiplicand as an u64 |
| `y` | `u128` | The multiplier as an u64 |
| `offset` | `i32` | The offset, can't be greater than 128 |

#### Returns

`u64`

The result as an u64

#### Defined in

[assembly/libraries/Math512Bits.ts:86](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/libraries/Math512Bits.ts#L86)

___

### mulShiftRoundUp

▸ `Static` **mulShiftRoundUp**(`x`, `y`, `offset`): `u64`

Calculates x * y >> offset with full precision
The result will be rounded up

Credit to Remco Bloemen under MIT license https://xn--2-umb.com/21/muldiv

Requirements:
- The offset needs to be strictly lower than 128
- The result must fit within u64

Caveats:
- This function does not work with fixed-point numbers

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `x` | `u128` | The multiplicand as an u64 |
| `y` | `u128` | The multiplier as an u64 |
| `offset` | `i32` | The offset, can't be greater than 128 |

#### Returns

`u64`

The result as an u64

#### Defined in

[assembly/libraries/Math512Bits.ts:149](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/libraries/Math512Bits.ts#L149)

___

### shiftDivRoundDown

▸ `Static` **shiftDivRoundDown**(`x`, `offset`, `denominator`): `u64`

Calculates x << offset / y with full precision
The result will be rounded down

Credit to Remco Bloemen under MIT license https://xn--2-umb.com/21/muldiv

Requirements:
- The offset needs to be strictly lower than 128
- The result must fit within u64

Caveats:
- This function does not work with fixed-point numbers

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `x` | `u128` | The multiplicand as an u128 |
| `offset` | `i32` | The number of bit to shift x |
| `denominator` | `u128` | The divisor as an u64 |

#### Returns

`u64`

The result as an u64

#### Defined in

[assembly/libraries/Math512Bits.ts:53](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/libraries/Math512Bits.ts#L53)

___

### shiftDivRoundUp

▸ `Static` **shiftDivRoundUp**(`x`, `offset`, `denominator`): `u64`

Calculates x << offset / y with full precision
The result will be rounded up

Credit to Remco Bloemen under MIT license https://xn--2-umb.com/21/muldiv

Requirements:
- The offset needs to be strictly lower than 128
- The result must fit within u64

Caveats:
- This function does not work with fixed-point numbers

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `x` | `u128` | The multiplicand as an u64 |
| `offset` | `i32` | The number of bit to shift x |
| `denominator` | `u128` | The divisor as an u64 |

#### Returns

`u64`

The result as an u64

#### Defined in

[assembly/libraries/Math512Bits.ts:124](https://github.com/dusaprotocol/v2.1/blob/ec71883/assembly/libraries/Math512Bits.ts#L124)
