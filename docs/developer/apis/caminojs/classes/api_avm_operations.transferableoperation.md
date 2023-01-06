# Class: TransferableOperation

A class which contains an [Operation](api_avm_operations.operation) for transfers.

## Hierarchy

- [Serializable](utils_serialization.serializable)

  ↳ **TransferableOperation**

## Index

### Constructors

- [constructor](api_avm_operations.transferableoperation#constructor)

### Properties

- [\_codecID](api_avm_operations.transferableoperation#protected-_codecid)
- [\_typeID](api_avm_operations.transferableoperation#protected-_typeid)
- [\_typeName](api_avm_operations.transferableoperation#protected-_typename)
- [assetID](api_avm_operations.transferableoperation#protected-assetid)
- [operation](api_avm_operations.transferableoperation#protected-operation)
- [utxoIDs](api_avm_operations.transferableoperation#protected-utxoids)

### Methods

- [deserialize](api_avm_operations.transferableoperation#deserialize)
- [fromBuffer](api_avm_operations.transferableoperation#frombuffer)
- [getAssetID](api_avm_operations.transferableoperation#getassetid)
- [getCodecID](api_avm_operations.transferableoperation#getcodecid)
- [getOperation](api_avm_operations.transferableoperation#getoperation)
- [getTypeID](api_avm_operations.transferableoperation#gettypeid)
- [getTypeName](api_avm_operations.transferableoperation#gettypename)
- [getUTXOIDs](api_avm_operations.transferableoperation#getutxoids)
- [sanitizeObject](api_avm_operations.transferableoperation#sanitizeobject)
- [serialize](api_avm_operations.transferableoperation#serialize)
- [toBuffer](api_avm_operations.transferableoperation#tobuffer)
- [comparator](api_avm_operations.transferableoperation#static-comparator)

## Constructors

### constructor

\+ **new TransferableOperation**(`assetID`: Buffer, `utxoids`: [UTXOID](api_avm_operations.utxoid)[] | string[] | Buffer[], `operation`: [Operation](api_avm_operations.operation)): _[TransferableOperation](api_avm_operations.transferableoperation)_

_Defined in [src/apis/avm/ops.ts:289](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L289)_

**Parameters:**

| Name        | Type                                                                  | Default   |
| ----------- | --------------------------------------------------------------------- | --------- |
| `assetID`   | Buffer                                                                | undefined |
| `utxoids`   | [UTXOID](api_avm_operations.utxoid)[] &#124; string[] &#124; Buffer[] | undefined |
| `operation` | [Operation](api_avm_operations.operation)                             | undefined |

**Returns:** _[TransferableOperation](api_avm_operations.transferableoperation)_

## Properties

### `Protected` \_codecID

• **\_codecID**: _number_ = undefined

_Inherited from [SigIdx](common_signature.sigidx).[\_codecID](common_signature.sigidx#protected-_codecid)_

_Defined in [src/utils/serialization.ts:51](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/serialization.ts#L51)_

---

### `Protected` \_typeID

• **\_typeID**: _any_ = undefined

_Overrides [Serializable](utils_serialization.serializable).[\_typeID](utils_serialization.serializable#protected-_typeid)_

_Defined in [src/apis/avm/ops.ts:187](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L187)_

---

### `Protected` \_typeName

• **\_typeName**: _string_ = "TransferableOperation"

_Overrides [Serializable](utils_serialization.serializable).[\_typeName](utils_serialization.serializable#protected-_typename)_

_Defined in [src/apis/avm/ops.ts:186](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L186)_

---

### `Protected` assetID

• **assetID**: _Buffer_ = Buffer.alloc(32)

_Defined in [src/apis/avm/ops.ts:216](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L216)_

---

### `Protected` operation

• **operation**: _[Operation](api_avm_operations.operation)_

_Defined in [src/apis/avm/ops.ts:218](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L218)_

---

### `Protected` utxoIDs

• **utxoIDs**: _[UTXOID](api_avm_operations.utxoid)[]_ = []

_Defined in [src/apis/avm/ops.ts:217](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L217)_

## Methods

### deserialize

▸ **deserialize**(`fields`: object, `encoding`: [SerializedEncoding](../modules/utils_serialization#serializedencoding)): _void_

_Overrides [StandardParseableInput](common_inputs.standardparseableinput).[deserialize](common_inputs.standardparseableinput#deserialize)_

_Defined in [src/apis/avm/ops.ts:198](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L198)_

**Parameters:**

| Name       | Type                                                                    | Default |
| ---------- | ----------------------------------------------------------------------- | ------- |
| `fields`   | object                                                                  | -       |
| `encoding` | [SerializedEncoding](../modules/utils_serialization#serializedencoding) | "hex"   |

**Returns:** _void_

---

### fromBuffer

▸ **fromBuffer**(`bytes`: Buffer, `offset`: number): _number_

_Defined in [src/apis/avm/ops.ts:249](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L249)_

**Parameters:**

| Name     | Type   | Default |
| -------- | ------ | ------- |
| `bytes`  | Buffer | -       |
| `offset` | number | 0       |

**Returns:** _number_

---

### getAssetID

▸ **getAssetID**(): _Buffer_

_Defined in [src/apis/avm/ops.ts:237](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L237)_

Returns the assetID as a [Buffer](https://github.com/feross/buffer).

**Returns:** _Buffer_

---

### getCodecID

▸ **getCodecID**(): _number_

_Inherited from [SigIdx](common_signature.sigidx).[getCodecID](common_signature.sigidx#getcodecid)_

_Defined in [src/utils/serialization.ts:70](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/serialization.ts#L70)_

Used in serialization. Optional. TypeID is a number for the typeID of object being output.

**Returns:** _number_

---

### getOperation

▸ **getOperation**(): _[Operation](api_avm_operations.operation)_

_Defined in [src/apis/avm/ops.ts:247](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L247)_

Returns the operation

**Returns:** _[Operation](api_avm_operations.operation)_

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

### getUTXOIDs

▸ **getUTXOIDs**(): _[UTXOID](api_avm_operations.utxoid)[]_

_Defined in [src/apis/avm/ops.ts:242](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L242)_

Returns an array of UTXOIDs in this operation.

**Returns:** _[UTXOID](api_avm_operations.utxoid)[]_

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

_Defined in [src/apis/avm/ops.ts:189](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L189)_

**Parameters:**

| Name       | Type                                                                    | Default |
| ---------- | ----------------------------------------------------------------------- | ------- |
| `encoding` | [SerializedEncoding](../modules/utils_serialization#serializedencoding) | "hex"   |

**Returns:** _object_

---

### toBuffer

▸ **toBuffer**(): _Buffer_

_Defined in [src/apis/avm/ops.ts:270](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L270)_

**Returns:** _Buffer_

---

### `Static` comparator

▸ **comparator**(): _function_

_Defined in [src/apis/avm/ops.ts:223](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L223)_

Returns a function used to sort an array of [TransferableOperation](api_avm_operations.transferableoperation)s

**Returns:** _function_

▸ (`a`: [TransferableOperation](api_avm_operations.transferableoperation), `b`: [TransferableOperation](api_avm_operations.transferableoperation)): _1 | -1 | 0_

**Parameters:**

| Name | Type                                                              |
| ---- | ----------------------------------------------------------------- |
| `a`  | [TransferableOperation](api_avm_operations.transferableoperation) |
| `b`  | [TransferableOperation](api_avm_operations.transferableoperation) |
