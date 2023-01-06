# Class: MetricsAPI

Class for interacting with a node API that is using the node's MetricsApi.

**`remarks`** This extends the [RESTAPI](common_restapi.restapi) class. This class should not be directly called. Instead, use the [Avalanche.addAPI](avalanche.avalanche-1#addapi) function to register this interface with Avalanche.

## Hierarchy

↳ [RESTAPI](common_restapi.restapi)

↳ **MetricsAPI**

## Index

### Constructors

- [constructor](api_metrics.metricsapi#constructor)

### Properties

- [acceptType](api_metrics.metricsapi#protected-accepttype)
- [baseURL](api_metrics.metricsapi#protected-baseurl)
- [contentType](api_metrics.metricsapi#protected-contenttype)
- [core](api_metrics.metricsapi#protected-core)
- [db](api_metrics.metricsapi#protected-db)

### Methods

- [axConf](api_metrics.metricsapi#protected-axconf)
- [delete](api_metrics.metricsapi#delete)
- [get](api_metrics.metricsapi#get)
- [getAcceptType](api_metrics.metricsapi#getaccepttype)
- [getBaseURL](api_metrics.metricsapi#getbaseurl)
- [getContentType](api_metrics.metricsapi#getcontenttype)
- [getDB](api_metrics.metricsapi#getdb)
- [getMetrics](api_metrics.metricsapi#getmetrics)
- [patch](api_metrics.metricsapi#patch)
- [post](api_metrics.metricsapi#post)
- [prepHeaders](api_metrics.metricsapi#protected-prepheaders)
- [put](api_metrics.metricsapi#put)
- [setBaseURL](api_metrics.metricsapi#setbaseurl)

## Constructors

### constructor

\+ **new MetricsAPI**(`core`: [AvalancheCore](avalanchecore.avalanchecore-1), `baseURL`: string): _[MetricsAPI](api_metrics.metricsapi)_

_Overrides [RESTAPI](common_restapi.restapi).[constructor](common_restapi.restapi#constructor)_

_Defined in [src/apis/metrics/api.ts:32](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/metrics/api.ts#L32)_

This class should not be instantiated directly. Instead use the [Avalanche.addAPI](avalanche.avalanche-1#addapi) method.

**Parameters:**

| Name      | Type                                           | Default        | Description                                                        |
| --------- | ---------------------------------------------- | -------------- | ------------------------------------------------------------------ |
| `core`    | [AvalancheCore](avalanchecore.avalanchecore-1) | -              | A reference to the Avalanche class                                 |
| `baseURL` | string                                         | "/ext/metrics" | Defaults to the string "/ext/metrics" as the path to rpc's baseurl |

**Returns:** _[MetricsAPI](api_metrics.metricsapi)_

## Properties

### `Protected` acceptType

• **acceptType**: _string_

_Inherited from [RESTAPI](common_restapi.restapi).[acceptType](common_restapi.restapi#protected-accepttype)_

_Defined in [src/common/restapi.ts:12](https://github.com/chain4travel/caminojs/blob/3883166/src/common/restapi.ts#L12)_

---

### `Protected` baseURL

• **baseURL**: _string_

_Inherited from [APIBase](common_apibase.apibase).[baseURL](common_apibase.apibase#protected-baseurl)_

_Defined in [src/common/apibase.ts:29](https://github.com/chain4travel/caminojs/blob/3883166/src/common/apibase.ts#L29)_

---

### `Protected` contentType

• **contentType**: _string_

_Inherited from [RESTAPI](common_restapi.restapi).[contentType](common_restapi.restapi#protected-contenttype)_

_Defined in [src/common/restapi.ts:11](https://github.com/chain4travel/caminojs/blob/3883166/src/common/restapi.ts#L11)_

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

## Methods

### `Protected` axConf

▸ **axConf**(): _AxiosRequestConfig_

_Overrides [RESTAPI](common_restapi.restapi).[axConf](common_restapi.restapi#protected-axconf)_

_Defined in [src/apis/metrics/api.ts:18](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/metrics/api.ts#L18)_

**Returns:** _AxiosRequestConfig_

---

### delete

▸ **delete**(`method`: string, `params?`: object[] | object, `baseURL?`: string, `contentType?`: string, `acceptType?`: string): _Promise‹[RequestResponseData](common_apibase.requestresponsedata)›_

_Inherited from [RESTAPI](common_restapi.restapi).[delete](common_restapi.restapi#delete)_

_Defined in [src/common/restapi.ts:110](https://github.com/chain4travel/caminojs/blob/3883166/src/common/restapi.ts#L110)_

**Parameters:**

| Name           | Type                   |
| -------------- | ---------------------- |
| `method`       | string                 |
| `params?`      | object[] &#124; object |
| `baseURL?`     | string                 |
| `contentType?` | string                 |
| `acceptType?`  | string                 |

**Returns:** _Promise‹[RequestResponseData](common_apibase.requestresponsedata)›_

---

### get

▸ **get**(`baseURL?`: string, `contentType?`: string, `acceptType?`: string): _Promise‹[RequestResponseData](common_apibase.requestresponsedata)›_

_Inherited from [RESTAPI](common_restapi.restapi).[get](common_restapi.restapi#get)_

_Defined in [src/common/restapi.ts:40](https://github.com/chain4travel/caminojs/blob/3883166/src/common/restapi.ts#L40)_

**Parameters:**

| Name           | Type   |
| -------------- | ------ |
| `baseURL?`     | string |
| `contentType?` | string |
| `acceptType?`  | string |

**Returns:** _Promise‹[RequestResponseData](common_apibase.requestresponsedata)›_

---

### getAcceptType

▸ **getAcceptType**(): _string_

_Inherited from [RESTAPI](common_restapi.restapi).[getAcceptType](common_restapi.restapi#getaccepttype)_

_Defined in [src/common/restapi.ts:171](https://github.com/chain4travel/caminojs/blob/3883166/src/common/restapi.ts#L171)_

Returns what type of representation is desired at the client side

**Returns:** _string_

---

### getBaseURL

▸ **getBaseURL**(): _string_

_Inherited from [APIBase](common_apibase.apibase).[getBaseURL](common_apibase.apibase#getbaseurl)_

_Defined in [src/common/apibase.ts:53](https://github.com/chain4travel/caminojs/blob/3883166/src/common/apibase.ts#L53)_

Returns the baseURL's path.

**Returns:** _string_

---

### getContentType

▸ **getContentType**(): _string_

_Inherited from [RESTAPI](common_restapi.restapi).[getContentType](common_restapi.restapi#getcontenttype)_

_Defined in [src/common/restapi.ts:166](https://github.com/chain4travel/caminojs/blob/3883166/src/common/restapi.ts#L166)_

Returns the type of the entity attached to the incoming request

**Returns:** _string_

---

### getDB

▸ **getDB**(): _StoreAPI_

_Inherited from [APIBase](common_apibase.apibase).[getDB](common_apibase.apibase#getdb)_

_Defined in [src/common/apibase.ts:58](https://github.com/chain4travel/caminojs/blob/3883166/src/common/apibase.ts#L58)_

Returns the baseURL's database.

**Returns:** _StoreAPI_

---

### getMetrics

▸ **getMetrics**(): _Promise‹string›_

_Defined in [src/apis/metrics/api.ts:29](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/metrics/api.ts#L29)_

**Returns:** _Promise‹string›_

Promise for an object containing the metrics response

---

### patch

▸ **patch**(`method`: string, `params?`: object[] | object, `baseURL?`: string, `contentType?`: string, `acceptType?`: string): _Promise‹[RequestResponseData](common_apibase.requestresponsedata)›_

_Inherited from [RESTAPI](common_restapi.restapi).[patch](common_restapi.restapi#patch)_

_Defined in [src/common/restapi.ts:136](https://github.com/chain4travel/caminojs/blob/3883166/src/common/restapi.ts#L136)_

**Parameters:**

| Name           | Type                   |
| -------------- | ---------------------- |
| `method`       | string                 |
| `params?`      | object[] &#124; object |
| `baseURL?`     | string                 |
| `contentType?` | string                 |
| `acceptType?`  | string                 |

**Returns:** _Promise‹[RequestResponseData](common_apibase.requestresponsedata)›_

---

### post

▸ **post**(`method`: string, `params?`: object[] | object, `baseURL?`: string, `contentType?`: string, `acceptType?`: string): _Promise‹[RequestResponseData](common_apibase.requestresponsedata)›_

_Inherited from [RESTAPI](common_restapi.restapi).[post](common_restapi.restapi#post)_

_Defined in [src/common/restapi.ts:56](https://github.com/chain4travel/caminojs/blob/3883166/src/common/restapi.ts#L56)_

**Parameters:**

| Name           | Type                   |
| -------------- | ---------------------- |
| `method`       | string                 |
| `params?`      | object[] &#124; object |
| `baseURL?`     | string                 |
| `contentType?` | string                 |
| `acceptType?`  | string                 |

**Returns:** _Promise‹[RequestResponseData](common_apibase.requestresponsedata)›_

---

### `Protected` prepHeaders

▸ **prepHeaders**(`contentType?`: string, `acceptType?`: string): _object_

_Inherited from [RESTAPI](common_restapi.restapi).[prepHeaders](common_restapi.restapi#protected-prepheaders)_

_Defined in [src/common/restapi.ts:14](https://github.com/chain4travel/caminojs/blob/3883166/src/common/restapi.ts#L14)_

**Parameters:**

| Name           | Type   |
| -------------- | ------ |
| `contentType?` | string |
| `acceptType?`  | string |

**Returns:** _object_

---

### put

▸ **put**(`method`: string, `params?`: object[] | object, `baseURL?`: string, `contentType?`: string, `acceptType?`: string): _Promise‹[RequestResponseData](common_apibase.requestresponsedata)›_

_Inherited from [RESTAPI](common_restapi.restapi).[put](common_restapi.restapi#put)_

_Defined in [src/common/restapi.ts:83](https://github.com/chain4travel/caminojs/blob/3883166/src/common/restapi.ts#L83)_

**Parameters:**

| Name           | Type                   |
| -------------- | ---------------------- |
| `method`       | string                 |
| `params?`      | object[] &#124; object |
| `baseURL?`     | string                 |
| `contentType?` | string                 |
| `acceptType?`  | string                 |

**Returns:** _Promise‹[RequestResponseData](common_apibase.requestresponsedata)›_

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
