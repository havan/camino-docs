# Class: UTXOSet

Class representing a set of [UTXO](api_evm_utxos.utxo)s.

## Hierarchy

↳ [StandardUTXOSet](common_utxos.standardutxoset)‹[UTXO](api_evm_utxos.utxo)›

↳ **UTXOSet**

## Index

### Properties

- [\_codecID](api_evm_utxos.utxoset#protected-_codecid)
- [\_typeID](api_evm_utxos.utxoset#protected-_typeid)
- [\_typeName](api_evm_utxos.utxoset#protected-_typename)
- [addressUTXOs](api_evm_utxos.utxoset#protected-addressutxos)
- [utxos](api_evm_utxos.utxoset#protected-utxos)

### Methods

- [\_feeCheck](api_evm_utxos.utxoset#_feecheck)
- [add](api_evm_utxos.utxoset#add)
- [addArray](api_evm_utxos.utxoset#addarray)
- [buildExportTx](api_evm_utxos.utxoset#buildexporttx)
- [buildImportTx](api_evm_utxos.utxoset#buildimporttx)
- [clone](api_evm_utxos.utxoset#clone)
- [create](api_evm_utxos.utxoset#create)
- [deserialize](api_evm_utxos.utxoset#deserialize)
- [difference](api_evm_utxos.utxoset#difference)
- [filter](api_evm_utxos.utxoset#filter)
- [getAddresses](api_evm_utxos.utxoset#getaddresses)
- [getAllUTXOStrings](api_evm_utxos.utxoset#getallutxostrings)
- [getAllUTXOs](api_evm_utxos.utxoset#getallutxos)
- [getAssetIDs](api_evm_utxos.utxoset#getassetids)
- [getBalance](api_evm_utxos.utxoset#getbalance)
- [getCodecID](api_evm_utxos.utxoset#getcodecid)
- [getMinimumSpendable](api_evm_utxos.utxoset#getminimumspendable)
- [getTypeID](api_evm_utxos.utxoset#gettypeid)
- [getTypeName](api_evm_utxos.utxoset#gettypename)
- [getUTXO](api_evm_utxos.utxoset#getutxo)
- [getUTXOIDs](api_evm_utxos.utxoset#getutxoids)
- [includes](api_evm_utxos.utxoset#includes)
- [intersection](api_evm_utxos.utxoset#intersection)
- [merge](api_evm_utxos.utxoset#merge)
- [mergeByRule](api_evm_utxos.utxoset#mergebyrule)
- [parseUTXO](api_evm_utxos.utxoset#parseutxo)
- [remove](api_evm_utxos.utxoset#remove)
- [removeArray](api_evm_utxos.utxoset#removearray)
- [sanitizeObject](api_evm_utxos.utxoset#sanitizeobject)
- [serialize](api_evm_utxos.utxoset#serialize)
- [symDifference](api_evm_utxos.utxoset#symdifference)
- [union](api_evm_utxos.utxoset#union)

## Properties

### `Protected` \_codecID

• **\_codecID**: _number_ = undefined

_Inherited from [SigIdx](common_signature.sigidx).[\_codecID](common_signature.sigidx#protected-_codecid)_

_Defined in [src/utils/serialization.ts:51](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/serialization.ts#L51)_

---

### `Protected` \_typeID

• **\_typeID**: _any_ = undefined

_Overrides [StandardUTXOSet](common_utxos.standardutxoset).[\_typeID](common_utxos.standardutxoset#protected-_typeid)_

_Defined in [src/apis/evm/utxos.ts:127](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/utxos.ts#L127)_

---

### `Protected` \_typeName

• **\_typeName**: _string_ = "UTXOSet"

_Overrides [StandardUTXOSet](common_utxos.standardutxoset).[\_typeName](common_utxos.standardutxoset#protected-_typename)_

_Defined in [src/apis/evm/utxos.ts:126](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/utxos.ts#L126)_

---

### `Protected` addressUTXOs

• **addressUTXOs**: _object_

_Inherited from [StandardUTXOSet](common_utxos.standardutxoset).[addressUTXOs](common_utxos.standardutxoset#protected-addressutxos)_

_Defined in [src/common/utxos.ts:265](https://github.com/chain4travel/caminojs/blob/3883166/src/common/utxos.ts#L265)_

#### Type declaration:

- \[ **address**: _string_\]: object

- \[ **utxoid**: _string_\]: BN

---

### `Protected` utxos

• **utxos**: _object_

_Inherited from [StandardUTXOSet](common_utxos.standardutxoset).[utxos](common_utxos.standardutxoset#protected-utxos)_

_Defined in [src/common/utxos.ts:264](https://github.com/chain4travel/caminojs/blob/3883166/src/common/utxos.ts#L264)_

#### Type declaration:

- \[ **utxoid**: _string_\]: [UTXO](api_evm_utxos.utxo)

## Methods

### \_feeCheck

▸ **\_feeCheck**(`fee`: BN, `feeAssetID`: Buffer): _boolean_

_Defined in [src/apis/evm/utxos.ts:203](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/utxos.ts#L203)_

**Parameters:**

| Name         | Type   |
| ------------ | ------ |
| `fee`        | BN     |
| `feeAssetID` | Buffer |

**Returns:** _boolean_

---

### add

▸ **add**(`utxo`: [UTXO](api_evm_utxos.utxo) | string, `overwrite`: boolean): _[UTXO](api_evm_utxos.utxo)_

_Inherited from [StandardUTXOSet](common_utxos.standardutxoset).[add](common_utxos.standardutxoset#add)_

_Defined in [src/common/utxos.ts:299](https://github.com/chain4travel/caminojs/blob/3883166/src/common/utxos.ts#L299)_

Adds a [StandardUTXO](common_utxos.standardutxo) to the StandardUTXOSet.

**Parameters:**

| Name        | Type                                     | Default | Description                                                                                              |
| ----------- | ---------------------------------------- | ------- | -------------------------------------------------------------------------------------------------------- |
| `utxo`      | [UTXO](api_evm_utxos.utxo) &#124; string | -       | Either a [StandardUTXO](common_utxos.standardutxo) an cb58 serialized string representing a StandardUTXO |
| `overwrite` | boolean                                  | false   | If true, if the UTXOID already exists, overwrite it... default false                                     |

**Returns:** _[UTXO](api_evm_utxos.utxo)_

A [StandardUTXO](common_utxos.standardutxo) if one was added and undefined if nothing was added.

---

### addArray

▸ **addArray**(`utxos`: string[] | [UTXO](api_evm_utxos.utxo)[], `overwrite`: boolean): _[StandardUTXO](common_utxos.standardutxo)[]_

_Inherited from [StandardUTXOSet](common_utxos.standardutxoset).[addArray](common_utxos.standardutxoset#addarray)_

_Defined in [src/common/utxos.ts:337](https://github.com/chain4travel/caminojs/blob/3883166/src/common/utxos.ts#L337)_

Adds an array of [StandardUTXO](common_utxos.standardutxo)s to the [StandardUTXOSet](common_utxos.standardutxoset).

**Parameters:**

| Name        | Type                                         | Default | Description                                                          |
| ----------- | -------------------------------------------- | ------- | -------------------------------------------------------------------- |
| `utxos`     | string[] &#124; [UTXO](api_evm_utxos.utxo)[] | -       | -                                                                    |
| `overwrite` | boolean                                      | false   | If true, if the UTXOID already exists, overwrite it... default false |

**Returns:** _[StandardUTXO](common_utxos.standardutxo)[]_

An array of StandardUTXOs which were added.

---

### buildExportTx

▸ **buildExportTx**(`networkID`: number, `blockchainID`: Buffer, `amount`: BN, `avaxAssetID`: Buffer, `toAddresses`: Buffer[], `fromAddresses`: Buffer[], `changeAddresses`: Buffer[], `destinationChain`: Buffer, `fee`: BN, `feeAssetID`: Buffer, `asOf`: BN, `locktime`: BN, `threshold`: number): _[UnsignedTx](api_evm_transactions.unsignedtx)_

_Defined in [src/apis/evm/utxos.ts:443](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/utxos.ts#L443)_

Creates an unsigned ExportTx transaction.

**Parameters:**

| Name               | Type     | Default   | Description                                                                                                               |
| ------------------ | -------- | --------- | ------------------------------------------------------------------------------------------------------------------------- |
| `networkID`        | number   | -         | The number representing NetworkID of the node                                                                             |
| `blockchainID`     | Buffer   | -         | The [Buffer](https://github.com/feross/buffer) representing the BlockchainID for the transaction                          |
| `amount`           | BN       | -         | The amount being exported as a [BN](https://github.com/indutny/bn.js/)                                                    |
| `avaxAssetID`      | Buffer   | -         | [Buffer](https://github.com/feross/buffer) of the AssetID for AVAX                                                        |
| `toAddresses`      | Buffer[] | -         | An array of addresses as [Buffer](https://github.com/feross/buffer) who recieves the AVAX                                 |
| `fromAddresses`    | Buffer[] | -         | An array of addresses as [Buffer](https://github.com/feross/buffer) who owns the AVAX                                     |
| `changeAddresses`  | Buffer[] | undefined | Optional. The addresses that can spend the change remaining from the spent UTXOs.                                         |
| `destinationChain` | Buffer   | undefined | Optional. A [Buffer](https://github.com/feross/buffer) for the chainid where to send the asset.                           |
| `fee`              | BN       | undefined | Optional. The amount of fees to burn in its smallest denomination, represented as [BN](https://github.com/indutny/bn.js/) |
| `feeAssetID`       | Buffer   | undefined | Optional. The assetID of the fees being burned.                                                                           |
| `asOf`             | BN       | UnixNow() | Optional. The timestamp to verify the transaction against as a [BN](https://github.com/indutny/bn.js/)                    |
| `locktime`         | BN       | new BN(0) | Optional. The locktime field created in the resulting outputs                                                             |
| `threshold`        | number   | 1         | Optional. The number of signatures required to spend the funds in the resultant UTXO                                      |

**Returns:** _[UnsignedTx](api_evm_transactions.unsignedtx)_

An unsigned transaction created from the passed in parameters.

---

### buildImportTx

▸ **buildImportTx**(`networkID`: number, `blockchainID`: Buffer, `toAddress`: string, `atomics`: [UTXO](api_evm_utxos.utxo)[], `sourceChain`: Buffer, `fee`: BN, `feeAssetID`: Buffer): _[UnsignedTx](api_evm_transactions.unsignedtx)_

_Defined in [src/apis/evm/utxos.ts:327](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/utxos.ts#L327)_

Creates an unsigned ImportTx transaction.

**Parameters:**

| Name           | Type                         | Default   | Description                                                                                                                                                                  |
| -------------- | ---------------------------- | --------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `networkID`    | number                       | -         | The number representing NetworkID of the node                                                                                                                                |
| `blockchainID` | Buffer                       | -         | The [Buffer](https://github.com/feross/buffer) representing the BlockchainID for the transaction                                                                             |
| `toAddress`    | string                       | -         | The address to send the funds                                                                                                                                                |
| `atomics`      | [UTXO](api_evm_utxos.utxo)[] | -         | -                                                                                                                                                                            |
| `sourceChain`  | Buffer                       | undefined | A [Buffer](https://github.com/feross/buffer) for the chainid where the imports are coming from.                                                                              |
| `fee`          | BN                           | undefined | Optional. The amount of fees to burn in its smallest denomination, represented as [BN](https://github.com/indutny/bn.js/). Fee will come from the inputs first, if they can. |
| `feeAssetID`   | Buffer                       | undefined | Optional. The assetID of the fees being burned.                                                                                                                              |

**Returns:** _[UnsignedTx](api_evm_transactions.unsignedtx)_

An unsigned transaction created from the passed in parameters.

---

### clone

▸ **clone**(): _this_

_Overrides [StandardUTXOSet](common_utxos.standardutxoset).[clone](common_utxos.standardutxoset#abstract-clone)_

_Defined in [src/apis/evm/utxos.ts:196](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/utxos.ts#L196)_

**Returns:** _this_

---

### create

▸ **create**(): _this_

_Overrides [StandardUTXOSet](common_utxos.standardutxoset).[create](common_utxos.standardutxoset#abstract-create)_

_Defined in [src/apis/evm/utxos.ts:192](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/utxos.ts#L192)_

**Returns:** _this_

---

### deserialize

▸ **deserialize**(`fields`: object, `encoding`: [SerializedEncoding](../modules/utils_serialization#serializedencoding)): _void_

_Overrides [StandardParseableInput](common_inputs.standardparseableinput).[deserialize](common_inputs.standardparseableinput#deserialize)_

_Defined in [src/apis/evm/utxos.ts:131](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/utxos.ts#L131)_

**Parameters:**

| Name       | Type                                                                    | Default |
| ---------- | ----------------------------------------------------------------------- | ------- |
| `fields`   | object                                                                  | -       |
| `encoding` | [SerializedEncoding](../modules/utils_serialization#serializedencoding) | "hex"   |

**Returns:** _void_

---

### difference

▸ **difference**(`utxoset`: this): _this_

_Inherited from [StandardUTXOSet](common_utxos.standardutxoset).[difference](common_utxos.standardutxoset#difference)_

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

_Inherited from [StandardUTXOSet](common_utxos.standardutxoset).[filter](common_utxos.standardutxoset#filter)_

_Defined in [src/common/utxos.ts:565](https://github.com/chain4travel/caminojs/blob/3883166/src/common/utxos.ts#L565)_

**Parameters:**

▪ **args**: _any[]_

▪ **lambda**: _function_

▸ (`utxo`: [UTXO](api_evm_utxos.utxo), ...`largs`: any[]): _boolean_

**Parameters:**

| Name       | Type                       |
| ---------- | -------------------------- |
| `utxo`     | [UTXO](api_evm_utxos.utxo) |
| `...largs` | any[]                      |

**Returns:** _this_

---

### getAddresses

▸ **getAddresses**(): _Buffer[]_

_Inherited from [StandardUTXOSet](common_utxos.standardutxoset).[getAddresses](common_utxos.standardutxoset#getaddresses)_

_Defined in [src/common/utxos.ts:496](https://github.com/chain4travel/caminojs/blob/3883166/src/common/utxos.ts#L496)_

Gets the addresses in the [StandardUTXOSet](common_utxos.standardutxoset) and returns an array of [Buffer](https://github.com/feross/buffer).

**Returns:** _Buffer[]_

---

### getAllUTXOStrings

▸ **getAllUTXOStrings**(`utxoids`: string[]): _string[]_

_Inherited from [StandardUTXOSet](common_utxos.standardutxoset).[getAllUTXOStrings](common_utxos.standardutxoset#getallutxostrings)_

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

▸ **getAllUTXOs**(`utxoids`: string[]): _[UTXO](api_evm_utxos.utxo)[]_

_Inherited from [StandardUTXOSet](common_utxos.standardutxoset).[getAllUTXOs](common_utxos.standardutxoset#getallutxos)_

_Defined in [src/common/utxos.ts:420](https://github.com/chain4travel/caminojs/blob/3883166/src/common/utxos.ts#L420)_

Gets all the [StandardUTXO](common_utxos.standardutxo)s, optionally that match with UTXOIDs in an array

**Parameters:**

| Name      | Type     | Default   | Description                                                                                          |
| --------- | -------- | --------- | ---------------------------------------------------------------------------------------------------- |
| `utxoids` | string[] | undefined | An optional array of UTXOIDs, returns all [StandardUTXO](common_utxos.standardutxo)s if not provided |

**Returns:** _[UTXO](api_evm_utxos.utxo)[]_

An array of [StandardUTXO](common_utxos.standardutxo)s.

---

### getAssetIDs

▸ **getAssetIDs**(`addresses`: Buffer[]): _Buffer[]_

_Inherited from [StandardUTXOSet](common_utxos.standardutxoset).[getAssetIDs](common_utxos.standardutxoset#getassetids)_

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

_Inherited from [StandardUTXOSet](common_utxos.standardutxoset).[getBalance](common_utxos.standardutxoset#getbalance)_

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

### getMinimumSpendable

▸ **getMinimumSpendable**(`aad`: [AssetAmountDestination](api_evm_utxos.assetamountdestination), `asOf`: BN, `locktime`: BN, `threshold`: number): _[Error](src_utils.avalancheerror#static-error)_

_Defined in [src/apis/evm/utxos.ts:212](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/utxos.ts#L212)_

**Parameters:**

| Name        | Type                                                           | Default   |
| ----------- | -------------------------------------------------------------- | --------- |
| `aad`       | [AssetAmountDestination](api_evm_utxos.assetamountdestination) | -         |
| `asOf`      | BN                                                             | UnixNow() |
| `locktime`  | BN                                                             | new BN(0) |
| `threshold` | number                                                         | 1         |

**Returns:** _[Error](src_utils.avalancheerror#static-error)_

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

▸ **getUTXO**(`utxoid`: string): _[UTXO](api_evm_utxos.utxo)_

_Inherited from [StandardUTXOSet](common_utxos.standardutxoset).[getUTXO](common_utxos.standardutxoset#getutxo)_

_Defined in [src/common/utxos.ts:411](https://github.com/chain4travel/caminojs/blob/3883166/src/common/utxos.ts#L411)_

Gets a [StandardUTXO](common_utxos.standardutxo) from the [StandardUTXOSet](common_utxos.standardutxoset) by its UTXOID.

**Parameters:**

| Name     | Type   | Description                    |
| -------- | ------ | ------------------------------ |
| `utxoid` | string | String representing the UTXOID |

**Returns:** _[UTXO](api_evm_utxos.utxo)_

A [StandardUTXO](common_utxos.standardutxo) if it exists in the set.

---

### getUTXOIDs

▸ **getUTXOIDs**(`addresses`: Buffer[], `spendable`: boolean): _string[]_

_Inherited from [StandardUTXOSet](common_utxos.standardutxoset).[getUTXOIDs](common_utxos.standardutxoset#getutxoids)_

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

▸ **includes**(`utxo`: [UTXO](api_evm_utxos.utxo) | string): _boolean_

_Inherited from [StandardUTXOSet](common_utxos.standardutxoset).[includes](common_utxos.standardutxoset#includes)_

_Defined in [src/common/utxos.ts:274](https://github.com/chain4travel/caminojs/blob/3883166/src/common/utxos.ts#L274)_

Returns true if the [StandardUTXO](common_utxos.standardutxo) is in the StandardUTXOSet.

**Parameters:**

| Name   | Type                                     | Description                                                                                             |
| ------ | ---------------------------------------- | ------------------------------------------------------------------------------------------------------- |
| `utxo` | [UTXO](api_evm_utxos.utxo) &#124; string | Either a [StandardUTXO](common_utxos.standardutxo) a cb58 serialized string representing a StandardUTXO |

**Returns:** _boolean_

---

### intersection

▸ **intersection**(`utxoset`: this): _this_

_Inherited from [StandardUTXOSet](common_utxos.standardutxoset).[intersection](common_utxos.standardutxoset#intersection)_

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

_Inherited from [StandardUTXOSet](common_utxos.standardutxoset).[merge](common_utxos.standardutxoset#merge)_

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

_Inherited from [StandardUTXOSet](common_utxos.standardutxoset).[mergeByRule](common_utxos.standardutxoset#mergebyrule)_

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

### parseUTXO

▸ **parseUTXO**(`utxo`: [UTXO](api_evm_utxos.utxo) | string): _[UTXO](api_evm_utxos.utxo)_

_Overrides [StandardUTXOSet](common_utxos.standardutxoset).[parseUTXO](common_utxos.standardutxoset#abstract-parseutxo)_

_Defined in [src/apis/evm/utxos.ts:176](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/utxos.ts#L176)_

**Parameters:**

| Name   | Type                                     |
| ------ | ---------------------------------------- |
| `utxo` | [UTXO](api_evm_utxos.utxo) &#124; string |

**Returns:** _[UTXO](api_evm_utxos.utxo)_

---

### remove

▸ **remove**(`utxo`: [UTXO](api_evm_utxos.utxo) | string): _[UTXO](api_evm_utxos.utxo)_

_Inherited from [StandardUTXOSet](common_utxos.standardutxoset).[remove](common_utxos.standardutxoset#remove)_

_Defined in [src/common/utxos.ts:358](https://github.com/chain4travel/caminojs/blob/3883166/src/common/utxos.ts#L358)_

Removes a [StandardUTXO](common_utxos.standardutxo) from the [StandardUTXOSet](common_utxos.standardutxoset) if it exists.

**Parameters:**

| Name   | Type                                     | Description                                                                                              |
| ------ | ---------------------------------------- | -------------------------------------------------------------------------------------------------------- |
| `utxo` | [UTXO](api_evm_utxos.utxo) &#124; string | Either a [StandardUTXO](common_utxos.standardutxo) an cb58 serialized string representing a StandardUTXO |

**Returns:** _[UTXO](api_evm_utxos.utxo)_

A [StandardUTXO](common_utxos.standardutxo) if it was removed and undefined if nothing was removed.

---

### removeArray

▸ **removeArray**(`utxos`: string[] | [UTXO](api_evm_utxos.utxo)[]): _[UTXO](api_evm_utxos.utxo)[]_

_Inherited from [StandardUTXOSet](common_utxos.standardutxoset).[removeArray](common_utxos.standardutxoset#removearray)_

_Defined in [src/common/utxos.ts:393](https://github.com/chain4travel/caminojs/blob/3883166/src/common/utxos.ts#L393)_

Removes an array of [StandardUTXO](common_utxos.standardutxo)s to the [StandardUTXOSet](common_utxos.standardutxoset).

**Parameters:**

| Name    | Type                                         |
| ------- | -------------------------------------------- |
| `utxos` | string[] &#124; [UTXO](api_evm_utxos.utxo)[] |

**Returns:** _[UTXO](api_evm_utxos.utxo)[]_

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

_Inherited from [StandardUTXOSet](common_utxos.standardutxoset).[serialize](common_utxos.standardutxoset#serialize)_

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

_Inherited from [StandardUTXOSet](common_utxos.standardutxoset).[symDifference](common_utxos.standardutxoset#symdifference)_

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

_Inherited from [StandardUTXOSet](common_utxos.standardutxoset).[union](common_utxos.standardutxoset#union)_

_Defined in [src/common/utxos.ts:650](https://github.com/chain4travel/caminojs/blob/3883166/src/common/utxos.ts#L650)_

Set union between this set and a parameter.

**Parameters:**

| Name      | Type | Description      |
| --------- | ---- | ---------------- |
| `utxoset` | this | The set to union |

**Returns:** _this_

A new StandardUTXOSet containing the union
