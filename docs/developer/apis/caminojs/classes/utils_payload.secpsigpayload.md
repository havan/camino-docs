# Class: SECPSIGPayload

Class for payloads representing secp256k1 signatures.
convention: secp256k1 signature (130 bytes)

## Hierarchy

↳ [B58STRPayload](utils_payload.b58strpayload)

↳ **SECPSIGPayload**

## Index

### Constructors

- [constructor](utils_payload.secpsigpayload#constructor)

### Properties

- [payload](utils_payload.secpsigpayload#protected-payload)
- [typeid](utils_payload.secpsigpayload#protected-typeid)

### Methods

- [fromBuffer](utils_payload.secpsigpayload#frombuffer)
- [getContent](utils_payload.secpsigpayload#getcontent)
- [getPayload](utils_payload.secpsigpayload#getpayload)
- [returnType](utils_payload.secpsigpayload#returntype)
- [toBuffer](utils_payload.secpsigpayload#tobuffer)
- [typeID](utils_payload.secpsigpayload#typeid)
- [typeName](utils_payload.secpsigpayload#typename)

## Constructors

### constructor

\+ **new SECPSIGPayload**(`payload`: any): _[SECPSIGPayload](utils_payload.secpsigpayload)_

_Inherited from [B58STRPayload](utils_payload.b58strpayload).[constructor](utils_payload.b58strpayload#constructor)_

_Overrides [PayloadBase](utils_payload.payloadbase).[constructor](utils_payload.payloadbase#constructor)_

_Defined in [src/utils/payload.ts:359](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/payload.ts#L359)_

**Parameters:**

| Name      | Type | Default   | Description                   |
| --------- | ---- | --------- | ----------------------------- |
| `payload` | any  | undefined | Buffer or cb58 encoded string |

**Returns:** _[SECPSIGPayload](utils_payload.secpsigpayload)_

## Properties

### `Protected` payload

• **payload**: _Buffer_ = Buffer.alloc(0)

_Inherited from [PayloadBase](utils_payload.payloadbase).[payload](utils_payload.payloadbase#protected-payload)_

_Defined in [src/utils/payload.ts:198](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/payload.ts#L198)_

---

### `Protected` typeid

• **typeid**: _number_ = 16

_Overrides [B58STRPayload](utils_payload.b58strpayload).[typeid](utils_payload.b58strpayload#protected-typeid)_

_Defined in [src/utils/payload.ts:567](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/payload.ts#L567)_

## Methods

### fromBuffer

▸ **fromBuffer**(`bytes`: Buffer, `offset`: number): _number_

_Inherited from [PayloadBase](utils_payload.payloadbase).[fromBuffer](utils_payload.payloadbase#frombuffer)_

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

_Inherited from [PayloadBase](utils_payload.payloadbase).[getContent](utils_payload.payloadbase#getcontent)_

_Defined in [src/utils/payload.ts:218](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/payload.ts#L218)_

Returns the payload content (minus typeID).

**Returns:** _Buffer_

---

### getPayload

▸ **getPayload**(): _Buffer_

_Inherited from [PayloadBase](utils_payload.payloadbase).[getPayload](utils_payload.payloadbase#getpayload)_

_Defined in [src/utils/payload.ts:226](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/payload.ts#L226)_

Returns the payload (with typeID).

**Returns:** _Buffer_

---

### returnType

▸ **returnType**(): _string_

_Inherited from [B58STRPayload](utils_payload.b58strpayload).[returnType](utils_payload.b58strpayload#returntype)_

_Overrides [PayloadBase](utils_payload.payloadbase).[returnType](utils_payload.payloadbase#abstract-returntype)_

_Defined in [src/utils/payload.ts:357](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/payload.ts#L357)_

Returns a base58 string for the payload.

**Returns:** _string_

---

### toBuffer

▸ **toBuffer**(): _Buffer_

_Inherited from [PayloadBase](utils_payload.payloadbase).[toBuffer](utils_payload.payloadbase#tobuffer)_

_Defined in [src/utils/payload.ts:251](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/payload.ts#L251)_

Encodes the payload as a [Buffer](https://github.com/feross/buffer) including 4 bytes for the length and TypeID.

**Returns:** _Buffer_

---

### typeID

▸ **typeID**(): _number_

_Inherited from [PayloadBase](utils_payload.payloadbase).[typeID](utils_payload.payloadbase#typeid)_

_Defined in [src/utils/payload.ts:204](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/payload.ts#L204)_

Returns the TypeID for the payload.

**Returns:** _number_

---

### typeName

▸ **typeName**(): _string_

_Inherited from [PayloadBase](utils_payload.payloadbase).[typeName](utils_payload.payloadbase#typename)_

_Defined in [src/utils/payload.ts:211](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/payload.ts#L211)_

Returns the string name for the payload's type.

**Returns:** _string_
