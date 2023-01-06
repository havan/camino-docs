# Class: Signature

Signature for a [Tx](api_evm_transactions.tx)

## Hierarchy

↳ [NBytes](common_nbytes.nbytes)

↳ **Signature**

## Index

### Constructors

- [constructor](common_signature.signature#constructor)

### Properties

- [\_codecID](common_signature.signature#protected-_codecid)
- [\_typeID](common_signature.signature#protected-_typeid)
- [\_typeName](common_signature.signature#protected-_typename)
- [bsize](common_signature.signature#protected-bsize)
- [bytes](common_signature.signature#protected-bytes)

### Methods

- [clone](common_signature.signature#clone)
- [create](common_signature.signature#create)
- [deserialize](common_signature.signature#deserialize)
- [fromBuffer](common_signature.signature#frombuffer)
- [fromString](common_signature.signature#fromstring)
- [getCodecID](common_signature.signature#getcodecid)
- [getSize](common_signature.signature#getsize)
- [getTypeID](common_signature.signature#gettypeid)
- [getTypeName](common_signature.signature#gettypename)
- [sanitizeObject](common_signature.signature#sanitizeobject)
- [serialize](common_signature.signature#serialize)
- [toBuffer](common_signature.signature#tobuffer)
- [toString](common_signature.signature#tostring)

## Constructors

### constructor

\+ **new Signature**(): _[Signature](common_signature.signature)_

_Defined in [src/common/credentials.ts:98](https://github.com/chain4travel/caminojs/blob/3883166/src/common/credentials.ts#L98)_

Signature for a [Tx](api_evm_transactions.tx)

**Returns:** _[Signature](common_signature.signature)_

## Properties

### `Protected` \_codecID

• **\_codecID**: _number_ = undefined

_Inherited from [SigIdx](common_signature.sigidx).[\_codecID](common_signature.sigidx#protected-_codecid)_

_Defined in [src/utils/serialization.ts:51](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/serialization.ts#L51)_

---

### `Protected` \_typeID

• **\_typeID**: _any_ = undefined

_Overrides [NBytes](common_nbytes.nbytes).[\_typeID](common_nbytes.nbytes#protected-_typeid)_

_Defined in [src/common/credentials.ts:83](https://github.com/chain4travel/caminojs/blob/3883166/src/common/credentials.ts#L83)_

---

### `Protected` \_typeName

• **\_typeName**: _string_ = "Signature"

_Overrides [NBytes](common_nbytes.nbytes).[\_typeName](common_nbytes.nbytes#protected-_typename)_

_Defined in [src/common/credentials.ts:82](https://github.com/chain4travel/caminojs/blob/3883166/src/common/credentials.ts#L82)_

---

### `Protected` bsize

• **bsize**: _number_ = 65

_Overrides [NBytes](common_nbytes.nbytes).[bsize](common_nbytes.nbytes#protected-bsize)_

_Defined in [src/common/credentials.ts:88](https://github.com/chain4travel/caminojs/blob/3883166/src/common/credentials.ts#L88)_

---

### `Protected` bytes

• **bytes**: _Buffer‹›_ = Buffer.alloc(65)

_Overrides [NBytes](common_nbytes.nbytes).[bytes](common_nbytes.nbytes#protected-bytes)_

_Defined in [src/common/credentials.ts:87](https://github.com/chain4travel/caminojs/blob/3883166/src/common/credentials.ts#L87)_

## Methods

### clone

▸ **clone**(): _this_

_Overrides [NBytes](common_nbytes.nbytes).[clone](common_nbytes.nbytes#abstract-clone)_

_Defined in [src/common/credentials.ts:90](https://github.com/chain4travel/caminojs/blob/3883166/src/common/credentials.ts#L90)_

**Returns:** _this_

---

### create

▸ **create**(...`args`: any[]): _this_

_Overrides [NBytes](common_nbytes.nbytes).[create](common_nbytes.nbytes#abstract-create)_

_Defined in [src/common/credentials.ts:96](https://github.com/chain4travel/caminojs/blob/3883166/src/common/credentials.ts#L96)_

**Parameters:**

| Name      | Type  |
| --------- | ----- |
| `...args` | any[] |

**Returns:** _this_

---

### deserialize

▸ **deserialize**(`fields`: object, `encoding`: [SerializedEncoding](../modules/utils_serialization#serializedencoding)): _void_

_Inherited from [Signature](common_signature.signature).[deserialize](common_signature.signature#deserialize)_

_Overrides [StandardParseableInput](common_inputs.standardparseableinput).[deserialize](common_inputs.standardparseableinput#deserialize)_

_Defined in [src/common/nbytes.ts:52](https://github.com/chain4travel/caminojs/blob/3883166/src/common/nbytes.ts#L52)_

**Parameters:**

| Name       | Type                                                                    | Default |
| ---------- | ----------------------------------------------------------------------- | ------- |
| `fields`   | object                                                                  | -       |
| `encoding` | [SerializedEncoding](../modules/utils_serialization#serializedencoding) | "hex"   |

**Returns:** _void_

---

### fromBuffer

▸ **fromBuffer**(`buff`: Buffer, `offset`: number): _number_

_Inherited from [SigIdx](common_signature.sigidx).[fromBuffer](common_signature.sigidx#frombuffer)_

_Defined in [src/common/nbytes.ts:102](https://github.com/chain4travel/caminojs/blob/3883166/src/common/nbytes.ts#L102)_

Takes a [[Buffer]], verifies its length, and stores it.

**Parameters:**

| Name     | Type   | Default |
| -------- | ------ | ------- |
| `buff`   | Buffer | -       |
| `offset` | number | 0       |

**Returns:** _number_

The size of the [Buffer](https://github.com/feross/buffer)

---

### fromString

▸ **fromString**(`b58str`: string): _number_

_Inherited from [SigIdx](common_signature.sigidx).[fromString](common_signature.sigidx#fromstring)_

_Defined in [src/common/nbytes.ts:85](https://github.com/chain4travel/caminojs/blob/3883166/src/common/nbytes.ts#L85)_

Takes a base-58 encoded string, verifies its length, and stores it.

**Parameters:**

| Name     | Type   |
| -------- | ------ |
| `b58str` | string |

**Returns:** _number_

The size of the [Buffer](https://github.com/feross/buffer)

---

### getCodecID

▸ **getCodecID**(): _number_

_Inherited from [SigIdx](common_signature.sigidx).[getCodecID](common_signature.sigidx#getcodecid)_

_Defined in [src/utils/serialization.ts:70](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/serialization.ts#L70)_

Used in serialization. Optional. TypeID is a number for the typeID of object being output.

**Returns:** _number_

---

### getSize

▸ **getSize**(): _number_

_Inherited from [SigIdx](common_signature.sigidx).[getSize](common_signature.sigidx#getsize)_

_Defined in [src/common/nbytes.ts:78](https://github.com/chain4travel/caminojs/blob/3883166/src/common/nbytes.ts#L78)_

Returns the length of the [Buffer](https://github.com/feross/buffer).

**Returns:** _number_

The exact length requirement of this class

---

### getTypeID

▸ **getTypeID**(): _number_

_Inherited from [SigIdx](common_signature.sigidx).[getTypeID](common_signature.sigidx#gettypeid)_

_Defined in [src/utils/serialization.ts:63](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/serialization.ts#L63)_

Used in serialization. Optional. TypeID is a number for the typeID of object being output.

**Returns:** _number_

---

### getTypeName

▸ **getTypeName**(): _string_

_Inherited from [SigIdx](common_signature.sigidx).[getTypeName](common_signature.sigidx#gettypename)_

_Defined in [src/utils/serialization.ts:56](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/serialization.ts#L56)_

Used in serialization. TypeName is a string name for the type of object being output.

**Returns:** _string_

---

### sanitizeObject

▸ **sanitizeObject**(`obj`: object): _object_

_Inherited from [SigIdx](common_signature.sigidx).[sanitizeObject](common_signature.sigidx#sanitizeobject)_

_Defined in [src/utils/serialization.ts:77](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/serialization.ts#L77)_

Sanitize to prevent cross scripting attacks.

**Parameters:**

| Name  | Type   |
| ----- | ------ |
| `obj` | object |

**Returns:** _object_

---

### serialize

▸ **serialize**(`encoding`: [SerializedEncoding](../modules/utils_serialization#serializedencoding)): _object_

_Inherited from [Signature](common_signature.signature).[serialize](common_signature.signature#serialize)_

_Overrides [Serializable](utils_serialization.serializable).[serialize](utils_serialization.serializable#serialize)_

_Defined in [src/common/nbytes.ts:32](https://github.com/chain4travel/caminojs/blob/3883166/src/common/nbytes.ts#L32)_

**Parameters:**

| Name       | Type                                                                    | Default |
| ---------- | ----------------------------------------------------------------------- | ------- |
| `encoding` | [SerializedEncoding](../modules/utils_serialization#serializedencoding) | "hex"   |

**Returns:** _object_

---

### toBuffer

▸ **toBuffer**(): _Buffer_

_Inherited from [SigIdx](common_signature.sigidx).[toBuffer](common_signature.sigidx#tobuffer)_

_Defined in [src/common/nbytes.ts:124](https://github.com/chain4travel/caminojs/blob/3883166/src/common/nbytes.ts#L124)_

**Returns:** _Buffer_

A reference to the stored [Buffer](https://github.com/feross/buffer)

---

### toString

▸ **toString**(): _string_

_Inherited from [SigIdx](common_signature.sigidx).[toString](common_signature.sigidx#tostring)_

_Defined in [src/common/nbytes.ts:131](https://github.com/chain4travel/caminojs/blob/3883166/src/common/nbytes.ts#L131)_

**Returns:** _string_

A base-58 string of the stored [Buffer](https://github.com/feross/buffer)
