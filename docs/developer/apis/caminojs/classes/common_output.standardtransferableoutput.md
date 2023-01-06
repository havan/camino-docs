# Class: StandardTransferableOutput

## Hierarchy

↳ [StandardParseableOutput](common_output.standardparseableoutput)

↳ **StandardTransferableOutput**

↳ [TransferableOutput](api_evm_outputs.transferableoutput)

↳ [TransferableOutput](api_avm_outputs.transferableoutput)

↳ [TransferableOutput](api_platformvm_outputs.transferableoutput)

## Index

### Constructors

- [constructor](common_output.standardtransferableoutput#constructor)

### Properties

- [\_codecID](common_output.standardtransferableoutput#protected-_codecid)
- [\_typeID](common_output.standardtransferableoutput#protected-_typeid)
- [\_typeName](common_output.standardtransferableoutput#protected-_typename)
- [assetID](common_output.standardtransferableoutput#protected-assetid)
- [output](common_output.standardtransferableoutput#protected-output)

### Methods

- [deserialize](common_output.standardtransferableoutput#deserialize)
- [fromBuffer](common_output.standardtransferableoutput#abstract-frombuffer)
- [getAssetID](common_output.standardtransferableoutput#getassetid)
- [getCodecID](common_output.standardtransferableoutput#getcodecid)
- [getOutput](common_output.standardtransferableoutput#getoutput)
- [getTypeID](common_output.standardtransferableoutput#gettypeid)
- [getTypeName](common_output.standardtransferableoutput#gettypename)
- [sanitizeObject](common_output.standardtransferableoutput#sanitizeobject)
- [serialize](common_output.standardtransferableoutput#serialize)
- [toBuffer](common_output.standardtransferableoutput#tobuffer)
- [comparator](common_output.standardtransferableoutput#static-comparator)

## Constructors

### constructor

\+ **new StandardTransferableOutput**(`assetID`: Buffer, `output`: [Output](common_output.output)): _[StandardTransferableOutput](common_output.standardtransferableoutput)_

_Overrides [StandardParseableOutput](common_output.standardparseableoutput).[constructor](common_output.standardparseableoutput#constructor)_

_Defined in [src/common/output.ts:486](https://github.com/chain4travel/caminojs/blob/3883166/src/common/output.ts#L486)_

Class representing an [StandardTransferableOutput](common_output.standardtransferableoutput) for a transaction.

**Parameters:**

| Name      | Type                           | Default   | Description                                                                                                     |
| --------- | ------------------------------ | --------- | --------------------------------------------------------------------------------------------------------------- |
| `assetID` | Buffer                         | undefined | A [Buffer](https://github.com/feross/buffer) representing the assetID of the [Output](common_output.output)     |
| `output`  | [Output](common_output.output) | undefined | A number representing the InputID of the [StandardTransferableOutput](common_output.standardtransferableoutput) |

**Returns:** _[StandardTransferableOutput](common_output.standardtransferableoutput)_

## Properties

### `Protected` \_codecID

• **\_codecID**: _number_ = undefined

_Inherited from [SigIdx](common_signature.sigidx).[\_codecID](common_signature.sigidx#protected-_codecid)_

_Defined in [src/utils/serialization.ts:51](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/serialization.ts#L51)_

---

### `Protected` \_typeID

• **\_typeID**: _any_ = undefined

_Overrides [StandardParseableOutput](common_output.standardparseableoutput).[\_typeID](common_output.standardparseableoutput#protected-_typeid)_

_Defined in [src/common/output.ts:455](https://github.com/chain4travel/caminojs/blob/3883166/src/common/output.ts#L455)_

---

### `Protected` \_typeName

• **\_typeName**: _string_ = "StandardTransferableOutput"

_Overrides [StandardParseableOutput](common_output.standardparseableoutput).[\_typeName](common_output.standardparseableoutput#protected-_typename)_

_Defined in [src/common/output.ts:454](https://github.com/chain4travel/caminojs/blob/3883166/src/common/output.ts#L454)_

---

### `Protected` assetID

• **assetID**: _Buffer_ = undefined

_Defined in [src/common/output.ts:475](https://github.com/chain4travel/caminojs/blob/3883166/src/common/output.ts#L475)_

---

### `Protected` output

• **output**: _[Output](common_output.output)_

_Inherited from [StandardParseableOutput](common_output.standardparseableoutput).[output](common_output.standardparseableoutput#protected-output)_

_Defined in [src/common/output.ts:411](https://github.com/chain4travel/caminojs/blob/3883166/src/common/output.ts#L411)_

## Methods

### deserialize

▸ **deserialize**(`fields`: object, `encoding`: [SerializedEncoding](../modules/utils_serialization#serializedencoding)): _void_

_Overrides [StandardParseableInput](common_inputs.standardparseableinput).[deserialize](common_inputs.standardparseableinput#deserialize)_

_Defined in [src/common/output.ts:464](https://github.com/chain4travel/caminojs/blob/3883166/src/common/output.ts#L464)_

**Parameters:**

| Name       | Type                                                                    | Default |
| ---------- | ----------------------------------------------------------------------- | ------- |
| `fields`   | object                                                                  | -       |
| `encoding` | [SerializedEncoding](../modules/utils_serialization#serializedencoding) | "hex"   |

**Returns:** _void_

---

### `Abstract` fromBuffer

▸ **fromBuffer**(`bytes`: Buffer, `offset?`: number): _number_

_Overrides [StandardParseableOutput](common_output.standardparseableoutput).[fromBuffer](common_output.standardparseableoutput#abstract-frombuffer)_

_Defined in [src/common/output.ts:480](https://github.com/chain4travel/caminojs/blob/3883166/src/common/output.ts#L480)_

**Parameters:**

| Name      | Type   |
| --------- | ------ |
| `bytes`   | Buffer |
| `offset?` | number |

**Returns:** _number_

---

### getAssetID

▸ **getAssetID**(): _Buffer_

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
