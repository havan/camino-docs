# Class: IndexAPI

Class for interacting with a node's IndexAPI.

**`remarks`** This extends the [JRPCAPI](../modules/src_common#jrpcapi) class. This class should not be directly called. Instead, use the [Avalanche.addAPI](avalanche.avalanche-1#addapi) function to register this interface with Avalanche.

## Hierarchy

↳ [JRPCAPI](common_jrpcapi.jrpcapi)

↳ **IndexAPI**

## Index

### Constructors

- [constructor](api_index.indexapi#constructor)

### Properties

- [baseURL](api_index.indexapi#protected-baseurl)
- [core](api_index.indexapi#protected-core)
- [db](api_index.indexapi#protected-db)
- [jrpcVersion](api_index.indexapi#protected-jrpcversion)
- [rpcID](api_index.indexapi#protected-rpcid)

### Methods

- [callMethod](api_index.indexapi#callmethod)
- [getBaseURL](api_index.indexapi#getbaseurl)
- [getContainerByID](api_index.indexapi#getcontainerbyid)
- [getContainerByIndex](api_index.indexapi#getcontainerbyindex)
- [getContainerRange](api_index.indexapi#getcontainerrange)
- [getDB](api_index.indexapi#getdb)
- [getIndex](api_index.indexapi#getindex)
- [getLastAccepted](api_index.indexapi#getlastaccepted)
- [getRPCID](api_index.indexapi#getrpcid)
- [isAccepted](api_index.indexapi#isaccepted)
- [setBaseURL](api_index.indexapi#setbaseurl)

## Constructors

### constructor

\+ **new IndexAPI**(`core`: [AvalancheCore](avalanchecore.avalanchecore-1), `baseURL`: string): _[IndexAPI](api_index.indexapi)_

_Overrides [JRPCAPI](common_jrpcapi.jrpcapi).[constructor](common_jrpcapi.jrpcapi#constructor)_

_Defined in [src/apis/index/api.ts:214](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/index/api.ts#L214)_

This class should not be instantiated directly. Instead use the [Avalanche.addAPI](avalanche.avalanche-1#addapi) method.

**Parameters:**

| Name      | Type                                           | Default           | Description                                                           |
| --------- | ---------------------------------------------- | ----------------- | --------------------------------------------------------------------- |
| `core`    | [AvalancheCore](avalanchecore.avalanchecore-1) | -                 | A reference to the Avalanche class                                    |
| `baseURL` | string                                         | "/ext/index/X/tx" | Defaults to the string "/ext/index/X/tx" as the path to rpc's baseURL |

**Returns:** _[IndexAPI](api_index.indexapi)_

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

### getContainerByID

▸ **getContainerByID**(`id`: string, `encoding`: string, `baseURL`: string): _Promise‹[GetContainerByIDResponse](../interfaces/index_interfaces.getcontainerbyidresponse)›_

_Defined in [src/apis/index/api.ts:98](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/index/api.ts#L98)_

Get contrainer by ID

**Parameters:**

| Name       | Type   | Default           | Description |
| ---------- | ------ | ----------------- | ----------- |
| `id`       | string | "0"               | -           |
| `encoding` | string | "hex"             | -           |
| `baseURL`  | string | this.getBaseURL() |             |

**Returns:** _Promise‹[GetContainerByIDResponse](../interfaces/index_interfaces.getcontainerbyidresponse)›_

Returns a Promise GetContainerByIDResponse.

---

### getContainerByIndex

▸ **getContainerByIndex**(`index`: string, `encoding`: string, `baseURL`: string): _Promise‹[GetContainerByIndexResponse](../interfaces/index_interfaces.getcontainerbyindexresponse)›_

_Defined in [src/apis/index/api.ts:67](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/index/api.ts#L67)_

Get container by index

**Parameters:**

| Name       | Type   | Default           | Description |
| ---------- | ------ | ----------------- | ----------- |
| `index`    | string | "0"               | -           |
| `encoding` | string | "hex"             | -           |
| `baseURL`  | string | this.getBaseURL() |             |

**Returns:** _Promise‹[GetContainerByIndexResponse](../interfaces/index_interfaces.getcontainerbyindexresponse)›_

Returns a Promise GetContainerByIndexResponse.

---

### getContainerRange

▸ **getContainerRange**(`startIndex`: number, `numToFetch`: number, `encoding`: string, `baseURL`: string): _Promise‹[GetContainerRangeResponse](../interfaces/index_interfaces.getcontainerrangeresponse)[]›_

_Defined in [src/apis/index/api.ts:130](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/index/api.ts#L130)_

Get container range

**Parameters:**

| Name         | Type   | Default           | Description |
| ------------ | ------ | ----------------- | ----------- |
| `startIndex` | number | 0                 | -           |
| `numToFetch` | number | 100               | -           |
| `encoding`   | string | "hex"             | -           |
| `baseURL`    | string | this.getBaseURL() |             |

**Returns:** _Promise‹[GetContainerRangeResponse](../interfaces/index_interfaces.getcontainerrangeresponse)[]›_

Returns a Promise GetContainerRangeResponse.

---

### getDB

▸ **getDB**(): _StoreAPI_

_Inherited from [APIBase](common_apibase.apibase).[getDB](common_apibase.apibase#getdb)_

_Defined in [src/common/apibase.ts:58](https://github.com/chain4travel/caminojs/blob/3883166/src/common/apibase.ts#L58)_

Returns the baseURL's database.

**Returns:** _StoreAPI_

---

### getIndex

▸ **getIndex**(`id`: string, `encoding`: string, `baseURL`: string): _Promise‹string›_

_Defined in [src/apis/index/api.ts:163](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/index/api.ts#L163)_

Get index by containerID

**Parameters:**

| Name       | Type   | Default           | Description |
| ---------- | ------ | ----------------- | ----------- |
| `id`       | string | ""                | -           |
| `encoding` | string | "hex"             | -           |
| `baseURL`  | string | this.getBaseURL() |             |

**Returns:** _Promise‹string›_

Returns a Promise GetIndexResponse.

---

### getLastAccepted

▸ **getLastAccepted**(`encoding`: string, `baseURL`: string): _Promise‹[GetLastAcceptedResponse](../interfaces/index_interfaces.getlastacceptedresponse)›_

_Defined in [src/apis/index/api.ts:38](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/index/api.ts#L38)_

Get last accepted tx, vtx or block

**Parameters:**

| Name       | Type   | Default           | Description |
| ---------- | ------ | ----------------- | ----------- |
| `encoding` | string | "hex"             | -           |
| `baseURL`  | string | this.getBaseURL() |             |

**Returns:** _Promise‹[GetLastAcceptedResponse](../interfaces/index_interfaces.getlastacceptedresponse)›_

Returns a Promise GetLastAcceptedResponse.

---

### getRPCID

▸ **getRPCID**(): _number_

_Inherited from [EVMAPI](api_evm.evmapi).[getRPCID](api_evm.evmapi#getrpcid)_

_Defined in [src/common/jrpcapi.ts:77](https://github.com/chain4travel/caminojs/blob/3883166/src/common/jrpcapi.ts#L77)_

Returns the rpcid, a strictly-increasing number, starting from 1, indicating the next
request ID that will be sent.

**Returns:** _number_

---

### isAccepted

▸ **isAccepted**(`id`: string, `encoding`: string, `baseURL`: string): _Promise‹[IsAcceptedResponse](../interfaces/index_interfaces.isacceptedresponse)›_

_Defined in [src/apis/index/api.ts:194](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/index/api.ts#L194)_

Check if container is accepted

**Parameters:**

| Name       | Type   | Default           | Description |
| ---------- | ------ | ----------------- | ----------- |
| `id`       | string | ""                | -           |
| `encoding` | string | "hex"             | -           |
| `baseURL`  | string | this.getBaseURL() |             |

**Returns:** _Promise‹[IsAcceptedResponse](../interfaces/index_interfaces.isacceptedresponse)›_

Returns a Promise GetIsAcceptedResponse.

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
