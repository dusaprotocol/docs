# IV0Pair

## Table of contents

### Constructors

- [constructor](IV0Pair#constructor)

### Properties

- [\_origin](IV0Pair#_origin)

### Methods

- [burn](IV0Pair#burn)
- [getBlockTimestampLast](IV0Pair#getblocktimestamplast)
- [getFactory](IV0Pair#getfactory)
- [getPrice0CumulativeLast](IV0Pair#getprice0cumulativelast)
- [getPrice1CumulativeLast](IV0Pair#getprice1cumulativelast)
- [getReserves](IV0Pair#getreserves)
- [init](IV0Pair#init)
- [mint](IV0Pair#mint)
- [skim](IV0Pair#skim)
- [swap](IV0Pair#swap)
- [sync](IV0Pair#sync)
- [token0](IV0Pair#token0)
- [token1](IV0Pair#token1)

## Constructors

### constructor

• **new IV0Pair**(`_origin`): [`IV0Pair`](IV0Pair)

#### Parameters

| Name      | Type      |
| :-------- | :-------- |
| `_origin` | `Address` |

#### Returns

[`IV0Pair`](IV0Pair)

#### Defined in

[assembly/interfaces/IV0Pair.ts:22](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/interfaces/IV0Pair.ts#L22)

## Properties

### \_origin

• **\_origin**: `Address`

#### Defined in

[assembly/interfaces/IV0Pair.ts:20](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/interfaces/IV0Pair.ts#L20)

## Methods

### burn

▸ **burn**(`to`): `Amounts`

Burn liquidity tokens.
This low-level function should be called from a contract which performs important safety checks.

#### Parameters

| Name | Type      | Description                                   |
| :--- | :-------- | :-------------------------------------------- |
| `to` | `Address` | The address to send the underlying assets to. |

#### Returns

`Amounts`

- The amounts of token0 and token1 burned.

#### Defined in

[assembly/interfaces/IV0Pair.ts:51](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/interfaces/IV0Pair.ts#L51)

---

### getBlockTimestampLast

▸ **getBlockTimestampLast**(): `u64`

#### Returns

`u64`

#### Defined in

[assembly/interfaces/IV0Pair.ts:88](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/interfaces/IV0Pair.ts#L88)

---

### getFactory

▸ **getFactory**(): [`IFactory`](IFactory.md)

#### Returns

[`IFactory`](IFactory.md)

#### Defined in

[assembly/interfaces/IV0Pair.ts:84](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/interfaces/IV0Pair.ts#L84)

---

### getPrice0CumulativeLast

▸ **getPrice0CumulativeLast**(): `u256`

#### Returns

`u256`

#### Defined in

[assembly/interfaces/IV0Pair.ts:94](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/interfaces/IV0Pair.ts#L94)

---

### getPrice1CumulativeLast

▸ **getPrice1CumulativeLast**(): `u256`

#### Returns

`u256`

#### Defined in

[assembly/interfaces/IV0Pair.ts:100](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/interfaces/IV0Pair.ts#L100)

---

### getReserves

▸ **getReserves**(): `Amounts`

#### Returns

`Amounts`

#### Defined in

[assembly/interfaces/IV0Pair.ts:106](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/interfaces/IV0Pair.ts#L106)

---

### init

▸ **init**(`tokenA`, `tokenB`): `StaticArray`<`u8`\>

#### Parameters

| Name     | Type      |
| :------- | :-------- |
| `tokenA` | `Address` |
| `tokenB` | `Address` |

#### Returns

`StaticArray`<`u8`\>

#### Defined in

[assembly/interfaces/IV0Pair.ts:26](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/interfaces/IV0Pair.ts#L26)

---

### mint

▸ **mint**(`to`, `fee`): `u256`

Mint liquidity tokens.
This low-level function should be called from a contract which performs important safety checks.

#### Parameters

| Name  | Type      | Description                                  |
| :---- | :-------- | :------------------------------------------- |
| `to`  | `Address` | The address to mint the liquidity tokens to. |
| `fee` | `u64`     | The fee to be paid for storage.              |

#### Returns

`u256`

- The amount of liquidity minted.

#### Defined in

[assembly/interfaces/IV0Pair.ts:39](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/interfaces/IV0Pair.ts#L39)

---

### skim

▸ **skim**(`to`): `void`

#### Parameters

| Name | Type      |
| :--- | :-------- |
| `to` | `Address` |

#### Returns

`void`

#### Defined in

[assembly/interfaces/IV0Pair.ts:113](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/interfaces/IV0Pair.ts#L113)

---

### swap

▸ **swap**(`amount0Out`, `amount1Out`, `to`, `data`): `void`

Swap tokens on a Uniswap V2-like DEX.
This function should be called from a contract which performs important safety checks.

#### Parameters

| Name         | Type                 | Description                               |
| :----------- | :------------------- | :---------------------------------------- |
| `amount0Out` | `u256`               | The amount of token0 to be sent.          |
| `amount1Out` | `u256`               | The amount of token1 to be sent.          |
| `to`         | `Address`            | The address to send the tokens to.        |
| `data`       | `StaticArray`<`u8`\> | Additional data to pass to the recipient. |

#### Returns

`void`

#### Defined in

[assembly/interfaces/IV0Pair.ts:66](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/interfaces/IV0Pair.ts#L66)

---

### sync

▸ **sync**(): `void`

#### Returns

`void`

#### Defined in

[assembly/interfaces/IV0Pair.ts:118](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/interfaces/IV0Pair.ts#L118)

---

### token0

▸ **token0**(): [`IERC20`](IERC20.md)

#### Returns

[`IERC20`](IERC20.md)

#### Defined in

[assembly/interfaces/IV0Pair.ts:76](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/interfaces/IV0Pair.ts#L76)

---

### token1

▸ **token1**(): [`IERC20`](IERC20.md)

#### Returns

[`IERC20`](IERC20.md)

#### Defined in

[assembly/interfaces/IV0Pair.ts:80](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/interfaces/IV0Pair.ts#L80)
