# Class: SECP256k1KeyPair

Class for representing a private and public keypair on the Platform Chain.

## Hierarchy

- [StandardKeyPair](common_keychain.standardkeypair)

  ↳ **SECP256k1KeyPair**

  ↳ [KeyPair](api_evm_keychain.keypair)

  ↳ [KeyPair](api_avm_keychain.keypair)

  ↳ [KeyPair](api_platformvm_keychain.keypair)

## Index

### Constructors

- [constructor](common_secp256k1keychain.secp256k1keypair#constructor)

### Properties

- [chainID](common_secp256k1keychain.secp256k1keypair#protected-chainid)
- [hrp](common_secp256k1keychain.secp256k1keypair#protected-hrp)
- [keypair](common_secp256k1keychain.secp256k1keypair#protected-keypair)
- [privk](common_secp256k1keychain.secp256k1keypair#protected-privk)
- [pubk](common_secp256k1keychain.secp256k1keypair#protected-pubk)

### Methods

- [clone](common_secp256k1keychain.secp256k1keypair#abstract-clone)
- [create](common_secp256k1keychain.secp256k1keypair#abstract-create)
- [generateKey](common_secp256k1keychain.secp256k1keypair#generatekey)
- [getAddress](common_secp256k1keychain.secp256k1keypair#getaddress)
- [getAddressString](common_secp256k1keychain.secp256k1keypair#getaddressstring)
- [getChainID](common_secp256k1keychain.secp256k1keypair#getchainid)
- [getHRP](common_secp256k1keychain.secp256k1keypair#gethrp)
- [getPrivateKey](common_secp256k1keychain.secp256k1keypair#getprivatekey)
- [getPrivateKeyString](common_secp256k1keychain.secp256k1keypair#getprivatekeystring)
- [getPublicKey](common_secp256k1keychain.secp256k1keypair#getpublickey)
- [getPublicKeyString](common_secp256k1keychain.secp256k1keypair#getpublickeystring)
- [importKey](common_secp256k1keychain.secp256k1keypair#importkey)
- [recover](common_secp256k1keychain.secp256k1keypair#recover)
- [setChainID](common_secp256k1keychain.secp256k1keypair#setchainid)
- [setHRP](common_secp256k1keychain.secp256k1keypair#sethrp)
- [sign](common_secp256k1keychain.secp256k1keypair#sign)
- [verify](common_secp256k1keychain.secp256k1keypair#verify)
- [addressFromPublicKey](common_secp256k1keychain.secp256k1keypair#static-addressfrompublickey)

## Constructors

### constructor

\+ **new SECP256k1KeyPair**(`hrp`: string, `chainID`: string): _[SECP256k1KeyPair](common_secp256k1keychain.secp256k1keypair)_

_Defined in [src/common/secp256k1.ts:253](https://github.com/chain4travel/caminojs/blob/3883166/src/common/secp256k1.ts#L253)_

**Parameters:**

| Name      | Type   |
| --------- | ------ |
| `hrp`     | string |
| `chainID` | string |

**Returns:** _[SECP256k1KeyPair](common_secp256k1keychain.secp256k1keypair)_

## Properties

### `Protected` chainID

• **chainID**: _string_ = ""

_Defined in [src/common/secp256k1.ts:45](https://github.com/chain4travel/caminojs/blob/3883166/src/common/secp256k1.ts#L45)_

---

### `Protected` hrp

• **hrp**: _string_ = ""

_Defined in [src/common/secp256k1.ts:46](https://github.com/chain4travel/caminojs/blob/3883166/src/common/secp256k1.ts#L46)_

---

### `Protected` keypair

• **keypair**: _elliptic.ec.KeyPair_

_Defined in [src/common/secp256k1.ts:44](https://github.com/chain4travel/caminojs/blob/3883166/src/common/secp256k1.ts#L44)_

---

### `Protected` privk

• **privk**: _Buffer_

_Inherited from [StandardKeyPair](common_keychain.standardkeypair).[privk](common_keychain.standardkeypair#protected-privk)_

_Defined in [src/common/keychain.ts:14](https://github.com/chain4travel/caminojs/blob/3883166/src/common/keychain.ts#L14)_

---

### `Protected` pubk

• **pubk**: _Buffer_

_Inherited from [StandardKeyPair](common_keychain.standardkeypair).[pubk](common_keychain.standardkeypair#protected-pubk)_

_Defined in [src/common/keychain.ts:13](https://github.com/chain4travel/caminojs/blob/3883166/src/common/keychain.ts#L13)_

## Methods

### `Abstract` clone

▸ **clone**(): _this_

_Inherited from [StandardKeyPair](common_keychain.standardkeypair).[clone](common_keychain.standardkeypair#abstract-clone)_

_Defined in [src/common/keychain.ts:112](https://github.com/chain4travel/caminojs/blob/3883166/src/common/keychain.ts#L112)_

**Returns:** _this_

---

### `Abstract` create

▸ **create**(...`args`: any[]): _this_

_Inherited from [StandardKeyPair](common_keychain.standardkeypair).[create](common_keychain.standardkeypair#abstract-create)_

_Defined in [src/common/keychain.ts:110](https://github.com/chain4travel/caminojs/blob/3883166/src/common/keychain.ts#L110)_

**Parameters:**

| Name      | Type  |
| --------- | ----- |
| `...args` | any[] |

**Returns:** _this_

---

### generateKey

▸ **generateKey**(): _void_

_Overrides [StandardKeyPair](common_keychain.standardkeypair).[generateKey](common_keychain.standardkeypair#abstract-generatekey)_

_Defined in [src/common/secp256k1.ts:68](https://github.com/chain4travel/caminojs/blob/3883166/src/common/secp256k1.ts#L68)_

Generates a new keypair.

**Returns:** _void_

---

### getAddress

▸ **getAddress**(): _Buffer_

_Overrides [StandardKeyPair](common_keychain.standardkeypair).[getAddress](common_keychain.standardkeypair#abstract-getaddress)_

_Defined in [src/common/secp256k1.ts:112](https://github.com/chain4travel/caminojs/blob/3883166/src/common/secp256k1.ts#L112)_

Returns the address as a [Buffer](https://github.com/feross/buffer).

**Returns:** _Buffer_

A [Buffer](https://github.com/feross/buffer) representation of the address

---

### getAddressString

▸ **getAddressString**(): _string_

_Overrides [StandardKeyPair](common_keychain.standardkeypair).[getAddressString](common_keychain.standardkeypair#abstract-getaddressstring)_

_Defined in [src/common/secp256k1.ts:121](https://github.com/chain4travel/caminojs/blob/3883166/src/common/secp256k1.ts#L121)_

Returns the address's string representation.

**Returns:** _string_

A string representation of the address

---

### getChainID

▸ **getChainID**(): _string_

_Defined in [src/common/secp256k1.ts:224](https://github.com/chain4travel/caminojs/blob/3883166/src/common/secp256k1.ts#L224)_

Returns the chainID associated with this key.

**Returns:** _string_

The [KeyPair](api_evm_keychain.keypair)'s chainID

---

### getHRP

▸ **getHRP**(): _string_

_Defined in [src/common/secp256k1.ts:242](https://github.com/chain4travel/caminojs/blob/3883166/src/common/secp256k1.ts#L242)_

Returns the Human-Readable-Part of the network associated with this key.

**Returns:** _string_

The [KeyPair](api_evm_keychain.keypair)'s Human-Readable-Part of the network's Bech32 addressing scheme

---

### getPrivateKey

▸ **getPrivateKey**(): _Buffer_

_Inherited from [StandardKeyPair](common_keychain.standardkeypair).[getPrivateKey](common_keychain.standardkeypair#getprivatekey)_

_Defined in [src/common/keychain.ts:69](https://github.com/chain4travel/caminojs/blob/3883166/src/common/keychain.ts#L69)_

Returns a reference to the private key.

**Returns:** _Buffer_

A [Buffer](https://github.com/feross/buffer) containing the private key

---

### getPrivateKeyString

▸ **getPrivateKeyString**(): _string_

_Overrides [StandardKeyPair](common_keychain.standardkeypair).[getPrivateKeyString](common_keychain.standardkeypair#abstract-getprivatekeystring)_

_Defined in [src/common/secp256k1.ts:160](https://github.com/chain4travel/caminojs/blob/3883166/src/common/secp256k1.ts#L160)_

Returns a string representation of the private key.

**Returns:** _string_

A cb58 serialized string representation of the private key

---

### getPublicKey

▸ **getPublicKey**(): _Buffer_

_Inherited from [StandardKeyPair](common_keychain.standardkeypair).[getPublicKey](common_keychain.standardkeypair#getpublickey)_

_Defined in [src/common/keychain.ts:78](https://github.com/chain4travel/caminojs/blob/3883166/src/common/keychain.ts#L78)_

Returns a reference to the public key.

**Returns:** _Buffer_

A [Buffer](https://github.com/feross/buffer) containing the public key

---

### getPublicKeyString

▸ **getPublicKeyString**(): _string_

_Overrides [StandardKeyPair](common_keychain.standardkeypair).[getPublicKeyString](common_keychain.standardkeypair#abstract-getpublickeystring)_

_Defined in [src/common/secp256k1.ts:169](https://github.com/chain4travel/caminojs/blob/3883166/src/common/secp256k1.ts#L169)_

Returns the public key.

**Returns:** _string_

A cb58 serialized string representation of the public key

---

### importKey

▸ **importKey**(`privk`: Buffer): _boolean_

_Overrides [StandardKeyPair](common_keychain.standardkeypair).[importKey](common_keychain.standardkeypair#abstract-importkey)_

_Defined in [src/common/secp256k1.ts:89](https://github.com/chain4travel/caminojs/blob/3883166/src/common/secp256k1.ts#L89)_

Imports a private key and generates the appropriate public key.

**Parameters:**

| Name    | Type   | Description                                                               |
| ------- | ------ | ------------------------------------------------------------------------- |
| `privk` | Buffer | A [Buffer](https://github.com/feross/buffer) representing the private key |

**Returns:** _boolean_

true on success, false on failure

---

### recover

▸ **recover**(`msg`: Buffer, `sig`: Buffer): _Buffer_

_Overrides [StandardKeyPair](common_keychain.standardkeypair).[recover](common_keychain.standardkeypair#abstract-recover)_

_Defined in [src/common/secp256k1.ts:213](https://github.com/chain4travel/caminojs/blob/3883166/src/common/secp256k1.ts#L213)_

Recovers the public key of a message signer from a message and its associated signature.

**Parameters:**

| Name  | Type   | Description                                |
| ----- | ------ | ------------------------------------------ |
| `msg` | Buffer | The message that's signed                  |
| `sig` | Buffer | The signature that's signed on the message |

**Returns:** _Buffer_

A [Buffer](https://github.com/feross/buffer) containing the public key of the signer

---

### setChainID

▸ **setChainID**(`chainID`: string): _void_

_Defined in [src/common/secp256k1.ts:233](https://github.com/chain4travel/caminojs/blob/3883166/src/common/secp256k1.ts#L233)_

Sets the the chainID associated with this key.

**Parameters:**

| Name      | Type   | Description            |
| --------- | ------ | ---------------------- |
| `chainID` | string | String for the chainID |

**Returns:** _void_

---

### setHRP

▸ **setHRP**(`hrp`: string): _void_

_Defined in [src/common/secp256k1.ts:251](https://github.com/chain4travel/caminojs/blob/3883166/src/common/secp256k1.ts#L251)_

Sets the the Human-Readable-Part of the network associated with this key.

**Parameters:**

| Name  | Type   | Description                                            |
| ----- | ------ | ------------------------------------------------------ |
| `hrp` | string | String for the Human-Readable-Part of Bech32 addresses |

**Returns:** _void_

---

### sign

▸ **sign**(`msg`: Buffer): _Buffer_

_Overrides [StandardKeyPair](common_keychain.standardkeypair).[sign](common_keychain.standardkeypair#abstract-sign)_

_Defined in [src/common/secp256k1.ts:180](https://github.com/chain4travel/caminojs/blob/3883166/src/common/secp256k1.ts#L180)_

Takes a message, signs it, and returns the signature.

**Parameters:**

| Name  | Type   | Description                                            |
| ----- | ------ | ------------------------------------------------------ |
| `msg` | Buffer | The message to sign, be sure to hash first if expected |

**Returns:** _Buffer_

A [Buffer](https://github.com/feross/buffer) containing the signature

---

### verify

▸ **verify**(`msg`: Buffer, `sig`: Buffer): _boolean_

_Overrides [StandardKeyPair](common_keychain.standardkeypair).[verify](common_keychain.standardkeypair#abstract-verify)_

_Defined in [src/common/secp256k1.ts:200](https://github.com/chain4travel/caminojs/blob/3883166/src/common/secp256k1.ts#L200)_

Verifies that the private key associated with the provided public key produces the signature associated with the given message.

**Parameters:**

| Name  | Type   | Description                               |
| ----- | ------ | ----------------------------------------- |
| `msg` | Buffer | The message associated with the signature |
| `sig` | Buffer | The signature of the signed message       |

**Returns:** _boolean_

True on success, false on failure

---

### `Static` addressFromPublicKey

▸ **addressFromPublicKey**(`pubk`: Buffer): _Buffer_

_Defined in [src/common/secp256k1.ts:134](https://github.com/chain4travel/caminojs/blob/3883166/src/common/secp256k1.ts#L134)_

Returns an address given a public key.

**Parameters:**

| Name   | Type   | Description                                                              |
| ------ | ------ | ------------------------------------------------------------------------ |
| `pubk` | Buffer | A [Buffer](https://github.com/feross/buffer) representing the public key |

**Returns:** _Buffer_

A [Buffer](https://github.com/feross/buffer) for the address of the public key.