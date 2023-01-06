# Class: AuthAPI

Class for interacting with a node's AuthAPI.

**`remarks`** This extends the [JRPCAPI](../modules/src_common#jrpcapi) class. This class should not be directly called. Instead, use the [Avalanche.addAPI](avalanche.avalanche-1#addapi) function to register this interface with Avalanche.

## Hierarchy

↳ [JRPCAPI](common_jrpcapi.jrpcapi)

↳ **AuthAPI**

## Index

### Constructors

- [constructor](api_auth.authapi#constructor)

### Properties

- [baseURL](api_auth.authapi#protected-baseurl)
- [core](api_auth.authapi#protected-core)
- [db](api_auth.authapi#protected-db)
- [jrpcVersion](api_auth.authapi#protected-jrpcversion)
- [rpcID](api_auth.authapi#protected-rpcid)

### Methods

- [callMethod](api_auth.authapi#callmethod)
- [changePassword](api_auth.authapi#changepassword)
- [getBaseURL](api_auth.authapi#getbaseurl)
- [getDB](api_auth.authapi#getdb)
- [getRPCID](api_auth.authapi#getrpcid)
- [newToken](api_auth.authapi#newtoken)
- [revokeToken](api_auth.authapi#revoketoken)
- [setBaseURL](api_auth.authapi#setbaseurl)

## Constructors

### constructor

\+ **new AuthAPI**(`core`: [AvalancheCore](avalanchecore.avalanchecore-1), `baseURL`: string): _[AuthAPI](api_auth.authapi)_

_Overrides [JRPCAPI](common_jrpcapi.jrpcapi).[constructor](common_jrpcapi.jrpcapi#constructor)_

_Defined in [src/apis/auth/api.ts:89](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/auth/api.ts#L89)_

This class should not be instantiated directly. Instead use the [Avalanche.addAPI](avalanche.avalanche-1#addapi)
method.

**Parameters:**

| Name      | Type                                           | Default     | Description                                                     |
| --------- | ---------------------------------------------- | ----------- | --------------------------------------------------------------- |
| `core`    | [AvalancheCore](avalanchecore.avalanchecore-1) | -           | A reference to the Avalanche class                              |
| `baseURL` | string                                         | "/ext/auth" | Defaults to the string "/ext/auth" as the path to rpc's baseURL |

**Returns:** _[AuthAPI](api_auth.authapi)_

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

### changePassword

▸ **changePassword**(`oldPassword`: string, `newPassword`: string): _Promise‹boolean›_

_Defined in [src/apis/auth/api.ts:76](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/auth/api.ts#L76)_

Change this node's authorization token password. **Any authorization tokens created under an old password will become invalid.**

**Parameters:**

| Name          | Type   | Description                                                                               |
| ------------- | ------ | ----------------------------------------------------------------------------------------- |
| `oldPassword` | string | This node's authorization token password, set through the CLI when the node was launched. |
| `newPassword` | string | A new password for this node's authorization token issuance.                              |

**Returns:** _Promise‹boolean›_

Returns a Promise boolean indicating if the password was successfully changed.

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

_Inherited from [EVMAPI](api_evm.evmapi).[getRPCID](api_evm.evmapi#getrpcid)_

_Defined in [src/common/jrpcapi.ts:77](https://github.com/chain4travel/caminojs/blob/3883166/src/common/jrpcapi.ts#L77)_

Returns the rpcid, a strictly-increasing number, starting from 1, indicating the next
request ID that will be sent.

**Returns:** _number_

---

### newToken

▸ **newToken**(`password`: string, `endpoints`: string[]): _Promise‹string | [ErrorResponseObject](../interfaces/src_utils.errorresponseobject)›_

_Defined in [src/apis/auth/api.ts:31](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/auth/api.ts#L31)_

Creates a new authorization token that grants access to one or more API endpoints.

**Parameters:**

| Name        | Type     | Description                                                                                                                                   |
| ----------- | -------- | --------------------------------------------------------------------------------------------------------------------------------------------- |
| `password`  | string   | This node's authorization token password, set through the CLI when the node was launched.                                                     |
| `endpoints` | string[] | A list of endpoints that will be accessible using the generated token. If there"s an element that is "\*", this token can reach any endpoint. |

**Returns:** _Promise‹string | [ErrorResponseObject](../interfaces/src_utils.errorresponseobject)›_

Returns a Promise string containing the authorization token.

---

### revokeToken

▸ **revokeToken**(`password`: string, `token`: string): _Promise‹boolean›_

_Defined in [src/apis/auth/api.ts:56](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/auth/api.ts#L56)_

Revokes an authorization token, removing all of its rights to access endpoints.

**Parameters:**

| Name       | Type   | Description                                                                               |
| ---------- | ------ | ----------------------------------------------------------------------------------------- |
| `password` | string | This node's authorization token password, set through the CLI when the node was launched. |
| `token`    | string | An authorization token whose access should be revoked.                                    |

**Returns:** _Promise‹boolean›_

Returns a Promise boolean indicating if a token was successfully revoked.

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
