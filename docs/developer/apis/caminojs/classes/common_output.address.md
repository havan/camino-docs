# Class: Address

Class for representing an address used in [Output](common_output.output) types

## Hierarchy

↳ [NBytes](common_nbytes.nbytes)

↳ **Address**

## Index

### Constructors

- [constructor](common_output.address#constructor)

### Properties

- [\_codecID](common_output.address#protected-_codecid)
- [\_typeID](common_output.address#protected-_typeid)
- [\_typeName](common_output.address#protected-_typename)
- [bsize](common_output.address#protected-bsize)
- [bytes](common_output.address#protected-bytes)

### Methods

- [clone](common_output.address#clone)
- [create](common_output.address#create)
- [deserialize](common_output.address#deserialize)
- [fromBuffer](common_output.address#frombuffer)
- [fromString](common_output.address#fromstring)
- [getCodecID](common_output.address#getcodecid)
- [getSize](common_output.address#getsize)
- [getTypeID](common_output.address#gettypeid)
- [getTypeName](common_output.address#gettypename)
- [sanitizeObject](common_output.address#sanitizeobject)
- [serialize](common_output.address#serialize)
- [toBuffer](common_output.address#tobuffer)
- [toString](common_output.address#tostring)
- [comparator](common_output.address#static-comparator)

## Constructors

### constructor

\+ **new Address**(): _[Address](common_output.address)_

_Defined in [src/common/output.ts:90](https://github.com/chain4travel/caminojs/blob/3883166/src/common/output.ts#L90)_

Class for representing an address used in [Output](common_output.output) types

**Returns:** _[Address](common_output.address)_

## Properties

### `Protected` \_codecID

• **\_codecID**: _number_ = undefined

_Inherited from [SigIdx](common_signature.sigidx).[\_codecID](common_signature.sigidx#protected-_codecid)_

_Defined in [src/utils/serialization.ts:51](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/serialization.ts#L51)_

---

### `Protected` \_typeID

• **\_typeID**: _any_ = undefined

_Overrides [NBytes](common_nbytes.nbytes).[\_typeID](common_nbytes.nbytes#protected-_typeid)_

_Defined in [src/common/output.ts:29](https://github.com/chain4travel/caminojs/blob/3883166/src/common/output.ts#L29)_

---

### `Protected` \_typeName

• **\_typeName**: _string_ = "Address"

_Overrides [NBytes](common_nbytes.nbytes).[\_typeName](common_nbytes.nbytes#protected-_typename)_

_Defined in [src/common/output.ts:28](https://github.com/chain4travel/caminojs/blob/3883166/src/common/output.ts#L28)_

---

### `Protected` bsize

• **bsize**: _number_ = 20

_Overrides [NBytes](common_nbytes.nbytes).[bsize](common_nbytes.nbytes#protected-bsize)_

_Defined in [src/common/output.ts:34](https://github.com/chain4travel/caminojs/blob/3883166/src/common/output.ts#L34)_

---

### `Protected` bytes

• **bytes**: _Buffer‹›_ = Buffer.alloc(20)

_Overrides [NBytes](common_nbytes.nbytes).[bytes](common_nbytes.nbytes#protected-bytes)_

_Defined in [src/common/output.ts:33](https://github.com/chain4travel/caminojs/blob/3883166/src/common/output.ts#L33)_

## Methods

### clone

▸ **clone**(): _this_

_Overrides [NBytes](common_nbytes.nbytes).[clone](common_nbytes.nbytes#abstract-clone)_

_Defined in [src/common/output.ts:82](https://github.com/chain4travel/caminojs/blob/3883166/src/common/output.ts#L82)_

**Returns:** _this_

---

### create

▸ **create**(...`args`: any[]): _this_

_Overrides [NBytes](common_nbytes.nbytes).[create](common_nbytes.nbytes#abstract-create)_

_Defined in [src/common/output.ts:88](https://github.com/chain4travel/caminojs/blob/3883166/src/common/output.ts#L88)_

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

▸ **fromString**(`addr`: string): _number_

_Overrides [SigIdx](common_signature.sigidx).[fromString](common_signature.sigidx#fromstring)_

_Defined in [src/common/output.ts:58](https://github.com/chain4travel/caminojs/blob/3883166/src/common/output.ts#L58)_

Takes a base-58 string containing an [Address](common_output.address), parses it, populates the class, and returns the length of the Address in bytes.

**Parameters:**

| Name   | Type   |
| ------ | ------ |
| `addr` | string |

**Returns:** _number_

The length of the raw [Address](common_output.address)

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

_Overrides [SigIdx](common_signature.sigidx).[toString](common_signature.sigidx#tostring)_

_Defined in [src/common/output.ts:47](https://github.com/chain4travel/caminojs/blob/3883166/src/common/output.ts#L47)_

Returns a base-58 representation of the [Address](common_output.address).

**Returns:** _string_

---

### `Static` comparator

▸ **comparator**(): _function_

_Defined in [src/common/output.ts:39](https://github.com/chain4travel/caminojs/blob/3883166/src/common/output.ts#L39)_

Returns a function used to sort an array of [Address](common_output.address)es

**Returns:** _function_

▸ (`a`: [Address](common_output.address), `b`: [Address](common_output.address)): _1 | -1 | 0_

**Parameters:**

| Name | Type                             |
| ---- | -------------------------------- |
| `a`  | [Address](common_output.address) |
| `b`  | [Address](common_output.address) |
