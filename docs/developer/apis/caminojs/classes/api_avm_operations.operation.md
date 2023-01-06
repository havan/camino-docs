# Class: Operation

A class representing an operation. All operation types must extend on this class.

## Hierarchy

- [Serializable](utils_serialization.serializable)

  ↳ **Operation**

  ↳ [SECPMintOperation](api_avm_operations.secpmintoperation)

  ↳ [NFTMintOperation](api_avm_operations.nftmintoperation)

  ↳ [NFTTransferOperation](api_avm_operations.nfttransferoperation)

## Index

### Properties

- [\_codecID](api_avm_operations.operation#protected-_codecid)
- [\_typeID](api_avm_operations.operation#protected-_typeid)
- [\_typeName](api_avm_operations.operation#protected-_typename)
- [sigCount](api_avm_operations.operation#protected-sigcount)
- [sigIdxs](api_avm_operations.operation#protected-sigidxs)

### Methods

- [addSignatureIdx](api_avm_operations.operation#addsignatureidx)
- [deserialize](api_avm_operations.operation#deserialize)
- [fromBuffer](api_avm_operations.operation#frombuffer)
- [getCodecID](api_avm_operations.operation#getcodecid)
- [getCredentialID](api_avm_operations.operation#abstract-getcredentialid)
- [getOperationID](api_avm_operations.operation#abstract-getoperationid)
- [getSigIdxs](api_avm_operations.operation#getsigidxs)
- [getTypeID](api_avm_operations.operation#gettypeid)
- [getTypeName](api_avm_operations.operation#gettypename)
- [sanitizeObject](api_avm_operations.operation#sanitizeobject)
- [serialize](api_avm_operations.operation#serialize)
- [toBuffer](api_avm_operations.operation#tobuffer)
- [toString](api_avm_operations.operation#tostring)
- [comparator](api_avm_operations.operation#static-comparator)

## Properties

### `Protected` \_codecID

• **\_codecID**: _number_ = undefined

_Inherited from [SigIdx](common_signature.sigidx).[\_codecID](common_signature.sigidx#protected-_codecid)_

_Defined in [src/utils/serialization.ts:51](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/serialization.ts#L51)_

---

### `Protected` \_typeID

• **\_typeID**: _any_ = undefined

_Overrides [Serializable](utils_serialization.serializable).[\_typeID](utils_serialization.serializable#protected-_typeid)_

_Defined in [src/apis/avm/ops.ts:74](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L74)_

---

### `Protected` \_typeName

• **\_typeName**: _string_ = "Operation"

_Overrides [Serializable](utils_serialization.serializable).[\_typeName](utils_serialization.serializable#protected-_typename)_

_Defined in [src/apis/avm/ops.ts:73](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L73)_

---

### `Protected` sigCount

• **sigCount**: _Buffer_ = Buffer.alloc(4)

_Defined in [src/apis/avm/ops.ts:93](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L93)_

---

### `Protected` sigIdxs

• **sigIdxs**: _[SigIdx](common_signature.sigidx)[]_ = []

_Defined in [src/apis/avm/ops.ts:94](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L94)_

## Methods

### addSignatureIdx

▸ **addSignatureIdx**(`addressIdx`: number, `address`: Buffer): _void_

_Defined in [src/apis/avm/ops.ts:136](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L136)_

Creates and adds a [SigIdx](common_signature.sigidx) to the [Operation](api_avm_operations.operation).

**Parameters:**

| Name         | Type   | Description                                             |
| ------------ | ------ | ------------------------------------------------------- |
| `addressIdx` | number | The index of the address to reference in the signatures |
| `address`    | Buffer | The address of the source of the signature              |

**Returns:** _void_

---

### deserialize

▸ **deserialize**(`fields`: object, `encoding`: [SerializedEncoding](../modules/utils_serialization#serializedencoding)): _void_

_Overrides [StandardParseableInput](common_inputs.standardparseableinput).[deserialize](common_inputs.standardparseableinput#deserialize)_

_Defined in [src/apis/avm/ops.ts:83](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L83)_

**Parameters:**

| Name       | Type                                                                    | Default |
| ---------- | ----------------------------------------------------------------------- | ------- |
| `fields`   | object                                                                  | -       |
| `encoding` | [SerializedEncoding](../modules/utils_serialization#serializedencoding) | "hex"   |

**Returns:** _void_

---

### fromBuffer

▸ **fromBuffer**(`bytes`: Buffer, `offset`: number): _number_

_Defined in [src/apis/avm/ops.ts:146](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L146)_

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

### `Abstract` getCredentialID

▸ **getCredentialID**(): _number_

_Defined in [src/apis/avm/ops.ts:128](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L128)_

Returns the credential ID.

**Returns:** _number_

---

### `Abstract` getOperationID

▸ **getOperationID**(): _number_

_Defined in [src/apis/avm/ops.ts:118](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L118)_

**Returns:** _number_

---

### getSigIdxs

▸ **getSigIdxs**(): _[SigIdx](common_signature.sigidx)[]_

_Defined in [src/apis/avm/ops.ts:123](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L123)_

Returns the array of [SigIdx](common_signature.sigidx) for this [Operation](api_avm_operations.operation)

**Returns:** _[SigIdx](common_signature.sigidx)[]_

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

_Defined in [src/apis/avm/ops.ts:76](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L76)_

**Parameters:**

| Name       | Type                                                                    | Default |
| ---------- | ----------------------------------------------------------------------- | ------- |
| `encoding` | [SerializedEncoding](../modules/utils_serialization#serializedencoding) | "hex"   |

**Returns:** _object_

---

### toBuffer

▸ **toBuffer**(): _Buffer_

_Defined in [src/apis/avm/ops.ts:161](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L161)_

**Returns:** _Buffer_

---

### toString

▸ **toString**(): _string_

_Defined in [src/apis/avm/ops.ts:176](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L176)_

Returns a base-58 string representing the [NFTMintOperation](api_avm_operations.nftmintoperation).

**Returns:** _string_

---

### `Static` comparator

▸ **comparator**(): _function_

_Defined in [src/apis/avm/ops.ts:96](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L96)_

**Returns:** _function_

▸ (`a`: [Operation](api_avm_operations.operation), `b`: [Operation](api_avm_operations.operation)): _1 | -1 | 0_

**Parameters:**

| Name | Type                                      |
| ---- | ----------------------------------------- |
| `a`  | [Operation](api_avm_operations.operation) |
| `b`  | [Operation](api_avm_operations.operation) |
