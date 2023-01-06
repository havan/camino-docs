# Class: Mnemonic

BIP39 Mnemonic code for generating deterministic keys.

## Hierarchy

- **Mnemonic**

## Index

### Constructors

- [constructor](utils_mnemonic.mnemonic#private-constructor)

### Properties

- [wordlists](utils_mnemonic.mnemonic#protected-wordlists)
- [instance](utils_mnemonic.mnemonic#static-private-instance)

### Methods

- [entropyToMnemonic](utils_mnemonic.mnemonic#entropytomnemonic)
- [generateMnemonic](utils_mnemonic.mnemonic#generatemnemonic)
- [getDefaultWordlist](utils_mnemonic.mnemonic#getdefaultwordlist)
- [getWordlists](utils_mnemonic.mnemonic#getwordlists)
- [mnemonicToEntropy](utils_mnemonic.mnemonic#mnemonictoentropy)
- [mnemonicToSeed](utils_mnemonic.mnemonic#mnemonictoseed)
- [mnemonicToSeedSync](utils_mnemonic.mnemonic#mnemonictoseedsync)
- [setDefaultWordlist](utils_mnemonic.mnemonic#setdefaultwordlist)
- [validateMnemonic](utils_mnemonic.mnemonic#validatemnemonic)
- [getInstance](utils_mnemonic.mnemonic#static-getinstance)

## Constructors

### `Private` constructor

\+ **new Mnemonic**(): _[Mnemonic](utils_mnemonic.mnemonic)_

_Defined in [src/utils/mnemonic.ts:17](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/mnemonic.ts#L17)_

**Returns:** _[Mnemonic](utils_mnemonic.mnemonic)_

## Properties

### `Protected` wordlists

• **wordlists**: _string[]_ = bip39.wordlists

_Defined in [src/utils/mnemonic.ts:19](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/mnemonic.ts#L19)_

---

### `Static` `Private` instance

▪ **instance**: _[Mnemonic](utils_mnemonic.mnemonic)_

_Defined in [src/utils/mnemonic.ts:17](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/mnemonic.ts#L17)_

## Methods

### entropyToMnemonic

▸ **entropyToMnemonic**(`entropy`: Buffer | string, `wordlist?`: string[]): _string_

_Defined in [src/utils/mnemonic.ts:95](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/mnemonic.ts#L95)_

Takes mnemonic and wordlist and returns buffer

**Parameters:**

| Name        | Type                 | Description                                                                |
| ----------- | -------------------- | -------------------------------------------------------------------------- |
| `entropy`   | Buffer &#124; string | the entropy as a [Buffer](https://github.com/feross/buffer) or as a string |
| `wordlist?` | string[]             | Optional, the wordlist as an array of strings                              |

**Returns:** _string_

A string

---

### generateMnemonic

▸ **generateMnemonic**(`strength?`: number, `rng?`: function, `wordlist?`: string[]): _string_

_Defined in [src/utils/mnemonic.ts:138](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/mnemonic.ts#L138)_

Generate a random mnemonic (uses crypto.randomBytes under the hood), defaults to 256-bits of entropy

**Parameters:**

▪`Optional` **strength**: _number_

Optional the strength as a number

▪`Optional` **rng**: _function_

Optional the random number generator. Defaults to crypto.randomBytes

▸ (`size`: number): _Buffer_

**Parameters:**

| Name   | Type   |
| ------ | ------ |
| `size` | number |

▪`Optional` **wordlist**: _string[]_

Optional

**Returns:** _string_

---

### getDefaultWordlist

▸ **getDefaultWordlist**(): _string_

_Defined in [src/utils/mnemonic.ts:126](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/mnemonic.ts#L126)_

Returns the language of the default word list

**Returns:** _string_

A string

---

### getWordlists

▸ **getWordlists**(`language?`: string): _string[] | Wordlist_

_Defined in [src/utils/mnemonic.ts:38](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/mnemonic.ts#L38)_

Return wordlists

**Parameters:**

| Name        | Type   | Description                      |
| ----------- | ------ | -------------------------------- |
| `language?` | string | a string specifying the language |

**Returns:** _string[] | Wordlist_

A [[Wordlist]] object or array of strings

---

### mnemonicToEntropy

▸ **mnemonicToEntropy**(`mnemonic`: string, `wordlist?`: string[]): _string_

_Defined in [src/utils/mnemonic.ts:83](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/mnemonic.ts#L83)_

Takes mnemonic and wordlist and returns buffer

**Parameters:**

| Name        | Type     | Description                                  |
| ----------- | -------- | -------------------------------------------- |
| `mnemonic`  | string   | the mnemonic as a string                     |
| `wordlist?` | string[] | Optional the wordlist as an array of strings |

**Returns:** _string_

A string

---

### mnemonicToSeed

▸ **mnemonicToSeed**(`mnemonic`: string, `password`: string): _Promise‹Buffer›_

_Defined in [src/utils/mnemonic.ts:67](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/mnemonic.ts#L67)_

Asynchronously takes mnemonic and password and returns Promise [Buffer](https://github.com/feross/buffer)

**Parameters:**

| Name       | Type   | Default | Description              |
| ---------- | ------ | ------- | ------------------------ |
| `mnemonic` | string | -       | the mnemonic as a string |
| `password` | string | ""      | the password as a string |

**Returns:** _Promise‹Buffer›_

A [Buffer](https://github.com/feross/buffer)

---

### mnemonicToSeedSync

▸ **mnemonicToSeedSync**(`mnemonic`: string, `password`: string): _Buffer_

_Defined in [src/utils/mnemonic.ts:54](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/mnemonic.ts#L54)_

Synchronously takes mnemonic and password and returns [Buffer](https://github.com/feross/buffer)

**Parameters:**

| Name       | Type   | Default | Description              |
| ---------- | ------ | ------- | ------------------------ |
| `mnemonic` | string | -       | the mnemonic as a string |
| `password` | string | ""      | the password as a string |

**Returns:** _Buffer_

A [Buffer](https://github.com/feross/buffer)

---

### setDefaultWordlist

▸ **setDefaultWordlist**(`language`: string): _void_

_Defined in [src/utils/mnemonic.ts:117](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/mnemonic.ts#L117)_

Sets the default word list

**Parameters:**

| Name       | Type   | Description              |
| ---------- | ------ | ------------------------ |
| `language` | string | the language as a string |

**Returns:** _void_

---

### validateMnemonic

▸ **validateMnemonic**(`mnemonic`: string, `wordlist?`: string[]): _string_

_Defined in [src/utils/mnemonic.ts:107](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/mnemonic.ts#L107)_

Validates a mnemonic
11\*

**Parameters:**

| Name        | Type     | Description                                  |
| ----------- | -------- | -------------------------------------------- |
| `mnemonic`  | string   | the mnemonic as a string                     |
| `wordlist?` | string[] | Optional the wordlist as an array of strings |

**Returns:** _string_

A string

---

### `Static` getInstance

▸ **getInstance**(): _[Mnemonic](utils_mnemonic.mnemonic)_

_Defined in [src/utils/mnemonic.ts:24](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/mnemonic.ts#L24)_

Retrieves the Mnemonic singleton.

**Returns:** _[Mnemonic](utils_mnemonic.mnemonic)_
