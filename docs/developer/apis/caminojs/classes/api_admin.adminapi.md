# Class: AdminAPI

Class for interacting with a node's AdminAPI.

**`remarks`** This extends the [JRPCAPI](../modules/src_common#jrpcapi) class. This class should not be directly called.
Instead, use the [Avalanche.addAPI](avalanche.avalanche-1#addapi) function to register this interface with Avalanche.

## Hierarchy

↳ [JRPCAPI](common_jrpcapi.jrpcapi)

↳ **AdminAPI**

## Index

### Constructors

- [constructor](api_admin.adminapi#constructor)

### Properties

- [baseURL](api_admin.adminapi#protected-baseurl)
- [core](api_admin.adminapi#protected-core)
- [db](api_admin.adminapi#protected-db)
- [jrpcVersion](api_admin.adminapi#protected-jrpcversion)
- [rpcID](api_admin.adminapi#protected-rpcid)

### Methods

- [alias](api_admin.adminapi#alias)
- [aliasChain](api_admin.adminapi#aliaschain)
- [callMethod](api_admin.adminapi#callmethod)
- [getBaseURL](api_admin.adminapi#getbaseurl)
- [getChainAliases](api_admin.adminapi#getchainaliases)
- [getDB](api_admin.adminapi#getdb)
- [getLoggerLevel](api_admin.adminapi#getloggerlevel)
- [getRPCID](api_admin.adminapi#getrpcid)
- [loadVMs](api_admin.adminapi#loadvms)
- [lockProfile](api_admin.adminapi#lockprofile)
- [memoryProfile](api_admin.adminapi#memoryprofile)
- [setBaseURL](api_admin.adminapi#setbaseurl)
- [setLoggerLevel](api_admin.adminapi#setloggerlevel)
- [startCPUProfiler](api_admin.adminapi#startcpuprofiler)
- [stopCPUProfiler](api_admin.adminapi#stopcpuprofiler)

## Constructors

### constructor

\+ **new AdminAPI**(`core`: [AvalancheCore](avalanchecore.avalanchecore-1), `baseURL`: string): _[AdminAPI](api_admin.adminapi)_

_Overrides [JRPCAPI](common_jrpcapi.jrpcapi).[constructor](common_jrpcapi.jrpcapi#constructor)_

_Defined in [src/apis/admin/api.ts:215](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/admin/api.ts#L215)_

This class should not be instantiated directly. Instead use the [Avalanche.addAPI](avalanche.avalanche-1#addapi)
method.

**Parameters:**

| Name      | Type                                           | Default      | Description                                                      |
| --------- | ---------------------------------------------- | ------------ | ---------------------------------------------------------------- |
| `core`    | [AvalancheCore](avalanchecore.avalanchecore-1) | -            | A reference to the Avalanche class                               |
| `baseURL` | string                                         | "/ext/admin" | Defaults to the string "/ext/admin" as the path to rpc's baseURL |

**Returns:** _[AdminAPI](api_admin.adminapi)_

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

### alias

▸ **alias**(`endpoint`: string, `alias`: string): _Promise‹boolean›_

_Defined in [src/apis/admin/api.ts:39](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/admin/api.ts#L39)_

Assign an API an alias, a different endpoint for the API. The original endpoint will still
work. This change only affects this node other nodes will not know about this alias.

The API being aliased can now be called at ext/alias

**Parameters:**

| Name       | Type   | Description                                                                                         |
| ---------- | ------ | --------------------------------------------------------------------------------------------------- |
| `endpoint` | string | The original endpoint of the API. endpoint should only include the part of the endpoint after /ext/ |
| `alias`    | string | -                                                                                                   |

**Returns:** _Promise‹boolean›_

Returns a Promise boolean containing success, true for success, false for failure.

---

### aliasChain

▸ **aliasChain**(`chain`: string, `alias`: string): _Promise‹boolean›_

_Defined in [src/apis/admin/api.ts:62](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/admin/api.ts#L62)_

Give a blockchain an alias, a different name that can be used any place the blockchain’s
ID is used.

**Parameters:**

| Name    | Type   | Description                                                                     |
| ------- | ------ | ------------------------------------------------------------------------------- |
| `chain` | string | The blockchain’s ID                                                             |
| `alias` | string | Can now be used in place of the blockchain’s ID (in API endpoints, for example) |

**Returns:** _Promise‹boolean›_

Returns a Promise boolean containing success, true for success, false for failure.

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

### getBaseURL

▸ **getBaseURL**(): _string_

_Inherited from [APIBase](common_apibase.apibase).[getBaseURL](common_apibase.apibase#getbaseurl)_

_Defined in [src/common/apibase.ts:53](https://github.com/chain4travel/caminojs/blob/3883166/src/common/apibase.ts#L53)_

Returns the baseURL's path.

**Returns:** _string_

---

### getChainAliases

▸ **getChainAliases**(`chain`: string): _Promise‹string[]›_

_Defined in [src/apis/admin/api.ts:83](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/admin/api.ts#L83)_

Get all aliases for given blockchain

**Parameters:**

| Name    | Type   | Description         |
| ------- | ------ | ------------------- |
| `chain` | string | The blockchain’s ID |

**Returns:** _Promise‹string[]›_

Returns a Promise string[] containing aliases of the blockchain.

---

### getDB

▸ **getDB**(): _StoreAPI_

_Inherited from [APIBase](common_apibase.apibase).[getDB](common_apibase.apibase#getdb)_

_Defined in [src/common/apibase.ts:58](https://github.com/chain4travel/caminojs/blob/3883166/src/common/apibase.ts#L58)_

Returns the baseURL's database.

**Returns:** _StoreAPI_

---

### getLoggerLevel

▸ **getLoggerLevel**(`loggerName?`: string): _Promise‹[GetLoggerLevelResponse](../interfaces/admin_interfaces.getloggerlevelresponse)›_

_Defined in [src/apis/admin/api.ts:103](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/admin/api.ts#L103)_

Returns log and display levels of loggers

**Parameters:**

| Name          | Type   | Description                                                                                                             |
| ------------- | ------ | ----------------------------------------------------------------------------------------------------------------------- |
| `loggerName?` | string | the name of the logger to be returned. This is an optional argument. If not specified, it returns all possible loggers. |

**Returns:** _Promise‹[GetLoggerLevelResponse](../interfaces/admin_interfaces.getloggerlevelresponse)›_

Returns a Promise containing logger levels

---

### getRPCID

▸ **getRPCID**(): _number_

_Inherited from [EVMAPI](api_evm.evmapi).[getRPCID](api_evm.evmapi#getrpcid)_

_Defined in [src/common/jrpcapi.ts:77](https://github.com/chain4travel/caminojs/blob/3883166/src/common/jrpcapi.ts#L77)_

Returns the rpcid, a strictly-increasing number, starting from 1, indicating the next
request ID that will be sent.

**Returns:** _number_

---

### loadVMs

▸ **loadVMs**(): _Promise‹[LoadVMsResponse](../interfaces/admin_interfaces.loadvmsresponse)›_

_Defined in [src/apis/admin/api.ts:122](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/admin/api.ts#L122)_

Dynamically loads any virtual machines installed on the node as plugins

**Returns:** _Promise‹[LoadVMsResponse](../interfaces/admin_interfaces.loadvmsresponse)›_

Returns a Promise containing new VMs and failed VMs

---

### lockProfile

▸ **lockProfile**(): _Promise‹boolean›_

_Defined in [src/apis/admin/api.ts:134](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/admin/api.ts#L134)_

Dump the mutex statistics of the node to the specified file.

**Returns:** _Promise‹boolean›_

Promise for a boolean that is true on success.

---

### memoryProfile

▸ **memoryProfile**(): _Promise‹boolean›_

_Defined in [src/apis/admin/api.ts:148](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/admin/api.ts#L148)_

Dump the current memory footprint of the node to the specified file.

**Returns:** _Promise‹boolean›_

Promise for a boolean that is true on success.

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

### setLoggerLevel

▸ **setLoggerLevel**(`loggerName?`: string, `logLevel?`: string, `displayLevel?`: string): _Promise‹[SetLoggerLevelResponse](../interfaces/admin_interfaces.setloggerlevelresponse)›_

_Defined in [src/apis/admin/api.ts:166](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/admin/api.ts#L166)_

Sets log and display levels of loggers.

**Parameters:**

| Name            | Type   | Description                                                          |
| --------------- | ------ | -------------------------------------------------------------------- |
| `loggerName?`   | string | the name of the logger to be changed. This is an optional parameter. |
| `logLevel?`     | string | the log level of written logs, can be omitted.                       |
| `displayLevel?` | string | the log level of displayed logs, can be omitted.                     |

**Returns:** _Promise‹[SetLoggerLevelResponse](../interfaces/admin_interfaces.setloggerlevelresponse)›_

Returns a Promise containing logger levels

---

### startCPUProfiler

▸ **startCPUProfiler**(): _Promise‹boolean›_

_Defined in [src/apis/admin/api.ts:194](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/admin/api.ts#L194)_

Start profiling the cpu utilization of the node. Will dump the profile information into
the specified file on stop.

**Returns:** _Promise‹boolean›_

Promise for a boolean that is true on success.

---

### stopCPUProfiler

▸ **stopCPUProfiler**(): _Promise‹boolean›_

_Defined in [src/apis/admin/api.ts:208](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/admin/api.ts#L208)_

Stop the CPU profile that was previously started.

**Returns:** _Promise‹boolean›_

Promise for a boolean that is true on success.
