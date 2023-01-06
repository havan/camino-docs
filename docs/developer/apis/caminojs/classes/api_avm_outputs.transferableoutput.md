# Class: TransferableOutput

## Hierarchy

↳ [StandardTransferableOutput](common_output.standardtransferableoutput)

↳ **TransferableOutput**

## Index

### Constructors

- [constructor](api_avm_outputs.transferableoutput#constructor)

### Properties

- [\_codecID](api_avm_outputs.transferableoutput#protected-_codecid)
- [\_typeID](api_avm_outputs.transferableoutput#protected-_typeid)
- [\_typeName](api_avm_outputs.transferableoutput#protected-_typename)
- [assetID](api_avm_outputs.transferableoutput#protected-assetid)
- [output](api_avm_outputs.transferableoutput#protected-output)

### Methods

- [deserialize](api_avm_outputs.transferableoutput#deserialize)
- [fromBuffer](api_avm_outputs.transferableoutput#frombuffer)
- [getAssetID](api_avm_outputs.transferableoutput#getassetid)
- [getCodecID](api_avm_outputs.transferableoutput#getcodecid)
- [getOutput](api_avm_outputs.transferableoutput#getoutput)
- [getTypeID](api_avm_outputs.transferableoutput#gettypeid)
- [getTypeName](api_avm_outputs.transferableoutput#gettypename)
- [sanitizeObject](api_avm_outputs.transferableoutput#sanitizeobject)
- [serialize](api_avm_outputs.transferableoutput#serialize)
- [toBuffer](api_avm_outputs.transferableoutput#tobuffer)
- [comparator](api_avm_outputs.transferableoutput#static-comparator)

## Constructors

### constructor

\+ **new TransferableOutput**(`assetID`: Buffer, `output`: [Output](common_output.output)): _[TransferableOutput](api_avm_outputs.transferableoutput)_

_Inherited from [StandardTransferableOutput](common_output.standardtransferableoutput).[constructor](common_output.standardtransferableoutput#constructor)_

_Overrides [StandardParseableOutput](common_output.standardparseableoutput).[constructor](common_output.standardparseableoutput#constructor)_

_Defined in [src/common/output.ts:486](https://github.com/chain4travel/caminojs/blob/3883166/src/common/output.ts#L486)_

Class representing an [StandardTransferableOutput](../modules/src_common#standardtransferableoutput) for a transaction.

**Parameters:**

| Name      | Type                           | Default   | Description                                                                                                             |
| --------- | ------------------------------ | --------- | ----------------------------------------------------------------------------------------------------------------------- |
| `assetID` | Buffer                         | undefined | A [Buffer](https://github.com/feross/buffer) representing the assetID of the [Output](../modules/src_common#output)     |
| `output`  | [Output](common_output.output) | undefined | A number representing the InputID of the [StandardTransferableOutput](../modules/src_common#standardtransferableoutput) |

**Returns:** _[TransferableOutput](api_avm_outputs.transferableoutput)_

## Properties

### `Protected` \_codecID

• **\_codecID**: _number_ = undefined

_Inherited from [SigIdx](common_signature.sigidx).[\_codecID](common_signature.sigidx#protected-_codecid)_

_Defined in [src/utils/serialization.ts:51](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/serialization.ts#L51)_

---

### `Protected` \_typeID

• **\_typeID**: _any_ = undefined

_Overrides [StandardTransferableOutput](common_output.standardtransferableoutput).[\_typeID](common_output.standardtransferableoutput#protected-_typeid)_

_Defined in [src/apis/avm/outputs.ts:57](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/outputs.ts#L57)_

---

### `Protected` \_typeName

• **\_typeName**: _string_ = "TransferableOutput"

_Overrides [StandardTransferableOutput](common_output.standardtransferableoutput).[\_typeName](common_output.standardtransferableoutput#protected-_typename)_

_Defined in [src/apis/avm/outputs.ts:56](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/outputs.ts#L56)_

---

### `Protected` assetID

• **assetID**: _Buffer_ = undefined

_Inherited from [StandardTransferableOutput](common_output.standardtransferableoutput).[assetID](common_output.standardtransferableoutput#protected-assetid)_

_Defined in [src/common/output.ts:475](https://github.com/chain4travel/caminojs/blob/3883166/src/common/output.ts#L475)_

---

### `Protected` output

• **output**: _[Output](common_output.output)_

_Inherited from [StandardParseableOutput](common_output.standardparseableoutput).[output](common_output.standardparseableoutput#protected-output)_

_Defined in [src/common/output.ts:411](https://github.com/chain4travel/caminojs/blob/3883166/src/common/output.ts#L411)_

## Methods

### deserialize

▸ **deserialize**(`fields`: object, `encoding`: [SerializedEncoding](../modules/utils_serialization#serializedencoding)): _void_

_Overrides [StandardTransferableOutput](common_output.standardtransferableoutput).[deserialize](common_output.standardtransferableoutput#deserialize)_

_Defined in [src/apis/avm/outputs.ts:61](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/outputs.ts#L61)_

**Parameters:**

| Name       | Type                                                                    | Default |
| ---------- | ----------------------------------------------------------------------- | ------- |
| `fields`   | object                                                                  | -       |
| `encoding` | [SerializedEncoding](../modules/utils_serialization#serializedencoding) | "hex"   |

**Returns:** _void_

---

### fromBuffer

▸ **fromBuffer**(`bytes`: Buffer, `offset`: number): _number_

_Overrides [StandardTransferableOutput](common_output.standardtransferableoutput).[fromBuffer](common_output.standardtransferableoutput#abstract-frombuffer)_

_Defined in [src/apis/avm/outputs.ts:67](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/outputs.ts#L67)_

**Parameters:**

| Name     | Type   | Default |
| -------- | ------ | ------- |
| `bytes`  | Buffer | -       |
| `offset` | number | 0       |

**Returns:** _number_

---

### getAssetID

▸ **getAssetID**(): _Buffer_

_Inherited from [StandardTransferableOutput](common_output.standardtransferableoutput).[getAssetID](common_output.standardtransferableoutput#getassetid)_

_Defined in [src/common/output.ts:477](https://github.com/chain4travel/caminojs/blob/3883166/src/common/output.ts#L477)_

**Returns:** _Buffer_

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

_Inherited from [StandardTransferableOutput](common_output.standardtransferableoutput).[serialize](common_output.standardtransferableoutput#serialize)_

_Overrides [StandardParseableOutput](common_output.standardparseableoutput).[serialize](common_output.standardparseableoutput#serialize)_

_Defined in [src/common/output.ts:457](https://github.com/chain4travel/caminojs/blob/3883166/src/common/output.ts#L457)_

**Parameters:**

| Name       | Type                                                                    | Default |
| ---------- | ----------------------------------------------------------------------- | ------- |
| `encoding` | [SerializedEncoding](../modules/utils_serialization#serializedencoding) | "hex"   |

**Returns:** _object_

---

### toBuffer

▸ **toBuffer**(): _Buffer_

_Inherited from [StandardTransferableOutput](common_output.standardtransferableoutput).[toBuffer](common_output.standardtransferableoutput#tobuffer)_

_Overrides [StandardParseableOutput](common_output.standardparseableoutput).[toBuffer](common_output.standardparseableoutput#tobuffer)_

_Defined in [src/common/output.ts:482](https://github.com/chain4travel/caminojs/blob/3883166/src/common/output.ts#L482)_

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
