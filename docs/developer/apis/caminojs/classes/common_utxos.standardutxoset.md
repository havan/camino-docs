# Class: StandardUTXOSet ‹**UTXOClass**›

Class representing a set of [StandardUTXO](common_utxos.standardutxo)s.

## Type parameters

▪ **UTXOClass**: _[StandardUTXO](common_utxos.standardutxo)_

## Hierarchy

- [Serializable](utils_serialization.serializable)

  ↳ **StandardUTXOSet**

  ↳ [UTXOSet](api_evm_utxos.utxoset)

  ↳ [UTXOSet](api_avm_utxos.utxoset)

  ↳ [UTXOSet](api_platformvm_utxos.utxoset)

## Index

### Properties

- [\_codecID](common_utxos.standardutxoset#protected-_codecid)
- [\_typeID](common_utxos.standardutxoset#protected-_typeid)
- [\_typeName](common_utxos.standardutxoset#protected-_typename)
- [addressUTXOs](common_utxos.standardutxoset#protected-addressutxos)
- [utxos](common_utxos.standardutxoset#protected-utxos)

### Methods

- [add](common_utxos.standardutxoset#add)
- [addArray](common_utxos.standardutxoset#addarray)
- [clone](common_utxos.standardutxoset#abstract-clone)
- [create](common_utxos.standardutxoset#abstract-create)
- [deserialize](common_utxos.standardutxoset#deserialize)
- [difference](common_utxos.standardutxoset#difference)
- [filter](common_utxos.standardutxoset#filter)
- [getAddresses](common_utxos.standardutxoset#getaddresses)
- [getAllUTXOStrings](common_utxos.standardutxoset#getallutxostrings)
- [getAllUTXOs](common_utxos.standardutxoset#getallutxos)
- [getAssetIDs](common_utxos.standardutxoset#getassetids)
- [getBalance](common_utxos.standardutxoset#getbalance)
- [getCodecID](common_utxos.standardutxoset#getcodecid)
- [getTypeID](common_utxos.standardutxoset#gettypeid)
- [getTypeName](common_utxos.standardutxoset#gettypename)
- [getUTXO](common_utxos.standardutxoset#getutxo)
- [getUTXOIDs](common_utxos.standardutxoset#getutxoids)
- [includes](common_utxos.standardutxoset#includes)
- [intersection](common_utxos.standardutxoset#intersection)
- [merge](common_utxos.standardutxoset#merge)
- [mergeByRule](common_utxos.standardutxoset#mergebyrule)
- [parseUTXO](common_utxos.standardutxoset#abstract-parseutxo)
- [remove](common_utxos.standardutxoset#remove)
- [removeArray](common_utxos.standardutxoset#removearray)
- [sanitizeObject](common_utxos.standardutxoset#sanitizeobject)
- [serialize](common_utxos.standardutxoset#serialize)
- [symDifference](common_utxos.standardutxoset#symdifference)
- [union](common_utxos.standardutxoset#union)

## Properties

### `Protected` \_codecID

• **\_codecID**: _number_ = undefined

_Inherited from [SigIdx](common_signature.sigidx).[\_codecID](common_signature.sigidx#protected-_codecid)_

_Defined in [src/utils/serialization.ts:51](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/serialization.ts#L51)_

---

### `Protected` \_typeID

• **\_typeID**: _any_ = undefined

_Overrides [Serializable](utils_serialization.serializable).[\_typeID](utils_serialization.serializable#protected-_typeid)_

_Defined in [src/common/utxos.ts:218](https://github.com/chain4travel/caminojs/blob/3883166/src/common/utxos.ts#L218)_

---

### `Protected` \_typeName

• **\_typeName**: _string_ = "StandardUTXOSet"

_Overrides [Serializable](utils_serialization.serializable).[\_typeName](utils_serialization.serializable#protected-_typename)_

_Defined in [src/common/utxos.ts:217](https://github.com/chain4travel/caminojs/blob/3883166/src/common/utxos.ts#L217)_

---

### `Protected` addressUTXOs

• **addressUTXOs**: _object_

_Defined in [src/common/utxos.ts:265](https://github.com/chain4travel/caminojs/blob/3883166/src/common/utxos.ts#L265)_

#### Type declaration:

- \[ **address**: _string_\]: object

- \[ **utxoid**: _string_\]: BN

---

### `Protected` utxos

• **utxos**: _object_

_Defined in [src/common/utxos.ts:264](https://github.com/chain4travel/caminojs/blob/3883166/src/common/utxos.ts#L264)_

#### Type declaration:

- \[ **utxoid**: _string_\]: UTXOClass

## Methods

### add

▸ **add**(`utxo`: UTXOClass | string, `overwrite`: boolean): _UTXOClass_

_Defined in [src/common/utxos.ts:299](https://github.com/chain4travel/caminojs/blob/3883166/src/common/utxos.ts#L299)_

Adds a [StandardUTXO](common_utxos.standardutxo) to the StandardUTXOSet.

**Parameters:**

| Name        | Type                    | Default | Description                                                                                              |
| ----------- | ----------------------- | ------- | -------------------------------------------------------------------------------------------------------- |
| `utxo`      | UTXOClass &#124; string | -       | Either a [StandardUTXO](common_utxos.standardutxo) an cb58 serialized string representing a StandardUTXO |
| `overwrite` | boolean                 | false   | If true, if the UTXOID already exists, overwrite it... default false                                     |

**Returns:** _UTXOClass_

A [StandardUTXO](common_utxos.standardutxo) if one was added and undefined if nothing was added.

---

### addArray

▸ **addArray**(`utxos`: string[] | UTXOClass[], `overwrite`: boolean): _[StandardUTXO](common_utxos.standardutxo)[]_

_Defined in [src/common/utxos.ts:337](https://github.com/chain4travel/caminojs/blob/3883166/src/common/utxos.ts#L337)_

Adds an array of [StandardUTXO](common_utxos.standardutxo)s to the [StandardUTXOSet](common_utxos.standardutxoset).

**Parameters:**

| Name        | Type                        | Default | Description                                                          |
| ----------- | --------------------------- | ------- | -------------------------------------------------------------------- |
| `utxos`     | string[] &#124; UTXOClass[] | -       | -                                                                    |
| `overwrite` | boolean                     | false   | If true, if the UTXOID already exists, overwrite it... default false |

**Returns:** _[StandardUTXO](common_utxos.standardutxo)[]_

An array of StandardUTXOs which were added.

---

### `Abstract` clone

▸ **clone**(): _this_

_Defined in [src/common/utxos.ts:561](https://github.com/chain4travel/caminojs/blob/3883166/src/common/utxos.ts#L561)_

**Returns:** _this_

---

### `Abstract` create

▸ **create**(...`args`: any[]): _this_

_Defined in [src/common/utxos.ts:563](https://github.com/chain4travel/caminojs/blob/3883166/src/common/utxos.ts#L563)_

**Parameters:**

| Name      | Type  |
| --------- | ----- |
| `...args` | any[] |

**Returns:** _this_

---

### deserialize

▸ **deserialize**(`fields`: object, `encoding?`: [SerializedEncoding](../modules/utils_serialization#serializedencoding)): _void_

_Inherited from [StandardParseableInput](common_inputs.standardparseableinput).[deserialize](common_inputs.standardparseableinput#deserialize)_

_Defined in [src/utils/serialization.ts:97](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/serialization.ts#L97)_

**Parameters:**

| Name        | Type                                                                    |
| ----------- | ----------------------------------------------------------------------- |
| `fields`    | object                                                                  |
| `encoding?` | [SerializedEncoding](../modules/utils_serialization#serializedencoding) |

**Returns:** _void_

---

### difference

▸ **difference**(`utxoset`: this): _this_

_Defined in [src/common/utxos.ts:620](https://github.com/chain4travel/caminojs/blob/3883166/src/common/utxos.ts#L620)_

Set difference between this set and a parameter.

**Parameters:**

| Name      | Type | Description           |
| --------- | ---- | --------------------- |
| `utxoset` | this | The set to difference |

**Returns:** _this_

A new StandardUTXOSet containing the difference

---

### filter

▸ **filter**(`args`: any[], `lambda`: function): _this_

_Defined in [src/common/utxos.ts:565](https://github.com/chain4travel/caminojs/blob/3883166/src/common/utxos.ts#L565)_

**Parameters:**

▪ **args**: _any[]_

▪ **lambda**: _function_

▸ (`utxo`: UTXOClass, ...`largs`: any[]): _boolean_

**Parameters:**

| Name       | Type      |
| ---------- | --------- |
| `utxo`     | UTXOClass |
| `...largs` | any[]     |

**Returns:** _this_

---

### getAddresses

▸ **getAddresses**(): _Buffer[]_

_Defined in [src/common/utxos.ts:496](https://github.com/chain4travel/caminojs/blob/3883166/src/common/utxos.ts#L496)_

Gets the addresses in the [StandardUTXOSet](common_utxos.standardutxoset) and returns an array of [Buffer](https://github.com/feross/buffer).

**Returns:** _Buffer[]_

---

### getAllUTXOStrings

▸ **getAllUTXOStrings**(`utxoids`: string[]): _string[]_

_Defined in [src/common/utxos.ts:439](https://github.com/chain4travel/caminojs/blob/3883166/src/common/utxos.ts#L439)_

Gets all the [StandardUTXO](common_utxos.standardutxo)s as strings, optionally that match with UTXOIDs in an array.

**Parameters:**

| Name      | Type     | Default   | Description                                                                                          |
| --------- | -------- | --------- | ---------------------------------------------------------------------------------------------------- |
| `utxoids` | string[] | undefined | An optional array of UTXOIDs, returns all [StandardUTXO](common_utxos.standardutxo)s if not provided |

**Returns:** _string[]_

An array of [StandardUTXO](common_utxos.standardutxo)s as cb58 serialized strings.

---

### getAllUTXOs

▸ **getAllUTXOs**(`utxoids`: string[]): _UTXOClass[]_

_Defined in [src/common/utxos.ts:420](https://github.com/chain4travel/caminojs/blob/3883166/src/common/utxos.ts#L420)_

Gets all the [StandardUTXO](common_utxos.standardutxo)s, optionally that match with UTXOIDs in an array

**Parameters:**

| Name      | Type     | Default   | Description                                                                                          |
| --------- | -------- | --------- | ---------------------------------------------------------------------------------------------------- |
| `utxoids` | string[] | undefined | An optional array of UTXOIDs, returns all [StandardUTXO](common_utxos.standardutxo)s if not provided |

**Returns:** _UTXOClass[]_

An array of [StandardUTXO](common_utxos.standardutxo)s.

---

### getAssetIDs

▸ **getAssetIDs**(`addresses`: Buffer[]): _Buffer[]_

_Defined in [src/common/utxos.ts:543](https://github.com/chain4travel/caminojs/blob/3883166/src/common/utxos.ts#L543)_

Gets all the Asset IDs, optionally that match with Asset IDs in an array

**Parameters:**

| Name        | Type     | Default   |
| ----------- | -------- | --------- |
| `addresses` | Buffer[] | undefined |

**Returns:** _Buffer[]_

An array of [Buffer](https://github.com/feross/buffer) representing the Asset IDs.

---

### getBalance

▸ **getBalance**(`addresses`: Buffer[], `assetID`: Buffer | string, `asOf`: BN): _BN_

_Defined in [src/common/utxos.ts:508](https://github.com/chain4travel/caminojs/blob/3883166/src/common/utxos.ts#L508)_

Returns the balance of a set of addresses in the StandardUTXOSet.

**Parameters:**

| Name        | Type                 | Default   | Description                                                                                            |
| ----------- | -------------------- | --------- | ------------------------------------------------------------------------------------------------------ |
| `addresses` | Buffer[]             | -         | An array of addresses                                                                                  |
| `assetID`   | Buffer &#124; string | -         | Either a [Buffer](https://github.com/feross/buffer) or an cb58 serialized representation of an AssetID |
| `asOf`      | BN                   | undefined | The timestamp to verify the transaction against as a [BN](https://github.com/indutny/bn.js/)           |

**Returns:** _BN_

Returns the total balance as a [BN](https://github.com/indutny/bn.js/).

---

### getCodecID

▸ **getCodecID**(): _number_

_Inherited from [SigIdx](common_signature.sigidx).[getCodecID](common_signature.sigidx#getcodecid)_

_Defined in [src/utils/serialization.ts:70](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/serialization.ts#L70)_

Used in serialization. Optional. TypeID is a number for the typeID of object being output.

**Returns:** _number_

---

### getTypeID

▸ **getTypeID**(): _number_

_Inherited from [SigIdx](common_signature.sigidx).[getTypeID](common_signature.sigidx#gettypeid)_

_Defined in [src/utils/serialization.ts:63](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/serialization.ts#L63)_

Used in serialization. Optional. TypeID is a number for the typeID of object being output.

**Returns:** _number_

---

### getTypeName

▸ **getTypeName**(): _string_

_Inherited from [SigIdx](common_signature.sigidx).[getTypeName](common_signature.sigidx#gettypename)_

_Defined in [src/utils/serialization.ts:56](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/serialization.ts#L56)_

Used in serialization. TypeName is a string name for the type of object being output.

**Returns:** _string_

---

### getUTXO

▸ **getUTXO**(`utxoid`: string): _UTXOClass_

_Defined in [src/common/utxos.ts:411](https://github.com/chain4travel/caminojs/blob/3883166/src/common/utxos.ts#L411)_

Gets a [StandardUTXO](common_utxos.standardutxo) from the [StandardUTXOSet](common_utxos.standardutxoset) by its UTXOID.

**Parameters:**

| Name     | Type   | Description                    |
| -------- | ------ | ------------------------------ |
| `utxoid` | string | String representing the UTXOID |

**Returns:** _UTXOClass_

A [StandardUTXO](common_utxos.standardutxo) if it exists in the set.

---

### getUTXOIDs

▸ **getUTXOIDs**(`addresses`: Buffer[], `spendable`: boolean): _string[]_

_Defined in [src/common/utxos.ts:464](https://github.com/chain4travel/caminojs/blob/3883166/src/common/utxos.ts#L464)_

Given an address or array of addresses, returns all the UTXOIDs for those addresses

**Parameters:**

| Name        | Type     | Default   | Description                                               |
| ----------- | -------- | --------- | --------------------------------------------------------- |
| `addresses` | Buffer[] | undefined | -                                                         |
| `spendable` | boolean  | true      | If true, only retrieves UTXOIDs whose locktime has passed |

**Returns:** _string[]_

An array of addresses.

---

### includes

▸ **includes**(`utxo`: UTXOClass | string): _boolean_

_Defined in [src/common/utxos.ts:274](https://github.com/chain4travel/caminojs/blob/3883166/src/common/utxos.ts#L274)_

Returns true if the [StandardUTXO](common_utxos.standardutxo) is in the StandardUTXOSet.

**Parameters:**

| Name   | Type                    | Description                                                                                             |
| ------ | ----------------------- | ------------------------------------------------------------------------------------------------------- |
| `utxo` | UTXOClass &#124; string | Either a [StandardUTXO](common_utxos.standardutxo) a cb58 serialized string representing a StandardUTXO |

**Returns:** _boolean_

---

### intersection

▸ **intersection**(`utxoset`: this): _this_

_Defined in [src/common/utxos.ts:606](https://github.com/chain4travel/caminojs/blob/3883166/src/common/utxos.ts#L606)_

Set intersetion between this set and a parameter.

**Parameters:**

| Name      | Type | Description          |
| --------- | ---- | -------------------- |
| `utxoset` | this | The set to intersect |

**Returns:** _this_

A new StandardUTXOSet containing the intersection

---

### merge

▸ **merge**(`utxoset`: this, `hasUTXOIDs`: string[]): _this_

_Defined in [src/common/utxos.ts:587](https://github.com/chain4travel/caminojs/blob/3883166/src/common/utxos.ts#L587)_

Returns a new set with copy of UTXOs in this and set parameter.

**Parameters:**

| Name         | Type     | Default   | Description                                                                                                                            |
| ------------ | -------- | --------- | -------------------------------------------------------------------------------------------------------------------------------------- |
| `utxoset`    | this     | -         | The [StandardUTXOSet](common_utxos.standardutxoset) to merge with this one                                                             |
| `hasUTXOIDs` | string[] | undefined | Will subselect a set of [StandardUTXO](common_utxos.standardutxo)s which have the UTXOIDs provided in this array, defults to all UTXOs |

**Returns:** _this_

A new StandardUTXOSet that contains all the filtered elements.

---

### mergeByRule

▸ **mergeByRule**(`utxoset`: this, `mergeRule`: [MergeRule](../modules/utils_constants#mergerule)): _this_

_Defined in [src/common/utxos.ts:670](https://github.com/chain4travel/caminojs/blob/3883166/src/common/utxos.ts#L670)_

Merges a set by the rule provided.

**`remarks`**
The merge rules are as follows:

- "intersection" - the intersection of the set
- "differenceSelf" - the difference between the existing data and new set
- "differenceNew" - the difference between the new data and the existing set
- "symDifference" - the union of the differences between both sets of data
- "union" - the unique set of all elements contained in both sets
- "unionMinusNew" - the unique set of all elements contained in both sets, excluding values only found in the new set
- "unionMinusSelf" - the unique set of all elements contained in both sets, excluding values only found in the existing set

**Parameters:**

| Name        | Type                                              | Description                                                    |
| ----------- | ------------------------------------------------- | -------------------------------------------------------------- |
| `utxoset`   | this                                              | The set to merge by the MergeRule                              |
| `mergeRule` | [MergeRule](../modules/utils_constants#mergerule) | The [MergeRule](../modules/utils_constants#mergerule) to apply |

**Returns:** _this_

A new StandardUTXOSet containing the merged data

---

### `Abstract` parseUTXO

▸ **parseUTXO**(`utxo`: UTXOClass | string): _UTXOClass_

_Defined in [src/common/utxos.ts:267](https://github.com/chain4travel/caminojs/blob/3883166/src/common/utxos.ts#L267)_

**Parameters:**

| Name   | Type                    |
| ------ | ----------------------- |
| `utxo` | UTXOClass &#124; string |

**Returns:** _UTXOClass_

---

### remove

▸ **remove**(`utxo`: UTXOClass | string): _UTXOClass_

_Defined in [src/common/utxos.ts:358](https://github.com/chain4travel/caminojs/blob/3883166/src/common/utxos.ts#L358)_

Removes a [StandardUTXO](common_utxos.standardutxo) from the [StandardUTXOSet](common_utxos.standardutxoset) if it exists.

**Parameters:**

| Name   | Type                    | Description                                                                                              |
| ------ | ----------------------- | -------------------------------------------------------------------------------------------------------- |
| `utxo` | UTXOClass &#124; string | Either a [StandardUTXO](common_utxos.standardutxo) an cb58 serialized string representing a StandardUTXO |

**Returns:** _UTXOClass_

A [StandardUTXO](common_utxos.standardutxo) if it was removed and undefined if nothing was removed.

---

### removeArray

▸ **removeArray**(`utxos`: string[] | UTXOClass[]): _UTXOClass[]_

_Defined in [src/common/utxos.ts:393](https://github.com/chain4travel/caminojs/blob/3883166/src/common/utxos.ts#L393)_

Removes an array of [StandardUTXO](common_utxos.standardutxo)s to the [StandardUTXOSet](common_utxos.standardutxoset).

**Parameters:**

| Name    | Type                        |
| ------- | --------------------------- |
| `utxos` | string[] &#124; UTXOClass[] |

**Returns:** _UTXOClass[]_

An array of UTXOs which were removed.

---

### sanitizeObject

▸ **sanitizeObject**(`obj`: object): _object_

_Inherited from [SigIdx](common_signature.sigidx).[sanitizeObject](common_signature.sigidx#sanitizeobject)_

_Defined in [src/utils/serialization.ts:77](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/serialization.ts#L77)_

Sanitize to prevent cross scripting attacks.

**Parameters:**

| Name  | Type   |
| ----- | ------ |
| `obj` | object |

**Returns:** _object_

---

### serialize

▸ **serialize**(`encoding`: [SerializedEncoding](../modules/utils_serialization#serializedencoding)): _object_

_Overrides [Serializable](utils_serialization.serializable).[serialize](utils_serialization.serializable#serialize)_

_Defined in [src/common/utxos.ts:220](https://github.com/chain4travel/caminojs/blob/3883166/src/common/utxos.ts#L220)_

**Parameters:**

| Name       | Type                                                                    | Default |
| ---------- | ----------------------------------------------------------------------- | ------- |
| `encoding` | [SerializedEncoding](../modules/utils_serialization#serializedencoding) | "hex"   |

**Returns:** _object_

---

### symDifference

▸ **symDifference**(`utxoset`: this): _this_

_Defined in [src/common/utxos.ts:634](https://github.com/chain4travel/caminojs/blob/3883166/src/common/utxos.ts#L634)_

Set symmetrical difference between this set and a parameter.

**Parameters:**

| Name      | Type | Description                       |
| --------- | ---- | --------------------------------- |
| `utxoset` | this | The set to symmetrical difference |

**Returns:** _this_

A new StandardUTXOSet containing the symmetrical difference

---

### union

▸ **union**(`utxoset`: this): _this_

_Defined in [src/common/utxos.ts:650](https://github.com/chain4travel/caminojs/blob/3883166/src/common/utxos.ts#L650)_

Set union between this set and a parameter.

**Parameters:**

| Name      | Type | Description      |
| --------- | ---- | ---------------- |
| `utxoset` | this | The set to union |

**Returns:** _this_

A new StandardUTXOSet containing the union
