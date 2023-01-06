# Class: PNGPayload

## Hierarchy

↳ [BINPayload](utils_payload.binpayload)

↳ **PNGPayload**

## Index

### Constructors

- [constructor](utils_payload.pngpayload#constructor)

### Properties

- [payload](utils_payload.pngpayload#protected-payload)
- [typeid](utils_payload.pngpayload#protected-typeid)

### Methods

- [fromBuffer](utils_payload.pngpayload#frombuffer)
- [getContent](utils_payload.pngpayload#getcontent)
- [getPayload](utils_payload.pngpayload#getpayload)
- [returnType](utils_payload.pngpayload#returntype)
- [toBuffer](utils_payload.pngpayload#tobuffer)
- [typeID](utils_payload.pngpayload#typeid)
- [typeName](utils_payload.pngpayload#typename)

## Constructors

### constructor

\+ **new PNGPayload**(`payload`: any): _[PNGPayload](utils_payload.pngpayload)_

_Inherited from [BINPayload](utils_payload.binpayload).[constructor](utils_payload.binpayload#constructor)_

_Overrides [PayloadBase](utils_payload.payloadbase).[constructor](utils_payload.payloadbase#constructor)_

_Defined in [src/utils/payload.ts:278](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/payload.ts#L278)_

**Parameters:**

| Name      | Type | Default   | Description |
| --------- | ---- | --------- | ----------- |
| `payload` | any  | undefined | Buffer only |

**Returns:** _[PNGPayload](utils_payload.pngpayload)_

## Properties

### `Protected` payload

• **payload**: _Buffer_ = Buffer.alloc(0)

_Inherited from [PayloadBase](utils_payload.payloadbase).[payload](utils_payload.payloadbase#protected-payload)_

_Defined in [src/utils/payload.ts:198](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/payload.ts#L198)_

---

### `Protected` typeid

• **typeid**: _number_ = 19

_Overrides [BINPayload](utils_payload.binpayload).[typeid](utils_payload.binpayload#protected-typeid)_

_Defined in [src/utils/payload.ts:586](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/payload.ts#L586)_

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

▸ **returnType**(): _Buffer_

_Inherited from [BINPayload](utils_payload.binpayload).[returnType](utils_payload.binpayload#returntype)_

_Overrides [PayloadBase](utils_payload.payloadbase).[returnType](utils_payload.payloadbase#abstract-returntype)_

_Defined in [src/utils/payload.ts:276](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/payload.ts#L276)_

Returns a [Buffer](https://github.com/feross/buffer) for the payload.

**Returns:** _Buffer_

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