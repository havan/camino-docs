# Class: TransferableInput

## Hierarchy

↳ [StandardTransferableInput](common_inputs.standardtransferableinput)

↳ **TransferableInput**

## Index

### Constructors

- [constructor](api_evm_inputs.transferableinput#constructor)

### Properties

- [\_codecID](api_evm_inputs.transferableinput#protected-_codecid)
- [\_typeID](api_evm_inputs.transferableinput#protected-_typeid)
- [\_typeName](api_evm_inputs.transferableinput#protected-_typename)
- [assetID](api_evm_inputs.transferableinput#protected-assetid)
- [input](api_evm_inputs.transferableinput#protected-input)
- [outputidx](api_evm_inputs.transferableinput#protected-outputidx)
- [txid](api_evm_inputs.transferableinput#protected-txid)

### Methods

- [deserialize](api_evm_inputs.transferableinput#deserialize)
- [fromBuffer](api_evm_inputs.transferableinput#frombuffer)
- [getAssetID](api_evm_inputs.transferableinput#getassetid)
- [getCodecID](api_evm_inputs.transferableinput#getcodecid)
- [getCost](api_evm_inputs.transferableinput#getcost)
- [getInput](api_evm_inputs.transferableinput#getinput)
- [getOutputIdx](api_evm_inputs.transferableinput#getoutputidx)
- [getTxID](api_evm_inputs.transferableinput#gettxid)
- [getTypeID](api_evm_inputs.transferableinput#gettypeid)
- [getTypeName](api_evm_inputs.transferableinput#gettypename)
- [getUTXOID](api_evm_inputs.transferableinput#getutxoid)
- [sanitizeObject](api_evm_inputs.transferableinput#sanitizeobject)
- [serialize](api_evm_inputs.transferableinput#serialize)
- [toBuffer](api_evm_inputs.transferableinput#tobuffer)
- [toString](api_evm_inputs.transferableinput#tostring)
- [comparator](api_evm_inputs.transferableinput#static-comparator)

## Constructors

### constructor

\+ **new TransferableInput**(`txid`: Buffer, `outputidx`: Buffer, `assetID`: Buffer, `input`: [Input](common_inputs.input)): _[TransferableInput](api_evm_inputs.transferableinput)_

_Inherited from [StandardTransferableInput](common_inputs.standardtransferableinput).[constructor](common_inputs.standardtransferableinput#constructor)_

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

**Returns:** _[TransferableInput](api_evm_inputs.transferableinput)_

## Properties

### `Protected` \_codecID

• **\_codecID**: _number_ = undefined

_Inherited from [SigIdx](common_signature.sigidx).[\_codecID](common_signature.sigidx#protected-_codecid)_

_Defined in [src/utils/serialization.ts:51](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/serialization.ts#L51)_

---

### `Protected` \_typeID

• **\_typeID**: _any_ = undefined

_Overrides [StandardTransferableInput](common_inputs.standardtransferableinput).[\_typeID](common_inputs.standardtransferableinput#protected-_typeid)_

_Defined in [src/apis/evm/inputs.ts:42](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/inputs.ts#L42)_

---

### `Protected` \_typeName

• **\_typeName**: _string_ = "TransferableInput"

_Overrides [StandardTransferableInput](common_inputs.standardtransferableinput).[\_typeName](common_inputs.standardtransferableinput#protected-_typename)_

_Defined in [src/apis/evm/inputs.ts:41](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/inputs.ts#L41)_

---

### `Protected` assetID

• **assetID**: _Buffer_ = Buffer.alloc(32)

_Inherited from [StandardTransferableInput](common_inputs.standardtransferableinput).[assetID](common_inputs.standardtransferableinput#protected-assetid)_

_Defined in [src/common/input.ts:233](https://github.com/chain4travel/caminojs/blob/3883166/src/common/input.ts#L233)_

---

### `Protected` input

• **input**: _[Input](common_inputs.input)_

_Inherited from [StandardParseableInput](common_inputs.standardparseableinput).[input](common_inputs.standardparseableinput#protected-input)_

_Defined in [src/common/input.ts:145](https://github.com/chain4travel/caminojs/blob/3883166/src/common/input.ts#L145)_

---

### `Protected` outputidx

• **outputidx**: _Buffer_ = Buffer.alloc(4)

_Inherited from [StandardTransferableInput](common_inputs.standardtransferableinput).[outputidx](common_inputs.standardtransferableinput#protected-outputidx)_

_Defined in [src/common/input.ts:232](https://github.com/chain4travel/caminojs/blob/3883166/src/common/input.ts#L232)_

---

### `Protected` txid

• **txid**: _Buffer_ = Buffer.alloc(32)

_Inherited from [StandardTransferableInput](common_inputs.standardtransferableinput).[txid](common_inputs.standardtransferableinput#protected-txid)_

_Defined in [src/common/input.ts:231](https://github.com/chain4travel/caminojs/blob/3883166/src/common/input.ts#L231)_

## Methods

### deserialize

▸ **deserialize**(`fields`: object, `encoding`: [SerializedEncoding](../modules/utils_serialization#serializedencoding)): _void_

_Overrides [StandardTransferableInput](common_inputs.standardtransferableinput).[deserialize](common_inputs.standardtransferableinput#deserialize)_

_Defined in [src/apis/evm/inputs.ts:46](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/inputs.ts#L46)_

**Parameters:**

| Name       | Type                                                                    | Default |
| ---------- | ----------------------------------------------------------------------- | ------- |
| `fields`   | object                                                                  | -       |
| `encoding` | [SerializedEncoding](../modules/utils_serialization#serializedencoding) | "hex"   |

**Returns:** _void_

---

### fromBuffer

▸ **fromBuffer**(`bytes`: Buffer, `offset`: number): _number_

_Overrides [StandardTransferableInput](common_inputs.standardtransferableinput).[fromBuffer](common_inputs.standardtransferableinput#abstract-frombuffer)_

_Defined in [src/apis/evm/inputs.ts:69](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/inputs.ts#L69)_

Takes a [Buffer](https://github.com/feross/buffer) containing a [TransferableInput](api_evm_inputs.transferableinput), parses it, populates the class, and returns the length of the [TransferableInput](api_evm_inputs.transferableinput) in bytes.

**Parameters:**

| Name     | Type   | Default | Description                                                                                                         |
| -------- | ------ | ------- | ------------------------------------------------------------------------------------------------------------------- |
| `bytes`  | Buffer | -       | A [Buffer](https://github.com/feross/buffer) containing a raw [TransferableInput](api_evm_inputs.transferableinput) |
| `offset` | number | 0       | -                                                                                                                   |

**Returns:** _number_

The length of the raw [TransferableInput](api_evm_inputs.transferableinput)

---

### getAssetID

▸ **getAssetID**(): _Buffer_

_Inherited from [StandardTransferableInput](common_inputs.standardtransferableinput).[getAssetID](common_inputs.standardtransferableinput#getassetid)_

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

### getCost

▸ **getCost**(`c`: [C](../interfaces/utils_networks.c)): _number_

_Defined in [src/apis/evm/inputs.ts:57](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/inputs.ts#L57)_

Assesses the amount to be paid based on the number of signatures required

**Parameters:**

| Name | Type                                |
| ---- | ----------------------------------- |
| `c`  | [C](../interfaces/utils_networks.c) |

**Returns:** _number_

the amount to be paid

---

### getInput

▸ **getInput**(): _[Input](common_inputs.input)_

_Inherited from [StandardTransferableInput](common_inputs.standardtransferableinput).[getInput](common_inputs.standardtransferableinput#getinput)_

_Overrides [StandardParseableInput](common_inputs.standardparseableinput).[getInput](common_inputs.standardparseableinput#getinput)_

_Defined in [src/common/input.ts:254](https://github.com/chain4travel/caminojs/blob/3883166/src/common/input.ts#L254)_

Returns the input.

**Returns:** _[Input](common_inputs.input)_

---

### getOutputIdx

▸ **getOutputIdx**(): _Buffer_

_Inherited from [StandardTransferableInput](common_inputs.standardtransferableinput).[getOutputIdx](common_inputs.standardtransferableinput#getoutputidx)_

_Defined in [src/common/input.ts:243](https://github.com/chain4travel/caminojs/blob/3883166/src/common/input.ts#L243)_

Returns a [Buffer](https://github.com/feross/buffer) of the OutputIdx.

**Returns:** _Buffer_

---

### getTxID

▸ **getTxID**(): _Buffer_

_Inherited from [StandardTransferableInput](common_inputs.standardtransferableinput).[getTxID](common_inputs.standardtransferableinput#gettxid)_

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

_Inherited from [StandardTransferableInput](common_inputs.standardtransferableinput).[getUTXOID](common_inputs.standardtransferableinput#getutxoid)_

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

_Inherited from [StandardTransferableInput](common_inputs.standardtransferableinput).[serialize](common_inputs.standardtransferableinput#serialize)_

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

_Inherited from [StandardTransferableInput](common_inputs.standardtransferableinput).[toBuffer](common_inputs.standardtransferableinput#tobuffer)_

_Overrides [StandardParseableInput](common_inputs.standardparseableinput).[toBuffer](common_inputs.standardparseableinput#tobuffer)_

_Defined in [src/common/input.ts:266](https://github.com/chain4travel/caminojs/blob/3883166/src/common/input.ts#L266)_

Returns a [Buffer](https://github.com/feross/buffer) representation of the [StandardTransferableInput](common_inputs.standardtransferableinput).

**Returns:** _Buffer_

---

### toString

▸ **toString**(): _string_

_Inherited from [StandardTransferableInput](common_inputs.standardtransferableinput).[toString](common_inputs.standardtransferableinput#tostring)_

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
