# Class: NBytes

Abstract class that implements basic functionality for managing a
[Buffer](https://github.com/feross/buffer) of an exact length.

Create a class that extends this one and override bsize to make it validate for exactly
the correct length.

## Hierarchy

- [Serializable](utils_serialization.serializable)

  ↳ **NBytes**

  ↳ [SigIdx](common_signature.sigidx)

  ↳ [Signature](common_signature.signature)

  ↳ [Address](common_output.address)

  ↳ [UTXOID](api_avm_operations.utxoid)

## Index

### Properties

- [\_codecID](common_nbytes.nbytes#protected-_codecid)
- [\_typeID](common_nbytes.nbytes#protected-_typeid)
- [\_typeName](common_nbytes.nbytes#protected-_typename)
- [bsize](common_nbytes.nbytes#protected-bsize)
- [bytes](common_nbytes.nbytes#protected-bytes)

### Methods

- [clone](common_nbytes.nbytes#abstract-clone)
- [create](common_nbytes.nbytes#abstract-create)
- [deserialize](common_nbytes.nbytes#deserialize)
- [fromBuffer](common_nbytes.nbytes#frombuffer)
- [fromString](common_nbytes.nbytes#fromstring)
- [getCodecID](common_nbytes.nbytes#getcodecid)
- [getSize](common_nbytes.nbytes#getsize)
- [getTypeID](common_nbytes.nbytes#gettypeid)
- [getTypeName](common_nbytes.nbytes#gettypename)
- [sanitizeObject](common_nbytes.nbytes#sanitizeobject)
- [serialize](common_nbytes.nbytes#serialize)
- [toBuffer](common_nbytes.nbytes#tobuffer)
- [toString](common_nbytes.nbytes#tostring)

## Properties

### `Protected` \_codecID

• **\_codecID**: _number_ = undefined

_Inherited from [SigIdx](common_signature.sigidx).[\_codecID](common_signature.sigidx#protected-_codecid)_

_Defined in [src/utils/serialization.ts:51](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/serialization.ts#L51)_

---

### `Protected` \_typeID

• **\_typeID**: _any_ = undefined

_Overrides [Serializable](utils_serialization.serializable).[\_typeID](utils_serialization.serializable#protected-_typeid)_

_Defined in [src/common/nbytes.ts:30](https://github.com/chain4travel/caminojs/blob/3883166/src/common/nbytes.ts#L30)_

---

### `Protected` \_typeName

• **\_typeName**: _string_ = "NBytes"

_Overrides [Serializable](utils_serialization.serializable).[\_typeName](utils_serialization.serializable#protected-_typename)_

_Defined in [src/common/nbytes.ts:29](https://github.com/chain4travel/caminojs/blob/3883166/src/common/nbytes.ts#L29)_

---

### `Protected` bsize

• **bsize**: _number_

_Defined in [src/common/nbytes.ts:71](https://github.com/chain4travel/caminojs/blob/3883166/src/common/nbytes.ts#L71)_

---

### `Protected` bytes

• **bytes**: _Buffer_

_Defined in [src/common/nbytes.ts:70](https://github.com/chain4travel/caminojs/blob/3883166/src/common/nbytes.ts#L70)_

## Methods

### `Abstract` clone

▸ **clone**(): _this_

_Defined in [src/common/nbytes.ts:135](https://github.com/chain4travel/caminojs/blob/3883166/src/common/nbytes.ts#L135)_

**Returns:** _this_

---

### `Abstract` create

▸ **create**(...`args`: any[]): _this_

_Defined in [src/common/nbytes.ts:136](https://github.com/chain4travel/caminojs/blob/3883166/src/common/nbytes.ts#L136)_

**Parameters:**

| Name      | Type  |
| --------- | ----- |
| `...args` | any[] |

**Returns:** _this_

---

### deserialize

▸ **deserialize**(`fields`: object, `encoding`: [SerializedEncoding](../modules/utils_serialization#serializedencoding)): _void_

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

_Defined in [src/common/nbytes.ts:124](https://github.com/chain4travel/caminojs/blob/3883166/src/common/nbytes.ts#L124)_

**Returns:** _Buffer_

A reference to the stored [Buffer](https://github.com/feross/buffer)

---

### toString

▸ **toString**(): _string_

_Defined in [src/common/nbytes.ts:131](https://github.com/chain4travel/caminojs/blob/3883166/src/common/nbytes.ts#L131)_

**Returns:** _string_

A base-58 string of the stored [Buffer](https://github.com/feross/buffer)
