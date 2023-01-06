# Class: PlatformVMAPI

Class for interacting with a node's PlatformVMAPI

**`remarks`** This extends the [JRPCAPI](../modules/src_common#jrpcapi) class. This class should not be directly called. Instead, use the [Avalanche.addAPI](avalanche.avalanche-1#addapi) function to register this interface with Avalanche.

## Hierarchy

↳ [JRPCAPI](common_jrpcapi.jrpcapi)

↳ **PlatformVMAPI**

## Index

### Constructors

- [constructor](api_platformvm.platformvmapi#constructor)

### Properties

- [AVAXAssetID](api_platformvm.platformvmapi#protected-avaxassetid)
- [baseURL](api_platformvm.platformvmapi#protected-baseurl)
- [blockchainAlias](api_platformvm.platformvmapi#protected-blockchainalias)
- [blockchainID](api_platformvm.platformvmapi#protected-blockchainid)
- [core](api_platformvm.platformvmapi#protected-core)
- [creationTxFee](api_platformvm.platformvmapi#protected-creationtxfee)
- [db](api_platformvm.platformvmapi#protected-db)
- [jrpcVersion](api_platformvm.platformvmapi#protected-jrpcversion)
- [minDelegatorStake](api_platformvm.platformvmapi#protected-mindelegatorstake)
- [minValidatorStake](api_platformvm.platformvmapi#protected-minvalidatorstake)
- [rpcID](api_platformvm.platformvmapi#protected-rpcid)
- [txFee](api_platformvm.platformvmapi#protected-txfee)

### Methods

- [addDelegator](api_platformvm.platformvmapi#adddelegator)
- [addSubnetValidator](api_platformvm.platformvmapi#addsubnetvalidator)
- [addValidator](api_platformvm.platformvmapi#addvalidator)
- [addressFromBuffer](api_platformvm.platformvmapi#addressfrombuffer)
- [buildAddDelegatorTx](api_platformvm.platformvmapi#buildadddelegatortx)
- [buildAddSubnetValidatorTx](api_platformvm.platformvmapi#buildaddsubnetvalidatortx)
- [buildAddValidatorTx](api_platformvm.platformvmapi#buildaddvalidatortx)
- [buildCreateChainTx](api_platformvm.platformvmapi#buildcreatechaintx)
- [buildCreateSubnetTx](api_platformvm.platformvmapi#buildcreatesubnettx)
- [buildExportTx](api_platformvm.platformvmapi#buildexporttx)
- [buildImportTx](api_platformvm.platformvmapi#buildimporttx)
- [callMethod](api_platformvm.platformvmapi#callmethod)
- [checkGooseEgg](api_platformvm.platformvmapi#checkgooseegg)
- [createAddress](api_platformvm.platformvmapi#createaddress)
- [createBlockchain](api_platformvm.platformvmapi#createblockchain)
- [createSubnet](api_platformvm.platformvmapi#createsubnet)
- [exportAVAX](api_platformvm.platformvmapi#exportavax)
- [exportKey](api_platformvm.platformvmapi#exportkey)
- [getAVAXAssetID](api_platformvm.platformvmapi#getavaxassetid)
- [getBalance](api_platformvm.platformvmapi#getbalance)
- [getBaseURL](api_platformvm.platformvmapi#getbaseurl)
- [getBlockchainAlias](api_platformvm.platformvmapi#getblockchainalias)
- [getBlockchainID](api_platformvm.platformvmapi#getblockchainid)
- [getBlockchainStatus](api_platformvm.platformvmapi#getblockchainstatus)
- [getBlockchains](api_platformvm.platformvmapi#getblockchains)
- [getConfiguration](api_platformvm.platformvmapi#getconfiguration)
- [getCreateChainTxFee](api_platformvm.platformvmapi#getcreatechaintxfee)
- [getCreateSubnetTxFee](api_platformvm.platformvmapi#getcreatesubnettxfee)
- [getCreationTxFee](api_platformvm.platformvmapi#getcreationtxfee)
- [getCurrentSupply](api_platformvm.platformvmapi#getcurrentsupply)
- [getCurrentValidators](api_platformvm.platformvmapi#getcurrentvalidators)
- [getDB](api_platformvm.platformvmapi#getdb)
- [getDefaultCreationTxFee](api_platformvm.platformvmapi#getdefaultcreationtxfee)
- [getDefaultTxFee](api_platformvm.platformvmapi#getdefaulttxfee)
- [getHeight](api_platformvm.platformvmapi#getheight)
- [getMaxStakeAmount](api_platformvm.platformvmapi#getmaxstakeamount)
- [getMinStake](api_platformvm.platformvmapi#getminstake)
- [getPendingValidators](api_platformvm.platformvmapi#getpendingvalidators)
- [getRPCID](api_platformvm.platformvmapi#getrpcid)
- [getRewardUTXOs](api_platformvm.platformvmapi#getrewardutxos)
- [getStake](api_platformvm.platformvmapi#getstake)
- [getStakingAssetID](api_platformvm.platformvmapi#getstakingassetid)
- [getSubnets](api_platformvm.platformvmapi#getsubnets)
- [getTimestamp](api_platformvm.platformvmapi#gettimestamp)
- [getTotalStake](api_platformvm.platformvmapi#gettotalstake)
- [getTx](api_platformvm.platformvmapi#gettx)
- [getTxFee](api_platformvm.platformvmapi#gettxfee)
- [getTxStatus](api_platformvm.platformvmapi#gettxstatus)
- [getUTXOs](api_platformvm.platformvmapi#getutxos)
- [getValidatorsAt](api_platformvm.platformvmapi#getvalidatorsat)
- [importAVAX](api_platformvm.platformvmapi#importavax)
- [importKey](api_platformvm.platformvmapi#importkey)
- [issueTx](api_platformvm.platformvmapi#issuetx)
- [keyChain](api_platformvm.platformvmapi#keychain)
- [listAddresses](api_platformvm.platformvmapi#listaddresses)
- [parseAddress](api_platformvm.platformvmapi#parseaddress)
- [sampleValidators](api_platformvm.platformvmapi#samplevalidators)
- [setAVAXAssetID](api_platformvm.platformvmapi#setavaxassetid)
- [setBaseURL](api_platformvm.platformvmapi#setbaseurl)
- [setCreationTxFee](api_platformvm.platformvmapi#setcreationtxfee)
- [setMinStake](api_platformvm.platformvmapi#setminstake)
- [setTxFee](api_platformvm.platformvmapi#settxfee)
- [validatedBy](api_platformvm.platformvmapi#validatedby)
- [validates](api_platformvm.platformvmapi#validates)

## Constructors

### constructor

\+ **new PlatformVMAPI**(`core`: [AvalancheCore](avalanchecore.avalanchecore-1), `baseURL`: string): _[PlatformVMAPI](api_platformvm.platformvmapi)_

_Overrides [JRPCAPI](common_jrpcapi.jrpcapi).[constructor](common_jrpcapi.jrpcapi#constructor)_

_Defined in [src/apis/platformvm/api.ts:1896](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/api.ts#L1896)_

This class should not be instantiated directly.
Instead use the [Avalanche.addAPI](avalanche.avalanche-1#addapi) method.

**Parameters:**

| Name      | Type                                           | Default     | Description                                                         |
| --------- | ---------------------------------------------- | ----------- | ------------------------------------------------------------------- |
| `core`    | [AvalancheCore](avalanchecore.avalanchecore-1) | -           | A reference to the Avalanche class                                  |
| `baseURL` | string                                         | "/ext/bc/P" | Defaults to the string "/ext/P" as the path to blockchain's baseURL |

**Returns:** _[PlatformVMAPI](api_platformvm.platformvmapi)_

## Properties

### `Protected` AVAXAssetID

• **AVAXAssetID**: _Buffer_ = undefined

_Defined in [src/apis/platformvm/api.ts:90](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/api.ts#L90)_

---

### `Protected` baseURL

• **baseURL**: _string_

_Inherited from [APIBase](common_apibase.apibase).[baseURL](common_apibase.apibase#protected-baseurl)_

_Defined in [src/common/apibase.ts:29](https://github.com/chain4travel/caminojs/blob/3883166/src/common/apibase.ts#L29)_

---

### `Protected` blockchainAlias

• **blockchainAlias**: _string_ = undefined

_Defined in [src/apis/platformvm/api.ts:88](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/api.ts#L88)_

---

### `Protected` blockchainID

• **blockchainID**: _string_ = ""

_Defined in [src/apis/platformvm/api.ts:86](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/api.ts#L86)_

---

### `Protected` core

• **core**: _[AvalancheCore](avalanchecore.avalanchecore-1)_

_Inherited from [APIBase](common_apibase.apibase).[core](common_apibase.apibase#protected-core)_

_Defined in [src/common/apibase.ts:28](https://github.com/chain4travel/caminojs/blob/3883166/src/common/apibase.ts#L28)_

---

### `Protected` creationTxFee

• **creationTxFee**: _BN_ = undefined

_Defined in [src/apis/platformvm/api.ts:94](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/api.ts#L94)_

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

### `Protected` minDelegatorStake

• **minDelegatorStake**: _BN_ = undefined

_Defined in [src/apis/platformvm/api.ts:98](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/api.ts#L98)_

---

### `Protected` minValidatorStake

• **minValidatorStake**: _BN_ = undefined

_Defined in [src/apis/platformvm/api.ts:96](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/api.ts#L96)_

---

### `Protected` rpcID

• **rpcID**: _number_ = 1

_Inherited from [EVMAPI](api_evm.evmapi).[rpcID](api_evm.evmapi#protected-rpcid)_

_Defined in [src/common/jrpcapi.ts:13](https://github.com/chain4travel/caminojs/blob/3883166/src/common/jrpcapi.ts#L13)_

---

### `Protected` txFee

• **txFee**: _BN_ = undefined

_Defined in [src/apis/platformvm/api.ts:92](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/api.ts#L92)_

## Methods

### addDelegator

▸ **addDelegator**(`username`: string, `password`: string, `nodeID`: string, `startTime`: Date, `endTime`: Date, `stakeAmount`: BN, `rewardAddress`: string): _Promise‹string›_

_Defined in [src/apis/platformvm/api.ts:660](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/api.ts#L660)_

Add a delegator to the Primary Network.

**Parameters:**

| Name            | Type   | Description                                                                                             |
| --------------- | ------ | ------------------------------------------------------------------------------------------------------- |
| `username`      | string | The username of the Keystore user                                                                       |
| `password`      | string | The password of the Keystore user                                                                       |
| `nodeID`        | string | The node ID of the delegatee                                                                            |
| `startTime`     | Date   | Javascript Date object for when the delegator starts delegating                                         |
| `endTime`       | Date   | Javascript Date object for when the delegator starts delegating                                         |
| `stakeAmount`   | BN     | The amount of nAVAX the delegator is staking as a [BN](https://github.com/indutny/bn.js/)               |
| `rewardAddress` | string | The address of the account the staked AVAX and validation reward (if applicable) are sent to at endTime |

**Returns:** _Promise‹string›_

Promise for an array of validator"s stakingIDs.

---

### addSubnetValidator

▸ **addSubnetValidator**(`username`: string, `password`: string, `nodeID`: string, `subnetID`: Buffer | string, `startTime`: Date, `endTime`: Date, `weight`: number): _Promise‹string›_

_Defined in [src/apis/platformvm/api.ts:616](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/api.ts#L616)_

Add a validator to a Subnet other than the Primary Network. The validator must validate the Primary Network for the entire duration they validate this Subnet.

**Parameters:**

| Name        | Type                 | Description                                                                                                    |
| ----------- | -------------------- | -------------------------------------------------------------------------------------------------------------- |
| `username`  | string               | The username of the Keystore user                                                                              |
| `password`  | string               | The password of the Keystore user                                                                              |
| `nodeID`    | string               | The node ID of the validator                                                                                   |
| `subnetID`  | Buffer &#124; string | Either a [Buffer](https://github.com/feross/buffer) or a cb58 serialized string for the SubnetID or its alias. |
| `startTime` | Date                 | Javascript Date object for the start time to validate                                                          |
| `endTime`   | Date                 | Javascript Date object for the end time to validate                                                            |
| `weight`    | number               | The validator’s weight used for sampling                                                                       |

**Returns:** _Promise‹string›_

Promise for the unsigned transaction. It must be signed (using sign) by the proper number of the Subnet’s control keys and by the key of the account paying the transaction fee before it can be issued.

---

### addValidator

▸ **addValidator**(`username`: string, `password`: string, `nodeID`: string, `startTime`: Date, `endTime`: Date, `stakeAmount`: BN, `rewardAddress`: string, `delegationFeeRate`: BN): _Promise‹string›_

_Defined in [src/apis/platformvm/api.ts:574](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/api.ts#L574)_

Add a validator to the Primary Network.

**Parameters:**

| Name                | Type   | Default   | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| ------------------- | ------ | --------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `username`          | string | -         | The username of the Keystore user                                                                                                                                                                                                                                                                                                                                                                                                                            |
| `password`          | string | -         | The password of the Keystore user                                                                                                                                                                                                                                                                                                                                                                                                                            |
| `nodeID`            | string | -         | The node ID of the validator                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| `startTime`         | Date   | -         | Javascript Date object for the start time to validate                                                                                                                                                                                                                                                                                                                                                                                                        |
| `endTime`           | Date   | -         | Javascript Date object for the end time to validate                                                                                                                                                                                                                                                                                                                                                                                                          |
| `stakeAmount`       | BN     | -         | The amount of nAVAX the validator is staking as a [BN](https://github.com/indutny/bn.js/)                                                                                                                                                                                                                                                                                                                                                                    |
| `rewardAddress`     | string | -         | The address the validator reward will go to, if there is one.                                                                                                                                                                                                                                                                                                                                                                                                |
| `delegationFeeRate` | BN     | undefined | Optional. A [BN](https://github.com/indutny/bn.js/) for the percent fee this validator charges when others delegate stake to them. Up to 4 decimal places allowed additional decimal places are ignored. Must be between 0 and 100, inclusive. For example, if delegationFeeRate is 1.2345 and someone delegates to this validator, then when the delegation period is over, 1.2345% of the reward goes to the validator and the rest goes to the delegator. |

**Returns:** _Promise‹string›_

Promise for a base58 string of the unsigned transaction.

---

### addressFromBuffer

▸ **addressFromBuffer**(`address`: Buffer): _string_

_Defined in [src/apis/platformvm/api.ts:132](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/api.ts#L132)_

**Parameters:**

| Name      | Type   |
| --------- | ------ |
| `address` | Buffer |

**Returns:** _string_

---

### buildAddDelegatorTx

▸ **buildAddDelegatorTx**(`utxoset`: [UTXOSet](api_platformvm_utxos.utxoset), `toAddresses`: string[], `fromAddresses`: string[], `changeAddresses`: string[], `nodeID`: string, `startTime`: BN, `endTime`: BN, `stakeAmount`: BN, `rewardAddresses`: string[], `rewardLocktime`: BN, `rewardThreshold`: number, `memo`: [PayloadBase](utils_payload.payloadbase) | Buffer, `asOf`: BN): _Promise‹[UnsignedTx](api_platformvm_transactions.unsignedtx)›_

_Defined in [src/apis/platformvm/api.ts:1527](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/api.ts#L1527)_

Helper function which creates an unsigned [AddDelegatorTx](api_platformvm_validationtx.adddelegatortx). For more granular control, you may create your own
[UnsignedTx](api_evm_transactions.unsignedtx) manually and import the [AddDelegatorTx](api_platformvm_validationtx.adddelegatortx) class directly.

**Parameters:**

| Name              | Type                                                   | Default   | Description                                                                                                                         |
| ----------------- | ------------------------------------------------------ | --------- | ----------------------------------------------------------------------------------------------------------------------------------- |
| `utxoset`         | [UTXOSet](api_platformvm_utxos.utxoset)                | -         | A set of UTXOs that the transaction is built on                                                                                     |
| `toAddresses`     | string[]                                               | -         | An array of addresses as [Buffer](https://github.com/feross/buffer) who received the staked tokens at the end of the staking period |
| `fromAddresses`   | string[]                                               | -         | An array of addresses as [Buffer](https://github.com/feross/buffer) who own the staking UTXOs the fees in AVAX                      |
| `changeAddresses` | string[]                                               | -         | An array of addresses as [Buffer](https://github.com/feross/buffer) who gets the change leftover from the fee payment               |
| `nodeID`          | string                                                 | -         | The node ID of the validator being added.                                                                                           |
| `startTime`       | BN                                                     | -         | The Unix time when the validator starts validating the Primary Network.                                                             |
| `endTime`         | BN                                                     | -         | The Unix time when the validator stops validating the Primary Network (and staked AVAX is returned).                                |
| `stakeAmount`     | BN                                                     | -         | The amount being delegated as a [BN](https://github.com/indutny/bn.js/)                                                             |
| `rewardAddresses` | string[]                                               | -         | The addresses which will recieve the rewards from the delegated stake.                                                              |
| `rewardLocktime`  | BN                                                     | new BN(0) | Optional. The locktime field created in the resulting reward outputs                                                                |
| `rewardThreshold` | number                                                 | 1         | Opional. The number of signatures required to spend the funds in the resultant reward UTXO. Default 1.                              |
| `memo`            | [PayloadBase](utils_payload.payloadbase) &#124; Buffer | undefined | Optional contains arbitrary bytes, up to 256 bytes                                                                                  |
| `asOf`            | BN                                                     | UnixNow() | Optional. The timestamp to verify the transaction against as a [BN](https://github.com/indutny/bn.js/)                              |

**Returns:** _Promise‹[UnsignedTx](api_platformvm_transactions.unsignedtx)›_

An unsigned transaction created from the passed in parameters.

---

### buildAddSubnetValidatorTx

▸ **buildAddSubnetValidatorTx**(`utxoset`: [UTXOSet](api_platformvm_utxos.utxoset), `fromAddresses`: string[], `changeAddresses`: string[], `nodeID`: string, `startTime`: BN, `endTime`: BN, `weight`: BN, `subnetID`: string, `memo`: [PayloadBase](utils_payload.payloadbase) | Buffer, `asOf`: BN, `subnetAuthCredentials`: [][]): _Promise‹[UnsignedTx](api_platformvm_transactions.unsignedtx)›_

_Defined in [src/apis/platformvm/api.ts:1447](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/api.ts#L1447)_

Helper function which creates an unsigned [AddSubnetValidatorTx](../modules/src_apis_platformvm#addsubnetvalidatortx). For more granular control, you may create your own
[UnsignedTx](api_evm_transactions.unsignedtx) manually and import the [AddSubnetValidatorTx](../modules/src_apis_platformvm#addsubnetvalidatortx) class directly.

**Parameters:**

| Name                    | Type                                                   | Default   | Description                                                                                                           |
| ----------------------- | ------------------------------------------------------ | --------- | --------------------------------------------------------------------------------------------------------------------- |
| `utxoset`               | [UTXOSet](api_platformvm_utxos.utxoset)                | -         | A set of UTXOs that the transaction is built on.                                                                      |
| `fromAddresses`         | string[]                                               | -         | An array of addresses as [Buffer](https://github.com/feross/buffer) who pays the fees in AVAX                         |
| `changeAddresses`       | string[]                                               | -         | An array of addresses as [Buffer](https://github.com/feross/buffer) who gets the change leftover from the fee payment |
| `nodeID`                | string                                                 | -         | The node ID of the validator being added.                                                                             |
| `startTime`             | BN                                                     | -         | The Unix time when the validator starts validating the Primary Network.                                               |
| `endTime`               | BN                                                     | -         | The Unix time when the validator stops validating the Primary Network (and staked AVAX is returned).                  |
| `weight`                | BN                                                     | -         | The amount of weight for this subnet validator.                                                                       |
| `subnetID`              | string                                                 | -         | -                                                                                                                     |
| `memo`                  | [PayloadBase](utils_payload.payloadbase) &#124; Buffer | undefined | Optional contains arbitrary bytes, up to 256 bytes                                                                    |
| `asOf`                  | BN                                                     | UnixNow() | Optional. The timestamp to verify the transaction against as a [BN](https://github.com/indutny/bn.js/)                |
| `subnetAuthCredentials` | [][]                                                   | []        | Optional. An array of index and address to sign for each SubnetAuth.                                                  |

**Returns:** _Promise‹[UnsignedTx](api_platformvm_transactions.unsignedtx)›_

An unsigned transaction created from the passed in parameters.

---

### buildAddValidatorTx

▸ **buildAddValidatorTx**(`utxoset`: [UTXOSet](api_platformvm_utxos.utxoset), `toAddresses`: string[], `fromAddresses`: string[], `changeAddresses`: string[], `nodeID`: string, `startTime`: BN, `endTime`: BN, `stakeAmount`: BN, `rewardAddresses`: string[], `delegationFee`: number, `rewardLocktime`: BN, `rewardThreshold`: number, `memo`: [PayloadBase](utils_payload.payloadbase) | Buffer, `asOf`: BN): _Promise‹[UnsignedTx](api_platformvm_transactions.unsignedtx)›_

_Defined in [src/apis/platformvm/api.ts:1629](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/api.ts#L1629)_

Helper function which creates an unsigned [AddValidatorTx](api_platformvm_validationtx.addvalidatortx). For more granular control, you may create your own
[UnsignedTx](api_evm_transactions.unsignedtx) manually and import the [AddValidatorTx](api_platformvm_validationtx.addvalidatortx) class directly.

**Parameters:**

| Name              | Type                                                   | Default   | Description                                                                                                                         |
| ----------------- | ------------------------------------------------------ | --------- | ----------------------------------------------------------------------------------------------------------------------------------- |
| `utxoset`         | [UTXOSet](api_platformvm_utxos.utxoset)                | -         | A set of UTXOs that the transaction is built on                                                                                     |
| `toAddresses`     | string[]                                               | -         | An array of addresses as [Buffer](https://github.com/feross/buffer) who received the staked tokens at the end of the staking period |
| `fromAddresses`   | string[]                                               | -         | An array of addresses as [Buffer](https://github.com/feross/buffer) who own the staking UTXOs the fees in AVAX                      |
| `changeAddresses` | string[]                                               | -         | An array of addresses as [Buffer](https://github.com/feross/buffer) who gets the change leftover from the fee payment               |
| `nodeID`          | string                                                 | -         | The node ID of the validator being added.                                                                                           |
| `startTime`       | BN                                                     | -         | The Unix time when the validator starts validating the Primary Network.                                                             |
| `endTime`         | BN                                                     | -         | The Unix time when the validator stops validating the Primary Network (and staked AVAX is returned).                                |
| `stakeAmount`     | BN                                                     | -         | The amount being delegated as a [BN](https://github.com/indutny/bn.js/)                                                             |
| `rewardAddresses` | string[]                                               | -         | The addresses which will recieve the rewards from the delegated stake.                                                              |
| `delegationFee`   | number                                                 | -         | A number for the percentage of reward to be given to the validator when someone delegates to them. Must be between 0 and 100.       |
| `rewardLocktime`  | BN                                                     | new BN(0) | Optional. The locktime field created in the resulting reward outputs                                                                |
| `rewardThreshold` | number                                                 | 1         | Opional. The number of signatures required to spend the funds in the resultant reward UTXO. Default 1.                              |
| `memo`            | [PayloadBase](utils_payload.payloadbase) &#124; Buffer | undefined | Optional contains arbitrary bytes, up to 256 bytes                                                                                  |
| `asOf`            | BN                                                     | UnixNow() | Optional. The timestamp to verify the transaction against as a [BN](https://github.com/indutny/bn.js/)                              |

**Returns:** _Promise‹[UnsignedTx](api_platformvm_transactions.unsignedtx)›_

An unsigned transaction created from the passed in parameters.

---

### buildCreateChainTx

▸ **buildCreateChainTx**(`utxoset`: [UTXOSet](api_platformvm_utxos.utxoset), `fromAddresses`: string[], `changeAddresses`: string[], `subnetID`: string | Buffer, `chainName`: string, `vmID`: string, `fxIDs`: string[], `genesisData`: string | [GenesisData](api_avm_genesisdata.genesisdata), `memo`: [PayloadBase](utils_payload.payloadbase) | Buffer, `asOf`: BN, `subnetAuthCredentials`: [][]): _Promise‹[UnsignedTx](api_platformvm_transactions.unsignedtx)›_

_Defined in [src/apis/platformvm/api.ts:1803](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/api.ts#L1803)_

Build an unsigned [CreateChainTx](api_platformvm_createchaintx.createchaintx).

**Parameters:**

| Name                    | Type                                                         | Default   | Description                                                                                            |
| ----------------------- | ------------------------------------------------------------ | --------- | ------------------------------------------------------------------------------------------------------ |
| `utxoset`               | [UTXOSet](api_platformvm_utxos.utxoset)                      | -         | A set of UTXOs that the transaction is built on                                                        |
| `fromAddresses`         | string[]                                                     | -         | The addresses being used to send the funds from the UTXOs [Buffer](https://github.com/feross/buffer)   |
| `changeAddresses`       | string[]                                                     | -         | The addresses that can spend the change remaining from the spent UTXOs                                 |
| `subnetID`              | string &#124; Buffer                                         | undefined | Optional ID of the Subnet that validates this blockchain                                               |
| `chainName`             | string                                                       | undefined | Optional A human readable name for the chain; need not be unique                                       |
| `vmID`                  | string                                                       | undefined | Optional ID of the VM running on the new chain                                                         |
| `fxIDs`                 | string[]                                                     | undefined | Optional IDs of the feature extensions running on the new chain                                        |
| `genesisData`           | string &#124; [GenesisData](api_avm_genesisdata.genesisdata) | undefined | Optional Byte representation of genesis state of the new chain                                         |
| `memo`                  | [PayloadBase](utils_payload.payloadbase) &#124; Buffer       | undefined | Optional contains arbitrary bytes, up to 256 bytes                                                     |
| `asOf`                  | BN                                                           | UnixNow() | Optional. The timestamp to verify the transaction against as a [BN](https://github.com/indutny/bn.js/) |
| `subnetAuthCredentials` | [][]                                                         | []        | Optional. An array of index and address to sign for each SubnetAuth.                                   |

**Returns:** _Promise‹[UnsignedTx](api_platformvm_transactions.unsignedtx)›_

An unsigned transaction created from the passed in parameters.

---

### buildCreateSubnetTx

▸ **buildCreateSubnetTx**(`utxoset`: [UTXOSet](api_platformvm_utxos.utxoset), `fromAddresses`: string[], `changeAddresses`: string[], `subnetOwnerAddresses`: string[], `subnetOwnerThreshold`: number, `memo`: [PayloadBase](utils_payload.payloadbase) | Buffer, `asOf`: BN): _Promise‹[UnsignedTx](api_platformvm_transactions.unsignedtx)›_

_Defined in [src/apis/platformvm/api.ts:1735](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/api.ts#L1735)_

Class representing an unsigned [CreateSubnetTx](api_platformvm_createsubnettx.createsubnettx) transaction.

**Parameters:**

| Name                   | Type                                                   | Default   | Description                                                                                            |
| ---------------------- | ------------------------------------------------------ | --------- | ------------------------------------------------------------------------------------------------------ |
| `utxoset`              | [UTXOSet](api_platformvm_utxos.utxoset)                | -         | A set of UTXOs that the transaction is built on                                                        |
| `fromAddresses`        | string[]                                               | -         | The addresses being used to send the funds from the UTXOs [Buffer](https://github.com/feross/buffer)   |
| `changeAddresses`      | string[]                                               | -         | The addresses that can spend the change remaining from the spent UTXOs                                 |
| `subnetOwnerAddresses` | string[]                                               | -         | An array of addresses for owners of the new subnet                                                     |
| `subnetOwnerThreshold` | number                                                 | -         | A number indicating the amount of signatures required to add validators to a subnet                    |
| `memo`                 | [PayloadBase](utils_payload.payloadbase) &#124; Buffer | undefined | Optional contains arbitrary bytes, up to 256 bytes                                                     |
| `asOf`                 | BN                                                     | UnixNow() | Optional. The timestamp to verify the transaction against as a [BN](https://github.com/indutny/bn.js/) |

**Returns:** _Promise‹[UnsignedTx](api_platformvm_transactions.unsignedtx)›_

An unsigned transaction created from the passed in parameters.

---

### buildExportTx

▸ **buildExportTx**(`utxoset`: [UTXOSet](api_platformvm_utxos.utxoset), `amount`: BN, `destinationChain`: Buffer | string, `toAddresses`: string[], `fromAddresses`: string[], `changeAddresses`: string[], `memo`: [PayloadBase](utils_payload.payloadbase) | Buffer, `asOf`: BN, `locktime`: BN, `threshold`: number): _Promise‹[UnsignedTx](api_platformvm_transactions.unsignedtx)›_

_Defined in [src/apis/platformvm/api.ts:1345](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/api.ts#L1345)_

Helper function which creates an unsigned Export Tx. For more granular control, you may create your own
[UnsignedTx](api_evm_transactions.unsignedtx) manually (with their corresponding [TransferableInput](api_evm_inputs.transferableinput)s, [TransferableOutput](api_evm_outputs.transferableoutput)s, and [[TransferOperation]]s).

**Parameters:**

| Name               | Type                                                   | Default   | Description                                                                                            |
| ------------------ | ------------------------------------------------------ | --------- | ------------------------------------------------------------------------------------------------------ |
| `utxoset`          | [UTXOSet](api_platformvm_utxos.utxoset)                | -         | A set of UTXOs that the transaction is built on                                                        |
| `amount`           | BN                                                     | -         | The amount being exported as a [BN](https://github.com/indutny/bn.js/)                                 |
| `destinationChain` | Buffer &#124; string                                   | -         | The chainid for where the assets will be sent.                                                         |
| `toAddresses`      | string[]                                               | -         | The addresses to send the funds                                                                        |
| `fromAddresses`    | string[]                                               | -         | The addresses being used to send the funds from the UTXOs provided                                     |
| `changeAddresses`  | string[]                                               | undefined | The addresses that can spend the change remaining from the spent UTXOs                                 |
| `memo`             | [PayloadBase](utils_payload.payloadbase) &#124; Buffer | undefined | Optional contains arbitrary bytes, up to 256 bytes                                                     |
| `asOf`             | BN                                                     | UnixNow() | Optional. The timestamp to verify the transaction against as a [BN](https://github.com/indutny/bn.js/) |
| `locktime`         | BN                                                     | new BN(0) | Optional. The locktime field created in the resulting outputs                                          |
| `threshold`        | number                                                 | 1         | Optional. The number of signatures required to spend the funds in the resultant UTXO                   |

**Returns:** _Promise‹[UnsignedTx](api_platformvm_transactions.unsignedtx)›_

An unsigned transaction ([UnsignedTx](api_evm_transactions.unsignedtx)) which contains an [ExportTx](api_evm_exporttx.exporttx).

---

### buildImportTx

▸ **buildImportTx**(`utxoset`: [UTXOSet](api_platformvm_utxos.utxoset), `ownerAddresses`: string[], `sourceChain`: Buffer | string, `toAddresses`: string[], `fromAddresses`: string[], `changeAddresses`: string[], `memo`: [PayloadBase](utils_payload.payloadbase) | Buffer, `asOf`: BN, `locktime`: BN, `threshold`: number): _Promise‹[UnsignedTx](api_platformvm_transactions.unsignedtx)›_

_Defined in [src/apis/platformvm/api.ts:1253](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/api.ts#L1253)_

Helper function which creates an unsigned Import Tx. For more granular control, you may create your own
[UnsignedTx](api_evm_transactions.unsignedtx) manually (with their corresponding [TransferableInput](api_evm_inputs.transferableinput)s, [TransferableOutput](api_evm_outputs.transferableoutput)s, and [[TransferOperation]]s).

**`remarks`**
This helper exists because the endpoint API should be the primary point of entry for most functionality.

**Parameters:**

| Name              | Type                                                   | Default   | Description                                                                                            |
| ----------------- | ------------------------------------------------------ | --------- | ------------------------------------------------------------------------------------------------------ |
| `utxoset`         | [UTXOSet](api_platformvm_utxos.utxoset)                | -         | A set of UTXOs that the transaction is built on                                                        |
| `ownerAddresses`  | string[]                                               | -         | The addresses being used to import                                                                     |
| `sourceChain`     | Buffer &#124; string                                   | -         | The chainid for where the import is coming from.                                                       |
| `toAddresses`     | string[]                                               | -         | The addresses to send the funds                                                                        |
| `fromAddresses`   | string[]                                               | -         | The addresses being used to send the funds from the UTXOs provided                                     |
| `changeAddresses` | string[]                                               | undefined | The addresses that can spend the change remaining from the spent UTXOs                                 |
| `memo`            | [PayloadBase](utils_payload.payloadbase) &#124; Buffer | undefined | Optional contains arbitrary bytes, up to 256 bytes                                                     |
| `asOf`            | BN                                                     | UnixNow() | Optional. The timestamp to verify the transaction against as a [BN](https://github.com/indutny/bn.js/) |
| `locktime`        | BN                                                     | new BN(0) | Optional. The locktime field created in the resulting outputs                                          |
| `threshold`       | number                                                 | 1         | Optional. The number of signatures required to spend the funds in the resultant UTXO                   |

**Returns:** _Promise‹[UnsignedTx](api_platformvm_transactions.unsignedtx)›_

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

### checkGooseEgg

▸ **checkGooseEgg**(`utx`: [UnsignedTx](api_platformvm_transactions.unsignedtx), `outTotal`: BN): _Promise‹boolean›_

_Defined in [src/apis/platformvm/api.ts:283](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/api.ts#L283)_

Helper function which determines if a tx is a goose egg transaction.

**`remarks`**
A "Goose Egg Transaction" is when the fee far exceeds a reasonable amount

**Parameters:**

| Name       | Type                                                 | Default   | Description   |
| ---------- | ---------------------------------------------------- | --------- | ------------- |
| `utx`      | [UnsignedTx](api_platformvm_transactions.unsignedtx) | -         | An UnsignedTx |
| `outTotal` | BN                                                   | new BN(0) | -             |

**Returns:** _Promise‹boolean›_

boolean true if passes goose egg test and false if fails.

---

### createAddress

▸ **createAddress**(`username`: string, `password`: string): _Promise‹string›_

_Defined in [src/apis/platformvm/api.ts:404](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/api.ts#L404)_

Create an address in the node's keystore.

**Parameters:**

| Name       | Type   | Description                                                     |
| ---------- | ------ | --------------------------------------------------------------- |
| `username` | string | The username of the Keystore user that controls the new account |
| `password` | string | The password of the Keystore user that controls the new account |

**Returns:** _Promise‹string›_

Promise for a string of the newly created account address.

---

### createBlockchain

▸ **createBlockchain**(`username`: string, `password`: string, `subnetID`: Buffer | string, `vmID`: string, `fxIDs`: number[], `name`: string, `genesis`: string): _Promise‹string›_

_Defined in [src/apis/platformvm/api.ts:324](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/api.ts#L324)_

Creates a new blockchain.

**Parameters:**

| Name       | Type                 | Default   | Description                                                                                                                                                                                          |
| ---------- | -------------------- | --------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `username` | string               | -         | The username of the Keystore user that controls the new account                                                                                                                                      |
| `password` | string               | -         | The password of the Keystore user that controls the new account                                                                                                                                      |
| `subnetID` | Buffer &#124; string | undefined | Optional. Either a [Buffer](https://github.com/feross/buffer) or an cb58 serialized string for the SubnetID or its alias.                                                                            |
| `vmID`     | string               | -         | The ID of the Virtual Machine the blockchain runs. Can also be an alias of the Virtual Machine.                                                                                                      |
| `fxIDs`    | number[]             | -         | The ids of the FXs the VM is running.                                                                                                                                                                |
| `name`     | string               | -         | A human-readable name for the new blockchain                                                                                                                                                         |
| `genesis`  | string               | -         | The base 58 (with checksum) representation of the genesis state of the new blockchain. Virtual Machines should have a static API method named buildGenesis that can be used to generate genesisData. |

**Returns:** _Promise‹string›_

Promise for the unsigned transaction to create this blockchain. Must be signed by a sufficient number of the Subnet’s control keys and by the account paying the transaction fee.

---

### createSubnet

▸ **createSubnet**(`username`: string, `password`: string, `controlKeys`: string[], `threshold`: number): _Promise‹string | [ErrorResponseObject](../interfaces/src_utils.errorresponseobject)›_

_Defined in [src/apis/platformvm/api.ts:697](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/api.ts#L697)_

Create an unsigned transaction to create a new Subnet. The unsigned transaction must be
signed with the key of the account paying the transaction fee. The Subnet’s ID is the ID of the transaction that creates it (ie the response from issueTx when issuing the signed transaction).

**Parameters:**

| Name          | Type     | Description                                                                                                                                                      |
| ------------- | -------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `username`    | string   | The username of the Keystore user                                                                                                                                |
| `password`    | string   | The password of the Keystore user                                                                                                                                |
| `controlKeys` | string[] | Array of platform addresses as strings                                                                                                                           |
| `threshold`   | number   | To add a validator to this Subnet, a transaction must have threshold signatures, where each signature is from a key whose address is an element of `controlKeys` |

**Returns:** _Promise‹string | [ErrorResponseObject](../interfaces/src_utils.errorresponseobject)›_

Promise for a string with the unsigned transaction encoded as base58.

---

### exportAVAX

▸ **exportAVAX**(`username`: string, `password`: string, `amount`: BN, `to`: string): _Promise‹string | [ErrorResponseObject](../interfaces/src_utils.errorresponseobject)›_

_Defined in [src/apis/platformvm/api.ts:787](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/api.ts#L787)_

Send AVAX from an account on the P-Chain to an address on the X-Chain. This transaction
must be signed with the key of the account that the AVAX is sent from and which pays the
transaction fee. After issuing this transaction, you must call the X-Chain’s importAVAX
method to complete the transfer.

**Parameters:**

| Name       | Type   | Description                                                                      |
| ---------- | ------ | -------------------------------------------------------------------------------- |
| `username` | string | The Keystore user that controls the account specified in `to`                    |
| `password` | string | The password of the Keystore user                                                |
| `amount`   | BN     | Amount of AVAX to export as a [BN](https://github.com/indutny/bn.js/)            |
| `to`       | string | The address on the X-Chain to send the AVAX to. Do not include X- in the address |

**Returns:** _Promise‹string | [ErrorResponseObject](../interfaces/src_utils.errorresponseobject)›_

Promise for an unsigned transaction to be signed by the account the the AVAX is
sent from and pays the transaction fee.

---

### exportKey

▸ **exportKey**(`username`: string, `password`: string, `address`: string): _Promise‹string | [ErrorResponseObject](../interfaces/src_utils.errorresponseobject)›_

_Defined in [src/apis/platformvm/api.ts:1060](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/api.ts#L1060)_

Exports the private key for an address.

**Parameters:**

| Name       | Type   | Description                                      |
| ---------- | ------ | ------------------------------------------------ |
| `username` | string | The name of the user with the private key        |
| `password` | string | The password used to decrypt the private key     |
| `address`  | string | The address whose private key should be exported |

**Returns:** _Promise‹string | [ErrorResponseObject](../interfaces/src_utils.errorresponseobject)›_

Promise with the decrypted private key as store in the database

---

### getAVAXAssetID

▸ **getAVAXAssetID**(`refresh`: boolean): _Promise‹Buffer›_

_Defined in [src/apis/platformvm/api.ts:152](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/api.ts#L152)_

Fetches the AVAX AssetID and returns it in a Promise.

**Parameters:**

| Name      | Type    | Default | Description                                                            |
| --------- | ------- | ------- | ---------------------------------------------------------------------- |
| `refresh` | boolean | false   | This function caches the response. Refresh = true will bust the cache. |

**Returns:** _Promise‹Buffer›_

The the provided string representing the AVAX AssetID

---

### getBalance

▸ **getBalance**(`address`: string): _Promise‹[GetBalanceResponse](../interfaces/platformvm_interfaces.getbalanceresponse)›_

_Defined in [src/apis/platformvm/api.ts:426](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/api.ts#L426)_

Gets the balance of a particular asset.

**Parameters:**

| Name      | Type   | Description                                |
| --------- | ------ | ------------------------------------------ |
| `address` | string | The address to pull the asset balance from |

**Returns:** _Promise‹[GetBalanceResponse](../interfaces/platformvm_interfaces.getbalanceresponse)›_

Promise with the balance as a [BN](https://github.com/indutny/bn.js/) on the provided address.

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

_Defined in [src/apis/platformvm/api.ts:105](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/api.ts#L105)_

Gets the alias for the blockchainID if it exists, otherwise returns `undefined`.

**Returns:** _string_

The alias for the blockchainID

---

### getBlockchainID

▸ **getBlockchainID**(): _string_

_Defined in [src/apis/platformvm/api.ts:114](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/api.ts#L114)_

Gets the blockchainID and returns it.

**Returns:** _string_

The blockchainID

---

### getBlockchainStatus

▸ **getBlockchainStatus**(`blockchainID`: string): _Promise‹string›_

_Defined in [src/apis/platformvm/api.ts:360](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/api.ts#L360)_

Gets the status of a blockchain.

**Parameters:**

| Name           | Type   | Description                                 |
| -------------- | ------ | ------------------------------------------- |
| `blockchainID` | string | The blockchainID requesting a status update |

**Returns:** _Promise‹string›_

Promise for a string of one of: "Validating", "Created", "Preferred", "Unknown".

---

### getBlockchains

▸ **getBlockchains**(): _Promise‹[Blockchain](../interfaces/platformvm_interfaces.blockchain)[]›_

_Defined in [src/apis/platformvm/api.ts:766](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/api.ts#L766)_

Get all the blockchains that exist (excluding the P-Chain).

**Returns:** _Promise‹[Blockchain](../interfaces/platformvm_interfaces.blockchain)[]›_

Promise for an array of objects containing fields "id", "subnetID", and "vmID".

---

### getConfiguration

▸ **getConfiguration**(): _Promise‹[GetConfigurationResponse](../interfaces/platformvm_interfaces.getconfigurationresponse)›_

_Defined in [src/apis/platformvm/api.ts:1946](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/api.ts#L1946)_

Get blockchains configuration (genesis)

**Returns:** _Promise‹[GetConfigurationResponse](../interfaces/platformvm_interfaces.getconfigurationresponse)›_

Promise for an GetConfigurationResponse

---

### getCreateChainTxFee

▸ **getCreateChainTxFee**(): _BN_

_Defined in [src/apis/platformvm/api.ts:209](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/api.ts#L209)_

Gets the CreateChainTx fee.

**Returns:** _BN_

The CreateChainTx fee as a [BN](https://github.com/indutny/bn.js/)

---

### getCreateSubnetTxFee

▸ **getCreateSubnetTxFee**(): _BN_

_Defined in [src/apis/platformvm/api.ts:200](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/api.ts#L200)_

Gets the CreateSubnetTx fee.

**Returns:** _BN_

The CreateSubnetTx fee as a [BN](https://github.com/indutny/bn.js/)

---

### getCreationTxFee

▸ **getCreationTxFee**(): _BN_

_Defined in [src/apis/platformvm/api.ts:236](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/api.ts#L236)_

Gets the creation fee for this chain.

**Returns:** _BN_

The creation fee as a [BN](https://github.com/indutny/bn.js/)

---

### getCurrentSupply

▸ **getCurrentSupply**(): _Promise‹BN›_

_Defined in [src/apis/platformvm/api.ts:881](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/api.ts#L881)_

Returns an upper bound on the amount of tokens that exist. Not monotonically increasing because this number can go down if a staker"s reward is denied.

**Returns:** _Promise‹BN›_

---

### getCurrentValidators

▸ **getCurrentValidators**(`subnetID`: Buffer | string, `nodeIDs`: string[]): _Promise‹object›_

_Defined in [src/apis/platformvm/api.ts:476](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/api.ts#L476)_

Lists the set of current validators.

**Parameters:**

| Name       | Type                 | Default   | Description                                                                                                               |
| ---------- | -------------------- | --------- | ------------------------------------------------------------------------------------------------------------------------- |
| `subnetID` | Buffer &#124; string | undefined | Optional. Either a [Buffer](https://github.com/feross/buffer) or an cb58 serialized string for the SubnetID or its alias. |
| `nodeIDs`  | string[]             | undefined | Optional. An array of strings                                                                                             |

**Returns:** _Promise‹object›_

Promise for an array of validators that are currently staking, see: [platform.getCurrentValidators documentation](https://docs.avax.network/v1.0/en/api/platform/#platformgetcurrentvalidators).

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

_Defined in [src/apis/platformvm/api.ts:227](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/api.ts#L227)_

Gets the default creation fee for this chain.

**Returns:** _BN_

The default creation fee as a [BN](https://github.com/indutny/bn.js/)

---

### getDefaultTxFee

▸ **getDefaultTxFee**(): _BN_

_Defined in [src/apis/platformvm/api.ts:179](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/api.ts#L179)_

Gets the default tx fee for this chain.

**Returns:** _BN_

The default tx fee as a [BN](https://github.com/indutny/bn.js/)

---

### getHeight

▸ **getHeight**(): _Promise‹BN›_

_Defined in [src/apis/platformvm/api.ts:891](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/api.ts#L891)_

Returns the height of the platform chain.

**Returns:** _Promise‹BN›_

---

### getMaxStakeAmount

▸ **getMaxStakeAmount**(`subnetID`: string | Buffer, `nodeID`: string, `startTime`: BN, `endTime`: BN): _Promise‹BN›_

_Defined in [src/apis/platformvm/api.ts:948](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/api.ts#L948)_

getMaxStakeAmount() returns the maximum amount of nAVAX staking to the named node during the time period.

**Parameters:**

| Name        | Type                 | Description                                                                                         |
| ----------- | -------------------- | --------------------------------------------------------------------------------------------------- |
| `subnetID`  | string &#124; Buffer | A Buffer or cb58 string representing subnet                                                         |
| `nodeID`    | string               | A string representing ID of the node whose stake amount is required during the given duration       |
| `startTime` | BN                   | A big number denoting start time of the duration during which stake amount of the node is required. |
| `endTime`   | BN                   | A big number denoting end time of the duration during which stake amount of the node is required.   |

**Returns:** _Promise‹BN›_

A big number representing total staked by validators on the primary network

---

### getMinStake

▸ **getMinStake**(`refresh`: boolean): _Promise‹[GetMinStakeResponse](../interfaces/platformvm_interfaces.getminstakeresponse)›_

_Defined in [src/apis/platformvm/api.ts:903](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/api.ts#L903)_

Gets the minimum staking amount.

**Parameters:**

| Name      | Type    | Default | Description                                                                                   |
| --------- | ------- | ------- | --------------------------------------------------------------------------------------------- |
| `refresh` | boolean | false   | A boolean to bypass the local cached value of Minimum Stake Amount, polling the node instead. |

**Returns:** _Promise‹[GetMinStakeResponse](../interfaces/platformvm_interfaces.getminstakeresponse)›_

---

### getPendingValidators

▸ **getPendingValidators**(`subnetID`: Buffer | string, `nodeIDs`: string[]): _Promise‹object›_

_Defined in [src/apis/platformvm/api.ts:506](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/api.ts#L506)_

Lists the set of pending validators.

**Parameters:**

| Name       | Type                 | Default   | Description                                                                                                              |
| ---------- | -------------------- | --------- | ------------------------------------------------------------------------------------------------------------------------ |
| `subnetID` | Buffer &#124; string | undefined | Optional. Either a [Buffer](https://github.com/feross/buffer) or a cb58 serialized string for the SubnetID or its alias. |
| `nodeIDs`  | string[]             | undefined | Optional. An array of strings                                                                                            |

**Returns:** _Promise‹object›_

Promise for an array of validators that are pending staking, see: [platform.getPendingValidators documentation](https://docs.avax.network/v1.0/en/api/platform/#platformgetpendingvalidators).

---

### getRPCID

▸ **getRPCID**(): _number_

_Inherited from [EVMAPI](api_evm.evmapi).[getRPCID](api_evm.evmapi#getrpcid)_

_Defined in [src/common/jrpcapi.ts:77](https://github.com/chain4travel/caminojs/blob/3883166/src/common/jrpcapi.ts#L77)_

Returns the rpcid, a strictly-increasing number, starting from 1, indicating the next
request ID that will be sent.

**Returns:** _number_

---

### getRewardUTXOs

▸ **getRewardUTXOs**(`txID`: string, `encoding?`: string): _Promise‹[GetRewardUTXOsResponse](../interfaces/platformvm_interfaces.getrewardutxosresponse)›_

_Defined in [src/apis/platformvm/api.ts:1926](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/api.ts#L1926)_

**Parameters:**

| Name        | Type   |
| ----------- | ------ |
| `txID`      | string |
| `encoding?` | string |

**Returns:** _Promise‹[GetRewardUTXOsResponse](../interfaces/platformvm_interfaces.getrewardutxosresponse)›_

the UTXOs that were rewarded after the provided transaction"s staking or delegation period ended.

---

### getStake

▸ **getStake**(`addresses`: string[], `encoding`: string): _Promise‹[GetStakeResponse](../interfaces/platformvm_interfaces.getstakeresponse)›_

_Defined in [src/apis/platformvm/api.ts:1000](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/api.ts#L1000)_

Gets the total amount staked for an array of addresses.

**Parameters:**

| Name        | Type     | Default |
| ----------- | -------- | ------- |
| `addresses` | string[] | -       |
| `encoding`  | string   | "hex"   |

**Returns:** _Promise‹[GetStakeResponse](../interfaces/platformvm_interfaces.getstakeresponse)›_

---

### getStakingAssetID

▸ **getStakingAssetID**(): _Promise‹string›_

_Defined in [src/apis/platformvm/api.ts:304](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/api.ts#L304)_

Retrieves an assetID for a subnet"s staking assset.

**Returns:** _Promise‹string›_

Returns a Promise string with cb58 encoded value of the assetID.

---

### getSubnets

▸ **getSubnets**(`ids`: string[]): _Promise‹[Subnet](../interfaces/platformvm_interfaces.subnet)[]›_

_Defined in [src/apis/platformvm/api.ts:1039](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/api.ts#L1039)_

Get all the subnets that exist.

**Parameters:**

| Name  | Type     | Default   | Description                                                                    |
| ----- | -------- | --------- | ------------------------------------------------------------------------------ |
| `ids` | string[] | undefined | IDs of the subnets to retrieve information about. If omitted, gets all subnets |

**Returns:** _Promise‹[Subnet](../interfaces/platformvm_interfaces.subnet)[]›_

Promise for an array of objects containing fields "id",
"controlKeys", and "threshold".

---

### getTimestamp

▸ **getTimestamp**(): _Promise‹number›_

_Defined in [src/apis/platformvm/api.ts:1916](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/api.ts#L1916)_

**Returns:** _Promise‹number›_

the current timestamp on chain.

---

### getTotalStake

▸ **getTotalStake**(): _Promise‹BN›_

_Defined in [src/apis/platformvm/api.ts:932](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/api.ts#L932)_

getTotalStake() returns the total amount staked on the Primary Network

**Returns:** _Promise‹BN›_

A big number representing total staked by validators on the primary network

---

### getTx

▸ **getTx**(`txID`: string, `encoding`: string): _Promise‹string | object›_

_Defined in [src/apis/platformvm/api.ts:1116](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/api.ts#L1116)_

Returns the treansaction data of a provided transaction ID by calling the node's `getTx` method.

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

_Defined in [src/apis/platformvm/api.ts:188](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/api.ts#L188)_

Gets the tx fee for this chain.

**Returns:** _BN_

The tx fee as a [BN](https://github.com/indutny/bn.js/)

---

### getTxStatus

▸ **getTxStatus**(`txid`: string, `includeReason`: boolean): _Promise‹string | [GetTxStatusResponse](../interfaces/platformvm_interfaces.gettxstatusresponse)›_

_Defined in [src/apis/platformvm/api.ts:1141](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/api.ts#L1141)_

Returns the status of a provided transaction ID by calling the node's `getTxStatus` method.

**Parameters:**

| Name            | Type    | Default | Description                                                       |
| --------------- | ------- | ------- | ----------------------------------------------------------------- |
| `txid`          | string  | -       | The string representation of the transaction ID                   |
| `includeReason` | boolean | true    | Return the reason tx was dropped, if applicable. Defaults to true |

**Returns:** _Promise‹string | [GetTxStatusResponse](../interfaces/platformvm_interfaces.gettxstatusresponse)›_

Returns a Promise string containing the status retrieved from the node and the reason a tx was dropped, if applicable.

---

### getUTXOs

▸ **getUTXOs**(`addresses`: string[] | string, `sourceChain`: string, `limit`: number, `startIndex`: object, `persistOpts`: [PersistanceOptions](utils_persistanceoptions.persistanceoptions), `encoding`: string): _Promise‹[GetUTXOsResponse](../interfaces/platformvm_interfaces.getutxosresponse)›_

_Defined in [src/apis/platformvm/api.ts:1172](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/api.ts#L1172)_

Retrieves the UTXOs related to the addresses provided from the node's `getUTXOs` method.

**`remarks`**
persistOpts is optional and must be of type [PersistanceOptions](utils_persistanceoptions.persistanceoptions)

**Parameters:**

▪ **addresses**: _string[] | string_

An array of addresses as cb58 strings or addresses as [Buffer](https://github.com/feross/buffer)s

▪`Default value` **sourceChain**: _string_= undefined

A string for the chain to look for the UTXO"s. Default is to use this chain, but if exported UTXOs exist from other chains, this can used to pull them instead.

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

Optional. is the encoding format to use for the payload argument. Can be either "cb58" or "hex". Defaults to "hex".

**Returns:** _Promise‹[GetUTXOsResponse](../interfaces/platformvm_interfaces.getutxosresponse)›_

---

### getValidatorsAt

▸ **getValidatorsAt**(`height`: number, `subnetID?`: string): _Promise‹[GetValidatorsAtResponse](../interfaces/platformvm_interfaces.getvalidatorsatresponse)›_

_Defined in [src/apis/platformvm/api.ts:379](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/api.ts#L379)_

Get the validators and their weights of a subnet or the Primary Network at a given P-Chain height.

**Parameters:**

| Name        | Type   | Description                                                       |
| ----------- | ------ | ----------------------------------------------------------------- |
| `height`    | number | The P-Chain height to get the validator set at.                   |
| `subnetID?` | string | Optional. A cb58 serialized string for the SubnetID or its alias. |

**Returns:** _Promise‹[GetValidatorsAtResponse](../interfaces/platformvm_interfaces.getvalidatorsatresponse)›_

Promise GetValidatorsAtResponse

---

### importAVAX

▸ **importAVAX**(`username`: string, `password`: string, `to`: string, `sourceChain`: string): _Promise‹string | [ErrorResponseObject](../interfaces/src_utils.errorresponseobject)›_

_Defined in [src/apis/platformvm/api.ts:823](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/api.ts#L823)_

Send AVAX from an account on the P-Chain to an address on the X-Chain. This transaction
must be signed with the key of the account that the AVAX is sent from and which pays
the transaction fee. After issuing this transaction, you must call the X-Chain’s
importAVAX method to complete the transfer.

**Parameters:**

| Name          | Type   | Description                                                                                                                               |
| ------------- | ------ | ----------------------------------------------------------------------------------------------------------------------------------------- |
| `username`    | string | The Keystore user that controls the account specified in `to`                                                                             |
| `password`    | string | The password of the Keystore user                                                                                                         |
| `to`          | string | The ID of the account the AVAX is sent to. This must be the same as the to argument in the corresponding call to the X-Chain’s exportAVAX |
| `sourceChain` | string | The chainID where the funds are coming from.                                                                                              |

**Returns:** _Promise‹string | [ErrorResponseObject](../interfaces/src_utils.errorresponseobject)›_

Promise for a string for the transaction, which should be sent to the network
by calling issueTx.

---

### importKey

▸ **importKey**(`username`: string, `password`: string, `privateKey`: string): _Promise‹string | [ErrorResponseObject](../interfaces/src_utils.errorresponseobject)›_

_Defined in [src/apis/platformvm/api.ts:1088](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/api.ts#L1088)_

Give a user control over an address by providing the private key that controls the address.

**Parameters:**

| Name         | Type   | Description                                              |
| ------------ | ------ | -------------------------------------------------------- |
| `username`   | string | The name of the user to store the private key            |
| `password`   | string | The password that unlocks the user                       |
| `privateKey` | string | A string representing the private key in the vm"s format |

**Returns:** _Promise‹string | [ErrorResponseObject](../interfaces/src_utils.errorresponseobject)›_

The address for the imported private key.

---

### issueTx

▸ **issueTx**(`tx`: string | Buffer | [Tx](api_platformvm_transactions.tx)): _Promise‹string›_

_Defined in [src/apis/platformvm/api.ts:851](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/api.ts#L851)_

Calls the node's issueTx method from the API and returns the resulting transaction ID as a string.

**Parameters:**

| Name | Type                                                             | Description                                                                                                       |
| ---- | ---------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------- |
| `tx` | string &#124; Buffer &#124; [Tx](api_platformvm_transactions.tx) | A string, [Buffer](https://github.com/feross/buffer), or [Tx](api_evm_transactions.tx) representing a transaction |

**Returns:** _Promise‹string›_

A Promise string representing the transaction ID of the posted transaction.

---

### keyChain

▸ **keyChain**(): _[KeyChain](api_platformvm_keychain.keychain)_

_Defined in [src/apis/platformvm/api.ts:257](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/api.ts#L257)_

Gets a reference to the keychain for this class.

**Returns:** _[KeyChain](api_platformvm_keychain.keychain)_

The instance of [[]] for this class

---

### listAddresses

▸ **listAddresses**(`username`: string, `password`: string): _Promise‹string[]›_

_Defined in [src/apis/platformvm/api.ts:451](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/api.ts#L451)_

List the addresses controlled by the user.

**Parameters:**

| Name       | Type   | Description                       |
| ---------- | ------ | --------------------------------- |
| `username` | string | The username of the Keystore user |
| `password` | string | The password of the Keystore user |

**Returns:** _Promise‹string[]›_

Promise for an array of addresses.

---

### parseAddress

▸ **parseAddress**(`addr`: string): _Buffer_

_Defined in [src/apis/platformvm/api.ts:121](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/api.ts#L121)_

Takes an address string and returns its [Buffer](https://github.com/feross/buffer) representation if valid.

**Parameters:**

| Name   | Type   |
| ------ | ------ |
| `addr` | string |

**Returns:** _Buffer_

A [Buffer](https://github.com/feross/buffer) for the address if valid, undefined if not valid.

---

### sampleValidators

▸ **sampleValidators**(`sampleSize`: number, `subnetID`: Buffer | string): _Promise‹string[]›_

_Defined in [src/apis/platformvm/api.ts:536](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/api.ts#L536)_

Samples `Size` validators from the current validator set.

**Parameters:**

| Name         | Type                 | Default   | Description                                                                                                               |
| ------------ | -------------------- | --------- | ------------------------------------------------------------------------------------------------------------------------- |
| `sampleSize` | number               | -         | Of the total universe of validators, select this many at random                                                           |
| `subnetID`   | Buffer &#124; string | undefined | Optional. Either a [Buffer](https://github.com/feross/buffer) or an cb58 serialized string for the SubnetID or its alias. |

**Returns:** _Promise‹string[]›_

Promise for an array of validator"s stakingIDs.

---

### setAVAXAssetID

▸ **setAVAXAssetID**(`avaxAssetID`: string | Buffer): _void_

_Defined in [src/apis/platformvm/api.ts:167](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/api.ts#L167)_

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

_Defined in [src/apis/platformvm/api.ts:248](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/api.ts#L248)_

Sets the creation fee for this chain.

**Parameters:**

| Name  | Type | Description                                                               |
| ----- | ---- | ------------------------------------------------------------------------- |
| `fee` | BN   | The creation fee amount to set as [BN](https://github.com/indutny/bn.js/) |

**Returns:** _void_

---

### setMinStake

▸ **setMinStake**(`minValidatorStake`: BN, `minDelegatorStake`: BN): _void_

_Defined in [src/apis/platformvm/api.ts:985](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/api.ts#L985)_

Sets the minimum stake cached in this class.

**Parameters:**

| Name                | Type | Default   | Description                                                                                          |
| ------------------- | ---- | --------- | ---------------------------------------------------------------------------------------------------- |
| `minValidatorStake` | BN   | undefined | A [BN](https://github.com/indutny/bn.js/) to set the minimum stake amount cached in this class.      |
| `minDelegatorStake` | BN   | undefined | A [BN](https://github.com/indutny/bn.js/) to set the minimum delegation amount cached in this class. |

**Returns:** _void_

---

### setTxFee

▸ **setTxFee**(`fee`: BN): _void_

_Defined in [src/apis/platformvm/api.ts:218](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/api.ts#L218)_

Sets the tx fee for this chain.

**Parameters:**

| Name  | Type | Description                                                         |
| ----- | ---- | ------------------------------------------------------------------- |
| `fee` | BN   | The tx fee amount to set as [BN](https://github.com/indutny/bn.js/) |

**Returns:** _void_

---

### validatedBy

▸ **validatedBy**(`blockchainID`: string): _Promise‹string›_

_Defined in [src/apis/platformvm/api.ts:726](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/api.ts#L726)_

Get the Subnet that validates a given blockchain.

**Parameters:**

| Name           | Type   | Description                                                                                                     |
| -------------- | ------ | --------------------------------------------------------------------------------------------------------------- |
| `blockchainID` | string | Either a [Buffer](https://github.com/feross/buffer) or a cb58 encoded string for the blockchainID or its alias. |

**Returns:** _Promise‹string›_

Promise for a string of the subnetID that validates the blockchain.

---

### validates

▸ **validates**(`subnetID`: Buffer | string): _Promise‹string[]›_

_Defined in [src/apis/platformvm/api.ts:745](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/api.ts#L745)_

Get the IDs of the blockchains a Subnet validates.

**Parameters:**

| Name       | Type                 | Description                                                                                                     |
| ---------- | -------------------- | --------------------------------------------------------------------------------------------------------------- |
| `subnetID` | Buffer &#124; string | Either a [Buffer](https://github.com/feross/buffer) or an AVAX serialized string for the SubnetID or its alias. |

**Returns:** _Promise‹string[]›_

Promise for an array of blockchainIDs the subnet validates.
