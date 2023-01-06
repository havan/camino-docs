# Class: BinTools

A class containing tools useful in interacting with binary data cross-platform using
nodejs & javascript.

This class should never be instantiated directly. Instead,
invoke the "BinTools.getInstance()" static \* function to grab the singleton
instance of the tools.

Everything in this library uses
the [feross's Buffer class](https://github.com/feross/buffer).

```js
const bintools: BinTools = BinTools.getInstance();
const b58str:  = bintools.bufferToB58(Buffer.from("Wubalubadubdub!"));
```

## Hierarchy

- **BinTools**

## Index

### Constructors

- [constructor](utils_bintools.bintools#private-constructor)

### Properties

- [b58](utils_bintools.bintools#private-b58)
- [instance](utils_bintools.bintools#static-private-instance)

### Methods

- [addChecksum](utils_bintools.bintools#addchecksum)
- [addressToString](utils_bintools.bintools#addresstostring)
- [b58ToBuffer](utils_bintools.bintools#b58tobuffer)
- [bufferToB58](utils_bintools.bintools#buffertob58)
- [bufferToString](utils_bintools.bintools#buffertostring)
- [cb58Decode](utils_bintools.bintools#cb58decode)
- [cb58DecodeWithChecksum](utils_bintools.bintools#cb58decodewithchecksum)
- [cb58Encode](utils_bintools.bintools#cb58encode)
- [copyFrom](utils_bintools.bintools#copyfrom)
- [fromArrayBufferToBuffer](utils_bintools.bintools#fromarraybuffertobuffer)
- [fromBNToBuffer](utils_bintools.bintools#frombntobuffer)
- [fromBufferToArrayBuffer](utils_bintools.bintools#frombuffertoarraybuffer)
- [fromBufferToBN](utils_bintools.bintools#frombuffertobn)
- [isBase58](utils_bintools.bintools#isbase58)
- [isBase64](utils_bintools.bintools#isbase64)
- [isCB58](utils_bintools.bintools#iscb58)
- [isDecimal](utils_bintools.bintools#isdecimal)
- [isHex](utils_bintools.bintools#ishex)
- [isPrimaryBechAddress](utils_bintools.bintools#isprimarybechaddress)
- [parseAddress](utils_bintools.bintools#parseaddress)
- [stringToAddress](utils_bintools.bintools#stringtoaddress)
- [stringToBuffer](utils_bintools.bintools#stringtobuffer)
- [validateChecksum](utils_bintools.bintools#validatechecksum)
- [getInstance](utils_bintools.bintools#static-getinstance)

## Constructors

### `Private` constructor

\+ **new BinTools**(): _[BinTools](utils_bintools.bintools)_

_Defined in [src/utils/bintools.ts:30](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/bintools.ts#L30)_

**Returns:** _[BinTools](utils_bintools.bintools)_

## Properties

### `Private` b58

• **b58**: _[Base58](utils_base58.base58)_

_Defined in [src/utils/bintools.ts:36](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/bintools.ts#L36)_

---

### `Static` `Private` instance

▪ **instance**: _[BinTools](utils_bintools.bintools)_

_Defined in [src/utils/bintools.ts:30](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/bintools.ts#L30)_

## Methods

### addChecksum

▸ **addChecksum**(`buff`: Buffer): _Buffer_

_Defined in [src/utils/bintools.ts:270](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/bintools.ts#L270)_

Takes a [Buffer](https://github.com/feross/buffer) and adds a checksum, returning
a [Buffer](https://github.com/feross/buffer) with the 4-byte checksum appended.

**Parameters:**

| Name   | Type   | Description                                                         |
| ------ | ------ | ------------------------------------------------------------------- |
| `buff` | Buffer | The [Buffer](https://github.com/feross/buffer) to append a checksum |

**Returns:** _Buffer_

---

### addressToString

▸ **addressToString**(`hrp`: string, `chainid`: string, `bytes`: Buffer): _string_

_Defined in [src/utils/bintools.ts:333](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/bintools.ts#L333)_

**Parameters:**

| Name      | Type   |
| --------- | ------ |
| `hrp`     | string |
| `chainid` | string |
| `bytes`   | Buffer |

**Returns:** _string_

---

### b58ToBuffer

▸ **b58ToBuffer**(`b58str`: string): _Buffer_

_Defined in [src/utils/bintools.ts:195](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/bintools.ts#L195)_

Takes a base-58 string and returns a [Buffer](https://github.com/feross/buffer).

**Parameters:**

| Name     | Type   | Description                                                                   |
| -------- | ------ | ----------------------------------------------------------------------------- |
| `b58str` | string | The base-58 string to convert to a [Buffer](https://github.com/feross/buffer) |

**Returns:** _Buffer_

---

### bufferToB58

▸ **bufferToB58**(`buff`: Buffer): _string_

_Defined in [src/utils/bintools.ts:187](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/bintools.ts#L187)_

Takes a [Buffer](https://github.com/feross/buffer) and returns a base-58 string of
the [Buffer](https://github.com/feross/buffer).

**Parameters:**

| Name   | Type   | Description                                                          |
| ------ | ------ | -------------------------------------------------------------------- |
| `buff` | Buffer | The [Buffer](https://github.com/feross/buffer) to convert to base-58 |

**Returns:** _string_

---

### bufferToString

▸ **bufferToString**(`buff`: Buffer): _string_

_Defined in [src/utils/bintools.ts:147](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/bintools.ts#L147)_

Produces a string from a [Buffer](https://github.com/feross/buffer)
representing a string. ONLY USED IN TRANSACTION FORMATTING, ASSUMED LENGTH IS PREPENDED.

**Parameters:**

| Name   | Type   | Description                                                           |
| ------ | ------ | --------------------------------------------------------------------- |
| `buff` | Buffer | The [Buffer](https://github.com/feross/buffer) to convert to a string |

**Returns:** _string_

---

### cb58Decode

▸ **cb58Decode**(`bytes`: Buffer | string): _Buffer_

_Defined in [src/utils/bintools.ts:313](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/bintools.ts#L313)_

Takes a cb58 serialized [Buffer](https://github.com/feross/buffer) or base-58 string
and returns a [Buffer](https://github.com/feross/buffer) of the original data. Throws on error.

**Parameters:**

| Name    | Type                 | Description                                                                    |
| ------- | -------------------- | ------------------------------------------------------------------------------ |
| `bytes` | Buffer &#124; string | A cb58 serialized [Buffer](https://github.com/feross/buffer) or base-58 string |

**Returns:** _Buffer_

---

### cb58DecodeWithChecksum

▸ **cb58DecodeWithChecksum**(`bytes`: Buffer | string): _string_

_Defined in [src/utils/bintools.ts:323](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/bintools.ts#L323)_

**Parameters:**

| Name    | Type                 |
| ------- | -------------------- |
| `bytes` | Buffer &#124; string |

**Returns:** _string_

---

### cb58Encode

▸ **cb58Encode**(`bytes`: Buffer): _string_

_Defined in [src/utils/bintools.ts:302](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/bintools.ts#L302)_

Takes a [Buffer](https://github.com/feross/buffer) and returns a base-58 string with
checksum as per the cb58 standard.

**Parameters:**

| Name    | Type   | Description                                               |
| ------- | ------ | --------------------------------------------------------- |
| `bytes` | Buffer | A [Buffer](https://github.com/feross/buffer) to serialize |

**Returns:** _string_

A serialized base-58 string of the Buffer.

---

### copyFrom

▸ **copyFrom**(`buff`: Buffer, `start`: number, `end`: number): _Buffer_

_Defined in [src/utils/bintools.ts:170](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/bintools.ts#L170)_

Makes a copy (no reference) of a [Buffer](https://github.com/feross/buffer)
over provided indecies.

**Parameters:**

| Name    | Type   | Default   | Description                                            |
| ------- | ------ | --------- | ------------------------------------------------------ |
| `buff`  | Buffer | -         | The [Buffer](https://github.com/feross/buffer) to copy |
| `start` | number | 0         | The index to start the copy                            |
| `end`   | number | undefined | The index to end the copy                              |

**Returns:** _Buffer_

---

### fromArrayBufferToBuffer

▸ **fromArrayBufferToBuffer**(`ab`: ArrayBuffer): _Buffer_

_Defined in [src/utils/bintools.ts:217](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/bintools.ts#L217)_

Takes an ArrayBuffer and converts it to a [Buffer](https://github.com/feross/buffer).

**Parameters:**

| Name | Type        | Description                                                                |
| ---- | ----------- | -------------------------------------------------------------------------- |
| `ab` | ArrayBuffer | The ArrayBuffer to convert to a [Buffer](https://github.com/feross/buffer) |

**Returns:** _Buffer_

---

### fromBNToBuffer

▸ **fromBNToBuffer**(`bn`: BN, `length?`: number): _Buffer_

_Defined in [src/utils/bintools.ts:246](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/bintools.ts#L246)_

Takes a [BN](https://github.com/indutny/bn.js/) and converts it
to a [Buffer](https://github.com/feross/buffer).

**Parameters:**

| Name      | Type   | Description                                                                                            |
| --------- | ------ | ------------------------------------------------------------------------------------------------------ |
| `bn`      | BN     | The [BN](https://github.com/indutny/bn.js/) to convert to a [Buffer](https://github.com/feross/buffer) |
| `length?` | number | The zero-padded length of the [Buffer](https://github.com/feross/buffer)                               |

**Returns:** _Buffer_

---

### fromBufferToArrayBuffer

▸ **fromBufferToArrayBuffer**(`buff`: Buffer): _ArrayBuffer_

_Defined in [src/utils/bintools.ts:203](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/bintools.ts#L203)_

Takes a [Buffer](https://github.com/feross/buffer) and returns an ArrayBuffer.

**Parameters:**

| Name   | Type   | Description                                                                 |
| ------ | ------ | --------------------------------------------------------------------------- |
| `buff` | Buffer | The [Buffer](https://github.com/feross/buffer) to convert to an ArrayBuffer |

**Returns:** _ArrayBuffer_

---

### fromBufferToBN

▸ **fromBufferToBN**(`buff`: Buffer): _BN_

_Defined in [src/utils/bintools.ts:232](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/bintools.ts#L232)_

Takes a [Buffer](https://github.com/feross/buffer) and converts it
to a [BN](https://github.com/indutny/bn.js/).

**Parameters:**

| Name   | Type   | Description                                                                                            |
| ------ | ------ | ------------------------------------------------------------------------------------------------------ |
| `buff` | Buffer | The [Buffer](https://github.com/feross/buffer) to convert to a [BN](https://github.com/indutny/bn.js/) |

**Returns:** _BN_

---

### isBase58

▸ **isBase58**(`base58`: string): _boolean_

_Defined in [src/utils/bintools.ts:76](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/bintools.ts#L76)_

Returns true if base58, otherwise false

**Parameters:**

| Name     | Type   | Description                    |
| -------- | ------ | ------------------------------ |
| `base58` | string | the string to verify is base58 |

**Returns:** _boolean_

---

### isBase64

▸ **isBase64**(`str`: string): _boolean_

_Defined in [src/utils/bintools.ts:52](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/bintools.ts#L52)_

Returns true if base64, otherwise false

**Parameters:**

| Name  | Type   | Description                    |
| ----- | ------ | ------------------------------ |
| `str` | string | the string to verify is Base64 |

**Returns:** _boolean_

---

### isCB58

▸ **isCB58**(`cb58`: string): _boolean_

_Defined in [src/utils/bintools.ts:68](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/bintools.ts#L68)_

Returns true if cb58, otherwise false

**Parameters:**

| Name   | Type   | Description                  |
| ------ | ------ | ---------------------------- |
| `cb58` | string | the string to verify is cb58 |

**Returns:** _boolean_

---

### isDecimal

▸ **isDecimal**(`str`: string): _boolean_

_Defined in [src/utils/bintools.ts:113](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/bintools.ts#L113)_

Returns true if decimal, otherwise false

**Parameters:**

| Name  | Type   | Description                         |
| ----- | ------ | ----------------------------------- |
| `str` | string | the string to verify is hexidecimal |

**Returns:** _boolean_

---

### isHex

▸ **isHex**(`hex`: string): _boolean_

_Defined in [src/utils/bintools.ts:91](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/bintools.ts#L91)_

Returns true if hexidecimal, otherwise false

**Parameters:**

| Name  | Type   | Description                         |
| ----- | ------ | ----------------------------------- |
| `hex` | string | the string to verify is hexidecimal |

**Returns:** _boolean_

---

### isPrimaryBechAddress

▸ **isPrimaryBechAddress**(`address`: string): _boolean_

_Defined in [src/utils/bintools.ts:128](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/bintools.ts#L128)_

Returns true if meets requirements to parse as an address as Bech32 on X-Chain or P-Chain, otherwise false

**Parameters:**

| Name      | Type   | Description                     |
| --------- | ------ | ------------------------------- |
| `address` | string | the string to verify is address |

**Returns:** _boolean_

---

### parseAddress

▸ **parseAddress**(`addr`: string, `blockchainID`: string, `alias`: string, `addrlen`: number): _Buffer_

_Defined in [src/utils/bintools.ts:395](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/bintools.ts#L395)_

Takes an address and returns its [Buffer](https://github.com/feross/buffer)
representation if valid. A more strict version of stringToAddress.

**Parameters:**

| Name           | Type   | Default   | Description                                                                                                       |
| -------------- | ------ | --------- | ----------------------------------------------------------------------------------------------------------------- |
| `addr`         | string | -         | A string representation of the address                                                                            |
| `blockchainID` | string | -         | A cb58 encoded string representation of the blockchainID                                                          |
| `alias`        | string | undefined | A chainID alias, if any, that the address can also parse from.                                                    |
| `addrlen`      | number | 20        | VMs can use any addressing scheme that they like, so this is the appropriate number of address bytes. Default 20. |

**Returns:** _Buffer_

A [Buffer](https://github.com/feross/buffer) for the address if valid,
undefined if not valid.

---

### stringToAddress

▸ **stringToAddress**(`address`: string, `hrp?`: string): _Buffer_

_Defined in [src/utils/bintools.ts:336](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/bintools.ts#L336)_

**Parameters:**

| Name      | Type   |
| --------- | ------ |
| `address` | string |
| `hrp?`    | string |

**Returns:** _Buffer_

---

### stringToBuffer

▸ **stringToBuffer**(`str`: string): _Buffer_

_Defined in [src/utils/bintools.ts:155](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/bintools.ts#L155)_

Produces a [Buffer](https://github.com/feross/buffer) from a string. ONLY USED IN TRANSACTION FORMATTING, LENGTH IS PREPENDED.

**Parameters:**

| Name  | Type   | Description                                                           |
| ----- | ------ | --------------------------------------------------------------------- |
| `str` | string | The string to convert to a [Buffer](https://github.com/feross/buffer) |

**Returns:** _Buffer_

---

### validateChecksum

▸ **validateChecksum**(`buff`: Buffer): _boolean_

_Defined in [src/utils/bintools.ts:283](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/bintools.ts#L283)_

Takes a [Buffer](https://github.com/feross/buffer) with an appended 4-byte checksum
and returns true if the checksum is valid, otherwise false.

**Parameters:**

| Name   | Type   |
| ------ | ------ |
| `buff` | Buffer |

**Returns:** _boolean_

---

### `Static` getInstance

▸ **getInstance**(): _[BinTools](utils_bintools.bintools)_

_Defined in [src/utils/bintools.ts:41](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/bintools.ts#L41)_

Retrieves the BinTools singleton.

**Returns:** _[BinTools](utils_bintools.bintools)_
