# Class: ParseableOutput

## Hierarchy

↳ [StandardParseableOutput](common_output.standardparseableoutput)

↳ **ParseableOutput**

## Index

### Constructors

- [constructor](api_platformvm_outputs.parseableoutput#constructor)

### Properties

- [\_codecID](api_platformvm_outputs.parseableoutput#protected-_codecid)
- [\_typeID](api_platformvm_outputs.parseableoutput#protected-_typeid)
- [\_typeName](api_platformvm_outputs.parseableoutput#protected-_typename)
- [output](api_platformvm_outputs.parseableoutput#protected-output)

### Methods

- [deserialize](api_platformvm_outputs.parseableoutput#deserialize)
- [fromBuffer](api_platformvm_outputs.parseableoutput#frombuffer)
- [getCodecID](api_platformvm_outputs.parseableoutput#getcodecid)
- [getOutput](api_platformvm_outputs.parseableoutput#getoutput)
- [getTypeID](api_platformvm_outputs.parseableoutput#gettypeid)
- [getTypeName](api_platformvm_outputs.parseableoutput#gettypename)
- [sanitizeObject](api_platformvm_outputs.parseableoutput#sanitizeobject)
- [serialize](api_platformvm_outputs.parseableoutput#serialize)
- [toBuffer](api_platformvm_outputs.parseableoutput#tobuffer)
- [comparator](api_platformvm_outputs.parseableoutput#static-comparator)

## Constructors

### constructor

\+ **new ParseableOutput**(`output`: [Output](common_output.output)): _[ParseableOutput](api_platformvm_outputs.parseableoutput)_

_Inherited from [StandardParseableOutput](common_output.standardparseableoutput).[constructor](common_output.standardparseableoutput#constructor)_

_Defined in [src/common/output.ts:438](https://github.com/chain4travel/caminojs/blob/3883166/src/common/output.ts#L438)_

Class representing an [ParseableOutput](api_platformvm_outputs.parseableoutput) for a transaction.

**Parameters:**

| Name     | Type                           | Default   | Description                                                                                        |
| -------- | ------------------------------ | --------- | -------------------------------------------------------------------------------------------------- |
| `output` | [Output](common_output.output) | undefined | A number representing the InputID of the [ParseableOutput](api_platformvm_outputs.parseableoutput) |

**Returns:** _[ParseableOutput](api_platformvm_outputs.parseableoutput)_

## Properties

### `Protected` \_codecID

• **\_codecID**: _number_ = undefined

_Inherited from [SigIdx](common_signature.sigidx).[\_codecID](common_signature.sigidx#protected-_codecid)_

_Defined in [src/utils/serialization.ts:51](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/serialization.ts#L51)_

---

### `Protected` \_typeID

• **\_typeID**: _any_ = undefined

_Overrides [StandardParseableOutput](common_output.standardparseableoutput).[\_typeID](common_output.standardparseableoutput#protected-_typeid)_

_Defined in [src/apis/platformvm/outputs.ts:72](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/outputs.ts#L72)_

---

### `Protected` \_typeName

• **\_typeName**: _string_ = "ParseableOutput"

_Overrides [StandardParseableOutput](common_output.standardparseableoutput).[\_typeName](common_output.standardparseableoutput#protected-_typename)_

_Defined in [src/apis/platformvm/outputs.ts:71](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/outputs.ts#L71)_

---

### `Protected` output

• **output**: _[Output](common_output.output)_

_Inherited from [StandardParseableOutput](common_output.standardparseableoutput).[output](common_output.standardparseableoutput#protected-output)_

_Defined in [src/common/output.ts:411](https://github.com/chain4travel/caminojs/blob/3883166/src/common/output.ts#L411)_

## Methods

### deserialize

▸ **deserialize**(`fields`: object, `encoding`: [SerializedEncoding](../modules/utils_serialization#serializedencoding)): _void_

_Overrides [StandardParseableInput](common_inputs.standardparseableinput).[deserialize](common_inputs.standardparseableinput#deserialize)_

_Defined in [src/apis/platformvm/outputs.ts:76](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/outputs.ts#L76)_

**Parameters:**

| Name       | Type                                                                    | Default |
| ---------- | ----------------------------------------------------------------------- | ------- |
| `fields`   | object                                                                  | -       |
| `encoding` | [SerializedEncoding](../modules/utils_serialization#serializedencoding) | "hex"   |

**Returns:** _void_

---

### fromBuffer

▸ **fromBuffer**(`bytes`: Buffer, `offset`: number): _number_

_Overrides [StandardParseableOutput](common_output.standardparseableoutput).[fromBuffer](common_output.standardparseableoutput#abstract-frombuffer)_

_Defined in [src/apis/platformvm/outputs.ts:82](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/outputs.ts#L82)_

**Parameters:**

| Name     | Type   | Default |
| -------- | ------ | ------- |
| `bytes`  | Buffer | -       |
| `offset` | number | 0       |

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

_Inherited from [StandardParseableOutput](common_output.standardparseableoutput).[getOutput](common_output.standardparseableoutput#getoutput)_

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

_Inherited from [StandardParseableOutput](common_output.standardparseableoutput).[serialize](common_output.standardparseableoutput#serialize)_

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

_Inherited from [StandardParseableOutput](common_output.standardparseableoutput).[toBuffer](common_output.standardparseableoutput#tobuffer)_

_Defined in [src/common/output.ts:432](https://github.com/chain4travel/caminojs/blob/3883166/src/common/output.ts#L432)_

**Returns:** _Buffer_

---

### `Static` comparator

▸ **comparator**(): _function_

_Inherited from [StandardParseableOutput](common_output.standardparseableoutput).[comparator](common_output.standardparseableoutput#static-comparator)_

_Defined in [src/common/output.ts:416](https://github.com/chain4travel/caminojs/blob/3883166/src/common/output.ts#L416)_

Returns a function used to sort an array of [ParseableOutput](api_platformvm_outputs.parseableoutput)s

**Returns:** _function_

▸ (`a`: [StandardParseableOutput](common_output.standardparseableoutput), `b`: [StandardParseableOutput](common_output.standardparseableoutput)): _1 | -1 | 0_

**Parameters:**

| Name | Type                                                             |
| ---- | ---------------------------------------------------------------- |
| `a`  | [StandardParseableOutput](common_output.standardparseableoutput) |
| `b`  | [StandardParseableOutput](common_output.standardparseableoutput) |
