# Class: Avalanche

CaminoJS is middleware for interacting with Camino node RPC APIs.

Example usage:

```js
const avalanche: Avalanche = new Avalanche("127.0.0.1", 9650, "https");
```

## Hierarchy

- [AvalancheCore](avalanchecore.avalanchecore-1)

  ↳ **Avalanche**

## Index

### Constructors

- [constructor](avalanche.avalanche-1#constructor)

### Properties

- [apis](avalanche.avalanche-1#protected-apis)
- [auth](avalanche.avalanche-1#protected-auth)
- [baseEndpoint](avalanche.avalanche-1#protected-baseendpoint)
- [headers](avalanche.avalanche-1#protected-headers)
- [host](avalanche.avalanche-1#protected-host)
- [ip](avalanche.avalanche-1#protected-ip)
- [network](avalanche.avalanche-1#protected-network)
- [networkID](avalanche.avalanche-1#protected-networkid)
- [port](avalanche.avalanche-1#protected-port)
- [protocol](avalanche.avalanche-1#protected-protocol)
- [requestConfig](avalanche.avalanche-1#protected-requestconfig)
- [url](avalanche.avalanche-1#protected-url)

### Methods

- [Admin](avalanche.avalanche-1#admin)
- [Auth](avalanche.avalanche-1#auth)
- [CChain](avalanche.avalanche-1#cchain)
- [Health](avalanche.avalanche-1#health)
- [Index](avalanche.avalanche-1#index)
- [Info](avalanche.avalanche-1#info)
- [Metrics](avalanche.avalanche-1#metrics)
- [NodeKeys](avalanche.avalanche-1#nodekeys)
- [PChain](avalanche.avalanche-1#pchain)
- [XChain](avalanche.avalanche-1#xchain)
- [\_setHeaders](avalanche.avalanche-1#protected-_setheaders)
- [addAPI](avalanche.avalanche-1#addapi)
- [api](avalanche.avalanche-1#api)
- [delete](avalanche.avalanche-1#delete)
- [fetchNetworkSettings](avalanche.avalanche-1#fetchnetworksettings)
- [get](avalanche.avalanche-1#get)
- [getBaseEndpoint](avalanche.avalanche-1#getbaseendpoint)
- [getHRP](avalanche.avalanche-1#gethrp)
- [getHeaders](avalanche.avalanche-1#getheaders)
- [getHost](avalanche.avalanche-1#gethost)
- [getIP](avalanche.avalanche-1#getip)
- [getNetwork](avalanche.avalanche-1#getnetwork)
- [getNetworkID](avalanche.avalanche-1#getnetworkid)
- [getPort](avalanche.avalanche-1#getport)
- [getPrimaryAssetAlias](avalanche.avalanche-1#getprimaryassetalias)
- [getProtocol](avalanche.avalanche-1#getprotocol)
- [getRequestConfig](avalanche.avalanche-1#getrequestconfig)
- [getURL](avalanche.avalanche-1#geturl)
- [patch](avalanche.avalanche-1#patch)
- [post](avalanche.avalanche-1#post)
- [put](avalanche.avalanche-1#put)
- [refreshAPI](avalanche.avalanche-1#protected-refreshapi)
- [removeAllHeaders](avalanche.avalanche-1#removeallheaders)
- [removeAllRequestConfigs](avalanche.avalanche-1#removeallrequestconfigs)
- [removeHeader](avalanche.avalanche-1#removeheader)
- [removeRequestConfig](avalanche.avalanche-1#removerequestconfig)
- [setAuthToken](avalanche.avalanche-1#setauthtoken)
- [setHeader](avalanche.avalanche-1#setheader)
- [setNetwork](avalanche.avalanche-1#setnetwork)
- [setRequestConfig](avalanche.avalanche-1#setrequestconfig)

## Constructors

### constructor

\+ **new Avalanche**(`host`: string, `port`: number, `protocol`: string, `networkID`: number, `XChainID`: string, `CChainID`: string, `skipinit`: boolean): _[Avalanche](avalanche.avalanche-1)_

_Overrides [AvalancheCore](avalanchecore.avalanchecore-1).[constructor](avalanchecore.avalanchecore-1#constructor)_

_Defined in [src/index.ts:99](https://github.com/chain4travel/caminojs/blob/3883166/src/index.ts#L99)_

Creates a new Avalanche instance. Sets the address and port of the main Avalanche Client.

**Parameters:**

| Name        | Type    | Default   | Description                                                                                                                        |
| ----------- | ------- | --------- | ---------------------------------------------------------------------------------------------------------------------------------- |
| `host`      | string  | -         | The hostname to resolve to reach the Avalanche Client RPC APIs                                                                     |
| `port`      | number  | -         | The port to resolve to reach the Avalanche Client RPC APIs                                                                         |
| `protocol`  | string  | -         | The protocol string to use before a "://" in a request, ex: "http", "https", "git", "ws", etc. Defaults to http                    |
| `networkID` | number  | undefined | Sets the NetworkID of the class. Default [DefaultNetworkID](../modules/utils_constants#const-defaultnetworkid)                     |
| `XChainID`  | string  | undefined | Sets the blockchainID for the AVM. Will try to auto-detect, otherwise default "2eNy1mUFdmaxXNj1eQHUe7Np4gju9sJsEtWQ4MX3ToiNKuADed" |
| `CChainID`  | string  | undefined | Sets the blockchainID for the EVM. Will try to auto-detect, otherwise default "2CA6j5zYzasynPsFeNoqWkmTCt3VScMvXUZHbfDJ8k3oGzAPtU" |
| `skipinit`  | boolean | false     | Skips creating the APIs. Defaults to false                                                                                         |

**Returns:** _[Avalanche](avalanche.avalanche-1)_

## Properties

### `Protected` apis

• **apis**: _object_

_Inherited from [AvalancheCore](avalanchecore.avalanchecore-1).[apis](avalanchecore.avalanchecore-1#protected-apis)_

_Defined in [src/camino.ts:38](https://github.com/chain4travel/caminojs/blob/3883166/src/camino.ts#L38)_

#### Type declaration:

- \[ **k**: _string_\]: [APIBase](common_apibase.apibase)

---

### `Protected` auth

• **auth**: _string_ = undefined

_Inherited from [AvalancheCore](avalanchecore.avalanchecore-1).[auth](avalanchecore.avalanchecore-1#protected-auth)_

_Defined in [src/camino.ts:35](https://github.com/chain4travel/caminojs/blob/3883166/src/camino.ts#L35)_

---

### `Protected` baseEndpoint

• **baseEndpoint**: _string_

_Inherited from [AvalancheCore](avalanchecore.avalanchecore-1).[baseEndpoint](avalanchecore.avalanchecore-1#protected-baseendpoint)_

_Defined in [src/camino.ts:33](https://github.com/chain4travel/caminojs/blob/3883166/src/camino.ts#L33)_

---

### `Protected` headers

• **headers**: _object_

_Inherited from [AvalancheCore](avalanchecore.avalanchecore-1).[headers](avalanchecore.avalanchecore-1#protected-headers)_

_Defined in [src/camino.ts:36](https://github.com/chain4travel/caminojs/blob/3883166/src/camino.ts#L36)_

#### Type declaration:

- \[ **k**: _string_\]: string

---

### `Protected` host

• **host**: _string_

_Inherited from [AvalancheCore](avalanchecore.avalanchecore-1).[host](avalanchecore.avalanchecore-1#protected-host)_

_Defined in [src/camino.ts:31](https://github.com/chain4travel/caminojs/blob/3883166/src/camino.ts#L31)_

---

### `Protected` ip

• **ip**: _string_

_Inherited from [AvalancheCore](avalanchecore.avalanchecore-1).[ip](avalanchecore.avalanchecore-1#protected-ip)_

_Defined in [src/camino.ts:30](https://github.com/chain4travel/caminojs/blob/3883166/src/camino.ts#L30)_

---

### `Protected` network

• **network**: _[Network](../interfaces/utils_networks.network)_ = undefined

_Inherited from [AvalancheCore](avalanchecore.avalanchecore-1).[network](avalanchecore.avalanchecore-1#protected-network)_

_Defined in [src/camino.ts:39](https://github.com/chain4travel/caminojs/blob/3883166/src/camino.ts#L39)_

---

### `Protected` networkID

• **networkID**: _number_ = 0

_Inherited from [AvalancheCore](avalanchecore.avalanchecore-1).[networkID](avalanchecore.avalanchecore-1#protected-networkid)_

_Defined in [src/camino.ts:28](https://github.com/chain4travel/caminojs/blob/3883166/src/camino.ts#L28)_

---

### `Protected` port

• **port**: _number_

_Inherited from [AvalancheCore](avalanchecore.avalanchecore-1).[port](avalanchecore.avalanchecore-1#protected-port)_

_Defined in [src/camino.ts:32](https://github.com/chain4travel/caminojs/blob/3883166/src/camino.ts#L32)_

---

### `Protected` protocol

• **protocol**: _string_

_Inherited from [AvalancheCore](avalanchecore.avalanchecore-1).[protocol](avalanchecore.avalanchecore-1#protected-protocol)_

_Defined in [src/camino.ts:29](https://github.com/chain4travel/caminojs/blob/3883166/src/camino.ts#L29)_

---

### `Protected` requestConfig

• **requestConfig**: _AxiosRequestConfig_

_Inherited from [AvalancheCore](avalanchecore.avalanchecore-1).[requestConfig](avalanchecore.avalanchecore-1#protected-requestconfig)_

_Defined in [src/camino.ts:37](https://github.com/chain4travel/caminojs/blob/3883166/src/camino.ts#L37)_

---

### `Protected` url

• **url**: _string_

_Inherited from [AvalancheCore](avalanchecore.avalanchecore-1).[url](avalanchecore.avalanchecore-1#protected-url)_

_Defined in [src/camino.ts:34](https://github.com/chain4travel/caminojs/blob/3883166/src/camino.ts#L34)_

## Methods

### Admin

▸ **Admin**(): _[AdminAPI](api_admin.adminapi)‹›_

_Defined in [src/index.ts:53](https://github.com/chain4travel/caminojs/blob/3883166/src/index.ts#L53)_

Returns a reference to the Admin RPC.

**Returns:** _[AdminAPI](api_admin.adminapi)‹›_

---

### Auth

▸ **Auth**(): _[AuthAPI](api_auth.authapi)‹›_

_Defined in [src/index.ts:58](https://github.com/chain4travel/caminojs/blob/3883166/src/index.ts#L58)_

Returns a reference to the Auth RPC.

**Returns:** _[AuthAPI](api_auth.authapi)‹›_

---

### CChain

▸ **CChain**(): _[EVMAPI](api_evm.evmapi)‹›_

_Defined in [src/index.ts:63](https://github.com/chain4travel/caminojs/blob/3883166/src/index.ts#L63)_

Returns a reference to the EVMAPI RPC pointed at the C-Chain.

**Returns:** _[EVMAPI](api_evm.evmapi)‹›_

---

### Health

▸ **Health**(): _[HealthAPI](api_health.healthapi)‹›_

_Defined in [src/index.ts:73](https://github.com/chain4travel/caminojs/blob/3883166/src/index.ts#L73)_

Returns a reference to the Health RPC for a node.

**Returns:** _[HealthAPI](api_health.healthapi)‹›_

---

### Index

▸ **Index**(): _[IndexAPI](api_index.indexapi)‹›_

_Defined in [src/index.ts:78](https://github.com/chain4travel/caminojs/blob/3883166/src/index.ts#L78)_

Returns a reference to the Index RPC for a node.

**Returns:** _[IndexAPI](api_index.indexapi)‹›_

---

### Info

▸ **Info**(): _[InfoAPI](api_info.infoapi)‹›_

_Defined in [src/index.ts:83](https://github.com/chain4travel/caminojs/blob/3883166/src/index.ts#L83)_

Returns a reference to the Info RPC for a node.

**Returns:** _[InfoAPI](api_info.infoapi)‹›_

---

### Metrics

▸ **Metrics**(): _[MetricsAPI](api_metrics.metricsapi)‹›_

_Defined in [src/index.ts:88](https://github.com/chain4travel/caminojs/blob/3883166/src/index.ts#L88)_

Returns a reference to the Metrics RPC.

**Returns:** _[MetricsAPI](api_metrics.metricsapi)‹›_

---

### NodeKeys

▸ **NodeKeys**(): _[KeystoreAPI](api_keystore.keystoreapi)‹›_

_Defined in [src/index.ts:94](https://github.com/chain4travel/caminojs/blob/3883166/src/index.ts#L94)_

Returns a reference to the Keystore RPC for a node. We label it "NodeKeys" to reduce
confusion about what it's accessing.

**Returns:** _[KeystoreAPI](api_keystore.keystoreapi)‹›_

---

### PChain

▸ **PChain**(): _[PlatformVMAPI](api_platformvm.platformvmapi)‹›_

_Defined in [src/index.ts:99](https://github.com/chain4travel/caminojs/blob/3883166/src/index.ts#L99)_

Returns a reference to the PlatformVM RPC pointed at the P-Chain.

**Returns:** _[PlatformVMAPI](api_platformvm.platformvmapi)‹›_

---

### XChain

▸ **XChain**(): _[AVMAPI](api_avm.avmapi)‹›_

_Defined in [src/index.ts:68](https://github.com/chain4travel/caminojs/blob/3883166/src/index.ts#L68)_

Returns a reference to the AVM RPC pointed at the X-Chain.

**Returns:** _[AVMAPI](api_avm.avmapi)‹›_

---

### `Protected` \_setHeaders

▸ **\_setHeaders**(`headers`: any): _AxiosRequestHeaders_

_Inherited from [AvalancheCore](avalanchecore.avalanchecore-1).[\_setHeaders](avalanchecore.avalanchecore-1#protected-_setheaders)_

_Defined in [src/camino.ts:227](https://github.com/chain4travel/caminojs/blob/3883166/src/camino.ts#L227)_

**Parameters:**

| Name      | Type |
| --------- | ---- |
| `headers` | any  |

**Returns:** _AxiosRequestHeaders_

---

### addAPI

▸ **addAPI**‹**GA**›(`apiName`: string, `ConstructorFN`: object, `baseurl`: string, ...`args`: any[]): _void_

_Inherited from [AvalancheCore](avalanchecore.avalanchecore-1).[addAPI](avalanchecore.avalanchecore-1#addapi)_

_Defined in [src/camino.ts:266](https://github.com/chain4travel/caminojs/blob/3883166/src/camino.ts#L266)_

Adds an API to the middleware. The API resolves to a registered blockchain's RPC.

In TypeScript:

```js
avalanche.addAPI < MyVMClass > ("mychain", MyVMClass, "/ext/bc/mychain");
```

In Javascript:

```js
avalanche.addAPI("mychain", MyVMClass, "/ext/bc/mychain");
```

**Type parameters:**

▪ **GA**: _[APIBase](common_apibase.apibase)_

Class of the API being added

**Parameters:**

| Name            | Type   | Default   | Description                                         |
| --------------- | ------ | --------- | --------------------------------------------------- |
| `apiName`       | string | -         | A label for referencing the API in the future       |
| `ConstructorFN` | object | -         | A reference to the class which instantiates the API |
| `baseurl`       | string | undefined | Path to resolve to reach the API                    |
| `...args`       | any[]  | -         | -                                                   |

**Returns:** _void_

---

### api

▸ **api**‹**GA**›(`apiName`: string): _GA_

_Inherited from [AvalancheCore](avalanchecore.avalanchecore-1).[api](avalanchecore.avalanchecore-1#api)_

_Defined in [src/camino.ts:288](https://github.com/chain4travel/caminojs/blob/3883166/src/camino.ts#L288)_

Retrieves a reference to an API by its apiName label.

**Type parameters:**

▪ **GA**: _[APIBase](common_apibase.apibase)_

**Parameters:**

| Name      | Type   | Description               |
| --------- | ------ | ------------------------- |
| `apiName` | string | Name of the API to return |

**Returns:** _GA_

---

### delete

▸ **delete**(`baseurl`: string, `getdata`: object, `headers`: object, `axiosConfig`: AxiosRequestConfig): _Promise‹[RequestResponseData](common_apibase.requestresponsedata)›_

_Inherited from [AvalancheCore](avalanchecore.avalanchecore-1).[delete](avalanchecore.avalanchecore-1#delete)_

_Defined in [src/camino.ts:373](https://github.com/chain4travel/caminojs/blob/3883166/src/camino.ts#L373)_

Makes a DELETE call to an API.

**Parameters:**

| Name          | Type               | Default   | Description                                                                                               |
| ------------- | ------------------ | --------- | --------------------------------------------------------------------------------------------------------- |
| `baseurl`     | string             | -         | Path to the API                                                                                           |
| `getdata`     | object             | -         | Object containing the key value pairs sent in DELETE                                                      |
| `headers`     | object             | {}        | An array HTTP Request Headers                                                                             |
| `axiosConfig` | AxiosRequestConfig | undefined | Configuration for the axios javascript library that will be the foundation for the rest of the parameters |

**Returns:** _Promise‹[RequestResponseData](common_apibase.requestresponsedata)›_

A promise for [RequestResponseData](common_apibase.requestresponsedata)

---

### fetchNetworkSettings

▸ **fetchNetworkSettings**(): _Promise‹boolean›_

_Defined in [src/index.ts:157](https://github.com/chain4travel/caminojs/blob/3883166/src/index.ts#L157)_

**Returns:** _Promise‹boolean›_

---

### get

▸ **get**(`baseurl`: string, `getdata`: object, `headers`: object, `axiosConfig`: AxiosRequestConfig): _Promise‹[RequestResponseData](common_apibase.requestresponsedata)›_

_Inherited from [AvalancheCore](avalanchecore.avalanchecore-1).[get](avalanchecore.avalanchecore-1#get)_

_Defined in [src/camino.ts:347](https://github.com/chain4travel/caminojs/blob/3883166/src/camino.ts#L347)_

Makes a GET call to an API.

**Parameters:**

| Name          | Type               | Default   | Description                                                                                               |
| ------------- | ------------------ | --------- | --------------------------------------------------------------------------------------------------------- |
| `baseurl`     | string             | -         | Path to the api                                                                                           |
| `getdata`     | object             | -         | Object containing the key value pairs sent in GET                                                         |
| `headers`     | object             | {}        | An array HTTP Request Headers                                                                             |
| `axiosConfig` | AxiosRequestConfig | undefined | Configuration for the axios javascript library that will be the foundation for the rest of the parameters |

**Returns:** _Promise‹[RequestResponseData](common_apibase.requestresponsedata)›_

A promise for [RequestResponseData](common_apibase.requestresponsedata)

---

### getBaseEndpoint

▸ **getBaseEndpoint**(): _string_

_Inherited from [AvalancheCore](avalanchecore.avalanchecore-1).[getBaseEndpoint](avalanchecore.avalanchecore-1#getbaseendpoint)_

_Defined in [src/camino.ts:129](https://github.com/chain4travel/caminojs/blob/3883166/src/camino.ts#L129)_

Returns the base endpoint for the Avalanche node.

**Returns:** _string_

---

### getHRP

▸ **getHRP**(): _string_

_Inherited from [AvalancheCore](avalanchecore.avalanchecore-1).[getHRP](avalanchecore.avalanchecore-1#gethrp)_

_Defined in [src/camino.ts:156](https://github.com/chain4travel/caminojs/blob/3883166/src/camino.ts#L156)_

Returns the Human-Readable-Part of the network associated with this key.

**Returns:** _string_

The [KeyPair](api_evm_keychain.keypair)'s Human-Readable-Part of the network's Bech32 addressing scheme

---

### getHeaders

▸ **getHeaders**(): _object_

_Inherited from [AvalancheCore](avalanchecore.avalanchecore-1).[getHeaders](avalanchecore.avalanchecore-1#getheaders)_

_Defined in [src/camino.ts:139](https://github.com/chain4travel/caminojs/blob/3883166/src/camino.ts#L139)_

Returns the custom headers

**Returns:** _object_

---

### getHost

▸ **getHost**(): _string_

_Inherited from [AvalancheCore](avalanchecore.avalanchecore-1).[getHost](avalanchecore.avalanchecore-1#gethost)_

_Defined in [src/camino.ts:114](https://github.com/chain4travel/caminojs/blob/3883166/src/camino.ts#L114)_

Returns the host for the Avalanche node.

**Returns:** _string_

---

### getIP

▸ **getIP**(): _string_

_Inherited from [AvalancheCore](avalanchecore.avalanchecore-1).[getIP](avalanchecore.avalanchecore-1#getip)_

_Defined in [src/camino.ts:119](https://github.com/chain4travel/caminojs/blob/3883166/src/camino.ts#L119)_

Returns the IP for the Avalanche node.

**Returns:** _string_

---

### getNetwork

▸ **getNetwork**(): _[Network](../interfaces/utils_networks.network)_

_Inherited from [AvalancheCore](avalanchecore.avalanchecore-1).[getNetwork](avalanchecore.avalanchecore-1#getnetwork)_

_Defined in [src/camino.ts:104](https://github.com/chain4travel/caminojs/blob/3883166/src/camino.ts#L104)_

Returns the network configuration.

**Returns:** _[Network](../interfaces/utils_networks.network)_

---

### getNetworkID

▸ **getNetworkID**(): _number_

_Inherited from [AvalancheCore](avalanchecore.avalanchecore-1).[getNetworkID](avalanchecore.avalanchecore-1#getnetworkid)_

_Defined in [src/camino.ts:149](https://github.com/chain4travel/caminojs/blob/3883166/src/camino.ts#L149)_

Returns the networkID

**Returns:** _number_

---

### getPort

▸ **getPort**(): _number_

_Inherited from [AvalancheCore](avalanchecore.avalanchecore-1).[getPort](avalanchecore.avalanchecore-1#getport)_

_Defined in [src/camino.ts:124](https://github.com/chain4travel/caminojs/blob/3883166/src/camino.ts#L124)_

Returns the port for the Avalanche node.

**Returns:** _number_

---

### getPrimaryAssetAlias

▸ **getPrimaryAssetAlias**(): _string_

_Inherited from [AvalancheCore](avalanchecore.avalanchecore-1).[getPrimaryAssetAlias](avalanchecore.avalanchecore-1#getprimaryassetalias)_

_Defined in [src/camino.ts:243](https://github.com/chain4travel/caminojs/blob/3883166/src/camino.ts#L243)_

Returns the primary asset alias.

**Returns:** _string_

---

### getProtocol

▸ **getProtocol**(): _string_

_Inherited from [AvalancheCore](avalanchecore.avalanchecore-1).[getProtocol](avalanchecore.avalanchecore-1#getprotocol)_

_Defined in [src/camino.ts:109](https://github.com/chain4travel/caminojs/blob/3883166/src/camino.ts#L109)_

Returns the protocol such as "http", "https", "git", "ws", etc.

**Returns:** _string_

---

### getRequestConfig

▸ **getRequestConfig**(): _AxiosRequestConfig_

_Inherited from [AvalancheCore](avalanchecore.avalanchecore-1).[getRequestConfig](avalanchecore.avalanchecore-1#getrequestconfig)_

_Defined in [src/camino.ts:144](https://github.com/chain4travel/caminojs/blob/3883166/src/camino.ts#L144)_

Returns the custom request config

**Returns:** _AxiosRequestConfig_

---

### getURL

▸ **getURL**(): _string_

_Inherited from [AvalancheCore](avalanchecore.avalanchecore-1).[getURL](avalanchecore.avalanchecore-1#geturl)_

_Defined in [src/camino.ts:134](https://github.com/chain4travel/caminojs/blob/3883166/src/camino.ts#L134)_

Returns the URL of the Avalanche node (ip + port)

**Returns:** _string_

---

### patch

▸ **patch**(`baseurl`: string, `getdata`: object, `postdata`: string | object | ArrayBuffer | ArrayBufferView, `headers`: object, `axiosConfig`: AxiosRequestConfig): _Promise‹[RequestResponseData](common_apibase.requestresponsedata)›_

_Inherited from [AvalancheCore](avalanchecore.avalanchecore-1).[patch](avalanchecore.avalanchecore-1#patch)_

_Defined in [src/camino.ts:457](https://github.com/chain4travel/caminojs/blob/3883166/src/camino.ts#L457)_

Makes a PATCH call to an API.

**Parameters:**

| Name          | Type                                                           | Default   | Description                                                                                               |
| ------------- | -------------------------------------------------------------- | --------- | --------------------------------------------------------------------------------------------------------- |
| `baseurl`     | string                                                         | -         | Path to the baseurl                                                                                       |
| `getdata`     | object                                                         | -         | Object containing the key value pairs sent in PATCH                                                       |
| `postdata`    | string &#124; object &#124; ArrayBuffer &#124; ArrayBufferView | -         | Object containing the key value pairs sent in PATCH                                                       |
| `headers`     | object                                                         | {}        | An array HTTP Request Headers                                                                             |
| `axiosConfig` | AxiosRequestConfig                                             | undefined | Configuration for the axios javascript library that will be the foundation for the rest of the parameters |

**Returns:** _Promise‹[RequestResponseData](common_apibase.requestresponsedata)›_

A promise for [RequestResponseData](common_apibase.requestresponsedata)

---

### post

▸ **post**(`baseurl`: string, `getdata`: object, `postdata`: string | object | ArrayBuffer | ArrayBufferView, `headers`: object, `axiosConfig`: AxiosRequestConfig): _Promise‹[RequestResponseData](common_apibase.requestresponsedata)›_

_Inherited from [AvalancheCore](avalanchecore.avalanchecore-1).[post](avalanchecore.avalanchecore-1#post)_

_Defined in [src/camino.ts:400](https://github.com/chain4travel/caminojs/blob/3883166/src/camino.ts#L400)_

Makes a POST call to an API.

**Parameters:**

| Name          | Type                                                           | Default   | Description                                                                                               |
| ------------- | -------------------------------------------------------------- | --------- | --------------------------------------------------------------------------------------------------------- |
| `baseurl`     | string                                                         | -         | Path to the API                                                                                           |
| `getdata`     | object                                                         | -         | Object containing the key value pairs sent in POST                                                        |
| `postdata`    | string &#124; object &#124; ArrayBuffer &#124; ArrayBufferView | -         | Object containing the key value pairs sent in POST                                                        |
| `headers`     | object                                                         | {}        | An array HTTP Request Headers                                                                             |
| `axiosConfig` | AxiosRequestConfig                                             | undefined | Configuration for the axios javascript library that will be the foundation for the rest of the parameters |

**Returns:** _Promise‹[RequestResponseData](common_apibase.requestresponsedata)›_

A promise for [RequestResponseData](common_apibase.requestresponsedata)

---

### put

▸ **put**(`baseurl`: string, `getdata`: object, `postdata`: string | object | ArrayBuffer | ArrayBufferView, `headers`: object, `axiosConfig`: AxiosRequestConfig): _Promise‹[RequestResponseData](common_apibase.requestresponsedata)›_

_Inherited from [AvalancheCore](avalanchecore.avalanchecore-1).[put](avalanchecore.avalanchecore-1#put)_

_Defined in [src/camino.ts:428](https://github.com/chain4travel/caminojs/blob/3883166/src/camino.ts#L428)_

Makes a PUT call to an API.

**Parameters:**

| Name          | Type                                                           | Default   | Description                                                                                               |
| ------------- | -------------------------------------------------------------- | --------- | --------------------------------------------------------------------------------------------------------- |
| `baseurl`     | string                                                         | -         | Path to the baseurl                                                                                       |
| `getdata`     | object                                                         | -         | Object containing the key value pairs sent in PUT                                                         |
| `postdata`    | string &#124; object &#124; ArrayBuffer &#124; ArrayBufferView | -         | Object containing the key value pairs sent in PUT                                                         |
| `headers`     | object                                                         | {}        | An array HTTP Request Headers                                                                             |
| `axiosConfig` | AxiosRequestConfig                                             | undefined | Configuration for the axios javascript library that will be the foundation for the rest of the parameters |

**Returns:** _Promise‹[RequestResponseData](common_apibase.requestresponsedata)›_

A promise for [RequestResponseData](common_apibase.requestresponsedata)

---

### `Protected` refreshAPI

▸ **refreshAPI**(): _boolean_

_Defined in [src/index.ts:232](https://github.com/chain4travel/caminojs/blob/3883166/src/index.ts#L232)_

**Returns:** _boolean_

---

### removeAllHeaders

▸ **removeAllHeaders**(): _void_

_Inherited from [AvalancheCore](avalanchecore.avalanchecore-1).[removeAllHeaders](avalanchecore.avalanchecore-1#removeallheaders)_

_Defined in [src/camino.ts:180](https://github.com/chain4travel/caminojs/blob/3883166/src/camino.ts#L180)_

Removes all headers.

**Returns:** _void_

---

### removeAllRequestConfigs

▸ **removeAllRequestConfigs**(): _void_

_Inherited from [AvalancheCore](avalanchecore.avalanchecore-1).[removeAllRequestConfigs](avalanchecore.avalanchecore-1#removeallrequestconfigs)_

_Defined in [src/camino.ts:210](https://github.com/chain4travel/caminojs/blob/3883166/src/camino.ts#L210)_

Removes all request configs.

**Returns:** _void_

---

### removeHeader

▸ **removeHeader**(`key`: string): _void_

_Inherited from [AvalancheCore](avalanchecore.avalanchecore-1).[removeHeader](avalanchecore.avalanchecore-1#removeheader)_

_Defined in [src/camino.ts:173](https://github.com/chain4travel/caminojs/blob/3883166/src/camino.ts#L173)_

Removes a previously added custom header.

**Parameters:**

| Name  | Type   | Description |
| ----- | ------ | ----------- |
| `key` | string | Header name |

**Returns:** _void_

---

### removeRequestConfig

▸ **removeRequestConfig**(`key`: string): _void_

_Inherited from [AvalancheCore](avalanchecore.avalanchecore-1).[removeRequestConfig](avalanchecore.avalanchecore-1#removerequestconfig)_

_Defined in [src/camino.ts:203](https://github.com/chain4travel/caminojs/blob/3883166/src/camino.ts#L203)_

Removes a previously added request config.

**Parameters:**

| Name  | Type   | Description |
| ----- | ------ | ----------- |
| `key` | string | Header name |

**Returns:** _void_

---

### setAuthToken

▸ **setAuthToken**(`auth`: string): _void_

_Inherited from [AvalancheCore](avalanchecore.avalanchecore-1).[setAuthToken](avalanchecore.avalanchecore-1#setauthtoken)_

_Defined in [src/camino.ts:223](https://github.com/chain4travel/caminojs/blob/3883166/src/camino.ts#L223)_

Sets the temporary auth token used for communicating with the node.

**Parameters:**

| Name   | Type   | Description                                                                          |
| ------ | ------ | ------------------------------------------------------------------------------------ |
| `auth` | string | A temporary token provided by the node enabling access to the endpoints on the node. |

**Returns:** _void_

---

### setHeader

▸ **setHeader**(`key`: string, `value`: string): _void_

_Inherited from [AvalancheCore](avalanchecore.avalanchecore-1).[setHeader](avalanchecore.avalanchecore-1#setheader)_

_Defined in [src/camino.ts:164](https://github.com/chain4travel/caminojs/blob/3883166/src/camino.ts#L164)_

Adds a new custom header to be included with all requests.

**Parameters:**

| Name    | Type   | Description  |
| ------- | ------ | ------------ |
| `key`   | string | Header name  |
| `value` | string | Header value |

**Returns:** _void_

---

### setNetwork

▸ **setNetwork**(`host`: string, `port`: number, `protocol`: string, `networkID`: number, `baseEndpoint`: string): _void_

_Inherited from [AvalancheCore](avalanchecore.avalanchecore-1).[setNetwork](avalanchecore.avalanchecore-1#setnetwork)_

_Defined in [src/camino.ts:53](https://github.com/chain4travel/caminojs/blob/3883166/src/camino.ts#L53)_

Sets the address and port of the main Avalanche Client.

**Parameters:**

| Name           | Type   | Default | Description                                                                                                                                                                                                        |
| -------------- | ------ | ------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `host`         | string | -       | The hostname to resolve to reach the Avalanche Client RPC APIs.                                                                                                                                                    |
| `port`         | number | -       | The port to resolve to reach the Avalanche Client RPC APIs.                                                                                                                                                        |
| `protocol`     | string | -       | The protocol string to use before a "://" in a request, ex: "http", "https", etc. Defaults to http                                                                                                                 |
| `networkID`    | number | -       | -                                                                                                                                                                                                                  |
| `baseEndpoint` | string | ""      | the base endpoint to reach the Avalanche Client RPC APIs, ex: "/rpc". Defaults to "/" The following special characters are removed from host and protocol &#,@+()$~%'":\*?{} also less than and greater than signs |

**Returns:** _void_

---

### setRequestConfig

▸ **setRequestConfig**(`key`: string, `value`: string | boolean): _void_

_Inherited from [AvalancheCore](avalanchecore.avalanchecore-1).[setRequestConfig](avalanchecore.avalanchecore-1#setrequestconfig)_

_Defined in [src/camino.ts:194](https://github.com/chain4travel/caminojs/blob/3883166/src/camino.ts#L194)_

Adds a new custom config value to be included with all requests.

**Parameters:**

| Name    | Type                  | Description  |
| ------- | --------------------- | ------------ |
| `key`   | string                | Config name  |
| `value` | string &#124; boolean | Config value |

**Returns:** _void_
