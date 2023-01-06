# Class: InfoAPI

Class for interacting with a node's InfoAPI.

**`remarks`** This extends the [JRPCAPI](../modules/src_common#jrpcapi) class. This class should not be directly called. Instead, use the [Avalanche.addAPI](avalanche.avalanche-1#addapi) function to register this interface with Avalanche.

## Hierarchy

↳ [JRPCAPI](common_jrpcapi.jrpcapi)

↳ **InfoAPI**

## Index

### Constructors

- [constructor](api_info.infoapi#constructor)

### Properties

- [baseURL](api_info.infoapi#protected-baseurl)
- [core](api_info.infoapi#protected-core)
- [db](api_info.infoapi#protected-db)
- [jrpcVersion](api_info.infoapi#protected-jrpcversion)
- [rpcID](api_info.infoapi#protected-rpcid)

### Methods

- [callMethod](api_info.infoapi#callmethod)
- [getBaseURL](api_info.infoapi#getbaseurl)
- [getBlockchainID](api_info.infoapi#getblockchainid)
- [getDB](api_info.infoapi#getdb)
- [getNetworkID](api_info.infoapi#getnetworkid)
- [getNetworkName](api_info.infoapi#getnetworkname)
- [getNodeID](api_info.infoapi#getnodeid)
- [getNodeIP](api_info.infoapi#getnodeip)
- [getNodeVersion](api_info.infoapi#getnodeversion)
- [getRPCID](api_info.infoapi#getrpcid)
- [getTxFee](api_info.infoapi#gettxfee)
- [isBootstrapped](api_info.infoapi#isbootstrapped)
- [peers](api_info.infoapi#peers)
- [setBaseURL](api_info.infoapi#setbaseurl)
- [uptime](api_info.infoapi#uptime)

## Constructors

### constructor

\+ **new InfoAPI**(`core`: [AvalancheCore](avalanchecore.avalanchecore-1), `baseURL`: string): _[InfoAPI](api_info.infoapi)_

_Overrides [JRPCAPI](common_jrpcapi.jrpcapi).[constructor](common_jrpcapi.jrpcapi#constructor)_

_Defined in [src/apis/info/api.ts:168](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/info/api.ts#L168)_

This class should not be instantiated directly. Instead use the [Avalanche.addAPI](avalanche.avalanche-1#addapi) method.

**Parameters:**

| Name      | Type                                           | Default     | Description                                                     |
| --------- | ---------------------------------------------- | ----------- | --------------------------------------------------------------- |
| `core`    | [AvalancheCore](avalanchecore.avalanchecore-1) | -           | A reference to the Avalanche class                              |
| `baseURL` | string                                         | "/ext/info" | Defaults to the string "/ext/info" as the path to rpc's baseURL |

**Returns:** _[InfoAPI](api_info.infoapi)_

## Properties

### `Protected` baseURL

• **baseURL**: _string_

_Inherited from [APIBase](common_apibase.apibase).[baseURL](common_apibase.apibase#protected-baseurl)_

_Defined in [src/common/apibase.ts:29](https://github.com/chain4travel/caminojs/blob/3883166/src/common/apibase.ts#L29)_

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

## Methods

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

### getBaseURL

▸ **getBaseURL**(): _string_

_Inherited from [APIBase](common_apibase.apibase).[getBaseURL](common_apibase.apibase#getbaseurl)_

_Defined in [src/common/apibase.ts:53](https://github.com/chain4travel/caminojs/blob/3883166/src/common/apibase.ts#L53)_

Returns the baseURL's path.

**Returns:** _string_

---

### getBlockchainID

▸ **getBlockchainID**(`alias`: string): _Promise‹string›_

_Defined in [src/apis/info/api.ts:33](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/info/api.ts#L33)_

Fetches the blockchainID from the node for a given alias.

**Parameters:**

| Name    | Type   | Description                                  |
| ------- | ------ | -------------------------------------------- |
| `alias` | string | The blockchain alias to get the blockchainID |

**Returns:** _Promise‹string›_

Returns a Promise string containing the base 58 string representation of the blockchainID.

---

### getDB

▸ **getDB**(): _StoreAPI_

_Inherited from [APIBase](common_apibase.apibase).[getDB](common_apibase.apibase#getdb)_

_Defined in [src/common/apibase.ts:58](https://github.com/chain4travel/caminojs/blob/3883166/src/common/apibase.ts#L58)_

Returns the baseURL's database.

**Returns:** _StoreAPI_

---

### getNetworkID

▸ **getNetworkID**(): _Promise‹number›_

_Defined in [src/apis/info/api.ts:62](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/info/api.ts#L62)_

Fetches the networkID from the node.

**Returns:** _Promise‹number›_

Returns a Promise number of the networkID.

---

### getNetworkName

▸ **getNetworkName**(): _Promise‹string›_

_Defined in [src/apis/info/api.ts:74](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/info/api.ts#L74)_

Fetches the network name this node is running on

**Returns:** _Promise‹string›_

Returns a Promise string containing the network name.

---

### getNodeID

▸ **getNodeID**(): _Promise‹string›_

_Defined in [src/apis/info/api.ts:86](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/info/api.ts#L86)_

Fetches the nodeID from the node.

**Returns:** _Promise‹string›_

Returns a Promise string of the nodeID.

---

### getNodeIP

▸ **getNodeIP**(): _Promise‹string›_

_Defined in [src/apis/info/api.ts:50](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/info/api.ts#L50)_

Fetches the IP address from the node.

**Returns:** _Promise‹string›_

Returns a Promise string of the node IP address.

---

### getNodeVersion

▸ **getNodeVersion**(): _Promise‹string›_

_Defined in [src/apis/info/api.ts:98](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/info/api.ts#L98)_

Fetches the version of Gecko this node is running

**Returns:** _Promise‹string›_

Returns a Promise string containing the version of Gecko.

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

▸ **getTxFee**(): _Promise‹[GetTxFeeResponse](../interfaces/info_interfaces.gettxfeeresponse)›_

_Defined in [src/apis/info/api.ts:110](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/info/api.ts#L110)_

Fetches the transaction fee from the node.

**Returns:** _Promise‹[GetTxFeeResponse](../interfaces/info_interfaces.gettxfeeresponse)›_

Returns a Promise object of the transaction fee in nAVAX.

---

### isBootstrapped

▸ **isBootstrapped**(`chain`: string): _Promise‹boolean›_

_Defined in [src/apis/info/api.ts:130](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/info/api.ts#L130)_

Check whether a given chain is done bootstrapping

**Parameters:**

| Name    | Type   | Description                 |
| ------- | ------ | --------------------------- |
| `chain` | string | The ID or alias of a chain. |

**Returns:** _Promise‹boolean›_

Returns a Promise boolean of whether the chain has completed bootstrapping.

---

### peers

▸ **peers**(`nodeIDs`: string[]): _Promise‹[PeersResponse](../interfaces/info_interfaces.peersresponse)[]›_

_Defined in [src/apis/info/api.ts:149](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/info/api.ts#L149)_

Returns the peers connected to the node.

**Parameters:**

| Name      | Type     | Default | Description                                                                                                                                                                                                                                                          |
| --------- | -------- | ------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `nodeIDs` | string[] | []      | an optional parameter to specify what nodeID's descriptions should be returned. If this parameter is left empty, descriptions for all active connections will be returned. If the node is not connected to a specified nodeID, it will be omitted from the response. |

**Returns:** _Promise‹[PeersResponse](../interfaces/info_interfaces.peersresponse)[]›_

Promise for the list of connected peers in PeersResponse format.

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

### uptime

▸ **uptime**(): _Promise‹[UptimeResponse](../interfaces/info_interfaces.uptimeresponse)›_

_Defined in [src/apis/info/api.ts:165](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/info/api.ts#L165)_

Returns the network's observed uptime of this node.

**Returns:** _Promise‹[UptimeResponse](../interfaces/info_interfaces.uptimeresponse)›_

Returns a Promise UptimeResponse which contains rewardingStakePercentage and weightedAveragePercentage.
