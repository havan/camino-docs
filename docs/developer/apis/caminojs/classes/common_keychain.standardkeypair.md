# Class: StandardKeyPair

Class for representing a private and public keypair in Avalanche.
All APIs that need key pairs should extend on this class.

## Hierarchy

- **StandardKeyPair**

  ↳ [SECP256k1KeyPair](common_secp256k1keychain.secp256k1keypair)

## Index

### Properties

- [privk](common_keychain.standardkeypair#protected-privk)
- [pubk](common_keychain.standardkeypair#protected-pubk)

### Methods

- [clone](common_keychain.standardkeypair#abstract-clone)
- [create](common_keychain.standardkeypair#abstract-create)
- [generateKey](common_keychain.standardkeypair#abstract-generatekey)
- [getAddress](common_keychain.standardkeypair#abstract-getaddress)
- [getAddressString](common_keychain.standardkeypair#abstract-getaddressstring)
- [getPrivateKey](common_keychain.standardkeypair#getprivatekey)
- [getPrivateKeyString](common_keychain.standardkeypair#abstract-getprivatekeystring)
- [getPublicKey](common_keychain.standardkeypair#getpublickey)
- [getPublicKeyString](common_keychain.standardkeypair#abstract-getpublickeystring)
- [importKey](common_keychain.standardkeypair#abstract-importkey)
- [recover](common_keychain.standardkeypair#abstract-recover)
- [sign](common_keychain.standardkeypair#abstract-sign)
- [verify](common_keychain.standardkeypair#abstract-verify)

## Properties

### `Protected` privk

• **privk**: _Buffer_

_Defined in [src/common/keychain.ts:14](https://github.com/chain4travel/caminojs/blob/3883166/src/common/keychain.ts#L14)_

---

### `Protected` pubk

• **pubk**: _Buffer_

_Defined in [src/common/keychain.ts:13](https://github.com/chain4travel/caminojs/blob/3883166/src/common/keychain.ts#L13)_

## Methods

### `Abstract` clone

▸ **clone**(): _this_

_Defined in [src/common/keychain.ts:112](https://github.com/chain4travel/caminojs/blob/3883166/src/common/keychain.ts#L112)_

**Returns:** _this_

---

### `Abstract` create

▸ **create**(...`args`: any[]): _this_

_Defined in [src/common/keychain.ts:110](https://github.com/chain4travel/caminojs/blob/3883166/src/common/keychain.ts#L110)_

**Parameters:**

| Name      | Type  |
| --------- | ----- |
| `...args` | any[] |

**Returns:** _this_

---

### `Abstract` generateKey

▸ **generateKey**(`entropy?`: Buffer): _void_

_Defined in [src/common/keychain.ts:21](https://github.com/chain4travel/caminojs/blob/3883166/src/common/keychain.ts#L21)_

Generates a new keypair.

**Parameters:**

| Name       | Type   | Description                                                     |
| ---------- | ------ | --------------------------------------------------------------- |
| `entropy?` | Buffer | Optional parameter that may be necessary to produce secure keys |

**Returns:** _void_

---

### `Abstract` getAddress

▸ **getAddress**(): _Buffer_

_Defined in [src/common/keychain.ts:101](https://github.com/chain4travel/caminojs/blob/3883166/src/common/keychain.ts#L101)_

Returns the address.

**Returns:** _Buffer_

A [Buffer](https://github.com/feross/buffer) representation of the address

---

### `Abstract` getAddressString

▸ **getAddressString**(): _string_

_Defined in [src/common/keychain.ts:108](https://github.com/chain4travel/caminojs/blob/3883166/src/common/keychain.ts#L108)_

Returns the address's string representation.

**Returns:** _string_

A string representation of the address

---

### getPrivateKey

▸ **getPrivateKey**(): _Buffer_

_Defined in [src/common/keychain.ts:69](https://github.com/chain4travel/caminojs/blob/3883166/src/common/keychain.ts#L69)_

Returns a reference to the private key.

**Returns:** _Buffer_

A [Buffer](https://github.com/feross/buffer) containing the private key

---

### `Abstract` getPrivateKeyString

▸ **getPrivateKeyString**(): _string_

_Defined in [src/common/keychain.ts:87](https://github.com/chain4travel/caminojs/blob/3883166/src/common/keychain.ts#L87)_

Returns a string representation of the private key.

**Returns:** _string_

A string representation of the public key

---

### getPublicKey

▸ **getPublicKey**(): _Buffer_

_Defined in [src/common/keychain.ts:78](https://github.com/chain4travel/caminojs/blob/3883166/src/common/keychain.ts#L78)_

Returns a reference to the public key.

**Returns:** _Buffer_

A [Buffer](https://github.com/feross/buffer) containing the public key

---

### `Abstract` getPublicKeyString

▸ **getPublicKeyString**(): _string_

_Defined in [src/common/keychain.ts:94](https://github.com/chain4travel/caminojs/blob/3883166/src/common/keychain.ts#L94)_

Returns the public key.

**Returns:** _string_

A string representation of the public key

---

### `Abstract` importKey

▸ **importKey**(`privk`: Buffer): _boolean_

_Defined in [src/common/keychain.ts:30](https://github.com/chain4travel/caminojs/blob/3883166/src/common/keychain.ts#L30)_

Imports a private key and generates the appropriate public key.

**Parameters:**

| Name    | Type   | Description                                                               |
| ------- | ------ | ------------------------------------------------------------------------- |
| `privk` | Buffer | A [Buffer](https://github.com/feross/buffer) representing the private key |

**Returns:** _boolean_

true on success, false on failure

---

### `Abstract` recover

▸ **recover**(`msg`: Buffer, `sig`: Buffer): _Buffer_

_Defined in [src/common/keychain.ts:50](https://github.com/chain4travel/caminojs/blob/3883166/src/common/keychain.ts#L50)_

Recovers the public key of a message signer from a message and its associated signature.

**Parameters:**

| Name  | Type   | Description                                |
| ----- | ------ | ------------------------------------------ |
| `msg` | Buffer | The message that's signed                  |
| `sig` | Buffer | The signature that's signed on the message |

**Returns:** _Buffer_

A [Buffer](https://github.com/feross/buffer) containing the public
key of the signer

---

### `Abstract` sign

▸ **sign**(`msg`: Buffer): _Buffer_

_Defined in [src/common/keychain.ts:39](https://github.com/chain4travel/caminojs/blob/3883166/src/common/keychain.ts#L39)_

Takes a message, signs it, and returns the signature.

**Parameters:**

| Name  | Type   | Description         |
| ----- | ------ | ------------------- |
| `msg` | Buffer | The message to sign |

**Returns:** _Buffer_

A [Buffer](https://github.com/feross/buffer) containing the signature

---

### `Abstract` verify

▸ **verify**(`msg`: Buffer, `sig`: Buffer, `pubk`: Buffer): _boolean_

_Defined in [src/common/keychain.ts:62](https://github.com/chain4travel/caminojs/blob/3883166/src/common/keychain.ts#L62)_

Verifies that the private key associated with the provided public key produces the
signature associated with the given message.

**Parameters:**

| Name   | Type   | Description                                          |
| ------ | ------ | ---------------------------------------------------- |
| `msg`  | Buffer | The message associated with the signature            |
| `sig`  | Buffer | The signature of the signed message                  |
| `pubk` | Buffer | The public key associated with the message signature |

**Returns:** _boolean_

True on success, false on failure
