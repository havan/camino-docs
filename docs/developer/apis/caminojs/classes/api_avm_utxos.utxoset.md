# Class: UTXOSet

Class representing a set of [UTXO](api_avm_utxos.utxo)s.

## Hierarchy

↳ [StandardUTXOSet](common_utxos.standardutxoset)‹[UTXO](api_avm_utxos.utxo)›

↳ **UTXOSet**

## Index

### Properties

- [\_codecID](api_avm_utxos.utxoset#protected-_codecid)
- [\_typeID](api_avm_utxos.utxoset#protected-_typeid)
- [\_typeName](api_avm_utxos.utxoset#protected-_typename)
- [addressUTXOs](api_avm_utxos.utxoset#protected-addressutxos)
- [utxos](api_avm_utxos.utxoset#protected-utxos)

### Methods

- [\_feeCheck](api_avm_utxos.utxoset#_feecheck)
- [add](api_avm_utxos.utxoset#add)
- [addArray](api_avm_utxos.utxoset#addarray)
- [buildBaseTx](api_avm_utxos.utxoset#buildbasetx)
- [buildCreateAssetTx](api_avm_utxos.utxoset#buildcreateassettx)
- [buildCreateNFTAssetTx](api_avm_utxos.utxoset#buildcreatenftassettx)
- [buildCreateNFTMintTx](api_avm_utxos.utxoset#buildcreatenftminttx)
- [buildExportTx](api_avm_utxos.utxoset#buildexporttx)
- [buildImportTx](api_avm_utxos.utxoset#buildimporttx)
- [buildNFTTransferTx](api_avm_utxos.utxoset#buildnfttransfertx)
- [buildSECPMintTx](api_avm_utxos.utxoset#buildsecpminttx)
- [clone](api_avm_utxos.utxoset#clone)
- [create](api_avm_utxos.utxoset#create)
- [deserialize](api_avm_utxos.utxoset#deserialize)
- [difference](api_avm_utxos.utxoset#difference)
- [filter](api_avm_utxos.utxoset#filter)
- [getAddresses](api_avm_utxos.utxoset#getaddresses)
- [getAllUTXOStrings](api_avm_utxos.utxoset#getallutxostrings)
- [getAllUTXOs](api_avm_utxos.utxoset#getallutxos)
- [getAssetIDs](api_avm_utxos.utxoset#getassetids)
- [getBalance](api_avm_utxos.utxoset#getbalance)
- [getCodecID](api_avm_utxos.utxoset#getcodecid)
- [getMinimumSpendable](api_avm_utxos.utxoset#getminimumspendable)
- [getTypeID](api_avm_utxos.utxoset#gettypeid)
- [getTypeName](api_avm_utxos.utxoset#gettypename)
- [getUTXO](api_avm_utxos.utxoset#getutxo)
- [getUTXOIDs](api_avm_utxos.utxoset#getutxoids)
- [includes](api_avm_utxos.utxoset#includes)
- [intersection](api_avm_utxos.utxoset#intersection)
- [merge](api_avm_utxos.utxoset#merge)
- [mergeByRule](api_avm_utxos.utxoset#mergebyrule)
- [parseUTXO](api_avm_utxos.utxoset#parseutxo)
- [remove](api_avm_utxos.utxoset#remove)
- [removeArray](api_avm_utxos.utxoset#removearray)
- [sanitizeObject](api_avm_utxos.utxoset#sanitizeobject)
- [serialize](api_avm_utxos.utxoset#serialize)
- [symDifference](api_avm_utxos.utxoset#symdifference)
- [union](api_avm_utxos.utxoset#union)

## Properties

### `Protected` \_codecID

• **\_codecID**: _number_ = undefined

_Inherited from [SigIdx](common_signature.sigidx).[\_codecID](common_signature.sigidx#protected-_codecid)_

_Defined in [src/utils/serialization.ts:51](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/serialization.ts#L51)_

---

### `Protected` \_typeID

• **\_typeID**: _any_ = undefined

_Overrides [StandardUTXOSet](common_utxos.standardutxoset).[\_typeID](common_utxos.standardutxoset#protected-_typeid)_

_Defined in [src/apis/avm/utxos.ts:141](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/utxos.ts#L141)_

---

### `Protected` \_typeName

• **\_typeName**: _string_ = "UTXOSet"

_Overrides [StandardUTXOSet](common_utxos.standardutxoset).[\_typeName](common_utxos.standardutxoset#protected-_typename)_

_Defined in [src/apis/avm/utxos.ts:140](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/utxos.ts#L140)_

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

- \[ **utxoid**: _string_\]: [UTXO](api_avm_utxos.utxo)

## Methods

### \_feeCheck

▸ **\_feeCheck**(`fee`: BN, `feeAssetID`: Buffer): _boolean_

_Defined in [src/apis/avm/utxos.ts:217](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/utxos.ts#L217)_

**Parameters:**

| Name         | Type   |
| ------------ | ------ |
| `fee`        | BN     |
| `feeAssetID` | Buffer |

**Returns:** _boolean_

---

### add

▸ **add**(`utxo`: [UTXO](api_avm_utxos.utxo) | string, `overwrite`: boolean): _[UTXO](api_avm_utxos.utxo)_

_Inherited from [StandardUTXOSet](common_utxos.standardutxoset).[add](common_utxos.standardutxoset#add)_

_Defined in [src/common/utxos.ts:299](https://github.com/chain4travel/caminojs/blob/3883166/src/common/utxos.ts#L299)_

Adds a [StandardUTXO](common_utxos.standardutxo) to the StandardUTXOSet.

**Parameters:**

| Name        | Type                                     | Default | Description                                                                                              |
| ----------- | ---------------------------------------- | ------- | -------------------------------------------------------------------------------------------------------- |
| `utxo`      | [UTXO](api_avm_utxos.utxo) &#124; string | -       | Either a [StandardUTXO](common_utxos.standardutxo) an cb58 serialized string representing a StandardUTXO |
| `overwrite` | boolean                                  | false   | If true, if the UTXOID already exists, overwrite it... default false                                     |

**Returns:** _[UTXO](api_avm_utxos.utxo)_

A [StandardUTXO](common_utxos.standardutxo) if one was added and undefined if nothing was added.

---

### addArray

▸ **addArray**(`utxos`: string[] | [UTXO](api_avm_utxos.utxo)[], `overwrite`: boolean): _[StandardUTXO](common_utxos.standardutxo)[]_

_Inherited from [StandardUTXOSet](common_utxos.standardutxoset).[addArray](common_utxos.standardutxoset#addarray)_

_Defined in [src/common/utxos.ts:337](https://github.com/chain4travel/caminojs/blob/3883166/src/common/utxos.ts#L337)_

Adds an array of [StandardUTXO](common_utxos.standardutxo)s to the [StandardUTXOSet](common_utxos.standardutxoset).

**Parameters:**

| Name        | Type                                         | Default | Description                                                          |
| ----------- | -------------------------------------------- | ------- | -------------------------------------------------------------------- |
| `utxos`     | string[] &#124; [UTXO](api_avm_utxos.utxo)[] | -       | -                                                                    |
| `overwrite` | boolean                                      | false   | If true, if the UTXOID already exists, overwrite it... default false |

**Returns:** _[StandardUTXO](common_utxos.standardutxo)[]_

An array of StandardUTXOs which were added.

---

### buildBaseTx

▸ **buildBaseTx**(`networkID`: number, `blockchainID`: Buffer, `amount`: BN, `assetID`: Buffer, `toAddresses`: Buffer[], `fromAddresses`: Buffer[], `changeAddresses`: Buffer[], `fee`: BN, `feeAssetID`: Buffer, `memo`: Buffer, `asOf`: BN, `locktime`: BN, `threshold`: number): _[UnsignedTx](api_avm_transactions.unsignedtx)_

_Defined in [src/apis/avm/utxos.ts:351](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/utxos.ts#L351)_

Creates an [UnsignedTx](api_evm_transactions.unsignedtx) wrapping a [BaseTx](api_avm_basetx.basetx). For more granular control, you may create your own
[UnsignedTx](api_evm_transactions.unsignedtx) wrapping a [BaseTx](api_avm_basetx.basetx) manually (with their corresponding [TransferableInput](api_evm_inputs.transferableinput)s and [TransferableOutput](api_evm_outputs.transferableoutput)s).

**Parameters:**

| Name              | Type     | Default   | Description                                                                                                               |
| ----------------- | -------- | --------- | ------------------------------------------------------------------------------------------------------------------------- |
| `networkID`       | number   | -         | The number representing NetworkID of the node                                                                             |
| `blockchainID`    | Buffer   | -         | The [Buffer](https://github.com/feross/buffer) representing the BlockchainID for the transaction                          |
| `amount`          | BN       | -         | The amount of the asset to be spent in its smallest denomination, represented as [BN](https://github.com/indutny/bn.js/). |
| `assetID`         | Buffer   | -         | [Buffer](https://github.com/feross/buffer) of the asset ID for the UTXO                                                   |
| `toAddresses`     | Buffer[] | -         | The addresses to send the funds                                                                                           |
| `fromAddresses`   | Buffer[] | -         | The addresses being used to send the funds from the UTXOs [Buffer](https://github.com/feross/buffer)                      |
| `changeAddresses` | Buffer[] | undefined | Optional. The addresses that can spend the change remaining from the spent UTXOs. Default: toAddresses                    |
| `fee`             | BN       | undefined | Optional. The amount of fees to burn in its smallest denomination, represented as [BN](https://github.com/indutny/bn.js/) |
| `feeAssetID`      | Buffer   | undefined | Optional. The assetID of the fees being burned. Default: assetID                                                          |
| `memo`            | Buffer   | undefined | Optional. Contains arbitrary data, up to 256 bytes                                                                        |
| `asOf`            | BN       | UnixNow() | Optional. The timestamp to verify the transaction against as a [BN](https://github.com/indutny/bn.js/)                    |
| `locktime`        | BN       | new BN(0) | Optional. The locktime field created in the resulting outputs                                                             |
| `threshold`       | number   | 1         | Optional. The number of signatures required to spend the funds in the resultant UTXO                                      |

**Returns:** _[UnsignedTx](api_avm_transactions.unsignedtx)_

An unsigned transaction created from the passed in parameters.

---

### buildCreateAssetTx

▸ **buildCreateAssetTx**(`networkID`: number, `blockchainID`: Buffer, `fromAddresses`: Buffer[], `changeAddresses`: Buffer[], `initialState`: [InitialStates](api_avm_initialstates.initialstates), `name`: string, `symbol`: string, `denomination`: number, `mintOutputs`: [SECPMintOutput](api_avm_outputs.secpmintoutput)[], `fee`: BN, `feeAssetID`: Buffer, `memo`: Buffer, `asOf`: BN): _[UnsignedTx](api_avm_transactions.unsignedtx)_

_Defined in [src/apis/avm/utxos.ts:442](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/utxos.ts#L442)_

Creates an unsigned Create Asset transaction. For more granular control, you may create your own
[[CreateAssetTX]] manually (with their corresponding [TransferableInput](api_evm_inputs.transferableinput)s, [TransferableOutput](api_evm_outputs.transferableoutput)s).

**Parameters:**

| Name              | Type                                                 | Default   | Description                                                                                                                                             |
| ----------------- | ---------------------------------------------------- | --------- | ------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `networkID`       | number                                               | -         | The number representing NetworkID of the node                                                                                                           |
| `blockchainID`    | Buffer                                               | -         | The [Buffer](https://github.com/feross/buffer) representing the BlockchainID for the transaction                                                        |
| `fromAddresses`   | Buffer[]                                             | -         | The addresses being used to send the funds from the UTXOs [Buffer](https://github.com/feross/buffer)                                                    |
| `changeAddresses` | Buffer[]                                             | -         | Optional. The addresses that can spend the change remaining from the spent UTXOs                                                                        |
| `initialState`    | [InitialStates](api_avm_initialstates.initialstates) | -         | The [InitialStates](api_avm_initialstates.initialstates) that represent the intial state of a created asset                                             |
| `name`            | string                                               | -         | String for the descriptive name of the asset                                                                                                            |
| `symbol`          | string                                               | -         | String for the ticker symbol of the asset                                                                                                               |
| `denomination`    | number                                               | -         | Optional number for the denomination which is 10^D. D must be >= 0 and <= 32. Ex: $1 AVAX = 10^9 $nAVAX                                                 |
| `mintOutputs`     | [SECPMintOutput](api_avm_outputs.secpmintoutput)[]   | undefined | Optional. Array of [SECPMintOutput](api_avm_outputs.secpmintoutput)s to be included in the transaction. These outputs can be spent to mint more tokens. |
| `fee`             | BN                                                   | undefined | Optional. The amount of fees to burn in its smallest denomination, represented as [BN](https://github.com/indutny/bn.js/)                               |
| `feeAssetID`      | Buffer                                               | undefined | Optional. The assetID of the fees being burned.                                                                                                         |
| `memo`            | Buffer                                               | undefined | Optional contains arbitrary bytes, up to 256 bytes                                                                                                      |
| `asOf`            | BN                                                   | UnixNow() | Optional. The timestamp to verify the transaction against as a [BN](https://github.com/indutny/bn.js/)                                                  |

**Returns:** _[UnsignedTx](api_avm_transactions.unsignedtx)_

An unsigned transaction created from the passed in parameters.

---

### buildCreateNFTAssetTx

▸ **buildCreateNFTAssetTx**(`networkID`: number, `blockchainID`: Buffer, `fromAddresses`: Buffer[], `changeAddresses`: Buffer[], `minterSets`: [MinterSet](api_avm_minterset.minterset)[], `name`: string, `symbol`: string, `fee`: BN, `feeAssetID`: Buffer, `memo`: Buffer, `asOf`: BN, `locktime`: BN): _[UnsignedTx](api_avm_transactions.unsignedtx)_

_Defined in [src/apis/avm/utxos.ts:615](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/utxos.ts#L615)_

Creates an unsigned Create Asset transaction. For more granular control, you may create your own
[[CreateAssetTX]] manually (with their corresponding [TransferableInput](api_evm_inputs.transferableinput)s, [TransferableOutput](api_evm_outputs.transferableoutput)s).

**Parameters:**

| Name              | Type                                       | Default   | Description                                                                                                               |
| ----------------- | ------------------------------------------ | --------- | ------------------------------------------------------------------------------------------------------------------------- |
| `networkID`       | number                                     | -         | The number representing NetworkID of the node                                                                             |
| `blockchainID`    | Buffer                                     | -         | The [Buffer](https://github.com/feross/buffer) representing the BlockchainID for the transaction                          |
| `fromAddresses`   | Buffer[]                                   | -         | The addresses being used to send the funds from the UTXOs [Buffer](https://github.com/feross/buffer)                      |
| `changeAddresses` | Buffer[]                                   | -         | Optional. The addresses that can spend the change remaining from the spent UTXOs.                                         |
| `minterSets`      | [MinterSet](api_avm_minterset.minterset)[] | -         | The minters and thresholds required to mint this nft asset                                                                |
| `name`            | string                                     | -         | String for the descriptive name of the nft asset                                                                          |
| `symbol`          | string                                     | -         | String for the ticker symbol of the nft asset                                                                             |
| `fee`             | BN                                         | undefined | Optional. The amount of fees to burn in its smallest denomination, represented as [BN](https://github.com/indutny/bn.js/) |
| `feeAssetID`      | Buffer                                     | undefined | Optional. The assetID of the fees being burned.                                                                           |
| `memo`            | Buffer                                     | undefined | Optional contains arbitrary bytes, up to 256 bytes                                                                        |
| `asOf`            | BN                                         | UnixNow() | Optional. The timestamp to verify the transaction against as a [BN](https://github.com/indutny/bn.js/)                    |
| `locktime`        | BN                                         | undefined | Optional. The locktime field created in the resulting mint output                                                         |

**Returns:** _[UnsignedTx](api_avm_transactions.unsignedtx)_

An unsigned transaction created from the passed in parameters.

---

### buildCreateNFTMintTx

▸ **buildCreateNFTMintTx**(`networkID`: number, `blockchainID`: Buffer, `owners`: [OutputOwners](common_output.outputowners)[], `fromAddresses`: Buffer[], `changeAddresses`: Buffer[], `utxoids`: string[], `groupID`: number, `payload`: Buffer, `fee`: BN, `feeAssetID`: Buffer, `memo`: Buffer, `asOf`: BN): _[UnsignedTx](api_avm_transactions.unsignedtx)_

_Defined in [src/apis/avm/utxos.ts:693](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/utxos.ts#L693)_

Creates an unsigned NFT mint transaction. For more granular control, you may create your own
[OperationTx](api_avm_operationtx.operationtx) manually (with their corresponding [TransferableInput](api_evm_inputs.transferableinput)s, [TransferableOutput](api_evm_outputs.transferableoutput)s, and [[TransferOperation]]s).

**Parameters:**

| Name              | Type                                         | Default   | Description                                                                                                               |
| ----------------- | -------------------------------------------- | --------- | ------------------------------------------------------------------------------------------------------------------------- |
| `networkID`       | number                                       | -         | The number representing NetworkID of the node                                                                             |
| `blockchainID`    | Buffer                                       | -         | The [Buffer](https://github.com/feross/buffer) representing the BlockchainID for the transaction                          |
| `owners`          | [OutputOwners](common_output.outputowners)[] | -         | An array of [OutputOwners](../modules/src_common#outputowners) who will be given the NFTs.                                |
| `fromAddresses`   | Buffer[]                                     | -         | The addresses being used to send the funds from the UTXOs                                                                 |
| `changeAddresses` | Buffer[]                                     | -         | Optional. The addresses that can spend the change remaining from the spent UTXOs.                                         |
| `utxoids`         | string[]                                     | -         | An array of strings for the NFTs being transferred                                                                        |
| `groupID`         | number                                       | 0         | Optional. The group this NFT is issued to.                                                                                |
| `payload`         | Buffer                                       | undefined | Optional. Data for NFT Payload.                                                                                           |
| `fee`             | BN                                           | undefined | Optional. The amount of fees to burn in its smallest denomination, represented as [BN](https://github.com/indutny/bn.js/) |
| `feeAssetID`      | Buffer                                       | undefined | Optional. The assetID of the fees being burned.                                                                           |
| `memo`            | Buffer                                       | undefined | Optional contains arbitrary bytes, up to 256 bytes                                                                        |
| `asOf`            | BN                                           | UnixNow() | Optional. The timestamp to verify the transaction against as a [BN](https://github.com/indutny/bn.js/)                    |

**Returns:** _[UnsignedTx](api_avm_transactions.unsignedtx)_

An unsigned transaction created from the passed in parameters.

---

### buildExportTx

▸ **buildExportTx**(`networkID`: number, `blockchainID`: Buffer, `amount`: BN, `assetID`: Buffer, `toAddresses`: Buffer[], `fromAddresses`: Buffer[], `changeAddresses`: Buffer[], `destinationChain`: Buffer, `fee`: BN, `feeAssetID`: Buffer, `memo`: Buffer, `asOf`: BN, `locktime`: BN, `threshold`: number): _[UnsignedTx](api_avm_transactions.unsignedtx)_

_Defined in [src/apis/avm/utxos.ts:1029](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/utxos.ts#L1029)_

Creates an unsigned ExportTx transaction.

**Parameters:**

| Name               | Type     | Default   | Description                                                                                                               |
| ------------------ | -------- | --------- | ------------------------------------------------------------------------------------------------------------------------- |
| `networkID`        | number   | -         | The number representing NetworkID of the node                                                                             |
| `blockchainID`     | Buffer   | -         | The [Buffer](https://github.com/feross/buffer) representing the BlockchainID for the transaction                          |
| `amount`           | BN       | -         | The amount being exported as a [BN](https://github.com/indutny/bn.js/)                                                    |
| `assetID`          | Buffer   | -         | -                                                                                                                         |
| `toAddresses`      | Buffer[] | -         | An array of addresses as [Buffer](https://github.com/feross/buffer) who recieves the AVAX                                 |
| `fromAddresses`    | Buffer[] | -         | An array of addresses as [Buffer](https://github.com/feross/buffer) who owns the AVAX                                     |
| `changeAddresses`  | Buffer[] | undefined | Optional. The addresses that can spend the change remaining from the spent UTXOs.                                         |
| `destinationChain` | Buffer   | undefined | Optional. A [Buffer](https://github.com/feross/buffer) for the chainid where to send the asset.                           |
| `fee`              | BN       | undefined | Optional. The amount of fees to burn in its smallest denomination, represented as [BN](https://github.com/indutny/bn.js/) |
| `feeAssetID`       | Buffer   | undefined | Optional. The assetID of the fees being burned.                                                                           |
| `memo`             | Buffer   | undefined | Optional contains arbitrary bytes, up to 256 bytes                                                                        |
| `asOf`             | BN       | UnixNow() | Optional. The timestamp to verify the transaction against as a [BN](https://github.com/indutny/bn.js/)                    |
| `locktime`         | BN       | new BN(0) | Optional. The locktime field created in the resulting outputs                                                             |
| `threshold`        | number   | 1         | Optional. The number of signatures required to spend the funds in the resultant UTXO                                      |

**Returns:** _[UnsignedTx](api_avm_transactions.unsignedtx)_

An unsigned transaction created from the passed in parameters.

---

### buildImportTx

▸ **buildImportTx**(`networkID`: number, `blockchainID`: Buffer, `toAddresses`: Buffer[], `fromAddresses`: Buffer[], `changeAddresses`: Buffer[], `atomics`: [UTXO](api_avm_utxos.utxo)[], `sourceChain`: Buffer, `fee`: BN, `feeAssetID`: Buffer, `memo`: Buffer, `asOf`: BN, `locktime`: BN, `threshold`: number): _[UnsignedTx](api_avm_transactions.unsignedtx)_

_Defined in [src/apis/avm/utxos.ts:885](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/utxos.ts#L885)_

Creates an unsigned ImportTx transaction.

**Parameters:**

| Name              | Type                         | Default   | Description                                                                                                                                                                  |
| ----------------- | ---------------------------- | --------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `networkID`       | number                       | -         | The number representing NetworkID of the node                                                                                                                                |
| `blockchainID`    | Buffer                       | -         | The [Buffer](https://github.com/feross/buffer) representing the BlockchainID for the transaction                                                                             |
| `toAddresses`     | Buffer[]                     | -         | The addresses to send the funds                                                                                                                                              |
| `fromAddresses`   | Buffer[]                     | -         | The addresses being used to send the funds from the UTXOs [Buffer](https://github.com/feross/buffer)                                                                         |
| `changeAddresses` | Buffer[]                     | -         | Optional. The addresses that can spend the change remaining from the spent UTXOs.                                                                                            |
| `atomics`         | [UTXO](api_avm_utxos.utxo)[] | -         | -                                                                                                                                                                            |
| `sourceChain`     | Buffer                       | undefined | A [Buffer](https://github.com/feross/buffer) for the chainid where the imports are coming from.                                                                              |
| `fee`             | BN                           | undefined | Optional. The amount of fees to burn in its smallest denomination, represented as [BN](https://github.com/indutny/bn.js/). Fee will come from the inputs first, if they can. |
| `feeAssetID`      | Buffer                       | undefined | Optional. The assetID of the fees being burned.                                                                                                                              |
| `memo`            | Buffer                       | undefined | Optional contains arbitrary bytes, up to 256 bytes                                                                                                                           |
| `asOf`            | BN                           | UnixNow() | Optional. The timestamp to verify the transaction against as a [BN](https://github.com/indutny/bn.js/)                                                                       |
| `locktime`        | BN                           | new BN(0) | Optional. The locktime field created in the resulting outputs                                                                                                                |
| `threshold`       | number                       | 1         | Optional. The number of signatures required to spend the funds in the resultant UTXO                                                                                         |

**Returns:** _[UnsignedTx](api_avm_transactions.unsignedtx)_

An unsigned transaction created from the passed in parameters.

---

### buildNFTTransferTx

▸ **buildNFTTransferTx**(`networkID`: number, `blockchainID`: Buffer, `toAddresses`: Buffer[], `fromAddresses`: Buffer[], `changeAddresses`: Buffer[], `utxoids`: string[], `fee`: BN, `feeAssetID`: Buffer, `memo`: Buffer, `asOf`: BN, `locktime`: BN, `threshold`: number): _[UnsignedTx](api_avm_transactions.unsignedtx)_

_Defined in [src/apis/avm/utxos.ts:787](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/utxos.ts#L787)_

Creates an unsigned NFT transfer transaction. For more granular control, you may create your own
[OperationTx](api_avm_operationtx.operationtx) manually (with their corresponding [TransferableInput](api_evm_inputs.transferableinput)s, [TransferableOutput](api_evm_outputs.transferableoutput)s, and [[TransferOperation]]s).

**Parameters:**

| Name              | Type     | Default   | Description                                                                                                               |
| ----------------- | -------- | --------- | ------------------------------------------------------------------------------------------------------------------------- |
| `networkID`       | number   | -         | The number representing NetworkID of the node                                                                             |
| `blockchainID`    | Buffer   | -         | The [Buffer](https://github.com/feross/buffer) representing the BlockchainID for the transaction                          |
| `toAddresses`     | Buffer[] | -         | An array of [Buffer](https://github.com/feross/buffer)s which indicate who recieves the NFT                               |
| `fromAddresses`   | Buffer[] | -         | An array for [Buffer](https://github.com/feross/buffer) who owns the NFT                                                  |
| `changeAddresses` | Buffer[] | -         | Optional. The addresses that can spend the change remaining from the spent UTXOs.                                         |
| `utxoids`         | string[] | -         | An array of strings for the NFTs being transferred                                                                        |
| `fee`             | BN       | undefined | Optional. The amount of fees to burn in its smallest denomination, represented as [BN](https://github.com/indutny/bn.js/) |
| `feeAssetID`      | Buffer   | undefined | Optional. The assetID of the fees being burned.                                                                           |
| `memo`            | Buffer   | undefined | Optional contains arbitrary bytes, up to 256 bytes                                                                        |
| `asOf`            | BN       | UnixNow() | Optional. The timestamp to verify the transaction against as a [BN](https://github.com/indutny/bn.js/)                    |
| `locktime`        | BN       | new BN(0) | Optional. The locktime field created in the resulting outputs                                                             |
| `threshold`       | number   | 1         | Optional. The number of signatures required to spend the funds in the resultant UTXO                                      |

**Returns:** _[UnsignedTx](api_avm_transactions.unsignedtx)_

An unsigned transaction created from the passed in parameters.

---

### buildSECPMintTx

▸ **buildSECPMintTx**(`networkID`: number, `blockchainID`: Buffer, `mintOwner`: [SECPMintOutput](api_avm_outputs.secpmintoutput), `transferOwner`: [SECPTransferOutput](api_avm_outputs.secptransferoutput), `fromAddresses`: Buffer[], `changeAddresses`: Buffer[], `mintUTXOID`: string, `fee`: BN, `feeAssetID`: Buffer, `memo`: Buffer, `asOf`: BN): _[UnsignedTx](api_avm_transactions.unsignedtx)_

_Defined in [src/apis/avm/utxos.ts:518](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/utxos.ts#L518)_

Creates an unsigned Secp mint transaction. For more granular control, you may create your own
[OperationTx](api_avm_operationtx.operationtx) manually (with their corresponding [TransferableInput](api_evm_inputs.transferableinput)s, [TransferableOutput](api_evm_outputs.transferableoutput)s, and [[TransferOperation]]s).

**Parameters:**

| Name              | Type                                                     | Default   | Description                                                                                                               |
| ----------------- | -------------------------------------------------------- | --------- | ------------------------------------------------------------------------------------------------------------------------- |
| `networkID`       | number                                                   | -         | The number representing NetworkID of the node                                                                             |
| `blockchainID`    | Buffer                                                   | -         | The [Buffer](https://github.com/feross/buffer) representing the BlockchainID for the transaction                          |
| `mintOwner`       | [SECPMintOutput](api_avm_outputs.secpmintoutput)         | -         | A [SECPMintOutput](api_avm_outputs.secpmintoutput) which specifies the new set of minters                                 |
| `transferOwner`   | [SECPTransferOutput](api_avm_outputs.secptransferoutput) | -         | A [SECPTransferOutput](api_evm_outputs.secptransferoutput) which specifies where the minted tokens will go                |
| `fromAddresses`   | Buffer[]                                                 | -         | The addresses being used to send the funds from the UTXOs [Buffer](https://github.com/feross/buffer)                      |
| `changeAddresses` | Buffer[]                                                 | -         | The addresses that can spend the change remaining from the spent UTXOs                                                    |
| `mintUTXOID`      | string                                                   | -         | The UTXOID for the [[SCPMintOutput]] being spent to produce more tokens                                                   |
| `fee`             | BN                                                       | undefined | Optional. The amount of fees to burn in its smallest denomination, represented as [BN](https://github.com/indutny/bn.js/) |
| `feeAssetID`      | Buffer                                                   | undefined | Optional. The assetID of the fees being burned.                                                                           |
| `memo`            | Buffer                                                   | undefined | Optional contains arbitrary bytes, up to 256 bytes                                                                        |
| `asOf`            | BN                                                       | UnixNow() | Optional. The timestamp to verify the transaction against as a [BN](https://github.com/indutny/bn.js/)                    |

**Returns:** _[UnsignedTx](api_avm_transactions.unsignedtx)_

---

### clone

▸ **clone**(): _this_

_Overrides [StandardUTXOSet](common_utxos.standardutxoset).[clone](common_utxos.standardutxoset#abstract-clone)_

_Defined in [src/apis/avm/utxos.ts:210](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/utxos.ts#L210)_

**Returns:** _this_

---

### create

▸ **create**(...`args`: any[]): _this_

_Overrides [StandardUTXOSet](common_utxos.standardutxoset).[create](common_utxos.standardutxoset#abstract-create)_

_Defined in [src/apis/avm/utxos.ts:206](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/utxos.ts#L206)_

**Parameters:**

| Name      | Type  |
| --------- | ----- |
| `...args` | any[] |

**Returns:** _this_

---

### deserialize

▸ **deserialize**(`fields`: object, `encoding`: [SerializedEncoding](../modules/utils_serialization#serializedencoding)): _void_

_Overrides [StandardParseableInput](common_inputs.standardparseableinput).[deserialize](common_inputs.standardparseableinput#deserialize)_

_Defined in [src/apis/avm/utxos.ts:145](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/utxos.ts#L145)_

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

▸ (`utxo`: [UTXO](api_avm_utxos.utxo), ...`largs`: any[]): _boolean_

**Parameters:**

| Name       | Type                       |
| ---------- | -------------------------- |
| `utxo`     | [UTXO](api_avm_utxos.utxo) |
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

▸ **getAllUTXOs**(`utxoids`: string[]): _[UTXO](api_avm_utxos.utxo)[]_

_Inherited from [StandardUTXOSet](common_utxos.standardutxoset).[getAllUTXOs](common_utxos.standardutxoset#getallutxos)_

_Defined in [src/common/utxos.ts:420](https://github.com/chain4travel/caminojs/blob/3883166/src/common/utxos.ts#L420)_

Gets all the [StandardUTXO](common_utxos.standardutxo)s, optionally that match with UTXOIDs in an array

**Parameters:**

| Name      | Type     | Default   | Description                                                                                          |
| --------- | -------- | --------- | ---------------------------------------------------------------------------------------------------- |
| `utxoids` | string[] | undefined | An optional array of UTXOIDs, returns all [StandardUTXO](common_utxos.standardutxo)s if not provided |

**Returns:** _[UTXO](api_avm_utxos.utxo)[]_

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

▸ **getMinimumSpendable**(`aad`: [AssetAmountDestination](api_avm_utxos.assetamountdestination), `asOf`: BN, `locktime`: BN, `threshold`: number): _[Error](src_utils.avalancheerror#static-error)_

_Defined in [src/apis/avm/utxos.ts:226](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/utxos.ts#L226)_

**Parameters:**

| Name        | Type                                                           | Default   |
| ----------- | -------------------------------------------------------------- | --------- |
| `aad`       | [AssetAmountDestination](api_avm_utxos.assetamountdestination) | -         |
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

▸ **getUTXO**(`utxoid`: string): _[UTXO](api_avm_utxos.utxo)_

_Inherited from [StandardUTXOSet](common_utxos.standardutxoset).[getUTXO](common_utxos.standardutxoset#getutxo)_

_Defined in [src/common/utxos.ts:411](https://github.com/chain4travel/caminojs/blob/3883166/src/common/utxos.ts#L411)_

Gets a [StandardUTXO](common_utxos.standardutxo) from the [StandardUTXOSet](common_utxos.standardutxoset) by its UTXOID.

**Parameters:**

| Name     | Type   | Description                    |
| -------- | ------ | ------------------------------ |
| `utxoid` | string | String representing the UTXOID |

**Returns:** _[UTXO](api_avm_utxos.utxo)_

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

▸ **includes**(`utxo`: [UTXO](api_avm_utxos.utxo) | string): _boolean_

_Inherited from [StandardUTXOSet](common_utxos.standardutxoset).[includes](common_utxos.standardutxoset#includes)_

_Defined in [src/common/utxos.ts:274](https://github.com/chain4travel/caminojs/blob/3883166/src/common/utxos.ts#L274)_

Returns true if the [StandardUTXO](common_utxos.standardutxo) is in the StandardUTXOSet.

**Parameters:**

| Name   | Type                                     | Description                                                                                             |
| ------ | ---------------------------------------- | ------------------------------------------------------------------------------------------------------- |
| `utxo` | [UTXO](api_avm_utxos.utxo) &#124; string | Either a [StandardUTXO](common_utxos.standardutxo) a cb58 serialized string representing a StandardUTXO |

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

▸ **parseUTXO**(`utxo`: [UTXO](api_avm_utxos.utxo) | string): _[UTXO](api_avm_utxos.utxo)_

_Overrides [StandardUTXOSet](common_utxos.standardutxoset).[parseUTXO](common_utxos.standardutxoset#abstract-parseutxo)_

_Defined in [src/apis/avm/utxos.ts:190](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/utxos.ts#L190)_

**Parameters:**

| Name   | Type                                     |
| ------ | ---------------------------------------- |
| `utxo` | [UTXO](api_avm_utxos.utxo) &#124; string |

**Returns:** _[UTXO](api_avm_utxos.utxo)_

---

### remove

▸ **remove**(`utxo`: [UTXO](api_avm_utxos.utxo) | string): _[UTXO](api_avm_utxos.utxo)_

_Inherited from [StandardUTXOSet](common_utxos.standardutxoset).[remove](common_utxos.standardutxoset#remove)_

_Defined in [src/common/utxos.ts:358](https://github.com/chain4travel/caminojs/blob/3883166/src/common/utxos.ts#L358)_

Removes a [StandardUTXO](common_utxos.standardutxo) from the [StandardUTXOSet](common_utxos.standardutxoset) if it exists.

**Parameters:**

| Name   | Type                                     | Description                                                                                              |
| ------ | ---------------------------------------- | -------------------------------------------------------------------------------------------------------- |
| `utxo` | [UTXO](api_avm_utxos.utxo) &#124; string | Either a [StandardUTXO](common_utxos.standardutxo) an cb58 serialized string representing a StandardUTXO |

**Returns:** _[UTXO](api_avm_utxos.utxo)_

A [StandardUTXO](common_utxos.standardutxo) if it was removed and undefined if nothing was removed.

---

### removeArray

▸ **removeArray**(`utxos`: string[] | [UTXO](api_avm_utxos.utxo)[]): _[UTXO](api_avm_utxos.utxo)[]_

_Inherited from [StandardUTXOSet](common_utxos.standardutxoset).[removeArray](common_utxos.standardutxoset#removearray)_

_Defined in [src/common/utxos.ts:393](https://github.com/chain4travel/caminojs/blob/3883166/src/common/utxos.ts#L393)_

Removes an array of [StandardUTXO](common_utxos.standardutxo)s to the [StandardUTXOSet](common_utxos.standardutxoset).

**Parameters:**

| Name    | Type                                         |
| ------- | -------------------------------------------- |
| `utxos` | string[] &#124; [UTXO](api_avm_utxos.utxo)[] |

**Returns:** _[UTXO](api_avm_utxos.utxo)[]_

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
