# Class: PayloadTypes

Class for determining payload types and managing the lookup table.

## Hierarchy

- **PayloadTypes**

## Index

### Constructors

- [constructor](utils_payload.payloadtypes#private-constructor)

### Properties

- [types](utils_payload.payloadtypes#protected-types)
- [instance](utils_payload.payloadtypes#static-private-instance)

### Methods

- [getContent](utils_payload.payloadtypes#getcontent)
- [getPayload](utils_payload.payloadtypes#getpayload)
- [getTypeID](utils_payload.payloadtypes#gettypeid)
- [lookupID](utils_payload.payloadtypes#lookupid)
- [lookupType](utils_payload.payloadtypes#lookuptype)
- [recast](utils_payload.payloadtypes#recast)
- [select](utils_payload.payloadtypes#select)
- [getInstance](utils_payload.payloadtypes#static-getinstance)

## Constructors

### `Private` constructor

\+ **new PayloadTypes**(): _[PayloadTypes](utils_payload.payloadtypes)_

_Defined in [src/utils/payload.ts:155](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/payload.ts#L155)_

**Returns:** _[PayloadTypes](utils_payload.payloadtypes)_

## Properties

### `Protected` types

• **types**: _string[]_ = []

_Defined in [src/utils/payload.ts:23](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/payload.ts#L23)_

---

### `Static` `Private` instance

▪ **instance**: _[PayloadTypes](utils_payload.payloadtypes)_

_Defined in [src/utils/payload.ts:22](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/payload.ts#L22)_

## Methods

### getContent

▸ **getContent**(`payload`: Buffer): _Buffer_

_Defined in [src/utils/payload.ts:28](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/payload.ts#L28)_

Given an encoded payload buffer returns the payload content (minus typeID).

**Parameters:**

| Name      | Type   |
| --------- | ------ |
| `payload` | Buffer |

**Returns:** _Buffer_

---

### getPayload

▸ **getPayload**(`payload`: Buffer): _Buffer_

_Defined in [src/utils/payload.ts:36](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/payload.ts#L36)_

Given an encoded payload buffer returns the payload (with typeID).

**Parameters:**

| Name      | Type   |
| --------- | ------ |
| `payload` | Buffer |

**Returns:** _Buffer_

---

### getTypeID

▸ **getTypeID**(`payload`: Buffer): _number_

_Defined in [src/utils/payload.ts:44](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/payload.ts#L44)_

Given a payload buffer returns the proper TypeID.

**Parameters:**

| Name      | Type   |
| --------- | ------ |
| `payload` | Buffer |

**Returns:** _number_

---

### lookupID

▸ **lookupID**(`typestr`: string): _number_

_Defined in [src/utils/payload.ts:55](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/payload.ts#L55)_

Given a type string returns the proper TypeID.

**Parameters:**

| Name      | Type   |
| --------- | ------ |
| `typestr` | string |

**Returns:** _number_

---

### lookupType

▸ **lookupType**(`value`: number): _string_

_Defined in [src/utils/payload.ts:62](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/payload.ts#L62)_

Given a TypeID returns a string describing the payload type.

**Parameters:**

| Name    | Type   |
| ------- | ------ |
| `value` | number |

**Returns:** _string_

---

### recast

▸ **recast**(`unknowPayload`: [PayloadBase](utils_payload.payloadbase)): _[PayloadBase](utils_payload.payloadbase)_

_Defined in [src/utils/payload.ts:142](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/payload.ts#L142)_

Given a [PayloadBase](utils_payload.payloadbase) which may not be cast properly, returns a properly cast [PayloadBase](utils_payload.payloadbase).

**Parameters:**

| Name            | Type                                     |
| --------------- | ---------------------------------------- |
| `unknowPayload` | [PayloadBase](utils_payload.payloadbase) |

**Returns:** _[PayloadBase](utils_payload.payloadbase)_

---

### select

▸ **select**(`typeID`: number, ...`args`: any[]): _[PayloadBase](utils_payload.payloadbase)_

_Defined in [src/utils/payload.ts:69](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/payload.ts#L69)_

Given a TypeID returns the proper [PayloadBase](utils_payload.payloadbase).

**Parameters:**

| Name      | Type   |
| --------- | ------ |
| `typeID`  | number |
| `...args` | any[]  |

**Returns:** _[PayloadBase](utils_payload.payloadbase)_

---

### `Static` getInstance

▸ **getInstance**(): _[PayloadTypes](utils_payload.payloadtypes)_

_Defined in [src/utils/payload.ts:149](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/payload.ts#L149)_

Returns the [PayloadTypes](utils_payload.payloadtypes) singleton.

**Returns:** _[PayloadTypes](utils_payload.payloadtypes)_
