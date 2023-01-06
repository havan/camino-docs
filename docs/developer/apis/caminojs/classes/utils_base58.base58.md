# Class: Base58

A Base58 class that uses the cross-platform Buffer module. Built so that Typescript
will accept the code.

```js
let b58: Base58 = new Base58();
let str: string = b58.encode(somebuffer);
let buff: Buffer = b58.decode(somestring);
```

## Hierarchy

- **Base58**

## Index

### Constructors

- [constructor](utils_base58.base58#private-constructor)

### Properties

- [alphabetIdx0](utils_base58.base58#protected-alphabetidx0)
- [b58](utils_base58.base58#protected-b58)
- [b58alphabet](utils_base58.base58#protected-b58alphabet)
- [big58Radix](utils_base58.base58#protected-big58radix)
- [bigZero](utils_base58.base58#protected-bigzero)
- [instance](utils_base58.base58#static-private-instance)

### Methods

- [decode](utils_base58.base58#decode)
- [encode](utils_base58.base58#encode)
- [getInstance](utils_base58.base58#static-getinstance)

## Constructors

### `Private` constructor

\+ **new Base58**(): _[Base58](utils_base58.base58)_

_Defined in [src/utils/base58.ts:20](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/base58.ts#L20)_

**Returns:** _[Base58](utils_base58.base58)_

## Properties

### `Protected` alphabetIdx0

• **alphabetIdx0**: _string_ = "1"

_Defined in [src/utils/base58.ts:37](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/base58.ts#L37)_

---

### `Protected` b58

• **b58**: _number[]_ = [
255, 255, 255, 255, 255, 255, 255, 255, 255, 255, 255, 255, 255, 255, 255,
255, 255, 255, 255, 255, 255, 255, 255, 255, 255, 255, 255, 255, 255, 255,
255, 255, 255, 255, 255, 255, 255, 255, 255, 255, 255, 255, 255, 255, 255,
255, 255, 255, 255, 0, 1, 2, 3, 4, 5, 6, 7, 8, 255, 255, 255, 255, 255, 255,
255, 9, 10, 11, 12, 13, 14, 15, 16, 255, 17, 18, 19, 20, 21, 255, 22, 23,
24, 25, 26, 27, 28, 29, 30, 31, 32, 255, 255, 255, 255, 255, 255, 33, 34,
35, 36, 37, 38, 39, 40, 41, 42, 43, 255, 44, 45, 46, 47, 48, 49, 50, 51, 52,
53, 54, 55, 56, 57, 255, 255, 255, 255, 255, 255, 255, 255, 255, 255, 255,
255, 255, 255, 255, 255, 255, 255, 255, 255, 255, 255, 255, 255, 255, 255,
255, 255, 255, 255, 255, 255, 255, 255, 255, 255, 255, 255, 255, 255, 255,
255, 255, 255, 255, 255, 255, 255, 255, 255, 255, 255, 255, 255, 255, 255,
255, 255, 255, 255, 255, 255, 255, 255, 255, 255, 255, 255, 255, 255, 255,
255, 255, 255, 255, 255, 255, 255, 255, 255, 255, 255, 255, 255, 255, 255,
255, 255, 255, 255, 255, 255, 255, 255, 255, 255, 255, 255, 255, 255, 255,
255, 255, 255, 255, 255, 255, 255, 255, 255, 255, 255, 255, 255, 255, 255,
255, 255, 255, 255, 255, 255, 255, 255, 255, 255, 255, 255, 255, 255, 255,
255, 255
]

_Defined in [src/utils/base58.ts:39](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/base58.ts#L39)_

---

### `Protected` b58alphabet

• **b58alphabet**: _string_ = "123456789ABCDEFGHJKLMNPQRSTUVWXYZabcdefghijkmnopqrstuvwxyz"

_Defined in [src/utils/base58.ts:34](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/base58.ts#L34)_

---

### `Protected` big58Radix

• **big58Radix**: _BN_ = new BN(58)

_Defined in [src/utils/base58.ts:59](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/base58.ts#L59)_

---

### `Protected` bigZero

• **bigZero**: _BN_ = new BN(0)

_Defined in [src/utils/base58.ts:61](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/base58.ts#L61)_

---

### `Static` `Private` instance

▪ **instance**: _[Base58](utils_base58.base58)_

_Defined in [src/utils/base58.ts:20](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/base58.ts#L20)_

## Methods

### decode

▸ **decode**(`b`: string): _Buffer_

_Defined in [src/utils/base58.ts:95](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/base58.ts#L95)_

Decodes a base-58 into a [Buffer](https://github.com/feross/buffer)

**Parameters:**

| Name | Type   | Description                |
| ---- | ------ | -------------------------- |
| `b`  | string | A base-58 string to decode |

**Returns:** _Buffer_

A [Buffer](https://github.com/feross/buffer) from the decoded string.

---

### encode

▸ **encode**(`buff`: Buffer): _string_

_Defined in [src/utils/base58.ts:70](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/base58.ts#L70)_

Encodes a [Buffer](https://github.com/feross/buffer) as a base-58 string

**Parameters:**

| Name   | Type   | Description                                            |
| ------ | ------ | ------------------------------------------------------ |
| `buff` | Buffer | A [Buffer](https://github.com/feross/buffer) to encode |

**Returns:** _string_

A base-58 string.

---

### `Static` getInstance

▸ **getInstance**(): _[Base58](utils_base58.base58)_

_Defined in [src/utils/base58.ts:27](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/base58.ts#L27)_

Retrieves the Base58 singleton.

**Returns:** _[Base58](utils_base58.base58)_
