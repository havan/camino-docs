# Class: CCHAINADDRPayload

Class for payloads representing C-Chain addresses.

## Hierarchy

↳ [ChainAddressPayload](utils_payload.chainaddresspayload)

↳ **CCHAINADDRPayload**

## Index

### Constructors

- [constructor](utils_payload.cchainaddrpayload#constructor)

### Properties

- [chainid](utils_payload.cchainaddrpayload#protected-chainid)
- [payload](utils_payload.cchainaddrpayload#protected-payload)
- [typeid](utils_payload.cchainaddrpayload#protected-typeid)

### Methods

- [fromBuffer](utils_payload.cchainaddrpayload#frombuffer)
- [getContent](utils_payload.cchainaddrpayload#getcontent)
- [getPayload](utils_payload.cchainaddrpayload#getpayload)
- [returnChainID](utils_payload.cchainaddrpayload#returnchainid)
- [returnType](utils_payload.cchainaddrpayload#returntype)
- [toBuffer](utils_payload.cchainaddrpayload#tobuffer)
- [typeID](utils_payload.cchainaddrpayload#typeid)
- [typeName](utils_payload.cchainaddrpayload#typename)

## Constructors

### constructor

\+ **new CCHAINADDRPayload**(`payload`: any, `hrp?`: string): _[CCHAINADDRPayload](utils_payload.cchainaddrpayload)_

_Inherited from [ChainAddressPayload](utils_payload.chainaddresspayload).[constructor](utils_payload.chainaddresspayload#constructor)_

_Overrides [PayloadBase](utils_payload.payloadbase).[constructor](utils_payload.payloadbase#constructor)_

_Defined in [src/utils/payload.ts:448](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/payload.ts#L448)_

**Parameters:**

| Name      | Type   | Default   | Description              |
| --------- | ------ | --------- | ------------------------ |
| `payload` | any    | undefined | Buffer or address string |
| `hrp?`    | string | -         | -                        |

**Returns:** _[CCHAINADDRPayload](utils_payload.cchainaddrpayload)_

## Properties

### `Protected` chainid

• **chainid**: _string_ = "C"

_Overrides [ChainAddressPayload](utils_payload.chainaddresspayload).[chainid](utils_payload.chainaddresspayload#protected-chainid)_

_Defined in [src/utils/payload.ts:487](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/payload.ts#L487)_

---

### `Protected` payload

• **payload**: _Buffer_ = Buffer.alloc(0)

_Inherited from [PayloadBase](utils_payload.payloadbase).[payload](utils_payload.payloadbase#protected-payload)_

_Defined in [src/utils/payload.ts:198](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/payload.ts#L198)_

---

### `Protected` typeid

• **typeid**: _number_ = 8

_Overrides [ChainAddressPayload](utils_payload.chainaddresspayload).[typeid](utils_payload.chainaddresspayload#protected-typeid)_

_Defined in [src/utils/payload.ts:486](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/payload.ts#L486)_

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

### returnChainID

▸ **returnChainID**(): _string_

_Inherited from [ChainAddressPayload](utils_payload.chainaddresspayload).[returnChainID](utils_payload.chainaddresspayload#returnchainid)_

_Defined in [src/utils/payload.ts:438](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/payload.ts#L438)_

Returns the chainid.

**Returns:** _string_

---

### returnType

▸ **returnType**(`hrp`: string): _string_

_Inherited from [ChainAddressPayload](utils_payload.chainaddresspayload).[returnType](utils_payload.chainaddresspayload#returntype)_

_Overrides [PayloadBase](utils_payload.payloadbase).[returnType](utils_payload.payloadbase#abstract-returntype)_

_Defined in [src/utils/payload.ts:445](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/payload.ts#L445)_

Returns an address string for the payload.

**Parameters:**

| Name  | Type   |
| ----- | ------ |
| `hrp` | string |

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
