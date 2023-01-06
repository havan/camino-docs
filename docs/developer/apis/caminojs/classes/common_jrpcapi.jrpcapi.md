# Class: JRPCAPI

## Hierarchy

- [APIBase](common_apibase.apibase)

  ↳ **JRPCAPI**

  ↳ [EVMAPI](api_evm.evmapi)

  ↳ [AdminAPI](api_admin.adminapi)

  ↳ [AuthAPI](api_auth.authapi)

  ↳ [AVMAPI](api_avm.avmapi)

  ↳ [HealthAPI](api_health.healthapi)

  ↳ [IndexAPI](api_index.indexapi)

  ↳ [InfoAPI](api_info.infoapi)

  ↳ [KeystoreAPI](api_keystore.keystoreapi)

  ↳ [PlatformVMAPI](api_platformvm.platformvmapi)

## Index

### Constructors

- [constructor](common_jrpcapi.jrpcapi#constructor)

### Properties

- [baseURL](common_jrpcapi.jrpcapi#protected-baseurl)
- [core](common_jrpcapi.jrpcapi#protected-core)
- [db](common_jrpcapi.jrpcapi#protected-db)
- [jrpcVersion](common_jrpcapi.jrpcapi#protected-jrpcversion)
- [rpcID](common_jrpcapi.jrpcapi#protected-rpcid)

### Methods

- [callMethod](common_jrpcapi.jrpcapi#callmethod)
- [getBaseURL](common_jrpcapi.jrpcapi#getbaseurl)
- [getDB](common_jrpcapi.jrpcapi#getdb)
- [getRPCID](common_jrpcapi.jrpcapi#getrpcid)
- [setBaseURL](common_jrpcapi.jrpcapi#setbaseurl)

## Constructors

### constructor

\+ **new JRPCAPI**(`core`: [AvalancheCore](avalanchecore.avalanchecore-1), `baseURL`: string, `jrpcVersion`: string): _[JRPCAPI](common_jrpcapi.jrpcapi)_

_Overrides [APIBase](common_apibase.apibase).[constructor](common_apibase.apibase#constructor)_

_Defined in [src/common/jrpcapi.ts:77](https://github.com/chain4travel/caminojs/blob/3883166/src/common/jrpcapi.ts#L77)_

**Parameters:**

| Name          | Type                                           | Default | Description                                             |
| ------------- | ---------------------------------------------- | ------- | ------------------------------------------------------- |
| `core`        | [AvalancheCore](avalanchecore.avalanchecore-1) | -       | Reference to the Avalanche instance using this endpoint |
| `baseURL`     | string                                         | -       | Path of the APIs baseURL - ex: "/ext/bc/avm"            |
| `jrpcVersion` | string                                         | "2.0"   | The jrpc version to use, default "2.0".                 |

**Returns:** _[JRPCAPI](common_jrpcapi.jrpcapi)_

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

_Defined in [src/common/jrpcapi.ts:12](https://github.com/chain4travel/caminojs/blob/3883166/src/common/jrpcapi.ts#L12)_

---

### `Protected` rpcID

• **rpcID**: _number_ = 1

_Defined in [src/common/jrpcapi.ts:13](https://github.com/chain4travel/caminojs/blob/3883166/src/common/jrpcapi.ts#L13)_

## Methods

### callMethod

▸ **callMethod**(`method`: string, `params?`: object[] | object, `baseURL?`: string, `headers?`: object): _Promise‹[RequestResponseData](common_apibase.requestresponsedata)›_

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

### getDB

▸ **getDB**(): _StoreAPI_

_Inherited from [APIBase](common_apibase.apibase).[getDB](common_apibase.apibase#getdb)_

_Defined in [src/common/apibase.ts:58](https://github.com/chain4travel/caminojs/blob/3883166/src/common/apibase.ts#L58)_

Returns the baseURL's database.

**Returns:** _StoreAPI_

---

### getRPCID

▸ **getRPCID**(): _number_

_Defined in [src/common/jrpcapi.ts:77](https://github.com/chain4travel/caminojs/blob/3883166/src/common/jrpcapi.ts#L77)_

Returns the rpcid, a strictly-increasing number, starting from 1, indicating the next
request ID that will be sent.

**Returns:** _number_

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
