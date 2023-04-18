ERC20

# Namespace: ERC20

## Table of contents

### Variables

-   [DECIMALS_KEY](ERC20.md#decimals_key)
-   [NAME_KEY](ERC20.md#name_key)
-   [SYMBOL_KEY](ERC20.md#symbol_key)
-   [TOTAL_SUPPLY_KEY](ERC20.md#total_supply_key)

### Functions

-   [allowance](ERC20.md#allowance)
-   [balanceOf](ERC20.md#balanceof)
-   [constructor](ERC20.md#constructor)
-   [decimals](ERC20.md#decimals)
-   [decreaseAllowance](ERC20.md#decreaseallowance)
-   [increaseAllowance](ERC20.md#increaseallowance)
-   [name](ERC20.md#name)
-   [received](ERC20.md#received)
-   [symbol](ERC20.md#symbol)
-   [totalSupply](ERC20.md#totalsupply)
-   [transfer](ERC20.md#transfer)
-   [transferFrom](ERC20.md#transferfrom)
-   [version](ERC20.md#version)

## Variables

### DECIMALS_KEY

• `Const` **DECIMALS_KEY**: `StaticArray`<`u8`\>

#### Defined in

node_modules/@massalabs/sc-standards/assembly/contracts/FT/token.ts:24

---

### NAME_KEY

• `Const` **NAME_KEY**: `StaticArray`<`u8`\>

#### Defined in

node_modules/@massalabs/sc-standards/assembly/contracts/FT/token.ts:21

---

### SYMBOL_KEY

• `Const` **SYMBOL_KEY**: `StaticArray`<`u8`\>

#### Defined in

node_modules/@massalabs/sc-standards/assembly/contracts/FT/token.ts:22

---

### TOTAL_SUPPLY_KEY

• `Const` **TOTAL_SUPPLY_KEY**: `StaticArray`<`u8`\>

#### Defined in

node_modules/@massalabs/sc-standards/assembly/contracts/FT/token.ts:23

## Functions

### allowance

▸ **allowance**(`binaryArgs`): `StaticArray`<`u8`\>

Returns the allowance set on the owner's account for the spender.

#### Parameters

| Name         | Type                 | Description                                                                                                       |
| :----------- | :------------------- | :---------------------------------------------------------------------------------------------------------------- |
| `binaryArgs` | `StaticArray`<`u8`\> | Args object serialized as a string containing: - the owner's account (address) - the spender's account (address). |

#### Returns

`StaticArray`<`u8`\>

#### Defined in

node_modules/@massalabs/sc-standards/assembly/contracts/FT/token.ts:231

---

### balanceOf

▸ **balanceOf**(`binaryArgs`): `StaticArray`<`u8`\>

Returns the balance of an account.

#### Parameters

| Name         | Type                 | Description                                                                 |
| :----------- | :------------------- | :-------------------------------------------------------------------------- |
| `binaryArgs` | `StaticArray`<`u8`\> | Args object serialized as a string containing an owner's account (Address). |

#### Returns

`StaticArray`<`u8`\>

#### Defined in

node_modules/@massalabs/sc-standards/assembly/contracts/FT/token.ts:148

---

### constructor

▸ **constructor**(`stringifyArgs`): `void`

Initialize the ERC20 contract
Can be called only once

**`Example`**

```typescript
constructor(
    new Args()
        .add("TOKEN_NAME")
        .add("TOKEN_SYMBOL")
        .add(3) // decimals
        .add(1000) // total supply
        .serialize()
);
```

#### Parameters

| Name            | Type                 | Description                                                                                                                                                                 |
| :-------------- | :------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `stringifyArgs` | `StaticArray`<`u8`\> | Args object serialized as a string containing: - the token name (string) - the token symbol (string). - the decimals (u8). - the totalSupply (u64) - first owner (address)e |

#### Returns

`void`

#### Defined in

node_modules/@massalabs/sc-standards/assembly/contracts/FT/token.ts:49

---

### decimals

▸ **decimals**(`_`): `StaticArray`<`u8`\>

Returns the maximum number of digits being part of the fractional part
of the token when using a decimal representation.

#### Parameters

| Name | Type                 | Description                                                    |
| :--- | :------------------- | :------------------------------------------------------------- |
| `_`  | `StaticArray`<`u8`\> | unused see https://github.com/massalabs/massa-sc-std/issues/18 |

#### Returns

`StaticArray`<`u8`\>

#### Defined in

node_modules/@massalabs/sc-standards/assembly/contracts/FT/token.ts:135

---

### decreaseAllowance

▸ **decreaseAllowance**(`binaryArgs`): `void`

Decreases the allowance of the spender the on owner's account by the amount.

This function can only be called by the owner.

#### Parameters

| Name         | Type                 | Description                                                                                           |
| :----------- | :------------------- | :---------------------------------------------------------------------------------------------------- |
| `binaryArgs` | `StaticArray`<`u8`\> | Args object serialized as a string containing: - the spender's account (address); - the amount (u64). |

#### Returns

`void`

#### Defined in

node_modules/@massalabs/sc-standards/assembly/contracts/FT/token.ts:300

---

### increaseAllowance

▸ **increaseAllowance**(`binaryArgs`): `void`

Increases the allowance of the spender on the owner's account by the amount.

This function can only be called by the owner.

#### Parameters

| Name         | Type                 | Description                                                                                           |
| :----------- | :------------------- | :---------------------------------------------------------------------------------------------------- |
| `binaryArgs` | `StaticArray`<`u8`\> | Args object serialized as a string containing: - the spender's account (address); - the amount (u64). |

#### Returns

`void`

#### Defined in

node_modules/@massalabs/sc-standards/assembly/contracts/FT/token.ts:265

---

### name

▸ **name**(`_`): `StaticArray`<`u8`\>

Returns the name of the token.

#### Parameters

| Name | Type                 | Description                                                    |
| :--- | :------------------- | :------------------------------------------------------------- |
| `_`  | `StaticArray`<`u8`\> | unused see https://github.com/massalabs/massa-sc-std/issues/18 |

#### Returns

`StaticArray`<`u8`\>

token name.

#### Defined in

node_modules/@massalabs/sc-standards/assembly/contracts/FT/token.ts:103

---

### received

▸ **received**(`bs`): `StaticArray`<`u8`\>

#### Parameters

| Name | Type                 |
| :--- | :------------------- |
| `bs` | `StaticArray`<`u8`\> |

#### Returns

`StaticArray`<`u8`\>

#### Defined in

[assembly/contracts/ERC20.ts:7](https://github.com/dusaprotocol/v2.1/blob/b07cbb8/assembly/contracts/ERC20.ts#L7)

---

### symbol

▸ **symbol**(`_`): `StaticArray`<`u8`\>

Returns the symbol of the token.

#### Parameters

| Name | Type                 | Description                                                    |
| :--- | :------------------- | :------------------------------------------------------------- |
| `_`  | `StaticArray`<`u8`\> | unused see https://github.com/massalabs/massa-sc-std/issues/18 |

#### Returns

`StaticArray`<`u8`\>

token symbol.

#### Defined in

node_modules/@massalabs/sc-standards/assembly/contracts/FT/token.ts:112

---

### totalSupply

▸ **totalSupply**(`_`): `StaticArray`<`u8`\>

Returns the total token supply.

The number of tokens that were initially minted.

#### Parameters

| Name | Type                 | Description                                                    |
| :--- | :------------------- | :------------------------------------------------------------- |
| `_`  | `StaticArray`<`u8`\> | unused see https://github.com/massalabs/massa-sc-std/issues/18 |

#### Returns

`StaticArray`<`u8`\>

u64

#### Defined in

node_modules/@massalabs/sc-standards/assembly/contracts/FT/token.ts:124

---

### transfer

▸ **transfer**(`binaryArgs`): `void`

Transfers tokens from the caller's account to the recipient's account.

#### Parameters

| Name         | Type                 | Description                                                                                                      |
| :----------- | :------------------- | :--------------------------------------------------------------------------------------------------------------- |
| `binaryArgs` | `StaticArray`<`u8`\> | Args object serialized as a string containing: - the recipient's account (address) - the number of tokens (u64). |

#### Returns

`void`

#### Defined in

node_modules/@massalabs/sc-standards/assembly/contracts/FT/token.ts:169

---

### transferFrom

▸ **transferFrom**(`binaryArgs`): `void`

Transfers token ownership from the owner's account to the recipient's account
using the spender's allowance.

This function can only be called by the spender.
This function is atomic:

-   both allowance and transfer are executed if possible;
-   or if allowance or transfer is not possible, both are discarded.

#### Parameters

| Name         | Type                 | Description                                                                                                                              |
| :----------- | :------------------- | :--------------------------------------------------------------------------------------------------------------------------------------- |
| `binaryArgs` | `StaticArray`<`u8`\> | Args object serialized as a string containing: - the owner's account (address); - the recipient's account (address); - the amount (u64). |

#### Returns

`void`

#### Defined in

node_modules/@massalabs/sc-standards/assembly/contracts/FT/token.ts:355

---

### version

▸ **version**(`_`): `StaticArray`<`u8`\>

Returns the version of this smart contract.
This versioning is following the best practices defined in https://semver.org/.

#### Parameters

| Name | Type                 | Description                                                    |
| :--- | :------------------- | :------------------------------------------------------------- |
| `_`  | `StaticArray`<`u8`\> | unused see https://github.com/massalabs/massa-sc-std/issues/18 |

#### Returns

`StaticArray`<`u8`\>

token version

#### Defined in

node_modules/@massalabs/sc-standards/assembly/contracts/FT/token.ts:89
