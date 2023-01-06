# Class: KeyChain

Class for representing a key chain in Avalanche.

**`typeparam`** Class extending [SECP256k1KeyChain](common_secp256k1keychain.secp256k1keychain) which is used as the key in [KeyChain](api_evm_keychain.keychain)

## Hierarchy

↳ [SECP256k1KeyChain](common_secp256k1keychain.secp256k1keychain)‹[KeyPair](api_evm_keychain.keypair)›

↳ **KeyChain**

## Index

### Constructors

- [constructor](api_evm_keychain.keychain#constructor)

### Properties

- [chainID](api_evm_keychain.keychain#chainid)
- [hrp](api_evm_keychain.keychain#hrp)
- [keys](api_evm_keychain.keychain#protected-keys)

### Methods

- [addKey](api_evm_keychain.keychain#addkey)
- [clone](api_evm_keychain.keychain#clone)
- [create](api_evm_keychain.keychain#create)
- [getAddressStrings](api_evm_keychain.keychain#getaddressstrings)
- [getAddresses](api_evm_keychain.keychain#getaddresses)
- [getKey](api_evm_keychain.keychain#getkey)
- [hasKey](api_evm_keychain.keychain#haskey)
- [importKey](api_evm_keychain.keychain#importkey)
- [makeKey](api_evm_keychain.keychain#makekey)
- [removeKey](api_evm_keychain.keychain#removekey)
- [union](api_evm_keychain.keychain#union)

## Constructors

### constructor

\+ **new KeyChain**(`hrp`: string, `chainID`: string): _[KeyChain](api_evm_keychain.keychain)_

_Defined in [src/apis/evm/keychain.ts:104](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/keychain.ts#L104)_

Returns instance of KeyChain.

**Parameters:**

| Name      | Type   |
| --------- | ------ |
| `hrp`     | string |
| `chainID` | string |

**Returns:** _[KeyChain](api_evm_keychain.keychain)_

## Properties

### chainID

• **chainID**: _string_ = ""

_Defined in [src/apis/evm/keychain.ts:42](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/keychain.ts#L42)_

---

### hrp

• **hrp**: _string_ = ""

_Defined in [src/apis/evm/keychain.ts:41](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/keychain.ts#L41)_

---

### `Protected` keys

• **keys**: _object_

_Inherited from [StandardKeyChain](common_keychain.standardkeychain).[keys](common_keychain.standardkeychain#protected-keys)_

_Defined in [src/common/keychain.ts:122](https://github.com/chain4travel/caminojs/blob/3883166/src/common/keychain.ts#L122)_

#### Type declaration:

- \[ **address**: _string_\]: [KeyPair](api_evm_keychain.keypair)

## Methods

### addKey

▸ **addKey**(`newKey`: [KeyPair](api_evm_keychain.keypair)): _void_

_Overrides [SECP256k1KeyChain](common_secp256k1keychain.secp256k1keychain).[addKey](common_secp256k1keychain.secp256k1keychain#addkey)_

_Defined in [src/apis/evm/keychain.ts:55](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/keychain.ts#L55)_

**Parameters:**

| Name     | Type                                |
| -------- | ----------------------------------- |
| `newKey` | [KeyPair](api_evm_keychain.keypair) |

**Returns:** _void_

---

### clone

▸ **clone**(): _this_

_Overrides [StandardKeyChain](common_keychain.standardkeychain).[clone](common_keychain.standardkeychain#abstract-clone)_

_Defined in [src/apis/evm/keychain.ts:90](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/keychain.ts#L90)_

**Returns:** _this_

---

### create

▸ **create**(...`args`: any[]): _this_

_Overrides [StandardKeyChain](common_keychain.standardkeychain).[create](common_keychain.standardkeychain#abstract-create)_

_Defined in [src/apis/evm/keychain.ts:83](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/keychain.ts#L83)_

**Parameters:**

| Name      | Type  |
| --------- | ----- |
| `...args` | any[] |

**Returns:** _this_

---

### getAddressStrings

▸ **getAddressStrings**(): _string[]_

_Inherited from [StandardKeyChain](common_keychain.standardkeychain).[getAddressStrings](common_keychain.standardkeychain#getaddressstrings)_

_Defined in [src/common/keychain.ts:154](https://github.com/chain4travel/caminojs/blob/3883166/src/common/keychain.ts#L154)_

Gets an array of addresses stored in the [StandardKeyChain](common_keychain.standardkeychain).

**Returns:** _string[]_

An array of string representations of the addresses

---

### getAddresses

▸ **getAddresses**(): _Buffer[]_

_Inherited from [StandardKeyChain](common_keychain.standardkeychain).[getAddresses](common_keychain.standardkeychain#getaddresses)_

_Defined in [src/common/keychain.ts:146](https://github.com/chain4travel/caminojs/blob/3883166/src/common/keychain.ts#L146)_

Gets an array of addresses stored in the [StandardKeyChain](common_keychain.standardkeychain).

**Returns:** _Buffer[]_

An array of [Buffer](https://github.com/feross/buffer) representations
of the addresses

---

### getKey

▸ **getKey**(`address`: Buffer): _[KeyPair](api_evm_keychain.keypair)_

_Inherited from [StandardKeyChain](common_keychain.standardkeychain).[getKey](common_keychain.standardkeychain#getkey)_

_Defined in [src/common/keychain.ts:205](https://github.com/chain4travel/caminojs/blob/3883166/src/common/keychain.ts#L205)_

Returns the [StandardKeyPair](common_keychain.standardkeypair) listed under the provided address

**Parameters:**

| Name      | Type   | Description                                                                                      |
| --------- | ------ | ------------------------------------------------------------------------------------------------ |
| `address` | Buffer | The [Buffer](https://github.com/feross/buffer) of the address to retrieve from the keys database |

**Returns:** _[KeyPair](api_evm_keychain.keypair)_

A reference to the [StandardKeyPair](common_keychain.standardkeypair) in the keys database

---

### hasKey

▸ **hasKey**(`address`: Buffer): _boolean_

_Inherited from [StandardKeyChain](common_keychain.standardkeychain).[hasKey](common_keychain.standardkeychain#haskey)_

_Defined in [src/common/keychain.ts:195](https://github.com/chain4travel/caminojs/blob/3883166/src/common/keychain.ts#L195)_

Checks if there is a key associated with the provided address.

**Parameters:**

| Name      | Type   | Description                                             |
| --------- | ------ | ------------------------------------------------------- |
| `address` | Buffer | The address to check for existence in the keys database |

**Returns:** _boolean_

True on success, false if not found

---

### importKey

▸ **importKey**(`privk`: Buffer | string): _[KeyPair](api_evm_keychain.keypair)_

_Overrides [SECP256k1KeyChain](common_secp256k1keychain.secp256k1keychain).[importKey](common_secp256k1keychain.secp256k1keychain#importkey)_

_Defined in [src/apis/evm/keychain.ts:68](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/keychain.ts#L68)_

Given a private key, makes a new key pair, returns the address.

**Parameters:**

| Name    | Type                 | Description                                                                                         |
| ------- | -------------------- | --------------------------------------------------------------------------------------------------- |
| `privk` | Buffer &#124; string | A [Buffer](https://github.com/feross/buffer) or cb58 serialized string representing the private key |

**Returns:** _[KeyPair](api_evm_keychain.keypair)_

The new key pair

---

### makeKey

▸ **makeKey**(): _[KeyPair](api_evm_keychain.keypair)_

_Overrides [SECP256k1KeyChain](common_secp256k1keychain.secp256k1keychain).[makeKey](common_secp256k1keychain.secp256k1keychain#makekey)_

_Defined in [src/apis/evm/keychain.ts:49](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/keychain.ts#L49)_

Makes a new key pair, returns the address.

**Returns:** _[KeyPair](api_evm_keychain.keypair)_

The new key pair

---

### removeKey

▸ **removeKey**(`key`: [KeyPair](api_evm_keychain.keypair) | Buffer): _boolean_

_Inherited from [StandardKeyChain](common_keychain.standardkeychain).[removeKey](common_keychain.standardkeychain#removekey)_

_Defined in [src/common/keychain.ts:174](https://github.com/chain4travel/caminojs/blob/3883166/src/common/keychain.ts#L174)_

Removes the key pair from the list of they keys managed in the [StandardKeyChain](common_keychain.standardkeychain).

**Parameters:**

| Name  | Type                                              | Description                                                                       |
| ----- | ------------------------------------------------- | --------------------------------------------------------------------------------- |
| `key` | [KeyPair](api_evm_keychain.keypair) &#124; Buffer | A [Buffer](https://github.com/feross/buffer) for the address or KPClass to remove |

**Returns:** _boolean_

The boolean true if a key was removed.

---

### union

▸ **union**(`kc`: this): _this_

_Overrides [StandardKeyChain](common_keychain.standardkeychain).[union](common_keychain.standardkeychain#abstract-union)_

_Defined in [src/apis/evm/keychain.ts:98](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/keychain.ts#L98)_

**Parameters:**

| Name | Type |
| ---- | ---- |
| `kc` | this |

**Returns:** _this_
