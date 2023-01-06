# Class: ParseableInput

## Hierarchy

↳ [StandardParseableInput](common_inputs.standardparseableinput)

↳ **ParseableInput**

## Index

### Constructors

- [constructor](api_platformvm_inputs.parseableinput#constructor)

### Properties

- [\_codecID](api_platformvm_inputs.parseableinput#protected-_codecid)
- [\_typeID](api_platformvm_inputs.parseableinput#protected-_typeid)
- [\_typeName](api_platformvm_inputs.parseableinput#protected-_typename)
- [input](api_platformvm_inputs.parseableinput#protected-input)

### Methods

- [deserialize](api_platformvm_inputs.parseableinput#deserialize)
- [fromBuffer](api_platformvm_inputs.parseableinput#frombuffer)
- [getCodecID](api_platformvm_inputs.parseableinput#getcodecid)
- [getInput](api_platformvm_inputs.parseableinput#getinput)
- [getTypeID](api_platformvm_inputs.parseableinput#gettypeid)
- [getTypeName](api_platformvm_inputs.parseableinput#gettypename)
- [sanitizeObject](api_platformvm_inputs.parseableinput#sanitizeobject)
- [serialize](api_platformvm_inputs.parseableinput#serialize)
- [toBuffer](api_platformvm_inputs.parseableinput#tobuffer)
- [comparator](api_platformvm_inputs.parseableinput#static-comparator)

## Constructors

### constructor

\+ **new ParseableInput**(`input`: [Input](common_inputs.input)): _[ParseableInput](api_platformvm_inputs.parseableinput)_

_Inherited from [StandardParseableInput](common_inputs.standardparseableinput).[constructor](common_inputs.standardparseableinput#constructor)_

_Defined in [src/common/input.ts:172](https://github.com/chain4travel/caminojs/blob/3883166/src/common/input.ts#L172)_

Class representing an [StandardParseableInput](common_inputs.standardparseableinput) for a transaction.

**Parameters:**

| Name    | Type                         | Default   | Description                                                                                             |
| ------- | ---------------------------- | --------- | ------------------------------------------------------------------------------------------------------- |
| `input` | [Input](common_inputs.input) | undefined | A number representing the InputID of the [StandardParseableInput](common_inputs.standardparseableinput) |

**Returns:** _[ParseableInput](api_platformvm_inputs.parseableinput)_

## Properties

### `Protected` \_codecID

• **\_codecID**: _number_ = undefined

_Inherited from [SigIdx](common_signature.sigidx).[\_codecID](common_signature.sigidx#protected-_codecid)_

_Defined in [src/utils/serialization.ts:51](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/serialization.ts#L51)_

---

### `Protected` \_typeID

• **\_typeID**: _any_ = undefined

_Overrides [StandardParseableInput](common_inputs.standardparseableinput).[\_typeID](common_inputs.standardparseableinput#protected-_typeid)_

_Defined in [src/apis/platformvm/inputs.ts:43](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/inputs.ts#L43)_

---

### `Protected` \_typeName

• **\_typeName**: _string_ = "ParseableInput"

_Overrides [StandardParseableInput](common_inputs.standardparseableinput).[\_typeName](common_inputs.standardparseableinput#protected-_typename)_

_Defined in [src/apis/platformvm/inputs.ts:42](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/inputs.ts#L42)_

---

### `Protected` input

• **input**: _[Input](common_inputs.input)_

_Inherited from [StandardParseableInput](common_inputs.standardparseableinput).[input](common_inputs.standardparseableinput#protected-input)_

_Defined in [src/common/input.ts:145](https://github.com/chain4travel/caminojs/blob/3883166/src/common/input.ts#L145)_

## Methods

### deserialize

▸ **deserialize**(`fields`: object, `encoding`: [SerializedEncoding](../modules/utils_serialization#serializedencoding)): _void_

_Overrides [StandardParseableInput](common_inputs.standardparseableinput).[deserialize](common_inputs.standardparseableinput#deserialize)_

_Defined in [src/apis/platformvm/inputs.ts:47](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/inputs.ts#L47)_

**Parameters:**

| Name       | Type                                                                    | Default |
| ---------- | ----------------------------------------------------------------------- | ------- |
| `fields`   | object                                                                  | -       |
| `encoding` | [SerializedEncoding](../modules/utils_serialization#serializedencoding) | "hex"   |

**Returns:** _void_

---

### fromBuffer

▸ **fromBuffer**(`bytes`: Buffer, `offset`: number): _number_

_Overrides [StandardParseableInput](common_inputs.standardparseableinput).[fromBuffer](common_inputs.standardparseableinput#abstract-frombuffer)_

_Defined in [src/apis/platformvm/inputs.ts:53](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/inputs.ts#L53)_

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

### getInput

▸ **getInput**(): _[Input](common_inputs.input)_

_Inherited from [StandardParseableInput](common_inputs.standardparseableinput).[getInput](common_inputs.standardparseableinput#getinput)_

_Defined in [src/common/input.ts:161](https://github.com/chain4travel/caminojs/blob/3883166/src/common/input.ts#L161)_

**Returns:** _[Input](common_inputs.input)_

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

_Inherited from [StandardParseableInput](common_inputs.standardparseableinput).[serialize](common_inputs.standardparseableinput#serialize)_

_Overrides [Serializable](utils_serialization.serializable).[serialize](utils_serialization.serializable#serialize)_

_Defined in [src/common/input.ts:137](https://github.com/chain4travel/caminojs/blob/3883166/src/common/input.ts#L137)_

**Parameters:**

| Name       | Type                                                                    | Default |
| ---------- | ----------------------------------------------------------------------- | ------- |
| `encoding` | [SerializedEncoding](../modules/utils_serialization#serializedencoding) | "hex"   |

**Returns:** _object_

---

### toBuffer

▸ **toBuffer**(): _Buffer_

_Inherited from [StandardParseableInput](common_inputs.standardparseableinput).[toBuffer](common_inputs.standardparseableinput#tobuffer)_

_Defined in [src/common/input.ts:166](https://github.com/chain4travel/caminojs/blob/3883166/src/common/input.ts#L166)_

**Returns:** _Buffer_

---

### `Static` comparator

▸ **comparator**(): _function_

_Inherited from [StandardParseableInput](common_inputs.standardparseableinput).[comparator](common_inputs.standardparseableinput#static-comparator)_

_Defined in [src/common/input.ts:150](https://github.com/chain4travel/caminojs/blob/3883166/src/common/input.ts#L150)_

Returns a function used to sort an array of [StandardParseableInput](common_inputs.standardparseableinput)s

**Returns:** _function_

▸ (`a`: [StandardParseableInput](common_inputs.standardparseableinput), `b`: [StandardParseableInput](common_inputs.standardparseableinput)): _1 | -1 | 0_

**Parameters:**

| Name | Type                                                           |
| ---- | -------------------------------------------------------------- |
| `a`  | [StandardParseableInput](common_inputs.standardparseableinput) |
| `b`  | [StandardParseableInput](common_inputs.standardparseableinput) |
