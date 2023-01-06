# Class: PayloadBase

Base class for payloads.

## Hierarchy

- **PayloadBase**

  ↳ [BINPayload](utils_payload.binpayload)

  ↳ [UTF8Payload](utils_payload.utf8payload)

  ↳ [HEXSTRPayload](utils_payload.hexstrpayload)

  ↳ [B58STRPayload](utils_payload.b58strpayload)

  ↳ [B64STRPayload](utils_payload.b64strpayload)

  ↳ [BIGNUMPayload](utils_payload.bignumpayload)

  ↳ [ChainAddressPayload](utils_payload.chainaddresspayload)

  ↳ [cb58EncodedPayload](utils_payload.cb58encodedpayload)

  ↳ [JSONPayload](utils_payload.jsonpayload)

## Index

### Constructors

- [constructor](utils_payload.payloadbase#constructor)

### Properties

- [payload](utils_payload.payloadbase#protected-payload)
- [typeid](utils_payload.payloadbase#protected-typeid)

### Methods

- [fromBuffer](utils_payload.payloadbase#frombuffer)
- [getContent](utils_payload.payloadbase#getcontent)
- [getPayload](utils_payload.payloadbase#getpayload)
- [returnType](utils_payload.payloadbase#abstract-returntype)
- [toBuffer](utils_payload.payloadbase#tobuffer)
- [typeID](utils_payload.payloadbase#typeid)
- [typeName](utils_payload.payloadbase#typename)

## Constructors

### constructor

\+ **new PayloadBase**(): _[PayloadBase](utils_payload.payloadbase)_

_Defined in [src/utils/payload.ts:262](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/payload.ts#L262)_

**Returns:** _[PayloadBase](utils_payload.payloadbase)_

## Properties

### `Protected` payload

• **payload**: _Buffer_ = Buffer.alloc(0)

_Defined in [src/utils/payload.ts:198](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/payload.ts#L198)_

---

### `Protected` typeid

• **typeid**: _number_ = undefined

_Defined in [src/utils/payload.ts:199](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/payload.ts#L199)_

## Methods

### fromBuffer

▸ **fromBuffer**(`bytes`: Buffer, `offset`: number): _number_

_Defined in [src/utils/payload.ts:236](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/payload.ts#L236)_

Decodes the payload as a [Buffer](https://github.com/feross/buffer) including 4 bytes for the length and TypeID.

**Parameters:**

| Name     | Type   | Default |
| -------- | ------ | ------- |
| `bytes`  | Buffer | -       |
| `offset` | number | 0       |

**Returns:** _number_

---

### getContent

▸ **getContent**(): _Buffer_

_Defined in [src/utils/payload.ts:218](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/payload.ts#L218)_

Returns the payload content (minus typeID).

**Returns:** _Buffer_

---

### getPayload

▸ **getPayload**(): _Buffer_

_Defined in [src/utils/payload.ts:226](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/payload.ts#L226)_

Returns the payload (with typeID).

**Returns:** _Buffer_

---

### `Abstract` returnType

▸ **returnType**(...`args`: any): _any_

_Defined in [src/utils/payload.ts:262](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/payload.ts#L262)_

Returns the expected type for the payload.

**Parameters:**

| Name      | Type |
| --------- | ---- |
| `...args` | any  |

**Returns:** _any_

---

### toBuffer

▸ **toBuffer**(): _Buffer_

_Defined in [src/utils/payload.ts:251](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/payload.ts#L251)_

Encodes the payload as a [Buffer](https://github.com/feross/buffer) including 4 bytes for the length and TypeID.

**Returns:** _Buffer_

---

### typeID

▸ **typeID**(): _number_

_Defined in [src/utils/payload.ts:204](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/payload.ts#L204)_

Returns the TypeID for the payload.

**Returns:** _number_

---

### typeName

▸ **typeName**(): _string_

_Defined in [src/utils/payload.ts:211](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/payload.ts#L211)_

Returns the string name for the payload's type.

**Returns:** _string_
