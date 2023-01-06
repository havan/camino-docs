# Class: RESTAPI

## Hierarchy

- [APIBase](common_apibase.apibase)

  ↳ **RESTAPI**

  ↳ [MetricsAPI](api_metrics.metricsapi)

## Index

### Constructors

- [constructor](common_restapi.restapi#constructor)

### Properties

- [acceptType](common_restapi.restapi#protected-accepttype)
- [baseURL](common_restapi.restapi#protected-baseurl)
- [contentType](common_restapi.restapi#protected-contenttype)
- [core](common_restapi.restapi#protected-core)
- [db](common_restapi.restapi#protected-db)

### Methods

- [axConf](common_restapi.restapi#protected-axconf)
- [delete](common_restapi.restapi#delete)
- [get](common_restapi.restapi#get)
- [getAcceptType](common_restapi.restapi#getaccepttype)
- [getBaseURL](common_restapi.restapi#getbaseurl)
- [getContentType](common_restapi.restapi#getcontenttype)
- [getDB](common_restapi.restapi#getdb)
- [patch](common_restapi.restapi#patch)
- [post](common_restapi.restapi#post)
- [prepHeaders](common_restapi.restapi#protected-prepheaders)
- [put](common_restapi.restapi#put)
- [setBaseURL](common_restapi.restapi#setbaseurl)

## Constructors

### constructor

\+ **new RESTAPI**(`core`: [AvalancheCore](avalanchecore.avalanchecore-1), `baseURL`: string, `contentType`: string, `acceptType`: string): _[RESTAPI](common_restapi.restapi)_

_Overrides [APIBase](common_apibase.apibase).[constructor](common_apibase.apibase#constructor)_

_Defined in [src/common/restapi.ts:171](https://github.com/chain4travel/caminojs/blob/3883166/src/common/restapi.ts#L171)_

**Parameters:**

| Name          | Type                                           | Default                          | Description                                                                        |
| ------------- | ---------------------------------------------- | -------------------------------- | ---------------------------------------------------------------------------------- |
| `core`        | [AvalancheCore](avalanchecore.avalanchecore-1) | -                                | Reference to the Avalanche instance using this endpoint                            |
| `baseURL`     | string                                         | -                                | Path of the APIs baseURL - ex: "/ext/bc/avm"                                       |
| `contentType` | string                                         | "application/json;charset=UTF-8" | Optional Determines the type of the entity attached to the incoming request        |
| `acceptType`  | string                                         | undefined                        | Optional Determines the type of representation which is desired on the client side |

**Returns:** _[RESTAPI](common_restapi.restapi)_

## Properties

### `Protected` acceptType

• **acceptType**: _string_

_Defined in [src/common/restapi.ts:12](https://github.com/chain4travel/caminojs/blob/3883166/src/common/restapi.ts#L12)_

---

### `Protected` baseURL

• **baseURL**: _string_

_Inherited from [APIBase](common_apibase.apibase).[baseURL](common_apibase.apibase#protected-baseurl)_

_Defined in [src/common/apibase.ts:29](https://github.com/chain4travel/caminojs/blob/3883166/src/common/apibase.ts#L29)_

---

### `Protected` contentType

• **contentType**: _string_

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

_Defined in [src/common/restapi.ts:33](https://github.com/chain4travel/caminojs/blob/3883166/src/common/restapi.ts#L33)_

**Returns:** _AxiosRequestConfig_

---

### delete

▸ **delete**(`method`: string, `params?`: object[] | object, `baseURL?`: string, `contentType?`: string, `acceptType?`: string): _Promise‹[RequestResponseData](common_apibase.requestresponsedata)›_

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

### patch

▸ **patch**(`method`: string, `params?`: object[] | object, `baseURL?`: string, `contentType?`: string, `acceptType?`: string): _Promise‹[RequestResponseData](common_apibase.requestresponsedata)›_

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
