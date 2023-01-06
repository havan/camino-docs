# Class: SECP256k1KeyChain ‹**SECPKPClass**›

Class for representing a key chain in Avalanche.

**`typeparam`** Class extending [StandardKeyPair](common_keychain.standardkeypair) which is used as the key in [SECP256k1KeyChain](common_secp256k1keychain.secp256k1keychain)

## Type parameters

▪ **SECPKPClass**: _[SECP256k1KeyPair](common_secp256k1keychain.secp256k1keypair)_

## Hierarchy

- [StandardKeyChain](common_keychain.standardkeychain)‹SECPKPClass›

  ↳ **SECP256k1KeyChain**

  ↳ [KeyChain](api_evm_keychain.keychain)

  ↳ [KeyChain](api_avm_keychain.keychain)

  ↳ [KeyChain](api_platformvm_keychain.keychain)

## Index

### Properties

- [importKey](common_secp256k1keychain.secp256k1keychain#importkey)
- [keys](common_secp256k1keychain.secp256k1keychain#protected-keys)
- [makeKey](common_secp256k1keychain.secp256k1keychain#makekey)

### Methods

- [addKey](common_secp256k1keychain.secp256k1keychain#addkey)
- [clone](common_secp256k1keychain.secp256k1keychain#abstract-clone)
- [create](common_secp256k1keychain.secp256k1keychain#abstract-create)
- [getAddressStrings](common_secp256k1keychain.secp256k1keychain#getaddressstrings)
- [getAddresses](common_secp256k1keychain.secp256k1keychain#getaddresses)
- [getKey](common_secp256k1keychain.secp256k1keychain#getkey)
- [hasKey](common_secp256k1keychain.secp256k1keychain#haskey)
- [removeKey](common_secp256k1keychain.secp256k1keychain#removekey)
- [union](common_secp256k1keychain.secp256k1keychain#abstract-union)

## Properties

### importKey

• **importKey**: _function_

_Overrides [StandardKeyChain](common_keychain.standardkeychain).[importKey](common_keychain.standardkeychain#importkey)_

_Defined in [src/common/secp256k1.ts:289](https://github.com/chain4travel/caminojs/blob/3883166/src/common/secp256k1.ts#L289)_

Given a private key, makes a new key pair, returns the address.

**`param`** A [Buffer](https://github.com/feross/buffer) or cb58 serialized string representing the private key

**`returns`** Address of the new key pair

#### Type declaration:

▸ (`privk`: Buffer | string): _SECPKPClass_

**Parameters:**

| Name    | Type                 |
| ------- | -------------------- |
| `privk` | Buffer &#124; string |

---

### `Protected` keys

• **keys**: _object_

_Inherited from [StandardKeyChain](common_keychain.standardkeychain).[keys](common_keychain.standardkeychain#protected-keys)_

_Defined in [src/common/keychain.ts:122](https://github.com/chain4travel/caminojs/blob/3883166/src/common/keychain.ts#L122)_

#### Type declaration:

- \[ **address**: _string_\]: SECPKPClass

---

### makeKey

• **makeKey**: _function_

_Overrides [StandardKeyChain](common_keychain.standardkeychain).[makeKey](common_keychain.standardkeychain#makekey)_

_Defined in [src/common/secp256k1.ts:276](https://github.com/chain4travel/caminojs/blob/3883166/src/common/secp256k1.ts#L276)_

Makes a new key pair, returns the address.

**`returns`** Address of the new key pair

#### Type declaration:

▸ (): _SECPKPClass_

## Methods

### addKey

▸ **addKey**(`newKey`: SECPKPClass): _void_

_Overrides [StandardKeyChain](common_keychain.standardkeychain).[addKey](common_keychain.standardkeychain#addkey)_

_Defined in [src/common/secp256k1.ts:278](https://github.com/chain4travel/caminojs/blob/3883166/src/common/secp256k1.ts#L278)_

**Parameters:**

| Name     | Type        |
| -------- | ----------- |
| `newKey` | SECPKPClass |

**Returns:** _void_

---

### `Abstract` clone

▸ **clone**(): _this_

_Inherited from [StandardKeyChain](common_keychain.standardkeychain).[clone](common_keychain.standardkeychain#abstract-clone)_

_Defined in [src/common/keychain.ts:209](https://github.com/chain4travel/caminojs/blob/3883166/src/common/keychain.ts#L209)_

**Returns:** _this_

---

### `Abstract` create

▸ **create**(...`args`: any[]): _this_

_Inherited from [StandardKeyChain](common_keychain.standardkeychain).[create](common_keychain.standardkeychain#abstract-create)_

_Defined in [src/common/keychain.ts:207](https://github.com/chain4travel/caminojs/blob/3883166/src/common/keychain.ts#L207)_

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

▸ **getKey**(`address`: Buffer): _SECPKPClass_

_Inherited from [StandardKeyChain](common_keychain.standardkeychain).[getKey](common_keychain.standardkeychain#getkey)_

_Defined in [src/common/keychain.ts:205](https://github.com/chain4travel/caminojs/blob/3883166/src/common/keychain.ts#L205)_

Returns the [StandardKeyPair](common_keychain.standardkeypair) listed under the provided address

**Parameters:**

| Name      | Type   | Description                                                                                      |
| --------- | ------ | ------------------------------------------------------------------------------------------------ |
| `address` | Buffer | The [Buffer](https://github.com/feross/buffer) of the address to retrieve from the keys database |

**Returns:** _SECPKPClass_

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

### removeKey

▸ **removeKey**(`key`: SECPKPClass | Buffer): _boolean_

_Inherited from [StandardKeyChain](common_keychain.standardkeychain).[removeKey](common_keychain.standardkeychain#removekey)_

_Defined in [src/common/keychain.ts:174](https://github.com/chain4travel/caminojs/blob/3883166/src/common/keychain.ts#L174)_

Removes the key pair from the list of they keys managed in the [StandardKeyChain](common_keychain.standardkeychain).

**Parameters:**

| Name  | Type                      | Description                                                                       |
| ----- | ------------------------- | --------------------------------------------------------------------------------- |
| `key` | SECPKPClass &#124; Buffer | A [Buffer](https://github.com/feross/buffer) for the address or KPClass to remove |

**Returns:** _boolean_

The boolean true if a key was removed.

---

### `Abstract` union

▸ **union**(`kc`: this): _this_

_Inherited from [StandardKeyChain](common_keychain.standardkeychain).[union](common_keychain.standardkeychain#abstract-union)_

_Defined in [src/common/keychain.ts:211](https://github.com/chain4travel/caminojs/blob/3883166/src/common/keychain.ts#L211)_

**Parameters:**

| Name | Type |
| ---- | ---- |
| `kc` | this |

**Returns:** _this_
