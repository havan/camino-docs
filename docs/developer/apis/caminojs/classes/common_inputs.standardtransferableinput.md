# Class: StandardTransferableInput

## Hierarchy

↳ [StandardParseableInput](common_inputs.standardparseableinput)

↳ **StandardTransferableInput**

↳ [TransferableInput](api_evm_inputs.transferableinput)

↳ [TransferableInput](api_avm_inputs.transferableinput)

↳ [TransferableInput](api_platformvm_inputs.transferableinput)

## Index

### Constructors

- [constructor](common_inputs.standardtransferableinput#constructor)

### Properties

- [\_codecID](common_inputs.standardtransferableinput#protected-_codecid)
- [\_typeID](common_inputs.standardtransferableinput#protected-_typeid)
- [\_typeName](common_inputs.standardtransferableinput#protected-_typename)
- [assetID](common_inputs.standardtransferableinput#protected-assetid)
- [input](common_inputs.standardtransferableinput#protected-input)
- [outputidx](common_inputs.standardtransferableinput#protected-outputidx)
- [txid](common_inputs.standardtransferableinput#protected-txid)

### Methods

- [deserialize](common_inputs.standardtransferableinput#deserialize)
- [fromBuffer](common_inputs.standardtransferableinput#abstract-frombuffer)
- [getAssetID](common_inputs.standardtransferableinput#getassetid)
- [getCodecID](common_inputs.standardtransferableinput#getcodecid)
- [getInput](common_inputs.standardtransferableinput#getinput)
- [getOutputIdx](common_inputs.standardtransferableinput#getoutputidx)
- [getTxID](common_inputs.standardtransferableinput#gettxid)
- [getTypeID](common_inputs.standardtransferableinput#gettypeid)
- [getTypeName](common_inputs.standardtransferableinput#gettypename)
- [getUTXOID](common_inputs.standardtransferableinput#getutxoid)
- [sanitizeObject](common_inputs.standardtransferableinput#sanitizeobject)
- [serialize](common_inputs.standardtransferableinput#serialize)
- [toBuffer](common_inputs.standardtransferableinput#tobuffer)
- [toString](common_inputs.standardtransferableinput#tostring)
- [comparator](common_inputs.standardtransferableinput#static-comparator)

## Constructors

### constructor

\+ **new StandardTransferableInput**(`txid`: Buffer, `outputidx`: Buffer, `assetID`: Buffer, `input`: [Input](common_inputs.input)): _[StandardTransferableInput](common_inputs.standardtransferableinput)_

_Overrides [StandardParseableInput](common_inputs.standardparseableinput).[constructor](common_inputs.standardparseableinput#constructor)_

_Defined in [src/common/input.ts:289](https://github.com/chain4travel/caminojs/blob/3883166/src/common/input.ts#L289)_

Class representing an [StandardTransferableInput](common_inputs.standardtransferableinput) for a transaction.

**Parameters:**

| Name        | Type                         | Default   | Description                                                                                                                                                                             |
| ----------- | ---------------------------- | --------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `txid`      | Buffer                       | undefined | A [Buffer](https://github.com/feross/buffer) containing the transaction ID of the referenced UTXO                                                                                       |
| `outputidx` | Buffer                       | undefined | A [Buffer](https://github.com/feross/buffer) containing the index of the output in the transaction consumed in the [StandardTransferableInput](common_inputs.standardtransferableinput) |
| `assetID`   | Buffer                       | undefined | A [Buffer](https://github.com/feross/buffer) representing the assetID of the [Input](common_inputs.input)                                                                               |
| `input`     | [Input](common_inputs.input) | undefined | An [Input](common_inputs.input) to be made transferable                                                                                                                                 |

**Returns:** _[StandardTransferableInput](common_inputs.standardtransferableinput)_

## Properties

### `Protected` \_codecID

• **\_codecID**: _number_ = undefined

_Inherited from [SigIdx](common_signature.sigidx).[\_codecID](common_signature.sigidx#protected-_codecid)_

_Defined in [src/utils/serialization.ts:51](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/serialization.ts#L51)_

---

### `Protected` \_typeID

• **\_typeID**: _any_ = undefined

_Overrides [StandardParseableInput](common_inputs.standardparseableinput).[\_typeID](common_inputs.standardparseableinput#protected-_typeid)_

_Defined in [src/common/input.ts:189](https://github.com/chain4travel/caminojs/blob/3883166/src/common/input.ts#L189)_

---

### `Protected` \_typeName

• **\_typeName**: _string_ = "StandardTransferableInput"

_Overrides [StandardParseableInput](common_inputs.standardparseableinput).[\_typeName](common_inputs.standardparseableinput#protected-_typename)_

_Defined in [src/common/input.ts:188](https://github.com/chain4travel/caminojs/blob/3883166/src/common/input.ts#L188)_

---

### `Protected` assetID

• **assetID**: _Buffer_ = Buffer.alloc(32)

_Defined in [src/common/input.ts:233](https://github.com/chain4travel/caminojs/blob/3883166/src/common/input.ts#L233)_

---

### `Protected` input

• **input**: _[Input](common_inputs.input)_

_Inherited from [StandardParseableInput](common_inputs.standardparseableinput).[input](common_inputs.standardparseableinput#protected-input)_

_Defined in [src/common/input.ts:145](https://github.com/chain4travel/caminojs/blob/3883166/src/common/input.ts#L145)_

---

### `Protected` outputidx

• **outputidx**: _Buffer_ = Buffer.alloc(4)

_Defined in [src/common/input.ts:232](https://github.com/chain4travel/caminojs/blob/3883166/src/common/input.ts#L232)_

---

### `Protected` txid

• **txid**: _Buffer_ = Buffer.alloc(32)

_Defined in [src/common/input.ts:231](https://github.com/chain4travel/caminojs/blob/3883166/src/common/input.ts#L231)_

## Methods

### deserialize

▸ **deserialize**(`fields`: object, `encoding`: [SerializedEncoding](../modules/utils_serialization#serializedencoding)): _void_

_Overrides [StandardParseableInput](common_inputs.standardparseableinput).[deserialize](common_inputs.standardparseableinput#deserialize)_

_Defined in [src/common/input.ts:205](https://github.com/chain4travel/caminojs/blob/3883166/src/common/input.ts#L205)_

**Parameters:**

| Name       | Type                                                                    | Default |
| ---------- | ----------------------------------------------------------------------- | ------- |
| `fields`   | object                                                                  | -       |
| `encoding` | [SerializedEncoding](../modules/utils_serialization#serializedencoding) | "hex"   |

**Returns:** _void_

---

### `Abstract` fromBuffer

▸ **fromBuffer**(`bytes`: Buffer, `offset?`: number): _number_

_Overrides [StandardParseableInput](common_inputs.standardparseableinput).[fromBuffer](common_inputs.standardparseableinput#abstract-frombuffer)_

_Defined in [src/common/input.ts:261](https://github.com/chain4travel/caminojs/blob/3883166/src/common/input.ts#L261)_

**Parameters:**

| Name      | Type   |
| --------- | ------ |
| `bytes`   | Buffer |
| `offset?` | number |

**Returns:** _number_

---

### getAssetID

▸ **getAssetID**(): _Buffer_

_Defined in [src/common/input.ts:259](https://github.com/chain4travel/caminojs/blob/3883166/src/common/input.ts#L259)_

Returns the assetID of the input.

**Returns:** _Buffer_

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

_Overrides [StandardParseableInput](common_inputs.standardparseableinput).[getInput](common_inputs.standardparseableinput#getinput)_

_Defined in [src/common/input.ts:254](https://github.com/chain4travel/caminojs/blob/3883166/src/common/input.ts#L254)_

Returns the input.

**Returns:** _[Input](common_inputs.input)_

---

### getOutputIdx

▸ **getOutputIdx**(): _Buffer_

_Defined in [src/common/input.ts:243](https://github.com/chain4travel/caminojs/blob/3883166/src/common/input.ts#L243)_

Returns a [Buffer](https://github.com/feross/buffer) of the OutputIdx.

**Returns:** _Buffer_

---

### getTxID

▸ **getTxID**(): _Buffer_

_Defined in [src/common/input.ts:238](https://github.com/chain4travel/caminojs/blob/3883166/src/common/input.ts#L238)_

Returns a [Buffer](https://github.com/feross/buffer) of the TxID.

**Returns:** _Buffer_

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

### getUTXOID

▸ **getUTXOID**(): _string_

_Defined in [src/common/input.ts:248](https://github.com/chain4travel/caminojs/blob/3883166/src/common/input.ts#L248)_

Returns a base-58 string representation of the UTXOID this [StandardTransferableInput](common_inputs.standardtransferableinput) references.

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

_Overrides [StandardParseableInput](common_inputs.standardparseableinput).[serialize](common_inputs.standardparseableinput#serialize)_

_Defined in [src/common/input.ts:191](https://github.com/chain4travel/caminojs/blob/3883166/src/common/input.ts#L191)_

**Parameters:**

| Name       | Type                                                                    | Default |
| ---------- | ----------------------------------------------------------------------- | ------- |
| `encoding` | [SerializedEncoding](../modules/utils_serialization#serializedencoding) | "hex"   |

**Returns:** _object_

---

### toBuffer

▸ **toBuffer**(): _Buffer_

_Overrides [StandardParseableInput](common_inputs.standardparseableinput).[toBuffer](common_inputs.standardparseableinput#tobuffer)_

_Defined in [src/common/input.ts:266](https://github.com/chain4travel/caminojs/blob/3883166/src/common/input.ts#L266)_

Returns a [Buffer](https://github.com/feross/buffer) representation of the [StandardTransferableInput](common_inputs.standardtransferableinput).

**Returns:** _Buffer_

---

### toString

▸ **toString**(): _string_

_Defined in [src/common/input.ts:286](https://github.com/chain4travel/caminojs/blob/3883166/src/common/input.ts#L286)_

Returns a base-58 representation of the [StandardTransferableInput](common_inputs.standardtransferableinput).

**Returns:** _string_

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
