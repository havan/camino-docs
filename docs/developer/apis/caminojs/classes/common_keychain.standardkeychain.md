# Class: StandardKeyChain ‹**KPClass**›

Class for representing a key chain in Avalanche.
All endpoints that need key chains should extend on this class.

## Type parameters

▪ **KPClass**: _[StandardKeyPair](common_keychain.standardkeypair)_

extending [StandardKeyPair](common_keychain.standardkeypair) which is used as the key in [StandardKeyChain](common_keychain.standardkeychain)

## Hierarchy

- **StandardKeyChain**

  ↳ [SECP256k1KeyChain](common_secp256k1keychain.secp256k1keychain)

## Index

### Properties

- [importKey](common_keychain.standardkeychain#importkey)
- [keys](common_keychain.standardkeychain#protected-keys)
- [makeKey](common_keychain.standardkeychain#makekey)

### Methods

- [addKey](common_keychain.standardkeychain#addkey)
- [clone](common_keychain.standardkeychain#abstract-clone)
- [create](common_keychain.standardkeychain#abstract-create)
- [getAddressStrings](common_keychain.standardkeychain#getaddressstrings)
- [getAddresses](common_keychain.standardkeychain#getaddresses)
- [getKey](common_keychain.standardkeychain#getkey)
- [hasKey](common_keychain.standardkeychain#haskey)
- [removeKey](common_keychain.standardkeychain#removekey)
- [union](common_keychain.standardkeychain#abstract-union)

## Properties

### importKey

• **importKey**: _function_

_Defined in [src/common/keychain.ts:138](https://github.com/chain4travel/caminojs/blob/3883166/src/common/keychain.ts#L138)_

Given a private key, makes a new [StandardKeyPair](common_keychain.standardkeypair), returns the address.

**`param`** A [Buffer](https://github.com/feross/buffer) representing the private key

**`returns`** A new [StandardKeyPair](common_keychain.standardkeypair)

#### Type declaration:

▸ (`privk`: Buffer): _KPClass_

**Parameters:**

| Name    | Type   |
| ------- | ------ |
| `privk` | Buffer |

---

### `Protected` keys

• **keys**: _object_

_Defined in [src/common/keychain.ts:122](https://github.com/chain4travel/caminojs/blob/3883166/src/common/keychain.ts#L122)_

#### Type declaration:

- \[ **address**: _string_\]: KPClass

---

### makeKey

• **makeKey**: _function_

_Defined in [src/common/keychain.ts:129](https://github.com/chain4travel/caminojs/blob/3883166/src/common/keychain.ts#L129)_

Makes a new [StandardKeyPair](common_keychain.standardkeypair), returns the address.

**`returns`** Address of the new [StandardKeyPair](common_keychain.standardkeypair)

#### Type declaration:

▸ (): _KPClass_

## Methods

### addKey

▸ **addKey**(`newKey`: KPClass): _void_

_Defined in [src/common/keychain.ts:162](https://github.com/chain4travel/caminojs/blob/3883166/src/common/keychain.ts#L162)_

Adds the key pair to the list of the keys managed in the [StandardKeyChain](common_keychain.standardkeychain).

**Parameters:**

| Name     | Type    | Description                                                                                                 |
| -------- | ------- | ----------------------------------------------------------------------------------------------------------- |
| `newKey` | KPClass | A key pair of the appropriate class to be added to the [StandardKeyChain](common_keychain.standardkeychain) |

**Returns:** _void_

---

### `Abstract` clone

▸ **clone**(): _this_

_Defined in [src/common/keychain.ts:209](https://github.com/chain4travel/caminojs/blob/3883166/src/common/keychain.ts#L209)_

**Returns:** _this_

---

### `Abstract` create

▸ **create**(...`args`: any[]): _this_

_Defined in [src/common/keychain.ts:207](https://github.com/chain4travel/caminojs/blob/3883166/src/common/keychain.ts#L207)_

**Parameters:**

| Name      | Type  |
| --------- | ----- |
| `...args` | any[] |

**Returns:** _this_

---

### getAddressStrings

▸ **getAddressStrings**(): _string[]_

_Defined in [src/common/keychain.ts:154](https://github.com/chain4travel/caminojs/blob/3883166/src/common/keychain.ts#L154)_

Gets an array of addresses stored in the [StandardKeyChain](common_keychain.standardkeychain).

**Returns:** _string[]_

An array of string representations of the addresses

---

### getAddresses

▸ **getAddresses**(): _Buffer[]_

_Defined in [src/common/keychain.ts:146](https://github.com/chain4travel/caminojs/blob/3883166/src/common/keychain.ts#L146)_

Gets an array of addresses stored in the [StandardKeyChain](common_keychain.standardkeychain).

**Returns:** _Buffer[]_

An array of [Buffer](https://github.com/feross/buffer) representations
of the addresses

---

### getKey

▸ **getKey**(`address`: Buffer): _KPClass_

_Defined in [src/common/keychain.ts:205](https://github.com/chain4travel/caminojs/blob/3883166/src/common/keychain.ts#L205)_

Returns the [StandardKeyPair](common_keychain.standardkeypair) listed under the provided address

**Parameters:**

| Name      | Type   | Description                                                                                      |
| --------- | ------ | ------------------------------------------------------------------------------------------------ |
| `address` | Buffer | The [Buffer](https://github.com/feross/buffer) of the address to retrieve from the keys database |

**Returns:** _KPClass_

A reference to the [StandardKeyPair](common_keychain.standardkeypair) in the keys database

---

### hasKey

▸ **hasKey**(`address`: Buffer): _boolean_

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

▸ **removeKey**(`key`: KPClass | Buffer): _boolean_

_Defined in [src/common/keychain.ts:174](https://github.com/chain4travel/caminojs/blob/3883166/src/common/keychain.ts#L174)_

Removes the key pair from the list of they keys managed in the [StandardKeyChain](common_keychain.standardkeychain).

**Parameters:**

| Name  | Type                  | Description                                                                       |
| ----- | --------------------- | --------------------------------------------------------------------------------- |
| `key` | KPClass &#124; Buffer | A [Buffer](https://github.com/feross/buffer) for the address or KPClass to remove |

**Returns:** _boolean_

The boolean true if a key was removed.

---

### `Abstract` union

▸ **union**(`kc`: this): _this_

_Defined in [src/common/keychain.ts:211](https://github.com/chain4travel/caminojs/blob/3883166/src/common/keychain.ts#L211)_

**Parameters:**

| Name | Type |
| ---- | ---- |
| `kc` | this |

**Returns:** _this_
