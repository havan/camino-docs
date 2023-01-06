# Class: AVMAPI

Class for interacting with a node endpoint that is using the AVM.

**`remarks`** This extends the [JRPCAPI](../modules/src_common#jrpcapi) class. This class should not be directly called. Instead, use the [Avalanche.addAPI](avalanche.avalanche-1#addapi) function to register this interface with Avalanche.

## Hierarchy

↳ [JRPCAPI](common_jrpcapi.jrpcapi)

↳ **AVMAPI**

## Index

### Constructors

- [constructor](api_avm.avmapi#constructor)

### Properties

- [AVAXAssetID](api_avm.avmapi#protected-avaxassetid)
- [baseURL](api_avm.avmapi#protected-baseurl)
- [blockchainAlias](api_avm.avmapi#protected-blockchainalias)
- [blockchainID](api_avm.avmapi#protected-blockchainid)
- [core](api_avm.avmapi#protected-core)
- [creationTxFee](api_avm.avmapi#protected-creationtxfee)
- [db](api_avm.avmapi#protected-db)
- [jrpcVersion](api_avm.avmapi#protected-jrpcversion)
- [mintTxFee](api_avm.avmapi#protected-minttxfee)
- [rpcID](api_avm.avmapi#protected-rpcid)
- [txFee](api_avm.avmapi#protected-txfee)

### Methods

- [addressFromBuffer](api_avm.avmapi#addressfrombuffer)
- [buildBaseTx](api_avm.avmapi#buildbasetx)
- [buildCreateAssetTx](api_avm.avmapi#buildcreateassettx)
- [buildCreateNFTAssetTx](api_avm.avmapi#buildcreatenftassettx)
- [buildCreateNFTMintTx](api_avm.avmapi#buildcreatenftminttx)
- [buildExportTx](api_avm.avmapi#buildexporttx)
- [buildGenesis](api_avm.avmapi#buildgenesis)
- [buildImportTx](api_avm.avmapi#buildimporttx)
- [buildNFTTransferTx](api_avm.avmapi#buildnfttransfertx)
- [buildSECPMintTx](api_avm.avmapi#buildsecpminttx)
- [callMethod](api_avm.avmapi#callmethod)
- [checkGooseEgg](api_avm.avmapi#checkgooseegg)
- [createAddress](api_avm.avmapi#createaddress)
- [createFixedCapAsset](api_avm.avmapi#createfixedcapasset)
- [createNFTAsset](api_avm.avmapi#createnftasset)
- [createVariableCapAsset](api_avm.avmapi#createvariablecapasset)
- [export](api_avm.avmapi#export)
- [exportKey](api_avm.avmapi#exportkey)
- [getAVAXAssetID](api_avm.avmapi#getavaxassetid)
- [getAddressTxs](api_avm.avmapi#getaddresstxs)
- [getAllBalances](api_avm.avmapi#getallbalances)
- [getAssetDescription](api_avm.avmapi#getassetdescription)
- [getBalance](api_avm.avmapi#getbalance)
- [getBaseURL](api_avm.avmapi#getbaseurl)
- [getBlockchainAlias](api_avm.avmapi#getblockchainalias)
- [getBlockchainID](api_avm.avmapi#getblockchainid)
- [getCreationTxFee](api_avm.avmapi#getcreationtxfee)
- [getDB](api_avm.avmapi#getdb)
- [getDefaultCreationTxFee](api_avm.avmapi#getdefaultcreationtxfee)
- [getDefaultMintTxFee](api_avm.avmapi#getdefaultminttxfee)
- [getDefaultTxFee](api_avm.avmapi#getdefaulttxfee)
- [getMintTxFee](api_avm.avmapi#getminttxfee)
- [getRPCID](api_avm.avmapi#getrpcid)
- [getTx](api_avm.avmapi#gettx)
- [getTxFee](api_avm.avmapi#gettxfee)
- [getTxStatus](api_avm.avmapi#gettxstatus)
- [getUTXOs](api_avm.avmapi#getutxos)
- [import](api_avm.avmapi#import)
- [importKey](api_avm.avmapi#importkey)
- [issueTx](api_avm.avmapi#issuetx)
- [keyChain](api_avm.avmapi#keychain)
- [listAddresses](api_avm.avmapi#listaddresses)
- [mint](api_avm.avmapi#mint)
- [mintNFT](api_avm.avmapi#mintnft)
- [parseAddress](api_avm.avmapi#parseaddress)
- [send](api_avm.avmapi#send)
- [sendMultiple](api_avm.avmapi#sendmultiple)
- [sendNFT](api_avm.avmapi#sendnft)
- [setAVAXAssetID](api_avm.avmapi#setavaxassetid)
- [setBaseURL](api_avm.avmapi#setbaseurl)
- [setCreationTxFee](api_avm.avmapi#setcreationtxfee)
- [setMintTxFee](api_avm.avmapi#setminttxfee)
- [setTxFee](api_avm.avmapi#settxfee)
- [signTx](api_avm.avmapi#signtx)

## Constructors

### constructor

\+ **new AVMAPI**(`core`: [AvalancheCore](avalanchecore.avalanchecore-1), `baseURL`: string, `blockchainID`: string): _[AVMAPI](api_avm.avmapi)_

_Overrides [JRPCAPI](common_jrpcapi.jrpcapi).[constructor](common_jrpcapi.jrpcapi#constructor)_

_Defined in [src/apis/avm/api.ts:2021](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/api.ts#L2021)_

This class should not be instantiated directly. Instead use the [[Avalanche.addAP`${I}`]] method.

**Parameters:**

| Name           | Type                                           | Default     | Description                                                            |
| -------------- | ---------------------------------------------- | ----------- | ---------------------------------------------------------------------- |
| `core`         | [AvalancheCore](avalanchecore.avalanchecore-1) | -           | A reference to the Avalanche class                                     |
| `baseURL`      | string                                         | "/ext/bc/X" | Defaults to the string "/ext/bc/X" as the path to blockchain's baseURL |
| `blockchainID` | string                                         | ""          | The Blockchain"s ID. Defaults to an empty string: ""                   |

**Returns:** _[AVMAPI](api_avm.avmapi)_

## Properties

### `Protected` AVAXAssetID

• **AVAXAssetID**: _Buffer_ = undefined

_Defined in [src/apis/avm/api.ts:89](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/api.ts#L89)_

---

### `Protected` baseURL

• **baseURL**: _string_

_Inherited from [APIBase](common_apibase.apibase).[baseURL](common_apibase.apibase#protected-baseurl)_

_Defined in [src/common/apibase.ts:29](https://github.com/chain4travel/caminojs/blob/3883166/src/common/apibase.ts#L29)_

---

### `Protected` blockchainAlias

• **blockchainAlias**: _string_ = undefined

_Defined in [src/apis/avm/api.ts:87](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/api.ts#L87)_

---

### `Protected` blockchainID

• **blockchainID**: _string_ = undefined

_Defined in [src/apis/avm/api.ts:88](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/api.ts#L88)_

---

### `Protected` core

• **core**: _[AvalancheCore](avalanchecore.avalanchecore-1)_

_Inherited from [APIBase](common_apibase.apibase).[core](common_apibase.apibase#protected-core)_

_Defined in [src/common/apibase.ts:28](https://github.com/chain4travel/caminojs/blob/3883166/src/common/apibase.ts#L28)_

---

### `Protected` creationTxFee

• **creationTxFee**: _BN_ = undefined

_Defined in [src/apis/avm/api.ts:91](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/api.ts#L91)_

---

### `Protected` db

• **db**: _StoreAPI_

_Inherited from [APIBase](common_apibase.apibase).[db](common_apibase.apibase#protected-db)_

_Defined in [src/common/apibase.ts:30](https://github.com/chain4travel/caminojs/blob/3883166/src/common/apibase.ts#L30)_

---

### `Protected` jrpcVersion

• **jrpcVersion**: _string_ = "2.0"

_Inherited from [EVMAPI](api_evm.evmapi).[jrpcVersion](api_evm.evmapi#protected-jrpcversion)_

_Defined in [src/common/jrpcapi.ts:12](https://github.com/chain4travel/caminojs/blob/3883166/src/common/jrpcapi.ts#L12)_

---

### `Protected` mintTxFee

• **mintTxFee**: _BN_ = undefined

_Defined in [src/apis/avm/api.ts:92](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/api.ts#L92)_

---

### `Protected` rpcID

• **rpcID**: _number_ = 1

_Inherited from [EVMAPI](api_evm.evmapi).[rpcID](api_evm.evmapi#protected-rpcid)_

_Defined in [src/common/jrpcapi.ts:13](https://github.com/chain4travel/caminojs/blob/3883166/src/common/jrpcapi.ts#L13)_

---

### `Protected` txFee

• **txFee**: _BN_ = undefined

_Defined in [src/apis/avm/api.ts:90](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/api.ts#L90)_

## Methods

### addressFromBuffer

▸ **addressFromBuffer**(`address`: Buffer): _string_

_Defined in [src/apis/avm/api.ts:129](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/api.ts#L129)_

**Parameters:**

| Name      | Type   |
| --------- | ------ |
| `address` | Buffer |

**Returns:** _string_

---

### buildBaseTx

▸ **buildBaseTx**(`utxoset`: [UTXOSet](api_avm_utxos.utxoset), `amount`: BN, `assetID`: Buffer | string, `toAddresses`: string[], `fromAddresses`: string[], `changeAddresses`: string[], `memo`: [PayloadBase](utils_payload.payloadbase) | Buffer, `asOf`: BN, `locktime`: BN, `threshold`: number): _Promise‹[UnsignedTx](api_avm_transactions.unsignedtx)›_

_Defined in [src/apis/avm/api.ts:1027](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/api.ts#L1027)_

Helper function which creates an unsigned transaction. For more granular control, you may create your own
[UnsignedTx](api_evm_transactions.unsignedtx) manually (with their corresponding [TransferableInput](api_evm_inputs.transferableinput)s, [TransferableOutput](api_evm_outputs.transferableoutput)s, and [[TransferOperation]]s).

**`remarks`**
This helper exists because the endpoint API should be the primary point of entry for most functionality.

**Parameters:**

| Name              | Type                                                   | Default   | Description                                                                                                             |
| ----------------- | ------------------------------------------------------ | --------- | ----------------------------------------------------------------------------------------------------------------------- |
| `utxoset`         | [UTXOSet](api_avm_utxos.utxoset)                       | -         | A set of UTXOs that the transaction is built on                                                                         |
| `amount`          | BN                                                     | -         | The amount of AssetID to be spent in its smallest denomination, represented as [BN](https://github.com/indutny/bn.js/). |
| `assetID`         | Buffer &#124; string                                   | undefined | The assetID of the value being sent                                                                                     |
| `toAddresses`     | string[]                                               | -         | The addresses to send the funds                                                                                         |
| `fromAddresses`   | string[]                                               | -         | The addresses being used to send the funds from the UTXOs provided                                                      |
| `changeAddresses` | string[]                                               | -         | The addresses that can spend the change remaining from the spent UTXOs                                                  |
| `memo`            | [PayloadBase](utils_payload.payloadbase) &#124; Buffer | undefined | Optional CB58 Buffer or String which contains arbitrary bytes, up to 256 bytes                                          |
| `asOf`            | BN                                                     | UnixNow() | Optional. The timestamp to verify the transaction against as a [BN](https://github.com/indutny/bn.js/)                  |
| `locktime`        | BN                                                     | new BN(0) | Optional. The locktime field created in the resulting outputs                                                           |
| `threshold`       | number                                                 | 1         | Optional. The number of signatures required to spend the funds in the resultant UTXO                                    |

**Returns:** _Promise‹[UnsignedTx](api_avm_transactions.unsignedtx)›_

An unsigned transaction ([UnsignedTx](api_evm_transactions.unsignedtx)) which contains a [BaseTx](api_avm_basetx.basetx).

---

### buildCreateAssetTx

▸ **buildCreateAssetTx**(`utxoset`: [UTXOSet](api_avm_utxos.utxoset), `fromAddresses`: string[], `changeAddresses`: string[], `initialStates`: [InitialStates](api_avm_initialstates.initialstates), `name`: string, `symbol`: string, `denomination`: number, `mintOutputs`: [SECPMintOutput](api_avm_outputs.secpmintoutput)[], `memo`: [PayloadBase](utils_payload.payloadbase) | Buffer, `asOf`: BN): _Promise‹[UnsignedTx](api_avm_transactions.unsignedtx)›_

_Defined in [src/apis/avm/api.ts:1406](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/api.ts#L1406)_

Creates an unsigned transaction. For more granular control, you may create your own
[UnsignedTx](api_evm_transactions.unsignedtx) manually (with their corresponding [TransferableInput](api_evm_inputs.transferableinput)s, [TransferableOutput](api_evm_outputs.transferableoutput)s, and [[TransferOperation]]s).

**Parameters:**

| Name              | Type                                                   | Default   | Description                                                                                                                                             |
| ----------------- | ------------------------------------------------------ | --------- | ------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `utxoset`         | [UTXOSet](api_avm_utxos.utxoset)                       | -         | A set of UTXOs that the transaction is built on                                                                                                         |
| `fromAddresses`   | string[]                                               | -         | The addresses being used to send the funds from the UTXOs [Buffer](https://github.com/feross/buffer)                                                    |
| `changeAddresses` | string[]                                               | -         | The addresses that can spend the change remaining from the spent UTXOs                                                                                  |
| `initialStates`   | [InitialStates](api_avm_initialstates.initialstates)   | -         | -                                                                                                                                                       |
| `name`            | string                                                 | -         | String for the descriptive name of the asset                                                                                                            |
| `symbol`          | string                                                 | -         | String for the ticker symbol of the asset                                                                                                               |
| `denomination`    | number                                                 | -         | Number for the denomination which is 10^D. D must be >= 0 and <= 32. Ex: $1 AVAX = 10^9 $nAVAX                                                          |
| `mintOutputs`     | [SECPMintOutput](api_avm_outputs.secpmintoutput)[]     | undefined | Optional. Array of [SECPMintOutput](api_avm_outputs.secpmintoutput)s to be included in the transaction. These outputs can be spent to mint more tokens. |
| `memo`            | [PayloadBase](utils_payload.payloadbase) &#124; Buffer | undefined | Optional CB58 Buffer or String which contains arbitrary bytes, up to 256 bytes                                                                          |
| `asOf`            | BN                                                     | UnixNow() | Optional. The timestamp to verify the transaction against as a [BN](https://github.com/indutny/bn.js/)                                                  |

**Returns:** _Promise‹[UnsignedTx](api_avm_transactions.unsignedtx)›_

An unsigned transaction ([UnsignedTx](api_evm_transactions.unsignedtx)) which contains a [CreateAssetTx](api_avm_createassettx.createassettx).

---

### buildCreateNFTAssetTx

▸ **buildCreateNFTAssetTx**(`utxoset`: [UTXOSet](api_avm_utxos.utxoset), `fromAddresses`: string[], `changeAddresses`: string[], `minterSets`: [MinterSet](api_avm_minterset.minterset)[], `name`: string, `symbol`: string, `memo`: [PayloadBase](utils_payload.payloadbase) | Buffer, `asOf`: BN, `locktime`: BN): _Promise‹[UnsignedTx](api_avm_transactions.unsignedtx)›_

_Defined in [src/apis/avm/api.ts:1560](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/api.ts#L1560)_

Creates an unsigned transaction. For more granular control, you may create your own
[UnsignedTx](api_evm_transactions.unsignedtx) manually (with their corresponding [TransferableInput](api_evm_inputs.transferableinput)s, [TransferableOutput](api_evm_outputs.transferableoutput)s, and [[TransferOperation]]s).

**Parameters:**

| Name              | Type                                                   | Default   | Description                                                                                                                                                                                                                                                                                                                                                             |
| ----------------- | ------------------------------------------------------ | --------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `utxoset`         | [UTXOSet](api_avm_utxos.utxoset)                       | -         | A set of UTXOs that the transaction is built on                                                                                                                                                                                                                                                                                                                         |
| `fromAddresses`   | string[]                                               | -         | The addresses being used to send the funds from the UTXOs [Buffer](https://github.com/feross/buffer)                                                                                                                                                                                                                                                                    |
| `changeAddresses` | string[]                                               | -         | The addresses that can spend the change remaining from the spent UTXOs                                                                                                                                                                                                                                                                                                  |
| `minterSets`      | [MinterSet](api_avm_minterset.minterset)[]             | -         | is a list where each element specifies that threshold of the addresses in minters may together mint more of the asset by signing a minting transaction                                                                                                                                                                                                                  |
| `name`            | string                                                 | -         | String for the descriptive name of the asset                                                                                                                                                                                                                                                                                                                            |
| `symbol`          | string                                                 | -         | String for the ticker symbol of the asset                                                                                                                                                                                                                                                                                                                               |
| `memo`            | [PayloadBase](utils_payload.payloadbase) &#124; Buffer | undefined | Optional CB58 Buffer or String which contains arbitrary bytes, up to 256 bytes                                                                                                                                                                                                                                                                                          |
| `asOf`            | BN                                                     | UnixNow() | Optional. The timestamp to verify the transaction against as a [BN](https://github.com/indutny/bn.js/)                                                                                                                                                                                                                                                                  |
| `locktime`        | BN                                                     | new BN(0) | Optional. The locktime field created in the resulting mint output `js Example minterSets: [ { "minters":[ "X-avax1ghstjukrtw8935lryqtnh643xe9a94u3tc75c7" ], "threshold": 1 }, { "minters": [ "X-avax1yell3e4nln0m39cfpdhgqprsd87jkh4qnakklx", "X-avax1k4nr26c80jaquzm9369j5a4shmwcjn0vmemcjz", "X-avax1ztkzsrjnkn0cek5ryvhqswdtcg23nhge3nnr5e" ], "threshold": 2 } ] ` |

**Returns:** _Promise‹[UnsignedTx](api_avm_transactions.unsignedtx)›_

An unsigned transaction ([UnsignedTx](api_evm_transactions.unsignedtx)) which contains a [CreateAssetTx](api_avm_createassettx.createassettx).

---

### buildCreateNFTMintTx

▸ **buildCreateNFTMintTx**(`utxoset`: [UTXOSet](api_avm_utxos.utxoset), `owners`: [OutputOwners](common_output.outputowners)[] | [OutputOwners](common_output.outputowners), `fromAddresses`: string[], `changeAddresses`: string[], `utxoid`: string | string[], `groupID`: number, `payload`: [PayloadBase](utils_payload.payloadbase) | Buffer, `memo`: [PayloadBase](utils_payload.payloadbase) | Buffer, `asOf`: BN): _Promise‹any›_

_Defined in [src/apis/avm/api.ts:1642](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/api.ts#L1642)_

Creates an unsigned transaction. For more granular control, you may create your own
[UnsignedTx](api_evm_transactions.unsignedtx) manually (with their corresponding [TransferableInput](api_evm_inputs.transferableinput)s, [TransferableOutput](api_evm_outputs.transferableoutput)s, and [[TransferOperation]]s).

**Parameters:**

| Name              | Type                                                                                           | Default   | Description                                                                                                                         |
| ----------------- | ---------------------------------------------------------------------------------------------- | --------- | ----------------------------------------------------------------------------------------------------------------------------------- |
| `utxoset`         | [UTXOSet](api_avm_utxos.utxoset)                                                               | -         | A set of UTXOs that the transaction is built on                                                                                     |
| `owners`          | [OutputOwners](common_output.outputowners)[] &#124; [OutputOwners](common_output.outputowners) | -         | Either a single or an array of [OutputOwners](../modules/src_common#outputowners) to send the nft output                            |
| `fromAddresses`   | string[]                                                                                       | -         | The addresses being used to send the NFT from the utxoID provided                                                                   |
| `changeAddresses` | string[]                                                                                       | -         | The addresses that can spend the change remaining from the spent UTXOs                                                              |
| `utxoid`          | string &#124; string[]                                                                         | -         | A base58 utxoID or an array of base58 utxoIDs for the nft mint output this transaction is sending                                   |
| `groupID`         | number                                                                                         | 0         | Optional. The group this NFT is issued to.                                                                                          |
| `payload`         | [PayloadBase](utils_payload.payloadbase) &#124; Buffer                                         | undefined | Optional. Data for NFT Payload as either a [PayloadBase](utils_payload.payloadbase) or a [Buffer](https://github.com/feross/buffer) |
| `memo`            | [PayloadBase](utils_payload.payloadbase) &#124; Buffer                                         | undefined | Optional CB58 Buffer or String which contains arbitrary bytes, up to 256 bytes                                                      |
| `asOf`            | BN                                                                                             | UnixNow() | Optional. The timestamp to verify the transaction against as a [BN](https://github.com/indutny/bn.js/)                              |

**Returns:** _Promise‹any›_

An unsigned transaction ([UnsignedTx](api_evm_transactions.unsignedtx)) which contains an [OperationTx](api_avm_operationtx.operationtx).

---

### buildExportTx

▸ **buildExportTx**(`utxoset`: [UTXOSet](api_avm_utxos.utxoset), `amount`: BN, `destinationChain`: Buffer | string, `toAddresses`: string[], `fromAddresses`: string[], `changeAddresses`: string[], `memo`: [PayloadBase](utils_payload.payloadbase) | Buffer, `asOf`: BN, `locktime`: BN, `threshold`: number, `assetID`: string): _Promise‹[UnsignedTx](api_avm_transactions.unsignedtx)›_

_Defined in [src/apis/avm/api.ts:1292](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/api.ts#L1292)_

Helper function which creates an unsigned Export Tx. For more granular control, you may create your own
[UnsignedTx](api_evm_transactions.unsignedtx) manually (with their corresponding [TransferableInput](api_evm_inputs.transferableinput)s, [TransferableOutput](api_evm_outputs.transferableoutput)s, and [[TransferOperation]]s).

**Parameters:**

| Name               | Type                                                   | Default   | Description                                                                                                                                      |
| ------------------ | ------------------------------------------------------ | --------- | ------------------------------------------------------------------------------------------------------------------------------------------------ |
| `utxoset`          | [UTXOSet](api_avm_utxos.utxoset)                       | -         | A set of UTXOs that the transaction is built on                                                                                                  |
| `amount`           | BN                                                     | -         | The amount being exported as a [BN](https://github.com/indutny/bn.js/)                                                                           |
| `destinationChain` | Buffer &#124; string                                   | -         | The chainid for where the assets will be sent.                                                                                                   |
| `toAddresses`      | string[]                                               | -         | The addresses to send the funds                                                                                                                  |
| `fromAddresses`    | string[]                                               | -         | The addresses being used to send the funds from the UTXOs provided                                                                               |
| `changeAddresses`  | string[]                                               | undefined | The addresses that can spend the change remaining from the spent UTXOs                                                                           |
| `memo`             | [PayloadBase](utils_payload.payloadbase) &#124; Buffer | undefined | Optional CB58 Buffer or String which contains arbitrary bytes, up to 256 bytes                                                                   |
| `asOf`             | BN                                                     | UnixNow() | Optional. The timestamp to verify the transaction against as a [BN](https://github.com/indutny/bn.js/)                                           |
| `locktime`         | BN                                                     | new BN(0) | Optional. The locktime field created in the resulting outputs                                                                                    |
| `threshold`        | number                                                 | 1         | Optional. The number of signatures required to spend the funds in the resultant UTXO                                                             |
| `assetID`          | string                                                 | undefined | Optional. The assetID of the asset to send. Defaults to AVAX assetID. Regardless of the asset which you"re exporting, all fees are paid in AVAX. |

**Returns:** _Promise‹[UnsignedTx](api_avm_transactions.unsignedtx)›_

An unsigned transaction ([UnsignedTx](api_evm_transactions.unsignedtx)) which contains an [ExportTx](api_evm_exporttx.exporttx).

---

### buildGenesis

▸ **buildGenesis**(`genesisData`: object): _Promise‹string›_

_Defined in [src/apis/avm/api.ts:1972](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/api.ts#L1972)_

Given a JSON representation of this Virtual Machine’s genesis state, create the byte representation of that state.

**Parameters:**

| Name          | Type   | Description                          |
| ------------- | ------ | ------------------------------------ |
| `genesisData` | object | The blockchain's genesis data object |

**Returns:** _Promise‹string›_

Promise of a string of bytes

---

### buildImportTx

▸ **buildImportTx**(`utxoset`: [UTXOSet](api_avm_utxos.utxoset), `ownerAddresses`: string[], `sourceChain`: Buffer | string, `toAddresses`: string[], `fromAddresses`: string[], `changeAddresses`: string[], `memo`: [PayloadBase](utils_payload.payloadbase) | Buffer, `asOf`: BN, `locktime`: BN, `threshold`: number): _Promise‹[UnsignedTx](api_avm_transactions.unsignedtx)›_

_Defined in [src/apis/avm/api.ts:1188](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/api.ts#L1188)_

Helper function which creates an unsigned Import Tx. For more granular control, you may create your own
[UnsignedTx](api_evm_transactions.unsignedtx) manually (with their corresponding [TransferableInput](api_evm_inputs.transferableinput)s, [TransferableOutput](api_evm_outputs.transferableoutput)s, and [[TransferOperation]]s).

**`remarks`**
This helper exists because the endpoint API should be the primary point of entry for most functionality.

**Parameters:**

| Name              | Type                                                   | Default   | Description                                                                                            |
| ----------------- | ------------------------------------------------------ | --------- | ------------------------------------------------------------------------------------------------------ |
| `utxoset`         | [UTXOSet](api_avm_utxos.utxoset)                       | -         | A set of UTXOs that the transaction is built on                                                        |
| `ownerAddresses`  | string[]                                               | -         | The addresses being used to import                                                                     |
| `sourceChain`     | Buffer &#124; string                                   | -         | The chainid for where the import is coming from                                                        |
| `toAddresses`     | string[]                                               | -         | The addresses to send the funds                                                                        |
| `fromAddresses`   | string[]                                               | -         | The addresses being used to send the funds from the UTXOs provided                                     |
| `changeAddresses` | string[]                                               | undefined | The addresses that can spend the change remaining from the spent UTXOs                                 |
| `memo`            | [PayloadBase](utils_payload.payloadbase) &#124; Buffer | undefined | Optional CB58 Buffer or String which contains arbitrary bytes, up to 256 bytes                         |
| `asOf`            | BN                                                     | UnixNow() | Optional. The timestamp to verify the transaction against as a [BN](https://github.com/indutny/bn.js/) |
| `locktime`        | BN                                                     | new BN(0) | Optional. The locktime field created in the resulting outputs                                          |
| `threshold`       | number                                                 | 1         | Optional. The number of signatures required to spend the funds in the resultant UTXO                   |

**Returns:** _Promise‹[UnsignedTx](api_avm_transactions.unsignedtx)›_

An unsigned transaction ([UnsignedTx](api_evm_transactions.unsignedtx)) which contains a [ImportTx](api_evm_importtx.importtx).

---

### buildNFTTransferTx

▸ **buildNFTTransferTx**(`utxoset`: [UTXOSet](api_avm_utxos.utxoset), `toAddresses`: string[], `fromAddresses`: string[], `changeAddresses`: string[], `utxoid`: string | string[], `memo`: [PayloadBase](utils_payload.payloadbase) | Buffer, `asOf`: BN, `locktime`: BN, `threshold`: number): _Promise‹[UnsignedTx](api_avm_transactions.unsignedtx)›_

_Defined in [src/apis/avm/api.ts:1108](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/api.ts#L1108)_

Helper function which creates an unsigned NFT Transfer. For more granular control, you may create your own
[UnsignedTx](api_evm_transactions.unsignedtx) manually (with their corresponding [TransferableInput](api_evm_inputs.transferableinput)s, [TransferableOutput](api_evm_outputs.transferableoutput)s, and [[TransferOperation]]s).

**`remarks`**
This helper exists because the endpoint API should be the primary point of entry for most functionality.

**Parameters:**

| Name              | Type                                                   | Default   | Description                                                                                            |
| ----------------- | ------------------------------------------------------ | --------- | ------------------------------------------------------------------------------------------------------ |
| `utxoset`         | [UTXOSet](api_avm_utxos.utxoset)                       | -         | A set of UTXOs that the transaction is built on                                                        |
| `toAddresses`     | string[]                                               | -         | The addresses to send the NFT                                                                          |
| `fromAddresses`   | string[]                                               | -         | The addresses being used to send the NFT from the utxoID provided                                      |
| `changeAddresses` | string[]                                               | -         | The addresses that can spend the change remaining from the spent UTXOs                                 |
| `utxoid`          | string &#124; string[]                                 | -         | A base58 utxoID or an array of base58 utxoIDs for the nfts this transaction is sending                 |
| `memo`            | [PayloadBase](utils_payload.payloadbase) &#124; Buffer | undefined | Optional CB58 Buffer or String which contains arbitrary bytes, up to 256 bytes                         |
| `asOf`            | BN                                                     | UnixNow() | Optional. The timestamp to verify the transaction against as a [BN](https://github.com/indutny/bn.js/) |
| `locktime`        | BN                                                     | new BN(0) | Optional. The locktime field created in the resulting outputs                                          |
| `threshold`       | number                                                 | 1         | Optional. The number of signatures required to spend the funds in the resultant UTXO                   |

**Returns:** _Promise‹[UnsignedTx](api_avm_transactions.unsignedtx)›_

An unsigned transaction ([UnsignedTx](api_evm_transactions.unsignedtx)) which contains a [[NFTTransferTx]].

---

### buildSECPMintTx

▸ **buildSECPMintTx**(`utxoset`: [UTXOSet](api_avm_utxos.utxoset), `mintOwner`: [SECPMintOutput](api_avm_outputs.secpmintoutput), `transferOwner`: [SECPTransferOutput](api_avm_outputs.secptransferoutput), `fromAddresses`: string[], `changeAddresses`: string[], `mintUTXOID`: string, `memo`: [PayloadBase](utils_payload.payloadbase) | Buffer, `asOf`: BN): _Promise‹any›_

_Defined in [src/apis/avm/api.ts:1474](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/api.ts#L1474)_

**Parameters:**

| Name              | Type                                                     | Default   |
| ----------------- | -------------------------------------------------------- | --------- |
| `utxoset`         | [UTXOSet](api_avm_utxos.utxoset)                         | -         |
| `mintOwner`       | [SECPMintOutput](api_avm_outputs.secpmintoutput)         | -         |
| `transferOwner`   | [SECPTransferOutput](api_avm_outputs.secptransferoutput) | -         |
| `fromAddresses`   | string[]                                                 | -         |
| `changeAddresses` | string[]                                                 | -         |
| `mintUTXOID`      | string                                                   | -         |
| `memo`            | [PayloadBase](utils_payload.payloadbase) &#124; Buffer   | undefined |
| `asOf`            | BN                                                       | UnixNow() |

**Returns:** _Promise‹any›_

---

### callMethod

▸ **callMethod**(`method`: string, `params?`: object[] | object, `baseURL?`: string, `headers?`: object): _Promise‹[RequestResponseData](common_apibase.requestresponsedata)›_

_Inherited from [EVMAPI](api_evm.evmapi).[callMethod](api_evm.evmapi#callmethod)_

_Defined in [src/common/jrpcapi.ts:15](https://github.com/chain4travel/caminojs/blob/3883166/src/common/jrpcapi.ts#L15)_

**Parameters:**

| Name       | Type                   |
| ---------- | ---------------------- |
| `method`   | string                 |
| `params?`  | object[] &#124; object |
| `baseURL?` | string                 |
| `headers?` | object                 |

**Returns:** _Promise‹[RequestResponseData](common_apibase.requestresponsedata)›_

---

### checkGooseEgg

▸ **checkGooseEgg**(`utx`: [UnsignedTx](api_avm_transactions.unsignedtx), `outTotal`: BN): _Promise‹boolean›_

_Defined in [src/apis/avm/api.ts:290](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/api.ts#L290)_

Helper function which determines if a tx is a goose egg transaction.

**`remarks`**
A "Goose Egg Transaction" is when the fee far exceeds a reasonable amount

**Parameters:**

| Name       | Type                                          | Default   | Description   |
| ---------- | --------------------------------------------- | --------- | ------------- |
| `utx`      | [UnsignedTx](api_avm_transactions.unsignedtx) | -         | An UnsignedTx |
| `outTotal` | BN                                            | new BN(0) | -             |

**Returns:** _Promise‹boolean›_

boolean true if passes goose egg test and false if fails.

---

### createAddress

▸ **createAddress**(`username`: string, `password`: string): _Promise‹string›_

_Defined in [src/apis/avm/api.ts:346](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/api.ts#L346)_

Creates an address (and associated private keys) on a user on a blockchain.

**Parameters:**

| Name       | Type   | Description                                             |
| ---------- | ------ | ------------------------------------------------------- |
| `username` | string | Name of the user to create the address under            |
| `password` | string | Password to unlock the user and encrypt the private key |

**Returns:** _Promise‹string›_

Promise for a string representing the address created by the vm.

---

### createFixedCapAsset

▸ **createFixedCapAsset**(`username`: string, `password`: string, `name`: string, `symbol`: string, `denomination`: number, `initialHolders`: object[]): _Promise‹string›_

_Defined in [src/apis/avm/api.ts:387](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/api.ts#L387)_

Create a new fixed-cap, fungible asset. A quantity of it is created at initialization and there no more is ever created.

**Parameters:**

| Name             | Type     | Description                                                                                                                                                                                                                                                                                                          |
| ---------------- | -------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `username`       | string   | The user paying the transaction fee (in $AVAX) for asset creation                                                                                                                                                                                                                                                    |
| `password`       | string   | The password for the user paying the transaction fee (in $AVAX) for asset creation                                                                                                                                                                                                                                   |
| `name`           | string   | The human-readable name for the asset                                                                                                                                                                                                                                                                                |
| `symbol`         | string   | Optional. The shorthand symbol for the asset. Between 0 and 4 characters                                                                                                                                                                                                                                             |
| `denomination`   | number   | Optional. Determines how balances of this asset are displayed by user interfaces. Default is 0                                                                                                                                                                                                                       |
| `initialHolders` | object[] | An array of objects containing the field "address" and "amount" to establish the genesis values for the new asset `js Example initialHolders: [ { "address": "X-avax1kj06lhgx84h39snsljcey3tpc046ze68mek3g5", "amount": 10000 }, { "address": "X-avax1am4w6hfrvmh3akduzkjthrtgtqafalce6an8cr", "amount": 50000 } ] ` |

**Returns:** _Promise‹string›_

Returns a Promise string containing the base 58 string representation of the ID of the newly created asset.

---

### createNFTAsset

▸ **createNFTAsset**(`username`: string, `password`: string, `from`: string[] | Buffer[], `changeAddr`: string, `name`: string, `symbol`: string, `minterSet`: [IMinterSet](../interfaces/avm_interfaces.iminterset)): _Promise‹string›_

_Defined in [src/apis/avm/api.ts:478](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/api.ts#L478)_

Creates a family of NFT Asset. No units of the asset exist at initialization. Minters can mint units of this asset using createMintTx, signMintTx and sendMintTx.

**Parameters:**

| Name         | Type                                                  | Default   | Description                                                                                                         |
| ------------ | ----------------------------------------------------- | --------- | ------------------------------------------------------------------------------------------------------------------- |
| `username`   | string                                                | -         | The user paying the transaction fee (in $AVAX) for asset creation                                                   |
| `password`   | string                                                | -         | The password for the user paying the transaction fee (in $AVAX) for asset creation                                  |
| `from`       | string[] &#124; Buffer[]                              | undefined | Optional. An array of addresses managed by the node's keystore for this blockchain which will fund this transaction |
| `changeAddr` | string                                                | -         | Optional. An address to send the change                                                                             |
| `name`       | string                                                | -         | The human-readable name for the asset                                                                               |
| `symbol`     | string                                                | -         | Optional. The shorthand symbol for the asset -- between 0 and 4 characters                                          |
| `minterSet`  | [IMinterSet](../interfaces/avm_interfaces.iminterset) | -         | -                                                                                                                   |

**Returns:** _Promise‹string›_

Returns a Promise string containing the base 58 string representation of the ID of the newly created asset.

---

### createVariableCapAsset

▸ **createVariableCapAsset**(`username`: string, `password`: string, `name`: string, `symbol`: string, `denomination`: number, `minterSets`: object[]): _Promise‹string›_

_Defined in [src/apis/avm/api.ts:442](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/api.ts#L442)_

Create a new variable-cap, fungible asset. No units of the asset exist at initialization. Minters can mint units of this asset using createMintTx, signMintTx and sendMintTx.

**Parameters:**

| Name           | Type     | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| -------------- | -------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `username`     | string   | The user paying the transaction fee (in $AVAX) for asset creation                                                                                                                                                                                                                                                                                                                                                                                            |
| `password`     | string   | The password for the user paying the transaction fee (in $AVAX) for asset creation                                                                                                                                                                                                                                                                                                                                                                           |
| `name`         | string   | The human-readable name for the asset                                                                                                                                                                                                                                                                                                                                                                                                                        |
| `symbol`       | string   | Optional. The shorthand symbol for the asset -- between 0 and 4 characters                                                                                                                                                                                                                                                                                                                                                                                   |
| `denomination` | number   | Optional. Determines how balances of this asset are displayed by user interfaces. Default is 0                                                                                                                                                                                                                                                                                                                                                               |
| `minterSets`   | object[] | is a list where each element specifies that threshold of the addresses in minters may together mint more of the asset by signing a minting transaction `js Example minterSets: [ { "minters":[ "X-avax1am4w6hfrvmh3akduzkjthrtgtqafalce6an8cr" ], "threshold": 1 }, { "minters": [ "X-avax1am4w6hfrvmh3akduzkjthrtgtqafalce6an8cr", "X-avax1kj06lhgx84h39snsljcey3tpc046ze68mek3g5", "X-avax1yell3e4nln0m39cfpdhgqprsd87jkh4qnakklx" ], "threshold": 2 } ] ` |

**Returns:** _Promise‹string›_

Returns a Promise string containing the base 58 string representation of the ID of the newly created asset.

---

### export

▸ **export**(`username`: string, `password`: string, `to`: string, `amount`: BN, `assetID`: string): _Promise‹string›_

_Defined in [src/apis/avm/api.ts:762](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/api.ts#L762)_

Send ANT (Avalanche Native Token) assets including AVAX from the X-Chain to an account on the P-Chain or C-Chain.

After calling this method, you must call the P-Chain's `import` or the C-Chain’s `import` method to complete the transfer.

**Parameters:**

| Name       | Type   | Description                                                                      |
| ---------- | ------ | -------------------------------------------------------------------------------- |
| `username` | string | The Keystore user that controls the P-Chain or C-Chain account specified in `to` |
| `password` | string | The password of the Keystore user                                                |
| `to`       | string | The account on the P-Chain or C-Chain to send the asset to.                      |
| `amount`   | BN     | Amount of asset to export as a [BN](https://github.com/indutny/bn.js/)           |
| `assetID`  | string | The asset id which is being sent                                                 |

**Returns:** _Promise‹string›_

String representing the transaction id

---

### exportKey

▸ **exportKey**(`username`: string, `password`: string, `address`: string): _Promise‹string›_

_Defined in [src/apis/avm/api.ts:702](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/api.ts#L702)_

Exports the private key for an address.

**Parameters:**

| Name       | Type   | Description                                      |
| ---------- | ------ | ------------------------------------------------ |
| `username` | string | The name of the user with the private key        |
| `password` | string | The password used to decrypt the private key     |
| `address`  | string | The address whose private key should be exported |

**Returns:** _Promise‹string›_

Promise with the decrypted private key as store in the database

---

### getAVAXAssetID

▸ **getAVAXAssetID**(`refresh`: boolean): _Promise‹Buffer›_

_Defined in [src/apis/avm/api.ts:145](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/api.ts#L145)_

Fetches the AVAX AssetID and returns it in a Promise.

**Parameters:**

| Name      | Type    | Default | Description                                                            |
| --------- | ------- | ------- | ---------------------------------------------------------------------- |
| `refresh` | boolean | false   | This function caches the response. Refresh = true will bust the cache. |

**Returns:** _Promise‹Buffer›_

The the provided string representing the AVAX AssetID

---

### getAddressTxs

▸ **getAddressTxs**(`address`: string, `cursor`: number, `pageSize`: number | undefined, `assetID`: string | Buffer): _Promise‹[GetAddressTxsResponse](../interfaces/avm_interfaces.getaddresstxsresponse)›_

_Defined in [src/apis/avm/api.ts:1759](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/api.ts#L1759)_

Calls the node's getAddressTxs method from the API and returns transactions corresponding to the provided address and assetID

**Parameters:**

| Name       | Type                    | Description                                                                                                                                                         |
| ---------- | ----------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `address`  | string                  | The address for which we're fetching related transactions.                                                                                                          |
| `cursor`   | number                  | Page number or offset.                                                                                                                                              |
| `pageSize` | number &#124; undefined | Number of items to return per page. Optional. Defaults to 1024. If [pageSize] == 0 or [pageSize] > [maxPageSize], then it fetches at max [maxPageSize] transactions |
| `assetID`  | string &#124; Buffer    | Only return transactions that changed the balance of this asset. Must be an ID or an alias for an asset.                                                            |

**Returns:** _Promise‹[GetAddressTxsResponse](../interfaces/avm_interfaces.getaddresstxsresponse)›_

A promise object representing the array of transaction IDs and page offset

---

### getAllBalances

▸ **getAllBalances**(`address`: string): _Promise‹object[]›_

_Defined in [src/apis/avm/api.ts:845](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/api.ts#L845)_

Retrieves all assets for an address on a server and their associated balances.

**Parameters:**

| Name      | Type   | Description                         |
| --------- | ------ | ----------------------------------- |
| `address` | string | The address to get a list of assets |

**Returns:** _Promise‹object[]›_

Promise of an object mapping assetID strings with [BN](https://github.com/indutny/bn.js/) balance for the address on the blockchain.

---

### getAssetDescription

▸ **getAssetDescription**(`assetID`: Buffer | string): _Promise‹[GetAssetDescriptionResponse](../interfaces/avm_interfaces.getassetdescriptionresponse)›_

_Defined in [src/apis/avm/api.ts:869](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/api.ts#L869)_

Retrieves an assets name and symbol.

**Parameters:**

| Name      | Type                 | Description                                                                                                   |
| --------- | -------------------- | ------------------------------------------------------------------------------------------------------------- |
| `assetID` | Buffer &#124; string | Either a [Buffer](https://github.com/feross/buffer) or an b58 serialized string for the AssetID or its alias. |

**Returns:** _Promise‹[GetAssetDescriptionResponse](../interfaces/avm_interfaces.getassetdescriptionresponse)›_

Returns a Promise object with keys "name" and "symbol".

---

### getBalance

▸ **getBalance**(`address`: string, `assetID`: string, `includePartial`: boolean): _Promise‹[GetBalanceResponse](../interfaces/avm_interfaces.getbalanceresponse)›_

_Defined in [src/apis/avm/api.ts:315](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/api.ts#L315)_

Gets the balance of a particular asset on a blockchain.

**Parameters:**

| Name             | Type    | Default | Description                                                   |
| ---------------- | ------- | ------- | ------------------------------------------------------------- |
| `address`        | string  | -       | The address to pull the asset balance from                    |
| `assetID`        | string  | -       | The assetID to pull the balance from                          |
| `includePartial` | boolean | false   | If includePartial=false, returns only the balance held solely |

**Returns:** _Promise‹[GetBalanceResponse](../interfaces/avm_interfaces.getbalanceresponse)›_

Promise with the balance of the assetID as a [BN](https://github.com/indutny/bn.js/) on the provided address for the blockchain.

---

### getBaseURL

▸ **getBaseURL**(): _string_

_Inherited from [APIBase](common_apibase.apibase).[getBaseURL](common_apibase.apibase#getbaseurl)_

_Defined in [src/common/apibase.ts:53](https://github.com/chain4travel/caminojs/blob/3883166/src/common/apibase.ts#L53)_

Returns the baseURL's path.

**Returns:** _string_

---

### getBlockchainAlias

▸ **getBlockchainAlias**(): _string_

_Defined in [src/apis/avm/api.ts:99](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/api.ts#L99)_

Gets the alias for the blockchainID if it exists, otherwise returns `undefined`.

**Returns:** _string_

The alias for the blockchainID

---

### getBlockchainID

▸ **getBlockchainID**(): _string_

_Defined in [src/apis/avm/api.ts:111](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/api.ts#L111)_

Gets the blockchainID and returns it.

**Returns:** _string_

The blockchainID

---

### getCreationTxFee

▸ **getCreationTxFee**(): _BN_

_Defined in [src/apis/avm/api.ts:234](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/api.ts#L234)_

Gets the creation fee for this chain.

**Returns:** _BN_

The creation fee as a [BN](https://github.com/indutny/bn.js/)

---

### getDB

▸ **getDB**(): _StoreAPI_

_Inherited from [APIBase](common_apibase.apibase).[getDB](common_apibase.apibase#getdb)_

_Defined in [src/common/apibase.ts:58](https://github.com/chain4travel/caminojs/blob/3883166/src/common/apibase.ts#L58)_

Returns the baseURL's database.

**Returns:** _StoreAPI_

---

### getDefaultCreationTxFee

▸ **getDefaultCreationTxFee**(): _BN_

_Defined in [src/apis/avm/api.ts:204](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/api.ts#L204)_

Gets the default creation fee for this chain.

**Returns:** _BN_

The default creation fee as a [BN](https://github.com/indutny/bn.js/)

---

### getDefaultMintTxFee

▸ **getDefaultMintTxFee**(): _BN_

_Defined in [src/apis/avm/api.ts:213](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/api.ts#L213)_

Gets the default mint fee for this chain.

**Returns:** _BN_

The default mint fee as a [BN](https://github.com/indutny/bn.js/)

---

### getDefaultTxFee

▸ **getDefaultTxFee**(): _BN_

_Defined in [src/apis/avm/api.ts:174](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/api.ts#L174)_

Gets the default tx fee for this chain.

**Returns:** _BN_

The default tx fee as a [BN](https://github.com/indutny/bn.js/)

---

### getMintTxFee

▸ **getMintTxFee**(): _BN_

_Defined in [src/apis/avm/api.ts:222](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/api.ts#L222)_

Gets the mint fee for this chain.

**Returns:** _BN_

The mint fee as a [BN](https://github.com/indutny/bn.js/)

---

### getRPCID

▸ **getRPCID**(): _number_

_Inherited from [EVMAPI](api_evm.evmapi).[getRPCID](api_evm.evmapi#getrpcid)_

_Defined in [src/common/jrpcapi.ts:77](https://github.com/chain4travel/caminojs/blob/3883166/src/common/jrpcapi.ts#L77)_

Returns the rpcid, a strictly-increasing number, starting from 1, indicating the next
request ID that will be sent.

**Returns:** _number_

---

### getTx

▸ **getTx**(`txID`: string, `encoding`: string): _Promise‹string | object›_

_Defined in [src/apis/avm/api.ts:901](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/api.ts#L901)_

Returns the transaction data of a provided transaction ID by calling the node's `getTx` method.

**Parameters:**

| Name       | Type   | Default | Description                                                                                       |
| ---------- | ------ | ------- | ------------------------------------------------------------------------------------------------- |
| `txID`     | string | -       | The string representation of the transaction ID                                                   |
| `encoding` | string | "hex"   | sets the format of the returned transaction. Can be, "cb58", "hex" or "json". Defaults to "cb58". |

**Returns:** _Promise‹string | object›_

Returns a Promise string or object containing the bytes retrieved from the node

---

### getTxFee

▸ **getTxFee**(): _BN_

_Defined in [src/apis/avm/api.ts:183](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/api.ts#L183)_

Gets the tx fee for this chain.

**Returns:** _BN_

The tx fee as a [BN](https://github.com/indutny/bn.js/)

---

### getTxStatus

▸ **getTxStatus**(`txID`: string): _Promise‹string›_

_Defined in [src/apis/avm/api.ts:923](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/api.ts#L923)_

Returns the status of a provided transaction ID by calling the node's `getTxStatus` method.

**Parameters:**

| Name   | Type   | Description                                     |
| ------ | ------ | ----------------------------------------------- |
| `txID` | string | The string representation of the transaction ID |

**Returns:** _Promise‹string›_

Returns a Promise string containing the status retrieved from the node

---

### getUTXOs

▸ **getUTXOs**(`addresses`: string[] | string, `sourceChain`: string, `limit`: number, `startIndex`: object, `persistOpts`: [PersistanceOptions](utils_persistanceoptions.persistanceoptions), `encoding`: string): _Promise‹[GetUTXOsResponse](../interfaces/avm_interfaces.getutxosresponse)›_

_Defined in [src/apis/avm/api.ts:949](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/api.ts#L949)_

Retrieves the UTXOs related to the addresses provided from the node's `getUTXOs` method.

**`remarks`**
persistOpts is optional and must be of type [PersistanceOptions](utils_persistanceoptions.persistanceoptions)

**Parameters:**

▪ **addresses**: _string[] | string_

An array of addresses as cb58 strings or addresses as [Buffer](https://github.com/feross/buffer)s

▪`Default value` **sourceChain**: _string_= undefined

A string for the chain to look for the UTXO's. Default is to use this chain, but if exported UTXOs exist from other chains, this can used to pull them instead.

▪`Default value` **limit**: _number_= 0

Optional. Returns at most [limit] addresses. If [limit] == 0 or > [maxUTXOsToFetch], fetches up to [maxUTXOsToFetch].

▪`Default value` **startIndex**: _object_= undefined

Optional. [StartIndex] defines where to start fetching UTXOs (for pagination.)
UTXOs fetched are from addresses equal to or greater than [StartIndex.Address]
For address [StartIndex.Address], only UTXOs with IDs greater than [StartIndex.Utxo] will be returned.

| Name      | Type   |
| --------- | ------ |
| `address` | string |
| `utxo`    | string |

▪`Default value` **persistOpts**: _[PersistanceOptions](utils_persistanceoptions.persistanceoptions)_= undefined

Options available to persist these UTXOs in local storage

▪`Default value` **encoding**: _string_= "hex"

**Returns:** _Promise‹[GetUTXOsResponse](../interfaces/avm_interfaces.getutxosresponse)›_

---

### import

▸ **import**(`username`: string, `password`: string, `to`: string, `sourceChain`: string): _Promise‹string›_

_Defined in [src/apis/avm/api.ts:796](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/api.ts#L796)_

Send ANT (Avalanche Native Token) assets including AVAX from an account on the P-Chain or C-Chain to an address on the X-Chain. This transaction
must be signed with the key of the account that the asset is sent from and which pays
the transaction fee.

**Parameters:**

| Name          | Type   | Description                                                   |
| ------------- | ------ | ------------------------------------------------------------- |
| `username`    | string | The Keystore user that controls the account specified in `to` |
| `password`    | string | The password of the Keystore user                             |
| `to`          | string | The address of the account the asset is sent to.              |
| `sourceChain` | string | The chainID where the funds are coming from. Ex: "C"          |

**Returns:** _Promise‹string›_

Promise for a string for the transaction, which should be sent to the network
by calling issueTx.

---

### importKey

▸ **importKey**(`username`: string, `password`: string, `privateKey`: string): _Promise‹string›_

_Defined in [src/apis/avm/api.ts:732](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/api.ts#L732)_

Imports a private key into the node's keystore under an user and for a blockchain.

**Parameters:**

| Name         | Type   | Description                                              |
| ------------ | ------ | -------------------------------------------------------- |
| `username`   | string | The name of the user to store the private key            |
| `password`   | string | The password that unlocks the user                       |
| `privateKey` | string | A string representing the private key in the vm's format |

**Returns:** _Promise‹string›_

The address for the imported private key.

---

### issueTx

▸ **issueTx**(`tx`: string | Buffer | [Tx](api_avm_transactions.tx)): _Promise‹string›_

_Defined in [src/apis/avm/api.ts:1722](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/api.ts#L1722)_

Calls the node's issueTx method from the API and returns the resulting transaction ID as a string.

**Parameters:**

| Name | Type                                                      | Description                                                                                                       |
| ---- | --------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------- |
| `tx` | string &#124; Buffer &#124; [Tx](api_avm_transactions.tx) | A string, [Buffer](https://github.com/feross/buffer), or [Tx](api_evm_transactions.tx) representing a transaction |

**Returns:** _Promise‹string›_

A Promise string representing the transaction ID of the posted transaction.

---

### keyChain

▸ **keyChain**(): _[KeyChain](api_avm_keychain.keychain)_

_Defined in [src/apis/avm/api.ts:264](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/api.ts#L264)_

Gets a reference to the keychain for this class.

**Returns:** _[KeyChain](api_avm_keychain.keychain)_

The instance of [KeyChain](api_evm_keychain.keychain) for this class

---

### listAddresses

▸ **listAddresses**(`username`: string, `password`: string): _Promise‹string[]›_

_Defined in [src/apis/avm/api.ts:823](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/api.ts#L823)_

Lists all the addresses under a user.

**Parameters:**

| Name       | Type   | Description                                    |
| ---------- | ------ | ---------------------------------------------- |
| `username` | string | The user to list addresses                     |
| `password` | string | The password of the user to list the addresses |

**Returns:** _Promise‹string[]›_

Promise of an array of address strings in the format specified by the blockchain.

---

### mint

▸ **mint**(`username`: string, `password`: string, `amount`: number | BN, `assetID`: Buffer | string, `to`: string, `minters`: string[]): _Promise‹string›_

_Defined in [src/apis/avm/api.ts:528](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/api.ts#L528)_

Create an unsigned transaction to mint more of an asset.

**Parameters:**

| Name       | Type                 | Description                                                      |
| ---------- | -------------------- | ---------------------------------------------------------------- |
| `username` | string               | -                                                                |
| `password` | string               | -                                                                |
| `amount`   | number &#124; BN     | The units of the asset to mint                                   |
| `assetID`  | Buffer &#124; string | The ID of the asset to mint                                      |
| `to`       | string               | The address to assign the units of the minted asset              |
| `minters`  | string[]             | Addresses of the minters responsible for signing the transaction |

**Returns:** _Promise‹string›_

Returns a Promise string containing the base 58 string representation of the unsigned transaction.

---

### mintNFT

▸ **mintNFT**(`username`: string, `password`: string, `from`: string[] | Buffer[], `changeAddr`: string, `payload`: string, `assetID`: string | Buffer, `to`: string, `encoding`: string): _Promise‹string›_

_Defined in [src/apis/avm/api.ts:576](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/api.ts#L576)_

Mint non-fungible tokens which were created with AVMAPI.createNFTAsset

**Parameters:**

| Name         | Type                     | Default   | Description                                                                                                         |
| ------------ | ------------------------ | --------- | ------------------------------------------------------------------------------------------------------------------- |
| `username`   | string                   | -         | The user paying the transaction fee (in $AVAX) for asset creation                                                   |
| `password`   | string                   | -         | The password for the user paying the transaction fee (in $AVAX) for asset creation                                  |
| `from`       | string[] &#124; Buffer[] | undefined | Optional. An array of addresses managed by the node's keystore for this blockchain which will fund this transaction |
| `changeAddr` | string                   | undefined | Optional. An address to send the change                                                                             |
| `payload`    | string                   | -         | -                                                                                                                   |
| `assetID`    | string &#124; Buffer     | -         | The asset id which is being sent                                                                                    |
| `to`         | string                   | -         | Address on X-Chain of the account to which this NFT is being sent                                                   |
| `encoding`   | string                   | "hex"     | Optional. is the encoding format to use for the payload argument. Can be either "cb58" or "hex". Defaults to "hex". |

**Returns:** _Promise‹string›_

ID of the transaction

---

### parseAddress

▸ **parseAddress**(`addr`: string): _Buffer_

_Defined in [src/apis/avm/api.ts:118](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/api.ts#L118)_

Takes an address string and returns its [Buffer](https://github.com/feross/buffer) representation if valid.

**Parameters:**

| Name   | Type   |
| ------ | ------ |
| `addr` | string |

**Returns:** _Buffer_

A [Buffer](https://github.com/feross/buffer) for the address if valid, undefined if not valid.

---

### send

▸ **send**(`username`: string, `password`: string, `assetID`: string | Buffer, `amount`: number | BN, `to`: string, `from`: string[] | Buffer[], `changeAddr`: string, `memo`: string | Buffer): _Promise‹[SendResponse](../interfaces/avm_interfaces.sendresponse)›_

_Defined in [src/apis/avm/api.ts:1808](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/api.ts#L1808)_

Sends an amount of assetID to the specified address from a list of owned of addresses.

**Parameters:**

| Name         | Type                     | Default   | Description                                                                                                         |
| ------------ | ------------------------ | --------- | ------------------------------------------------------------------------------------------------------------------- |
| `username`   | string                   | -         | The user that owns the private keys associated with the `from` addresses                                            |
| `password`   | string                   | -         | The password unlocking the user                                                                                     |
| `assetID`    | string &#124; Buffer     | -         | The assetID of the asset to send                                                                                    |
| `amount`     | number &#124; BN         | -         | The amount of the asset to be sent                                                                                  |
| `to`         | string                   | -         | The address of the recipient                                                                                        |
| `from`       | string[] &#124; Buffer[] | undefined | Optional. An array of addresses managed by the node's keystore for this blockchain which will fund this transaction |
| `changeAddr` | string                   | undefined | Optional. An address to send the change                                                                             |
| `memo`       | string &#124; Buffer     | undefined | Optional. CB58 Buffer or String which contains arbitrary bytes, up to 256 bytes                                     |

**Returns:** _Promise‹[SendResponse](../interfaces/avm_interfaces.sendresponse)›_

Promise for the string representing the transaction's ID.

---

### sendMultiple

▸ **sendMultiple**(`username`: string, `password`: string, `sendOutputs`: object[], `from`: string[] | Buffer[], `changeAddr`: string, `memo`: string | Buffer): _Promise‹[SendMultipleResponse](../interfaces/avm_interfaces.sendmultipleresponse)›_

_Defined in [src/apis/avm/api.ts:1885](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/api.ts#L1885)_

Sends an amount of assetID to an array of specified addresses from a list of owned of addresses.

**Parameters:**

| Name          | Type                     | Default   | Description                                                                                                         |
| ------------- | ------------------------ | --------- | ------------------------------------------------------------------------------------------------------------------- |
| `username`    | string                   | -         | The user that owns the private keys associated with the `from` addresses                                            |
| `password`    | string                   | -         | The password unlocking the user                                                                                     |
| `sendOutputs` | object[]                 | -         | The array of SendOutputs. A SendOutput is an object literal which contains an assetID, amount, and to.              |
| `from`        | string[] &#124; Buffer[] | undefined | Optional. An array of addresses managed by the node's keystore for this blockchain which will fund this transaction |
| `changeAddr`  | string                   | undefined | Optional. An address to send the change                                                                             |
| `memo`        | string &#124; Buffer     | undefined | Optional. CB58 Buffer or String which contains arbitrary bytes, up to 256 bytes                                     |

**Returns:** _Promise‹[SendMultipleResponse](../interfaces/avm_interfaces.sendmultipleresponse)›_

Promise for the string representing the transaction"s ID.

---

### sendNFT

▸ **sendNFT**(`username`: string, `password`: string, `from`: string[] | Buffer[], `changeAddr`: string, `assetID`: string | Buffer, `groupID`: number, `to`: string): _Promise‹string›_

_Defined in [src/apis/avm/api.ts:642](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/api.ts#L642)_

Send NFT from one account to another on X-Chain

**Parameters:**

| Name         | Type                     | Default   | Description                                                                                                         |
| ------------ | ------------------------ | --------- | ------------------------------------------------------------------------------------------------------------------- |
| `username`   | string                   | -         | The user paying the transaction fee (in $AVAX) for asset creation                                                   |
| `password`   | string                   | -         | The password for the user paying the transaction fee (in $AVAX) for asset creation                                  |
| `from`       | string[] &#124; Buffer[] | undefined | Optional. An array of addresses managed by the node's keystore for this blockchain which will fund this transaction |
| `changeAddr` | string                   | undefined | Optional. An address to send the change                                                                             |
| `assetID`    | string &#124; Buffer     | -         | The asset id which is being sent                                                                                    |
| `groupID`    | number                   | -         | The group this NFT is issued to.                                                                                    |
| `to`         | string                   | -         | Address on X-Chain of the account to which this NFT is being sent                                                   |

**Returns:** _Promise‹string›_

ID of the transaction

---

### setAVAXAssetID

▸ **setAVAXAssetID**(`avaxAssetID`: string | Buffer): _void_

_Defined in [src/apis/avm/api.ts:162](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/api.ts#L162)_

Overrides the defaults and sets the cache to a specific AVAX AssetID

**Parameters:**

| Name          | Type                 | Description                                           |
| ------------- | -------------------- | ----------------------------------------------------- |
| `avaxAssetID` | string &#124; Buffer | A cb58 string or Buffer representing the AVAX AssetID |

**Returns:** _void_

The the provided string representing the AVAX AssetID

---

### setBaseURL

▸ **setBaseURL**(`baseURL`: string): _void_

_Inherited from [APIBase](common_apibase.apibase).[setBaseURL](common_apibase.apibase#setbaseurl)_

_Defined in [src/common/apibase.ts:37](https://github.com/chain4travel/caminojs/blob/3883166/src/common/apibase.ts#L37)_

Sets the path of the APIs baseURL.

**Parameters:**

| Name      | Type   | Description                                |
| --------- | ------ | ------------------------------------------ |
| `baseURL` | string | Path of the APIs baseURL - ex: "/ext/bc/X" |

**Returns:** _void_

---

### setCreationTxFee

▸ **setCreationTxFee**(`fee`: BN): _void_

_Defined in [src/apis/avm/api.ts:255](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/api.ts#L255)_

Sets the creation fee for this chain.

**Parameters:**

| Name  | Type | Description                                                               |
| ----- | ---- | ------------------------------------------------------------------------- |
| `fee` | BN   | The creation fee amount to set as [BN](https://github.com/indutny/bn.js/) |

**Returns:** _void_

---

### setMintTxFee

▸ **setMintTxFee**(`fee`: BN): _void_

_Defined in [src/apis/avm/api.ts:246](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/api.ts#L246)_

Sets the mint fee for this chain.

**Parameters:**

| Name  | Type | Description                                                           |
| ----- | ---- | --------------------------------------------------------------------- |
| `fee` | BN   | The mint fee amount to set as [BN](https://github.com/indutny/bn.js/) |

**Returns:** _void_

---

### setTxFee

▸ **setTxFee**(`fee`: BN): _void_

_Defined in [src/apis/avm/api.ts:195](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/api.ts#L195)_

Sets the tx fee for this chain.

**Parameters:**

| Name  | Type | Description                                                         |
| ----- | ---- | ------------------------------------------------------------------- |
| `fee` | BN   | The tx fee amount to set as [BN](https://github.com/indutny/bn.js/) |

**Returns:** _void_

---

### signTx

▸ **signTx**(`utx`: [UnsignedTx](api_avm_transactions.unsignedtx)): _[Tx](api_avm_transactions.tx)_

_Defined in [src/apis/avm/api.ts:1713](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/api.ts#L1713)_

Helper function which takes an unsigned transaction and signs it, returning the resulting [Tx](api_evm_transactions.tx).

**Parameters:**

| Name  | Type                                          | Description                                                                    |
| ----- | --------------------------------------------- | ------------------------------------------------------------------------------ |
| `utx` | [UnsignedTx](api_avm_transactions.unsignedtx) | The unsigned transaction of type [UnsignedTx](api_evm_transactions.unsignedtx) |

**Returns:** _[Tx](api_avm_transactions.tx)_

A signed transaction of type [Tx](api_evm_transactions.tx)
