# Class: UTXOID

Class for representing a UTXOID used in [[TransferableOp]] types

## Hierarchy

↳ [NBytes](common_nbytes.nbytes)

↳ **UTXOID**

## Index

### Constructors

- [constructor](api_avm_operations.utxoid#constructor)

### Properties

- [\_codecID](api_avm_operations.utxoid#protected-_codecid)
- [\_typeID](api_avm_operations.utxoid#protected-_typeid)
- [\_typeName](api_avm_operations.utxoid#protected-_typename)
- [bsize](api_avm_operations.utxoid#protected-bsize)
- [bytes](api_avm_operations.utxoid#protected-bytes)

### Methods

- [clone](api_avm_operations.utxoid#clone)
- [create](api_avm_operations.utxoid#create)
- [deserialize](api_avm_operations.utxoid#deserialize)
- [fromBuffer](api_avm_operations.utxoid#frombuffer)
- [fromString](api_avm_operations.utxoid#fromstring)
- [getCodecID](api_avm_operations.utxoid#getcodecid)
- [getSize](api_avm_operations.utxoid#getsize)
- [getTypeID](api_avm_operations.utxoid#gettypeid)
- [getTypeName](api_avm_operations.utxoid#gettypename)
- [sanitizeObject](api_avm_operations.utxoid#sanitizeobject)
- [serialize](api_avm_operations.utxoid#serialize)
- [toBuffer](api_avm_operations.utxoid#tobuffer)
- [toString](api_avm_operations.utxoid#tostring)
- [comparator](api_avm_operations.utxoid#static-comparator)

## Constructors

### constructor

\+ **new UTXOID**(): _[UTXOID](api_avm_operations.utxoid)_

_Defined in [src/apis/avm/ops.ts:839](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L839)_

Class for representing a UTXOID used in [[TransferableOp]] types

**Returns:** _[UTXOID](api_avm_operations.utxoid)_

## Properties

### `Protected` \_codecID

• **\_codecID**: _number_ = undefined

_Inherited from [SigIdx](common_signature.sigidx).[\_codecID](common_signature.sigidx#protected-_codecid)_

_Defined in [src/utils/serialization.ts:51](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/serialization.ts#L51)_

---

### `Protected` \_typeID

• **\_typeID**: _any_ = undefined

_Overrides [NBytes](common_nbytes.nbytes).[\_typeID](common_nbytes.nbytes#protected-_typeid)_

_Defined in [src/apis/avm/ops.ts:778](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L778)_

---

### `Protected` \_typeName

• **\_typeName**: _string_ = "UTXOID"

_Overrides [NBytes](common_nbytes.nbytes).[\_typeName](common_nbytes.nbytes#protected-_typename)_

_Defined in [src/apis/avm/ops.ts:777](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L777)_

---

### `Protected` bsize

• **bsize**: _number_ = 36

_Overrides [NBytes](common_nbytes.nbytes).[bsize](common_nbytes.nbytes#protected-bsize)_

_Defined in [src/apis/avm/ops.ts:783](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L783)_

---

### `Protected` bytes

• **bytes**: _Buffer‹›_ = Buffer.alloc(36)

_Overrides [NBytes](common_nbytes.nbytes).[bytes](common_nbytes.nbytes#protected-bytes)_

_Defined in [src/apis/avm/ops.ts:782](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L782)_

## Methods

### clone

▸ **clone**(): _this_

_Overrides [NBytes](common_nbytes.nbytes).[clone](common_nbytes.nbytes#abstract-clone)_

_Defined in [src/apis/avm/ops.ts:831](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L831)_

**Returns:** _this_

---

### create

▸ **create**(...`args`: any[]): _this_

_Overrides [NBytes](common_nbytes.nbytes).[create](common_nbytes.nbytes#abstract-create)_

_Defined in [src/apis/avm/ops.ts:837](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L837)_

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

▸ **fromString**(`utxoid`: string): _number_

_Overrides [SigIdx](common_signature.sigidx).[fromString](common_signature.sigidx#fromstring)_

_Defined in [src/apis/avm/ops.ts:807](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L807)_

Takes a base-58 string containing an [UTXOID](api_avm_operations.utxoid), parses it, populates the class, and returns the length of the UTXOID in bytes.

**Parameters:**

| Name     | Type   |
| -------- | ------ |
| `utxoid` | string |

**Returns:** _number_

The length of the raw [UTXOID](api_avm_operations.utxoid)

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

_Defined in [src/apis/avm/ops.ts:796](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L796)_

Returns a base-58 representation of the [UTXOID](api_avm_operations.utxoid).

**Returns:** _string_

---

### `Static` comparator

▸ **comparator**(): _function_

_Defined in [src/apis/avm/ops.ts:788](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L788)_

Returns a function used to sort an array of [UTXOID](api_avm_operations.utxoid)s

**Returns:** _function_

▸ (`a`: [UTXOID](api_avm_operations.utxoid), `b`: [UTXOID](api_avm_operations.utxoid)): _1 | -1 | 0_

**Parameters:**

| Name | Type                                |
| ---- | ----------------------------------- |
| `a`  | [UTXOID](api_avm_operations.utxoid) |
| `b`  | [UTXOID](api_avm_operations.utxoid) |
