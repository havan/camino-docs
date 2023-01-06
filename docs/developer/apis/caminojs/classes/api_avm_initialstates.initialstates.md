# Class: InitialStates

Class for creating initial output states used in asset creation

## Hierarchy

- [Serializable](utils_serialization.serializable)

  ↳ **InitialStates**

## Index

### Properties

- [\_codecID](api_avm_initialstates.initialstates#protected-_codecid)
- [\_typeID](api_avm_initialstates.initialstates#protected-_typeid)
- [\_typeName](api_avm_initialstates.initialstates#protected-_typename)
- [fxs](api_avm_initialstates.initialstates#protected-fxs)

### Methods

- [addOutput](api_avm_initialstates.initialstates#addoutput)
- [deserialize](api_avm_initialstates.initialstates#deserialize)
- [fromBuffer](api_avm_initialstates.initialstates#frombuffer)
- [getCodecID](api_avm_initialstates.initialstates#getcodecid)
- [getTypeID](api_avm_initialstates.initialstates#gettypeid)
- [getTypeName](api_avm_initialstates.initialstates#gettypename)
- [sanitizeObject](api_avm_initialstates.initialstates#sanitizeobject)
- [serialize](api_avm_initialstates.initialstates#serialize)
- [toBuffer](api_avm_initialstates.initialstates#tobuffer)

## Properties

### `Protected` \_codecID

• **\_codecID**: _number_ = undefined

_Inherited from [SigIdx](common_signature.sigidx).[\_codecID](common_signature.sigidx#protected-_codecid)_

_Defined in [src/utils/serialization.ts:51](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/serialization.ts#L51)_

---

### `Protected` \_typeID

• **\_typeID**: _any_ = undefined

_Overrides [Serializable](utils_serialization.serializable).[\_typeID](utils_serialization.serializable#protected-_typeid)_

_Defined in [src/apis/avm/initialstates.ts:22](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/initialstates.ts#L22)_

---

### `Protected` \_typeName

• **\_typeName**: _string_ = "InitialStates"

_Overrides [Serializable](utils_serialization.serializable).[\_typeName](utils_serialization.serializable#protected-_typename)_

_Defined in [src/apis/avm/initialstates.ts:21](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/initialstates.ts#L21)_

---

### `Protected` fxs

• **fxs**: _object_

_Defined in [src/apis/avm/initialstates.ts:50](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/initialstates.ts#L50)_

#### Type declaration:

- \[ **fxid**: _number_\]: [Output](common_output.output)[]

## Methods

### addOutput

▸ **addOutput**(`out`: [Output](common_output.output), `fxid`: number): _void_

_Defined in [src/apis/avm/initialstates.ts:57](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/initialstates.ts#L57)_

**Parameters:**

| Name   | Type                           | Default               | Description                                                               |
| ------ | ------------------------------ | --------------------- | ------------------------------------------------------------------------- |
| `out`  | [Output](common_output.output) | -                     | The output state to add to the collection                                 |
| `fxid` | number                         | AVMConstants.SECPFXID | The FxID that will be used for this output, default AVMConstants.SECPFXID |

**Returns:** _void_

---

### deserialize

▸ **deserialize**(`fields`: object, `encoding`: [SerializedEncoding](../modules/utils_serialization#serializedencoding)): _void_

_Overrides [StandardParseableInput](common_inputs.standardparseableinput).[deserialize](common_inputs.standardparseableinput#deserialize)_

_Defined in [src/apis/avm/initialstates.ts:37](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/initialstates.ts#L37)_

**Parameters:**

| Name       | Type                                                                    | Default |
| ---------- | ----------------------------------------------------------------------- | ------- |
| `fields`   | object                                                                  | -       |
| `encoding` | [SerializedEncoding](../modules/utils_serialization#serializedencoding) | "hex"   |

**Returns:** _void_

---

### fromBuffer

▸ **fromBuffer**(`bytes`: Buffer, `offset`: number): _number_

_Defined in [src/apis/avm/initialstates.ts:64](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/initialstates.ts#L64)_

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

_Defined in [src/apis/avm/initialstates.ts:24](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/initialstates.ts#L24)_

**Parameters:**

| Name       | Type                                                                    | Default |
| ---------- | ----------------------------------------------------------------------- | ------- |
| `encoding` | [SerializedEncoding](../modules/utils_serialization#serializedencoding) | "hex"   |

**Returns:** _object_

---

### toBuffer

▸ **toBuffer**(): _Buffer_

_Defined in [src/apis/avm/initialstates.ts:91](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/initialstates.ts#L91)_

**Returns:** _Buffer_
