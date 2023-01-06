# Class: APIBase

Abstract class defining a generic endpoint that all endpoints must implement (extend).

## Hierarchy

- **APIBase**

  ↳ [RESTAPI](common_restapi.restapi)

  ↳ [JRPCAPI](common_jrpcapi.jrpcapi)

## Index

### Constructors

- [constructor](common_apibase.apibase#constructor)

### Properties

- [baseURL](common_apibase.apibase#protected-baseurl)
- [core](common_apibase.apibase#protected-core)
- [db](common_apibase.apibase#protected-db)

### Methods

- [getBaseURL](common_apibase.apibase#getbaseurl)
- [getDB](common_apibase.apibase#getdb)
- [setBaseURL](common_apibase.apibase#setbaseurl)

## Constructors

### constructor

\+ **new APIBase**(`core`: [AvalancheCore](avalanchecore.avalanchecore-1), `baseURL`: string): _[APIBase](common_apibase.apibase)_

_Defined in [src/common/apibase.ts:58](https://github.com/chain4travel/caminojs/blob/3883166/src/common/apibase.ts#L58)_

**Parameters:**

| Name      | Type                                           | Description                                            |
| --------- | ---------------------------------------------- | ------------------------------------------------------ |
| `core`    | [AvalancheCore](avalanchecore.avalanchecore-1) | Reference to the Avalanche instance using this baseURL |
| `baseURL` | string                                         | Path to the baseURL                                    |

**Returns:** _[APIBase](common_apibase.apibase)_

## Properties

### `Protected` baseURL

• **baseURL**: _string_

_Defined in [src/common/apibase.ts:29](https://github.com/chain4travel/caminojs/blob/3883166/src/common/apibase.ts#L29)_

---

### `Protected` core

• **core**: _[AvalancheCore](avalanchecore.avalanchecore-1)_

_Defined in [src/common/apibase.ts:28](https://github.com/chain4travel/caminojs/blob/3883166/src/common/apibase.ts#L28)_

---

### `Protected` db

• **db**: _StoreAPI_

_Defined in [src/common/apibase.ts:30](https://github.com/chain4travel/caminojs/blob/3883166/src/common/apibase.ts#L30)_

## Methods

### getBaseURL

▸ **getBaseURL**(): _string_

_Defined in [src/common/apibase.ts:53](https://github.com/chain4travel/caminojs/blob/3883166/src/common/apibase.ts#L53)_

Returns the baseURL's path.

**Returns:** _string_

---

### getDB

▸ **getDB**(): _StoreAPI_

_Defined in [src/common/apibase.ts:58](https://github.com/chain4travel/caminojs/blob/3883166/src/common/apibase.ts#L58)_

Returns the baseURL's database.

**Returns:** _StoreAPI_

---

### setBaseURL

▸ **setBaseURL**(`baseURL`: string): _void_

_Defined in [src/common/apibase.ts:37](https://github.com/chain4travel/caminojs/blob/3883166/src/common/apibase.ts#L37)_

Sets the path of the APIs baseURL.

**Parameters:**

| Name      | Type   | Description                                |
| --------- | ------ | ------------------------------------------ |
| `baseURL` | string | Path of the APIs baseURL - ex: "/ext/bc/X" |

**Returns:** _void_
