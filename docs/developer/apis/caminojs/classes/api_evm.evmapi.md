# Class: EVMAPI

Class for interacting with a node's EVMAPI

**`remarks`** This extends the [JRPCAPI](../modules/src_common#jrpcapi) class. This class should not be directly called. Instead, use the [Avalanche.addAPI](avalanche.avalanche-1#addapi) function to register this interface with Avalanche.

## Hierarchy

↳ [JRPCAPI](common_jrpcapi.jrpcapi)

↳ **EVMAPI**

## Index

### Constructors

- [constructor](api_evm.evmapi#constructor)

### Properties

- [AVAXAssetID](api_evm.evmapi#protected-avaxassetid)
- [baseURL](api_evm.evmapi#protected-baseurl)
- [blockchainAlias](api_evm.evmapi#protected-blockchainalias)
- [blockchainID](api_evm.evmapi#protected-blockchainid)
- [core](api_evm.evmapi#protected-core)
- [db](api_evm.evmapi#protected-db)
- [jrpcVersion](api_evm.evmapi#protected-jrpcversion)
- [rpcID](api_evm.evmapi#protected-rpcid)
- [txFee](api_evm.evmapi#protected-txfee)

### Methods

- [addressFromBuffer](api_evm.evmapi#addressfrombuffer)
- [buildExportTx](api_evm.evmapi#buildexporttx)
- [buildImportTx](api_evm.evmapi#buildimporttx)
- [callMethod](api_evm.evmapi#callmethod)
- [export](api_evm.evmapi#export)
- [exportAVAX](api_evm.evmapi#exportavax)
- [exportKey](api_evm.evmapi#exportkey)
- [getAVAXAssetID](api_evm.evmapi#getavaxassetid)
- [getAssetBalance](api_evm.evmapi#getassetbalance)
- [getAssetDescription](api_evm.evmapi#getassetdescription)
- [getAtomicTx](api_evm.evmapi#getatomictx)
- [getAtomicTxStatus](api_evm.evmapi#getatomictxstatus)
- [getBaseFee](api_evm.evmapi#getbasefee)
- [getBaseURL](api_evm.evmapi#getbaseurl)
- [getBlockchainAlias](api_evm.evmapi#getblockchainalias)
- [getBlockchainID](api_evm.evmapi#getblockchainid)
- [getDB](api_evm.evmapi#getdb)
- [getDefaultTxFee](api_evm.evmapi#getdefaulttxfee)
- [getMaxPriorityFeePerGas](api_evm.evmapi#getmaxpriorityfeepergas)
- [getRPCID](api_evm.evmapi#getrpcid)
- [getTxFee](api_evm.evmapi#gettxfee)
- [getUTXOs](api_evm.evmapi#getutxos)
- [import](api_evm.evmapi#import)
- [importAVAX](api_evm.evmapi#importavax)
- [importKey](api_evm.evmapi#importkey)
- [issueTx](api_evm.evmapi#issuetx)
- [keyChain](api_evm.evmapi#keychain)
- [newKeyChain](api_evm.evmapi#newkeychain)
- [parseAddress](api_evm.evmapi#parseaddress)
- [setAVAXAssetID](api_evm.evmapi#setavaxassetid)
- [setBaseURL](api_evm.evmapi#setbaseurl)

## Constructors

### constructor

\+ **new EVMAPI**(`core`: [AvalancheCore](avalanchecore.avalanchecore-1), `baseURL`: string, `blockchainID`: string): _[EVMAPI](api_evm.evmapi)_

_Overrides [JRPCAPI](common_jrpcapi.jrpcapi).[constructor](common_jrpcapi.jrpcapi#constructor)_

_Defined in [src/apis/evm/api.ts:813](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/api.ts#L813)_

This class should not be instantiated directly.
Instead use the [Avalanche.addAPI](avalanche.avalanche-1#addapi) method.

**Parameters:**

| Name           | Type                                           | Default          | Description                                                                 |
| -------------- | ---------------------------------------------- | ---------------- | --------------------------------------------------------------------------- |
| `core`         | [AvalancheCore](avalanchecore.avalanchecore-1) | -                | A reference to the Avalanche class                                          |
| `baseURL`      | string                                         | "/ext/bc/C/avax" | Defaults to the string "/ext/bc/C/avax" as the path to blockchain's baseURL |
| `blockchainID` | string                                         | ""               | The Blockchain's ID. Defaults to an empty string: ""                        |

**Returns:** _[EVMAPI](api_evm.evmapi)_

## Properties

### `Protected` AVAXAssetID

• **AVAXAssetID**: _Buffer_ = undefined

_Defined in [src/apis/evm/api.ts:65](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/api.ts#L65)_

---

### `Protected` baseURL

• **baseURL**: _string_

_Inherited from [APIBase](common_apibase.apibase).[baseURL](common_apibase.apibase#protected-baseurl)_

_Defined in [src/common/apibase.ts:29](https://github.com/chain4travel/caminojs/blob/3883166/src/common/apibase.ts#L29)_

---

### `Protected` blockchainAlias

• **blockchainAlias**: _string_ = undefined

_Defined in [src/apis/evm/api.ts:64](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/api.ts#L64)_

---

### `Protected` blockchainID

• **blockchainID**: _string_ = ""

_Defined in [src/apis/evm/api.ts:63](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/api.ts#L63)_

---

### `Protected` core

• **core**: _[AvalancheCore](avalanchecore.avalanchecore-1)_

_Inherited from [APIBase](common_apibase.apibase).[core](common_apibase.apibase#protected-core)_

_Defined in [src/common/apibase.ts:28](https://github.com/chain4travel/caminojs/blob/3883166/src/common/apibase.ts#L28)_

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

### `Protected` rpcID

• **rpcID**: _number_ = 1

_Inherited from [EVMAPI](api_evm.evmapi).[rpcID](api_evm.evmapi#protected-rpcid)_

_Defined in [src/common/jrpcapi.ts:13](https://github.com/chain4travel/caminojs/blob/3883166/src/common/jrpcapi.ts#L13)_

---

### `Protected` txFee

• **txFee**: _BN_ = undefined

_Defined in [src/apis/evm/api.ts:66](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/api.ts#L66)_

## Methods

### addressFromBuffer

▸ **addressFromBuffer**(`address`: Buffer): _string_

_Defined in [src/apis/evm/api.ts:103](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/api.ts#L103)_

**Parameters:**

| Name      | Type   |
| --------- | ------ |
| `address` | Buffer |

**Returns:** _string_

---

### buildExportTx

▸ **buildExportTx**(`amount`: BN, `assetID`: Buffer | string, `destinationChain`: Buffer | string, `fromAddressHex`: string, `fromAddressBech`: string, `toAddresses`: string[], `nonce`: number, `locktime`: BN, `threshold`: number, `fee`: BN): _Promise‹[UnsignedTx](api_evm_transactions.unsignedtx)›_

_Defined in [src/apis/evm/api.ts:650](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/api.ts#L650)_

Helper function which creates an unsigned Export Tx. For more granular control, you may create your own
[UnsignedTx](api_evm_transactions.unsignedtx) manually (with their corresponding [TransferableInput](api_evm_inputs.transferableinput)s, [TransferableOutput](api_evm_outputs.transferableoutput)s).

**Parameters:**

| Name               | Type                 | Default   | Description                                                                          |
| ------------------ | -------------------- | --------- | ------------------------------------------------------------------------------------ |
| `amount`           | BN                   | -         | The amount being exported as a [BN](https://github.com/indutny/bn.js/)               |
| `assetID`          | Buffer &#124; string | -         | The asset id which is being sent                                                     |
| `destinationChain` | Buffer &#124; string | -         | The chainid for where the assets will be sent.                                       |
| `fromAddressHex`   | string               | -         | -                                                                                    |
| `fromAddressBech`  | string               | -         | -                                                                                    |
| `toAddresses`      | string[]             | -         | The addresses to send the funds                                                      |
| `nonce`            | number               | 0         | -                                                                                    |
| `locktime`         | BN                   | new BN(0) | Optional. The locktime field created in the resulting outputs                        |
| `threshold`        | number               | 1         | Optional. The number of signatures required to spend the funds in the resultant UTXO |
| `fee`              | BN                   | new BN(0) | -                                                                                    |

**Returns:** _Promise‹[UnsignedTx](api_evm_transactions.unsignedtx)›_

An unsigned transaction ([UnsignedTx](api_evm_transactions.unsignedtx)) which contains an [ExportTx](api_evm_exporttx.exporttx).

---

### buildImportTx

▸ **buildImportTx**(`utxoset`: [UTXOSet](api_evm_utxos.utxoset), `toAddress`: string, `ownerAddresses`: string[], `sourceChain`: Buffer | string, `fromAddresses`: string[], `fee`: BN): _Promise‹[UnsignedTx](api_evm_transactions.unsignedtx)›_

_Defined in [src/apis/evm/api.ts:575](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/api.ts#L575)_

Helper function which creates an unsigned Import Tx. For more granular control, you may create your own
[UnsignedTx](api_evm_transactions.unsignedtx) manually (with their corresponding [TransferableInput](api_evm_inputs.transferableinput)s, [TransferableOutput](api_evm_outputs.transferableoutput)s).

**`remarks`**
This helper exists because the endpoint API should be the primary point of entry for most functionality.

**Parameters:**

| Name             | Type                             | Default   | Description                                                        |
| ---------------- | -------------------------------- | --------- | ------------------------------------------------------------------ |
| `utxoset`        | [UTXOSet](api_evm_utxos.utxoset) | -         | A set of UTXOs that the transaction is built on                    |
| `toAddress`      | string                           | -         | The address to send the funds                                      |
| `ownerAddresses` | string[]                         | -         | The addresses being used to import                                 |
| `sourceChain`    | Buffer &#124; string             | -         | The chainid for where the import is coming from                    |
| `fromAddresses`  | string[]                         | -         | The addresses being used to send the funds from the UTXOs provided |
| `fee`            | BN                               | new BN(0) | -                                                                  |

**Returns:** _Promise‹[UnsignedTx](api_evm_transactions.unsignedtx)›_

An unsigned transaction ([UnsignedTx](api_evm_transactions.unsignedtx)) which contains a [ImportTx](api_evm_importtx.importtx).

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

### export

▸ **export**(`username`: string, `password`: string, `to`: string, `amount`: BN, `assetID`: string): _Promise‹string›_

_Defined in [src/apis/evm/api.ts:286](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/api.ts#L286)_

Send ANT (Avalanche Native Token) assets including AVAX from the C-Chain to an account on the X-Chain.

After calling this method, you must call the X-Chain’s import method to complete the transfer.

**Parameters:**

| Name       | Type   | Description                                                            |
| ---------- | ------ | ---------------------------------------------------------------------- |
| `username` | string | The Keystore user that controls the X-Chain account specified in `to`  |
| `password` | string | The password of the Keystore user                                      |
| `to`       | string | The account on the X-Chain to send the AVAX to.                        |
| `amount`   | BN     | Amount of asset to export as a [BN](https://github.com/indutny/bn.js/) |
| `assetID`  | string | The asset id which is being sent                                       |

**Returns:** _Promise‹string›_

String representing the transaction id

---

### exportAVAX

▸ **exportAVAX**(`username`: string, `password`: string, `to`: string, `amount`: BN): _Promise‹string›_

_Defined in [src/apis/evm/api.ts:321](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/api.ts#L321)_

Send AVAX from the C-Chain to an account on the X-Chain.

After calling this method, you must call the X-Chain’s importAVAX method to complete the transfer.

**Parameters:**

| Name       | Type   | Description                                                           |
| ---------- | ------ | --------------------------------------------------------------------- |
| `username` | string | The Keystore user that controls the X-Chain account specified in `to` |
| `password` | string | The password of the Keystore user                                     |
| `to`       | string | The account on the X-Chain to send the AVAX to.                       |
| `amount`   | BN     | Amount of AVAX to export as a [BN](https://github.com/indutny/bn.js/) |

**Returns:** _Promise‹string›_

String representing the transaction id

---

### exportKey

▸ **exportKey**(`username`: string, `password`: string, `address`: string): _Promise‹object›_

_Defined in [src/apis/evm/api.ts:543](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/api.ts#L543)_

Exports the private key for an address.

**Parameters:**

| Name       | Type   | Description                                      |
| ---------- | ------ | ------------------------------------------------ |
| `username` | string | The name of the user with the private key        |
| `password` | string | The password used to decrypt the private key     |
| `address`  | string | The address whose private key should be exported |

**Returns:** _Promise‹object›_

Promise with the decrypted private key and private key hex as store in the database

---

### getAVAXAssetID

▸ **getAVAXAssetID**(`refresh`: boolean): _Promise‹Buffer›_

_Defined in [src/apis/evm/api.ts:161](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/api.ts#L161)_

Fetches the AVAX AssetID and returns it in a Promise.

**Parameters:**

| Name      | Type    | Default | Description                                                            |
| --------- | ------- | ------- | ---------------------------------------------------------------------- |
| `refresh` | boolean | false   | This function caches the response. Refresh = true will bust the cache. |

**Returns:** _Promise‹Buffer›_

The the provided string representing the AVAX AssetID

---

### getAssetBalance

▸ **getAssetBalance**(`hexAddress`: string, `blockHeight`: string, `assetID`: string): _Promise‹object›_

_Defined in [src/apis/evm/api.ts:204](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/api.ts#L204)_

returns the amount of [assetID] for the given address in the state of the given block number.
"latest", "pending", and "accepted" meta block numbers are also allowed.

**Parameters:**

| Name          | Type   | Description                           |
| ------------- | ------ | ------------------------------------- |
| `hexAddress`  | string | The hex representation of the address |
| `blockHeight` | string | The block height                      |
| `assetID`     | string | The asset ID                          |

**Returns:** _Promise‹object›_

Returns a Promise object containing the balance

---

### getAssetDescription

▸ **getAssetDescription**(`assetID`: Buffer | string): _Promise‹any›_

_Defined in [src/apis/evm/api.ts:123](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/api.ts#L123)_

Retrieves an assets name and symbol.

**Parameters:**

| Name      | Type                 | Description                                                                                                   |
| --------- | -------------------- | ------------------------------------------------------------------------------------------------------------- |
| `assetID` | Buffer &#124; string | Either a [Buffer](https://github.com/feross/buffer) or an b58 serialized string for the AssetID or its alias. |

**Returns:** _Promise‹any›_

Returns a Promise Asset with keys "name", "symbol", "assetID" and "denomination".

---

### getAtomicTx

▸ **getAtomicTx**(`txID`: string): _Promise‹string›_

_Defined in [src/apis/evm/api.ts:249](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/api.ts#L249)_

Returns the transaction data of a provided transaction ID by calling the node's `getAtomicTx` method.

**Parameters:**

| Name   | Type   | Description                                     |
| ------ | ------ | ----------------------------------------------- |
| `txID` | string | The string representation of the transaction ID |

**Returns:** _Promise‹string›_

Returns a Promise string containing the bytes retrieved from the node

---

### getAtomicTxStatus

▸ **getAtomicTxStatus**(`txID`: string): _Promise‹string›_

_Defined in [src/apis/evm/api.ts:228](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/api.ts#L228)_

Returns the status of a provided atomic transaction ID by calling the node's `getAtomicTxStatus` method.

**Parameters:**

| Name   | Type   | Description                                     |
| ------ | ------ | ----------------------------------------------- |
| `txID` | string | The string representation of the transaction ID |

**Returns:** _Promise‹string›_

Returns a Promise string containing the status retrieved from the node

---

### getBaseFee

▸ **getBaseFee**(): _Promise‹string›_

_Defined in [src/apis/evm/api.ts:845](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/api.ts#L845)_

**Returns:** _Promise‹string›_

a Promise string containing the base fee for the next block.

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

_Defined in [src/apis/evm/api.ts:73](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/api.ts#L73)_

Gets the alias for the blockchainID if it exists, otherwise returns `undefined`.

**Returns:** _string_

The alias for the blockchainID

---

### getBlockchainID

▸ **getBlockchainID**(): _string_

_Defined in [src/apis/evm/api.ts:85](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/api.ts#L85)_

Gets the blockchainID and returns it.

**Returns:** _string_

The blockchainID

---

### getDB

▸ **getDB**(): _StoreAPI_

_Inherited from [APIBase](common_apibase.apibase).[getDB](common_apibase.apibase#getdb)_

_Defined in [src/common/apibase.ts:58](https://github.com/chain4travel/caminojs/blob/3883166/src/common/apibase.ts#L58)_

Returns the baseURL's database.

**Returns:** _StoreAPI_

---

### getDefaultTxFee

▸ **getDefaultTxFee**(): _BN_

_Defined in [src/apis/evm/api.ts:190](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/api.ts#L190)_

Gets the default tx fee for this chain.

**Returns:** _BN_

The default tx fee as a [BN](https://github.com/indutny/bn.js/)

---

### getMaxPriorityFeePerGas

▸ **getMaxPriorityFeePerGas**(): _Promise‹string›_

_Defined in [src/apis/evm/api.ts:862](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/api.ts#L862)_

returns the priority fee needed to be included in a block.

**Returns:** _Promise‹string›_

Returns a Promise string containing the priority fee needed to be included in a block.

---

### getRPCID

▸ **getRPCID**(): _number_

_Inherited from [EVMAPI](api_evm.evmapi).[getRPCID](api_evm.evmapi#getrpcid)_

_Defined in [src/common/jrpcapi.ts:77](https://github.com/chain4travel/caminojs/blob/3883166/src/common/jrpcapi.ts#L77)_

Returns the rpcid, a strictly-increasing number, starting from 1, indicating the next
request ID that will be sent.

**Returns:** _number_

---

### getTxFee

▸ **getTxFee**(): _BN_

_Defined in [src/apis/evm/api.ts:266](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/api.ts#L266)_

Gets the tx fee for this chain.

**Returns:** _BN_

The tx fee as a [BN](https://github.com/indutny/bn.js/)

---

### getUTXOs

▸ **getUTXOs**(`addresses`: string[] | string, `sourceChain`: string, `limit`: number, `startIndex`: [Index](../interfaces/common_interfaces.index), `encoding`: string): _Promise‹object›_

_Defined in [src/apis/evm/api.ts:353](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/api.ts#L353)_

Retrieves the UTXOs related to the addresses provided from the node's `getUTXOs` method.

**Parameters:**

| Name          | Type                                           | Default   | Description                                                                                                                                                                                                                                                          |
| ------------- | ---------------------------------------------- | --------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `addresses`   | string[] &#124; string                         | -         | An array of addresses as cb58 strings or addresses as [Buffer](https://github.com/feross/buffer)s                                                                                                                                                                    |
| `sourceChain` | string                                         | undefined | A string for the chain to look for the UTXO's. Default is to use this chain, but if exported UTXOs exist from other chains, this can used to pull them instead.                                                                                                      |
| `limit`       | number                                         | 0         | Optional. Returns at most [limit] addresses. If [limit] == 0 or > [maxUTXOsToFetch], fetches up to [maxUTXOsToFetch].                                                                                                                                                |
| `startIndex`  | [Index](../interfaces/common_interfaces.index) | undefined | Optional. [StartIndex] defines where to start fetching UTXOs (for pagination.) UTXOs fetched are from addresses equal to or greater than [StartIndex.Address] For address [StartIndex.Address], only UTXOs with IDs greater than [StartIndex.Utxo] will be returned. |
| `encoding`    | string                                         | "hex"     | -                                                                                                                                                                                                                                                                    |

**Returns:** _Promise‹object›_

---

### import

▸ **import**(`username`: string, `password`: string, `to`: string, `sourceChain`: string): _Promise‹string›_

_Defined in [src/apis/evm/api.ts:414](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/api.ts#L414)_

Send ANT (Avalanche Native Token) assets including AVAX from an account on the X-Chain to an address on the C-Chain. This transaction
must be signed with the key of the account that the asset is sent from and which pays
the transaction fee.

**Parameters:**

| Name          | Type   | Description                                                   |
| ------------- | ------ | ------------------------------------------------------------- |
| `username`    | string | The Keystore user that controls the account specified in `to` |
| `password`    | string | The password of the Keystore user                             |
| `to`          | string | The address of the account the asset is sent to.              |
| `sourceChain` | string | The chainID where the funds are coming from. Ex: "X"          |

**Returns:** _Promise‹string›_

Promise for a string for the transaction, which should be sent to the network
by calling issueTx.

---

### importAVAX

▸ **importAVAX**(`username`: string, `password`: string, `to`: string, `sourceChain`: string): _Promise‹string›_

_Defined in [src/apis/evm/api.ts:449](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/api.ts#L449)_

Send AVAX from an account on the X-Chain to an address on the C-Chain. This transaction
must be signed with the key of the account that the AVAX is sent from and which pays
the transaction fee.

**Parameters:**

| Name          | Type   | Description                                                                                                                                    |
| ------------- | ------ | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| `username`    | string | The Keystore user that controls the account specified in `to`                                                                                  |
| `password`    | string | The password of the Keystore user                                                                                                              |
| `to`          | string | The address of the account the AVAX is sent to. This must be the same as the to argument in the corresponding call to the X-Chain’s exportAVAX |
| `sourceChain` | string | The chainID where the funds are coming from.                                                                                                   |

**Returns:** _Promise‹string›_

Promise for a string for the transaction, which should be sent to the network
by calling issueTx.

---

### importKey

▸ **importKey**(`username`: string, `password`: string, `privateKey`: string): _Promise‹string›_

_Defined in [src/apis/evm/api.ts:479](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/api.ts#L479)_

Give a user control over an address by providing the private key that controls the address.

**Parameters:**

| Name         | Type   | Description                                              |
| ------------ | ------ | -------------------------------------------------------- |
| `username`   | string | The name of the user to store the private key            |
| `password`   | string | The password that unlocks the user                       |
| `privateKey` | string | A string representing the private key in the vm"s format |

**Returns:** _Promise‹string›_

The address for the imported private key.

---

### issueTx

▸ **issueTx**(`tx`: string | Buffer | [Tx](api_evm_transactions.tx)): _Promise‹string›_

_Defined in [src/apis/evm/api.ts:505](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/api.ts#L505)_

Calls the node's issueTx method from the API and returns the resulting transaction ID as a string.

**Parameters:**

| Name | Type                                                      | Description                                                                                                       |
| ---- | --------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------- |
| `tx` | string &#124; Buffer &#124; [Tx](api_evm_transactions.tx) | A string, [Buffer](https://github.com/feross/buffer), or [Tx](api_evm_transactions.tx) representing a transaction |

**Returns:** _Promise‹string›_

A Promise string representing the transaction ID of the posted transaction.

---

### keyChain

▸ **keyChain**(): _[KeyChain](api_evm_keychain.keychain)_

_Defined in [src/apis/evm/api.ts:763](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/api.ts#L763)_

Gets a reference to the keychain for this class.

**Returns:** _[KeyChain](api_evm_keychain.keychain)_

The instance of [KeyChain](api_evm_keychain.keychain) for this class

---

### newKeyChain

▸ **newKeyChain**(): _[KeyChain](api_evm_keychain.keychain)_

_Defined in [src/apis/evm/api.ts:769](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/api.ts#L769)_

**Returns:** _[KeyChain](api_evm_keychain.keychain)_

new instance of [KeyChain](api_evm_keychain.keychain)

---

### parseAddress

▸ **parseAddress**(`addr`: string): _Buffer_

_Defined in [src/apis/evm/api.ts:92](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/api.ts#L92)_

Takes an address string and returns its [Buffer](https://github.com/feross/buffer) representation if valid.

**Parameters:**

| Name   | Type   |
| ------ | ------ |
| `addr` | string |

**Returns:** _Buffer_

A [Buffer](https://github.com/feross/buffer) for the address if valid, undefined if not valid.

---

### setAVAXAssetID

▸ **setAVAXAssetID**(`avaxAssetID`: string | Buffer): _void_

_Defined in [src/apis/evm/api.ts:178](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/api.ts#L178)_

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
