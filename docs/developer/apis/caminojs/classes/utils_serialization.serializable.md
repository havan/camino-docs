# Class: Serializable

## Hierarchy

- **Serializable**

  ↳ [Credential](common_signature.credential)

  ↳ [Input](common_inputs.input)

  ↳ [StandardParseableInput](common_inputs.standardparseableinput)

  ↳ [EVMStandardBaseTx](common_transactions.evmstandardbasetx)

  ↳ [EVMStandardUnsignedTx](common_transactions.evmstandardunsignedtx)

  ↳ [EVMStandardTx](common_transactions.evmstandardtx)

  ↳ [StandardBaseTx](common_transactions.standardbasetx)

  ↳ [StandardUnsignedTx](common_transactions.standardunsignedtx)

  ↳ [StandardTx](common_transactions.standardtx)

  ↳ [StandardUTXO](common_utxos.standardutxo)

  ↳ [StandardUTXOSet](common_utxos.standardutxoset)

  ↳ [NBytes](common_nbytes.nbytes)

  ↳ [OutputOwners](common_output.outputowners)

  ↳ [StandardParseableOutput](common_output.standardparseableoutput)

  ↳ [InitialStates](api_avm_initialstates.initialstates)

  ↳ [Operation](api_avm_operations.operation)

  ↳ [TransferableOperation](api_avm_operations.transferableoperation)

  ↳ [MinterSet](api_avm_minterset.minterset)

  ↳ [Vertex](api_avm_vertex.vertex)

  ↳ [GenesisData](api_avm_genesisdata.genesisdata)

  ↳ [SubnetAuth](api_platformvm_subnetauth.subnetauth)

## Index

### Properties

- [\_codecID](utils_serialization.serializable#protected-_codecid)
- [\_typeID](utils_serialization.serializable#protected-_typeid)
- [\_typeName](utils_serialization.serializable#protected-_typename)

### Methods

- [deserialize](utils_serialization.serializable#deserialize)
- [getCodecID](utils_serialization.serializable#getcodecid)
- [getTypeID](utils_serialization.serializable#gettypeid)
- [getTypeName](utils_serialization.serializable#gettypename)
- [sanitizeObject](utils_serialization.serializable#sanitizeobject)
- [serialize](utils_serialization.serializable#serialize)

## Properties

### `Protected` \_codecID

• **\_codecID**: _number_ = undefined

_Defined in [src/utils/serialization.ts:51](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/serialization.ts#L51)_

---

### `Protected` \_typeID

• **\_typeID**: _number_ = undefined

_Defined in [src/utils/serialization.ts:50](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/serialization.ts#L50)_

---

### `Protected` \_typeName

• **\_typeName**: _string_ = undefined

_Defined in [src/utils/serialization.ts:49](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/serialization.ts#L49)_

## Methods

### deserialize

▸ **deserialize**(`fields`: object, `encoding?`: [SerializedEncoding](../modules/utils_serialization#serializedencoding)): _void_

_Defined in [src/utils/serialization.ts:97](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/serialization.ts#L97)_

**Parameters:**

| Name        | Type                                                                    |
| ----------- | ----------------------------------------------------------------------- |
| `fields`    | object                                                                  |
| `encoding?` | [SerializedEncoding](../modules/utils_serialization#serializedencoding) |

**Returns:** _void_

---

### getCodecID

▸ **getCodecID**(): _number_

_Defined in [src/utils/serialization.ts:70](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/serialization.ts#L70)_

Used in serialization. Optional. TypeID is a number for the typeID of object being output.

**Returns:** _number_

---

### getTypeID

▸ **getTypeID**(): _number_

_Defined in [src/utils/serialization.ts:63](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/serialization.ts#L63)_

Used in serialization. Optional. TypeID is a number for the typeID of object being output.

**Returns:** _number_

---

### getTypeName

▸ **getTypeName**(): _string_

_Defined in [src/utils/serialization.ts:56](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/serialization.ts#L56)_

Used in serialization. TypeName is a string name for the type of object being output.

**Returns:** _string_

---

### sanitizeObject

▸ **sanitizeObject**(`obj`: object): _object_

_Defined in [src/utils/serialization.ts:77](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/serialization.ts#L77)_

Sanitize to prevent cross scripting attacks.

**Parameters:**

| Name  | Type   |
| ----- | ------ |
| `obj` | object |

**Returns:** _object_

---

### serialize

▸ **serialize**(`encoding?`: [SerializedEncoding](../modules/utils_serialization#serializedencoding)): _object_

_Defined in [src/utils/serialization.ts:90](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/serialization.ts#L90)_

**Parameters:**

| Name        | Type                                                                    |
| ----------- | ----------------------------------------------------------------------- |
| `encoding?` | [SerializedEncoding](../modules/utils_serialization#serializedencoding) |

**Returns:** _object_
