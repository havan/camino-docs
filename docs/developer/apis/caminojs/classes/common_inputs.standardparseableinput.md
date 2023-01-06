# Class: StandardParseableInput

## Hierarchy

- [Serializable](utils_serialization.serializable)

  ↳ **StandardParseableInput**

  ↳ [StandardTransferableInput](common_inputs.standardtransferableinput)

  ↳ [ParseableInput](api_platformvm_inputs.parseableinput)

## Index

### Constructors

- [constructor](common_inputs.standardparseableinput#constructor)

### Properties

- [\_codecID](common_inputs.standardparseableinput#protected-_codecid)
- [\_typeID](common_inputs.standardparseableinput#protected-_typeid)
- [\_typeName](common_inputs.standardparseableinput#protected-_typename)
- [input](common_inputs.standardparseableinput#protected-input)

### Methods

- [deserialize](common_inputs.standardparseableinput#deserialize)
- [fromBuffer](common_inputs.standardparseableinput#abstract-frombuffer)
- [getCodecID](common_inputs.standardparseableinput#getcodecid)
- [getInput](common_inputs.standardparseableinput#getinput)
- [getTypeID](common_inputs.standardparseableinput#gettypeid)
- [getTypeName](common_inputs.standardparseableinput#gettypename)
- [sanitizeObject](common_inputs.standardparseableinput#sanitizeobject)
- [serialize](common_inputs.standardparseableinput#serialize)
- [toBuffer](common_inputs.standardparseableinput#tobuffer)
- [comparator](common_inputs.standardparseableinput#static-comparator)

## Constructors

### constructor

\+ **new StandardParseableInput**(`input`: [Input](common_inputs.input)): _[StandardParseableInput](common_inputs.standardparseableinput)_

_Defined in [src/common/input.ts:172](https://github.com/chain4travel/caminojs/blob/3883166/src/common/input.ts#L172)_

Class representing an [StandardParseableInput](common_inputs.standardparseableinput) for a transaction.

**Parameters:**

| Name    | Type                         | Default   | Description                                                                                             |
| ------- | ---------------------------- | --------- | ------------------------------------------------------------------------------------------------------- |
| `input` | [Input](common_inputs.input) | undefined | A number representing the InputID of the [StandardParseableInput](common_inputs.standardparseableinput) |

**Returns:** _[StandardParseableInput](common_inputs.standardparseableinput)_

## Properties

### `Protected` \_codecID

• **\_codecID**: _number_ = undefined

_Inherited from [SigIdx](common_signature.sigidx).[\_codecID](common_signature.sigidx#protected-_codecid)_

_Defined in [src/utils/serialization.ts:51](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/serialization.ts#L51)_

---

### `Protected` \_typeID

• **\_typeID**: _any_ = undefined

_Overrides [Serializable](utils_serialization.serializable).[\_typeID](utils_serialization.serializable#protected-_typeid)_

_Defined in [src/common/input.ts:135](https://github.com/chain4travel/caminojs/blob/3883166/src/common/input.ts#L135)_

---

### `Protected` \_typeName

• **\_typeName**: _string_ = "StandardParseableInput"

_Overrides [Serializable](utils_serialization.serializable).[\_typeName](utils_serialization.serializable#protected-_typename)_

_Defined in [src/common/input.ts:134](https://github.com/chain4travel/caminojs/blob/3883166/src/common/input.ts#L134)_

---

### `Protected` input

• **input**: _[Input](common_inputs.input)_

_Defined in [src/common/input.ts:145](https://github.com/chain4travel/caminojs/blob/3883166/src/common/input.ts#L145)_

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

_Defined in [src/common/input.ts:164](https://github.com/chain4travel/caminojs/blob/3883166/src/common/input.ts#L164)_

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

### getInput

▸ **getInput**(): _[Input](common_inputs.input)_

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

_Defined in [src/common/input.ts:166](https://github.com/chain4travel/caminojs/blob/3883166/src/common/input.ts#L166)_

**Returns:** _Buffer_

---

### `Static` comparator

▸ **comparator**(): _function_

_Defined in [src/common/input.ts:150](https://github.com/chain4travel/caminojs/blob/3883166/src/common/input.ts#L150)_

Returns a function used to sort an array of [StandardParseableInput](common_inputs.standardparseableinput)s

**Returns:** _function_

▸ (`a`: [StandardParseableInput](common_inputs.standardparseableinput), `b`: [StandardParseableInput](common_inputs.standardparseableinput)): _1 | -1 | 0_

**Parameters:**

| Name | Type                                                           |
| ---- | -------------------------------------------------------------- |
| `a`  | [StandardParseableInput](common_inputs.standardparseableinput) |
| `b`  | [StandardParseableInput](common_inputs.standardparseableinput) |
