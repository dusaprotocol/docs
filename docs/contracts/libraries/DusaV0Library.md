# DusaV0Library

## Table of contents

### Constructors

- [constructor](DusaV0Library#constructor)

### Methods

- [getAmountIn](DusaV0Library#getamountin)
- [getAmountOut](DusaV0Library#getamountout)
- [getAmountsIn](DusaV0Library#getamountsin)
- [getAmountsOut](DusaV0Library#getamountsout)
- [getReserves](DusaV0Library#getreserves)
- [quote](DusaV0Library#quote)

## Constructors

### constructor

• **new DusaV0Library**(): [`DusaV0Library`](DusaV0Library)

#### Returns

[`DusaV0Library`](DusaV0Library)

## Methods

### getAmountIn

▸ **getAmountIn**(`amountOut`, `reserveIn`, `reserveOut`): `u256`

#### Parameters

| Name         | Type   |
| :----------- | :----- |
| `amountOut`  | `u256` |
| `reserveIn`  | `u256` |
| `reserveOut` | `u256` |

#### Returns

`u256`

#### Defined in

[assembly/libraries/DusaV0Library.ts:51](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/DusaV0Library.ts#L51)

---

### getAmountOut

▸ **getAmountOut**(`amountIn`, `reserveIn`, `reserveOut`): `u256`

#### Parameters

| Name         | Type   |
| :----------- | :----- |
| `amountIn`   | `u256` |
| `reserveIn`  | `u256` |
| `reserveOut` | `u256` |

#### Returns

`u256`

#### Defined in

[assembly/libraries/DusaV0Library.ts:35](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/DusaV0Library.ts#L35)

---

### getAmountsIn

▸ **getAmountsIn**(`factory`, `amountOut`, `path`): `u256`[]

#### Parameters

| Name        | Type                                     |
| :---------- | :--------------------------------------- |
| `factory`   | [`IV0Factory`](../interfaces/IV0Factory) |
| `amountOut` | `u256`                                   |
| `path`      | `Address`[]                              |

#### Returns

`u256`[]

#### Defined in

[assembly/libraries/DusaV0Library.ts:90](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/DusaV0Library.ts#L90)

---

### getAmountsOut

▸ **getAmountsOut**(`factory`, `amountIn`, `path`): `u256`[]

#### Parameters

| Name       | Type                                     |
| :--------- | :--------------------------------------- |
| `factory`  | [`IV0Factory`](../interfaces/IV0Factory) |
| `amountIn` | `u256`                                   |
| `path`     | `Address`[]                              |

#### Returns

`u256`[]

#### Defined in

[assembly/libraries/DusaV0Library.ts:69](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/DusaV0Library.ts#L69)

---

### getReserves

▸ **getReserves**(`factory`, `tokenA`, `tokenB`): `Amounts`

#### Parameters

| Name      | Type                                     |
| :-------- | :--------------------------------------- |
| `factory` | [`IV0Factory`](../interfaces/IV0Factory) |
| `tokenA`  | `Address`                                |
| `tokenB`  | `Address`                                |

#### Returns

`Amounts`

#### Defined in

[assembly/libraries/DusaV0Library.ts:11](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/DusaV0Library.ts#L11)

---

### quote

▸ **quote**(`amountA`, `reserveA`, `reserveB`): `u256`

#### Parameters

| Name       | Type   |
| :--------- | :----- |
| `amountA`  | `u256` |
| `reserveA` | `u256` |
| `reserveB` | `u256` |

#### Returns

`u256`

#### Defined in

[assembly/libraries/DusaV0Library.ts:25](https://github.com/dusaprotocol/v1-core/blob/V2/assembly/libraries/DusaV0Library.ts#L25)
