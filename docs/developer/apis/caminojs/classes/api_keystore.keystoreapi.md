# Class: KeystoreAPI

Class for interacting with a node API that is using the node's KeystoreAPI.

**WARNING**: The KeystoreAPI is to be used by the node-owner as the data is stored locally on the node. Do not trust the root user. If you are not the node-owner, do not use this as your wallet.

**`remarks`** This extends the [JRPCAPI](../modules/src_common#jrpcapi) class. This class should not be directly called. Instead, use the [Avalanche.addAPI](avalanche.avalanche-1#addapi) function to register this interface with Avalanche.

## Hierarchy

↳ [JRPCAPI](common_jrpcapi.jrpcapi)

↳ **KeystoreAPI**

## Index

### Constructors

- [constructor](api_keystore.keystoreapi#constructor)

### Properties

- [baseURL](api_keystore.keystoreapi#protected-baseurl)
- [core](api_keystore.keystoreapi#protected-core)
- [db](api_keystore.keystoreapi#protected-db)
- [jrpcVersion](api_keystore.keystoreapi#protected-jrpcversion)
- [rpcID](api_keystore.keystoreapi#protected-rpcid)

### Methods

- [callMethod](api_keystore.keystoreapi#callmethod)
- [createUser](api_keystore.keystoreapi#createuser)
- [deleteUser](api_keystore.keystoreapi#deleteuser)
- [exportUser](api_keystore.keystoreapi#exportuser)
- [getBaseURL](api_keystore.keystoreapi#getbaseurl)
- [getDB](api_keystore.keystoreapi#getdb)
- [getRPCID](api_keystore.keystoreapi#getrpcid)
- [importUser](api_keystore.keystoreapi#importuser)
- [listUsers](api_keystore.keystoreapi#listusers)
- [setBaseURL](api_keystore.keystoreapi#setbaseurl)

## Constructors

### constructor

\+ **new KeystoreAPI**(`core`: [AvalancheCore](avalanchecore.avalanchecore-1), `baseURL`: string): _[KeystoreAPI](api_keystore.keystoreapi)_

_Overrides [JRPCAPI](common_jrpcapi.jrpcapi).[constructor](common_jrpcapi.jrpcapi#constructor)_

_Defined in [src/apis/keystore/api.ts:125](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/keystore/api.ts#L125)_

This class should not be instantiated directly. Instead use the [Avalanche.addAPI](avalanche.avalanche-1#addapi) method.

**Parameters:**

| Name      | Type                                           | Default         | Description                                                         |
| --------- | ---------------------------------------------- | --------------- | ------------------------------------------------------------------- |
| `core`    | [AvalancheCore](avalanchecore.avalanchecore-1) | -               | A reference to the Avalanche class                                  |
| `baseURL` | string                                         | "/ext/keystore" | Defaults to the string "/ext/keystore" as the path to rpc's baseURL |

**Returns:** _[KeystoreAPI](api_keystore.keystoreapi)_

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

### createUser

▸ **createUser**(`username`: string, `password`: string): _Promise‹boolean›_

_Defined in [src/apis/keystore/api.ts:29](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/keystore/api.ts#L29)_

Creates a user in the node's database.

**Parameters:**

| Name       | Type   | Description                |
| ---------- | ------ | -------------------------- |
| `username` | string | Name of the user to create |
| `password` | string | Password for the user      |

**Returns:** _Promise‹boolean›_

Promise for a boolean with true on success

---

### deleteUser

▸ **deleteUser**(`username`: string, `password`: string): _Promise‹boolean›_

_Defined in [src/apis/keystore/api.ts:113](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/keystore/api.ts#L113)_

Deletes a user in the node's database.

**Parameters:**

| Name       | Type   | Description                |
| ---------- | ------ | -------------------------- |
| `username` | string | Name of the user to delete |
| `password` | string | Password for the user      |

**Returns:** _Promise‹boolean›_

Promise for a boolean with true on success

---

### exportUser

▸ **exportUser**(`username`: string, `password`: string): _Promise‹string›_

_Defined in [src/apis/keystore/api.ts:51](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/keystore/api.ts#L51)_

Exports a user. The user can be imported to another node with keystore.importUser .

**Parameters:**

| Name       | Type   | Description                        |
| ---------- | ------ | ---------------------------------- |
| `username` | string | The name of the user to export     |
| `password` | string | The password of the user to export |

**Returns:** _Promise‹string›_

Promise with a string importable using importUser

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

### importUser

▸ **importUser**(`username`: string, `user`: string, `password`: string): _Promise‹boolean›_

_Defined in [src/apis/keystore/api.ts:74](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/keystore/api.ts#L74)_

Imports a user file into the node's user database and assigns it to a username.

**Parameters:**

| Name       | Type   | Description                                       |
| ---------- | ------ | ------------------------------------------------- |
| `username` | string | The name the user file should be imported into    |
| `user`     | string | cb58 serialized string represetning a user"s data |
| `password` | string | The user"s password                               |

**Returns:** _Promise‹boolean›_

A promise with a true-value on success.

---

### listUsers

▸ **listUsers**(): _Promise‹string[]›_

_Defined in [src/apis/keystore/api.ts:98](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/keystore/api.ts#L98)_

Lists the names of all users on the node.

**Returns:** _Promise‹string[]›_

Promise of an array with all user names.

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
