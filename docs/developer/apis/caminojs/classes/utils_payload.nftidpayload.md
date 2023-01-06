# Class: NFTIDPayload

Class for payloads representing NFTIDs (UTXOIDs in an NFT context).

## Hierarchy

↳ [UTXOIDPayload](utils_payload.utxoidpayload)

↳ **NFTIDPayload**

## Index

### Constructors

- [constructor](utils_payload.nftidpayload#constructor)

### Properties

- [payload](utils_payload.nftidpayload#protected-payload)
- [typeid](utils_payload.nftidpayload#protected-typeid)

### Methods

- [fromBuffer](utils_payload.nftidpayload#frombuffer)
- [getContent](utils_payload.nftidpayload#getcontent)
- [getPayload](utils_payload.nftidpayload#getpayload)
- [returnType](utils_payload.nftidpayload#returntype)
- [toBuffer](utils_payload.nftidpayload#tobuffer)
- [typeID](utils_payload.nftidpayload#typeid)
- [typeName](utils_payload.nftidpayload#typename)

## Constructors

### constructor

\+ **new NFTIDPayload**(`payload`: any): _[NFTIDPayload](utils_payload.nftidpayload)_

_Inherited from [cb58EncodedPayload](utils_payload.cb58encodedpayload).[constructor](utils_payload.cb58encodedpayload#constructor)_

_Overrides [PayloadBase](utils_payload.payloadbase).[constructor](utils_payload.payloadbase#constructor)_

_Defined in [src/utils/payload.ts:499](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/payload.ts#L499)_

**Parameters:**

| Name      | Type | Default   | Description                   |
| --------- | ---- | --------- | ----------------------------- |
| `payload` | any  | undefined | Buffer or cb58 encoded string |

**Returns:** _[NFTIDPayload](utils_payload.nftidpayload)_

## Properties

### `Protected` payload

• **payload**: _Buffer_ = Buffer.alloc(0)

_Inherited from [PayloadBase](utils_payload.payloadbase).[payload](utils_payload.payloadbase#protected-payload)_

_Defined in [src/utils/payload.ts:198](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/payload.ts#L198)_

---

### `Protected` typeid

• **typeid**: _number_ = 12

_Overrides [UTXOIDPayload](utils_payload.utxoidpayload).[typeid](utils_payload.utxoidpayload#protected-typeid)_

_Defined in [src/utils/payload.ts:538](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/payload.ts#L538)_

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

_Inherited from [cb58EncodedPayload](utils_payload.cb58encodedpayload).[returnType](utils_payload.cb58encodedpayload#returntype)_

_Overrides [PayloadBase](utils_payload.payloadbase).[returnType](utils_payload.payloadbase#abstract-returntype)_

_Defined in [src/utils/payload.ts:497](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/payload.ts#L497)_

Returns a bintools.cb58Encoded string for the payload.

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
