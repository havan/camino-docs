# Class: HDNode

BIP32 hierarchical deterministic keys.

## Hierarchy

- **HDNode**

## Index

### Constructors

- [constructor](utils_hdnode.hdnode#constructor)

### Properties

- [chainCode](utils_hdnode.hdnode#chaincode)
- [hdkey](utils_hdnode.hdnode#private-hdkey)
- [privateExtendedKey](utils_hdnode.hdnode#privateextendedkey)
- [privateKey](utils_hdnode.hdnode#privatekey)
- [privateKeyCB58](utils_hdnode.hdnode#privatekeycb58)
- [publicExtendedKey](utils_hdnode.hdnode#publicextendedkey)
- [publicKey](utils_hdnode.hdnode#publickey)

### Methods

- [derive](utils_hdnode.hdnode#derive)
- [sign](utils_hdnode.hdnode#sign)
- [verify](utils_hdnode.hdnode#verify)
- [wipePrivateData](utils_hdnode.hdnode#wipeprivatedata)

## Constructors

### constructor

\+ **new HDNode**(`from`: string | Buffer): _[HDNode](utils_hdnode.hdnode)_

_Defined in [src/utils/hdnode.ts:70](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/hdnode.ts#L70)_

Creates an HDNode from a master seed or an extended public/private key

**Parameters:**

| Name   | Type                 | Description                       |
| ------ | -------------------- | --------------------------------- |
| `from` | string &#124; Buffer | seed or key to create HDNode from |

**Returns:** _[HDNode](utils_hdnode.hdnode)_

## Properties

### chainCode

• **chainCode**: _Buffer_

_Defined in [src/utils/hdnode.ts:20](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/hdnode.ts#L20)_

---

### `Private` hdkey

• **hdkey**: _any_

_Defined in [src/utils/hdnode.ts:16](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/hdnode.ts#L16)_

---

### privateExtendedKey

• **privateExtendedKey**: _string_

_Defined in [src/utils/hdnode.ts:21](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/hdnode.ts#L21)_

---

### privateKey

• **privateKey**: _Buffer_

_Defined in [src/utils/hdnode.ts:18](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/hdnode.ts#L18)_

---

### privateKeyCB58

• **privateKeyCB58**: _string_

_Defined in [src/utils/hdnode.ts:19](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/hdnode.ts#L19)_

---

### publicExtendedKey

• **publicExtendedKey**: _string_

_Defined in [src/utils/hdnode.ts:22](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/hdnode.ts#L22)_

---

### publicKey

• **publicKey**: _Buffer_

_Defined in [src/utils/hdnode.ts:17](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/hdnode.ts#L17)_

## Methods

### derive

▸ **derive**(`path`: string): _[HDNode](utils_hdnode.hdnode)_

_Defined in [src/utils/hdnode.ts:29](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/hdnode.ts#L29)_

Derives the HDNode at path from the current HDNode.

**Parameters:**

| Name   | Type   |
| ------ | ------ |
| `path` | string |

**Returns:** _[HDNode](utils_hdnode.hdnode)_

derived child HDNode

---

### sign

▸ **sign**(`hash`: Buffer): _Buffer_

_Defined in [src/utils/hdnode.ts:45](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/hdnode.ts#L45)_

Signs the buffer hash with the private key using secp256k1 and returns the signature as a buffer.

**Parameters:**

| Name   | Type   |
| ------ | ------ |
| `hash` | Buffer |

**Returns:** _Buffer_

signature as a Buffer

---

### verify

▸ **verify**(`hash`: Buffer, `signature`: Buffer): _boolean_

_Defined in [src/utils/hdnode.ts:57](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/hdnode.ts#L57)_

Verifies that the signature is valid for hash and the HDNode's public key using secp256k1.

**`throws`** if the hash or signature is the wrong length.

**Parameters:**

| Name        | Type   |
| ----------- | ------ |
| `hash`      | Buffer |
| `signature` | Buffer |

**Returns:** _boolean_

true for valid, false for invalid.

---

### wipePrivateData

▸ **wipePrivateData**(): _void_

_Defined in [src/utils/hdnode.ts:65](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/hdnode.ts#L65)_

Wipes all record of the private key from the HDNode instance.
After calling this method, the instance will behave as if it was created via an xpub.

**Returns:** _void_
