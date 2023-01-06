# Class: Socket

## Hierarchy

- any

  ↳ **Socket**

## Index

### Constructors

- [constructor](api_socket.socket#constructor)

### Properties

- [onclose](api_socket.socket#onclose)
- [onerror](api_socket.socket#onerror)
- [onmessage](api_socket.socket#onmessage)
- [onopen](api_socket.socket#onopen)

### Methods

- [close](api_socket.socket#close)
- [send](api_socket.socket#send)

## Constructors

### constructor

\+ **new Socket**(`url`: string, `options?`: WebSocket.ClientOptions | ClientRequestArgs): _[Socket](api_socket.socket)_

_Defined in [src/apis/socket/socket.ts:35](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/socket/socket.ts#L35)_

Provides the API for creating and managing a WebSocket connection to a server, as well as for sending and receiving data on the connection.

**Parameters:**

| Name       | Type                                             | Description                |
| ---------- | ------------------------------------------------ | -------------------------- |
| `url`      | string                                           | Defaults to [[MainnetAPI]] |
| `options?` | WebSocket.ClientOptions &#124; ClientRequestArgs | Optional                   |

**Returns:** _[Socket](api_socket.socket)_

## Properties

### onclose

• **onclose**: _any_

_Defined in [src/apis/socket/socket.ts:13](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/socket/socket.ts#L13)_

---

### onerror

• **onerror**: _any_

_Defined in [src/apis/socket/socket.ts:15](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/socket/socket.ts#L15)_

---

### onmessage

• **onmessage**: _any_

_Defined in [src/apis/socket/socket.ts:11](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/socket/socket.ts#L11)_

---

### onopen

• **onopen**: _any_

_Defined in [src/apis/socket/socket.ts:9](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/socket/socket.ts#L9)_

## Methods

### close

▸ **close**(`mcode?`: number, `data?`: string): _void_

_Defined in [src/apis/socket/socket.ts:33](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/socket/socket.ts#L33)_

Terminates the connection completely

**Parameters:**

| Name     | Type   | Description |
| -------- | ------ | ----------- |
| `mcode?` | number | Optional    |
| `data?`  | string | Optional    |

**Returns:** _void_

---

### send

▸ **send**(`data`: any, `cb?`: any): _void_

_Defined in [src/apis/socket/socket.ts:23](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/socket/socket.ts#L23)_

Send a message to the server

**Parameters:**

| Name   | Type | Description |
| ------ | ---- | ----------- |
| `data` | any  | -           |
| `cb?`  | any  | Optional    |

**Returns:** _void_
