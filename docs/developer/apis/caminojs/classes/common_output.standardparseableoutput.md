# Class: StandardParseableOutput

## Hierarchy

- [Serializable](utils_serialization.serializable)

  ↳ **StandardParseableOutput**

  ↳ [StandardTransferableOutput](common_output.standardtransferableoutput)

  ↳ [ParseableOutput](api_platformvm_outputs.parseableoutput)

## Index

### Constructors

- [constructor](common_output.standardparseableoutput#constructor)

### Properties

- [\_codecID](common_output.standardparseableoutput#protected-_codecid)
- [\_typeID](common_output.standardparseableoutput#protected-_typeid)
- [\_typeName](common_output.standardparseableoutput#protected-_typename)
- [output](common_output.standardparseableoutput#protected-output)

### Methods

- [deserialize](common_output.standardparseableoutput#deserialize)
- [fromBuffer](common_output.standardparseableoutput#abstract-frombuffer)
- [getCodecID](common_output.standardparseableoutput#getcodecid)
- [getOutput](common_output.standardparseableoutput#getoutput)
- [getTypeID](common_output.standardparseableoutput#gettypeid)
- [getTypeName](common_output.standardparseableoutput#gettypename)
- [sanitizeObject](common_output.standardparseableoutput#sanitizeobject)
- [serialize](common_output.standardparseableoutput#serialize)
- [toBuffer](common_output.standardparseableoutput#tobuffer)
- [comparator](common_output.standardparseableoutput#static-comparator)

## Constructors

### constructor

\+ **new StandardParseableOutput**(`output`: [Output](common_output.output)): _[StandardParseableOutput](common_output.standardparseableoutput)_

_Defined in [src/common/output.ts:438](https://github.com/chain4travel/caminojs/blob/3883166/src/common/output.ts#L438)_

Class representing an [ParseableOutput](api_platformvm_outputs.parseableoutput) for a transaction.

**Parameters:**

| Name     | Type                           | Default   | Description                                                                                        |
| -------- | ------------------------------ | --------- | -------------------------------------------------------------------------------------------------- |
| `output` | [Output](common_output.output) | undefined | A number representing the InputID of the [ParseableOutput](api_platformvm_outputs.parseableoutput) |

**Returns:** _[StandardParseableOutput](common_output.standardparseableoutput)_

## Properties

### `Protected` \_codecID

• **\_codecID**: _number_ = undefined

_Inherited from [SigIdx](common_signature.sigidx).[\_codecID](common_signature.sigidx#protected-_codecid)_

_Defined in [src/utils/serialization.ts:51](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/serialization.ts#L51)_

---

### `Protected` \_typeID

• **\_typeID**: _any_ = undefined

_Overrides [Serializable](utils_serialization.serializable).[\_typeID](utils_serialization.serializable#protected-_typeid)_

_Defined in [src/common/output.ts:401](https://github.com/chain4travel/caminojs/blob/3883166/src/common/output.ts#L401)_

---

### `Protected` \_typeName

• **\_typeName**: _string_ = "StandardParseableOutput"

_Overrides [Serializable](utils_serialization.serializable).[\_typeName](utils_serialization.serializable#protected-_typename)_

_Defined in [src/common/output.ts:400](https://github.com/chain4travel/caminojs/blob/3883166/src/common/output.ts#L400)_

---

### `Protected` output

• **output**: _[Output](common_output.output)_

_Defined in [src/common/output.ts:411](https://github.com/chain4travel/caminojs/blob/3883166/src/common/output.ts#L411)_

## Methods

### deserialize

▸ **deserialize**(`fields`: object, `encoding?`: [SerializedEncoding](../modules/utils_serialization#serializedencoding)): _void_

_Inherited from [StandardParseableInput](common_inputs.standardparseableinput).[deserialize](common_inputs.standardparseableinput#deserialize)_

_Defined in [src/utils/serialization.ts:97](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/serialization.ts#L97)_

**Parameters:**

| Name        | Type                                                                    |
| ----------- | ----------------------------------------------------------------------- |
| `fields`    | object                                                                  |
| `encoding?` | [SerializedEncoding](../modules/utils_serialization#serializedencoding) |

**Returns:** _void_

---

### `Abstract` fromBuffer

▸ **fromBuffer**(`bytes`: Buffer, `offset?`: number): _number_

_Defined in [src/common/output.ts:430](https://github.com/chain4travel/caminojs/blob/3883166/src/common/output.ts#L430)_

**Parameters:**

| Name      | Type   |
| --------- | ------ |
| `bytes`   | Buffer |
| `offset?` | number |

**Returns:** _number_

---

### getCodecID

▸ **getCodecID**(): _number_

_Inherited from [SigIdx](common_signature.sigidx).[getCodecID](common_signature.sigidx#getcodecid)_

_Defined in [src/utils/serialization.ts:70](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/serialization.ts#L70)_

Used in serialization. Optional. TypeID is a number for the typeID of object being output.

**Returns:** _number_

---

### getOutput

▸ **getOutput**(): _[Output](common_output.output)_

_Defined in [src/common/output.ts:427](https://github.com/chain4travel/caminojs/blob/3883166/src/common/output.ts#L427)_

**Returns:** _[Output](common_output.output)_

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

_Defined in [src/common/output.ts:403](https://github.com/chain4travel/caminojs/blob/3883166/src/common/output.ts#L403)_

**Parameters:**

| Name       | Type                                                                    | Default |
| ---------- | ----------------------------------------------------------------------- | ------- |
| `encoding` | [SerializedEncoding](../modules/utils_serialization#serializedencoding) | "hex"   |

**Returns:** _object_

---

### toBuffer

▸ **toBuffer**(): _Buffer_

_Defined in [src/common/output.ts:432](https://github.com/chain4travel/caminojs/blob/3883166/src/common/output.ts#L432)_

**Returns:** _Buffer_

---

### `Static` comparator

▸ **comparator**(): _function_

_Defined in [src/common/output.ts:416](https://github.com/chain4travel/caminojs/blob/3883166/src/common/output.ts#L416)_

Returns a function used to sort an array of [ParseableOutput](api_platformvm_outputs.parseableoutput)s

**Returns:** _function_

▸ (`a`: [StandardParseableOutput](common_output.standardparseableoutput), `b`: [StandardParseableOutput](common_output.standardparseableoutput)): _1 | -1 | 0_

**Parameters:**

| Name | Type                                                             |
| ---- | ---------------------------------------------------------------- |
| `a`  | [StandardParseableOutput](common_output.standardparseableoutput) |
| `b`  | [StandardParseableOutput](common_output.standardparseableoutput) |
