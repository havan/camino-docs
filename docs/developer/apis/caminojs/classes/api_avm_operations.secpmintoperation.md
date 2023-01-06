# Class: SECPMintOperation

An [Operation](api_avm_operations.operation) class which specifies a SECP256k1 Mint Op.

## Hierarchy

↳ [Operation](api_avm_operations.operation)

↳ **SECPMintOperation**

## Index

### Constructors

- [constructor](api_avm_operations.secpmintoperation#constructor)

### Properties

- [\_codecID](api_avm_operations.secpmintoperation#protected-_codecid)
- [\_typeID](api_avm_operations.secpmintoperation#protected-_typeid)
- [\_typeName](api_avm_operations.secpmintoperation#protected-_typename)
- [mintOutput](api_avm_operations.secpmintoperation#protected-mintoutput)
- [sigCount](api_avm_operations.secpmintoperation#protected-sigcount)
- [sigIdxs](api_avm_operations.secpmintoperation#protected-sigidxs)
- [transferOutput](api_avm_operations.secpmintoperation#protected-transferoutput)

### Methods

- [addSignatureIdx](api_avm_operations.secpmintoperation#addsignatureidx)
- [deserialize](api_avm_operations.secpmintoperation#deserialize)
- [fromBuffer](api_avm_operations.secpmintoperation#frombuffer)
- [getCodecID](api_avm_operations.secpmintoperation#getcodecid)
- [getCredentialID](api_avm_operations.secpmintoperation#getcredentialid)
- [getMintOutput](api_avm_operations.secpmintoperation#getmintoutput)
- [getOperationID](api_avm_operations.secpmintoperation#getoperationid)
- [getSigIdxs](api_avm_operations.secpmintoperation#getsigidxs)
- [getTransferOutput](api_avm_operations.secpmintoperation#gettransferoutput)
- [getTypeID](api_avm_operations.secpmintoperation#gettypeid)
- [getTypeName](api_avm_operations.secpmintoperation#gettypename)
- [sanitizeObject](api_avm_operations.secpmintoperation#sanitizeobject)
- [serialize](api_avm_operations.secpmintoperation#serialize)
- [setCodecID](api_avm_operations.secpmintoperation#setcodecid)
- [toBuffer](api_avm_operations.secpmintoperation#tobuffer)
- [toString](api_avm_operations.secpmintoperation#tostring)
- [comparator](api_avm_operations.secpmintoperation#static-comparator)

## Constructors

### constructor

\+ **new SECPMintOperation**(`mintOutput`: [SECPMintOutput](api_avm_outputs.secpmintoutput), `transferOutput`: [SECPTransferOutput](api_avm_outputs.secptransferoutput)): _[SECPMintOperation](api_avm_operations.secpmintoperation)_

_Defined in [src/apis/avm/ops.ts:427](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L427)_

An [Operation](api_avm_operations.operation) class which mints new tokens on an assetID.

**Parameters:**

| Name             | Type                                                     | Default   | Description                                                                                                   |
| ---------------- | -------------------------------------------------------- | --------- | ------------------------------------------------------------------------------------------------------------- |
| `mintOutput`     | [SECPMintOutput](api_avm_outputs.secpmintoutput)         | undefined | The [SECPMintOutput](api_avm_outputs.secpmintoutput) that will be produced by this transaction.               |
| `transferOutput` | [SECPTransferOutput](api_avm_outputs.secptransferoutput) | undefined | A [SECPTransferOutput](api_evm_outputs.secptransferoutput) that will be produced from this minting operation. |

**Returns:** _[SECPMintOperation](api_avm_operations.secpmintoperation)_

## Properties

### `Protected` \_codecID

• **\_codecID**: _number_ = AVMConstants.LATESTCODEC

_Overrides [SigIdx](common_signature.sigidx).[\_codecID](common_signature.sigidx#protected-_codecid)_

_Defined in [src/apis/avm/ops.ts:326](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L326)_

---

### `Protected` \_typeID

• **\_typeID**: _number_ = this.\_codecID === 0
? AVMConstants.SECPMINTOPID
: AVMConstants.SECPMINTOPID_CODECONE

_Overrides [Operation](api_avm_operations.operation).[\_typeID](api_avm_operations.operation#protected-_typeid)_

_Defined in [src/apis/avm/ops.ts:327](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L327)_

---

### `Protected` \_typeName

• **\_typeName**: _string_ = "SECPMintOperation"

_Overrides [Operation](api_avm_operations.operation).[\_typeName](api_avm_operations.operation#protected-_typename)_

_Defined in [src/apis/avm/ops.ts:325](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L325)_

---

### `Protected` mintOutput

• **mintOutput**: _[SECPMintOutput](api_avm_outputs.secpmintoutput)_ = undefined

_Defined in [src/apis/avm/ops.ts:348](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L348)_

---

### `Protected` sigCount

• **sigCount**: _Buffer_ = Buffer.alloc(4)

_Inherited from [Operation](api_avm_operations.operation).[sigCount](api_avm_operations.operation#protected-sigcount)_

_Defined in [src/apis/avm/ops.ts:93](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L93)_

---

### `Protected` sigIdxs

• **sigIdxs**: _[SigIdx](common_signature.sigidx)[]_ = []

_Inherited from [Operation](api_avm_operations.operation).[sigIdxs](api_avm_operations.operation#protected-sigidxs)_

_Defined in [src/apis/avm/ops.ts:94](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L94)_

---

### `Protected` transferOutput

• **transferOutput**: _[SECPTransferOutput](api_avm_outputs.secptransferoutput)_ = undefined

_Defined in [src/apis/avm/ops.ts:349](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L349)_

## Methods

### addSignatureIdx

▸ **addSignatureIdx**(`addressIdx`: number, `address`: Buffer): _void_

_Inherited from [Operation](api_avm_operations.operation).[addSignatureIdx](api_avm_operations.operation#addsignatureidx)_

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

_Overrides [Operation](api_avm_operations.operation).[deserialize](api_avm_operations.operation#deserialize)_

_Defined in [src/apis/avm/ops.ts:340](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L340)_

**Parameters:**

| Name       | Type                                                                    | Default |
| ---------- | ----------------------------------------------------------------------- | ------- |
| `fields`   | object                                                                  | -       |
| `encoding` | [SerializedEncoding](../modules/utils_serialization#serializedencoding) | "hex"   |

**Returns:** _void_

---

### fromBuffer

▸ **fromBuffer**(`bytes`: Buffer, `offset`: number): _number_

_Overrides [Operation](api_avm_operations.operation).[fromBuffer](api_avm_operations.operation#frombuffer)_

_Defined in [src/apis/avm/ops.ts:405](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L405)_

Popuates the instance from a [Buffer](https://github.com/feross/buffer) representing the [SECPMintOperation](api_avm_operations.secpmintoperation) and returns the updated offset.

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

### getCredentialID

▸ **getCredentialID**(): _number_

_Overrides [Operation](api_avm_operations.operation).[getCredentialID](api_avm_operations.operation#abstract-getcredentialid)_

_Defined in [src/apis/avm/ops.ts:380](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L380)_

Returns the credential ID.

**Returns:** _number_

---

### getMintOutput

▸ **getMintOutput**(): _[SECPMintOutput](api_avm_outputs.secpmintoutput)_

_Defined in [src/apis/avm/ops.ts:391](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L391)_

Returns the [SECPMintOutput](api_avm_outputs.secpmintoutput) to be produced by this operation.

**Returns:** _[SECPMintOutput](api_avm_outputs.secpmintoutput)_

---

### getOperationID

▸ **getOperationID**(): _number_

_Overrides [Operation](api_avm_operations.operation).[getOperationID](api_avm_operations.operation#abstract-getoperationid)_

_Defined in [src/apis/avm/ops.ts:373](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L373)_

Returns the operation ID.

**Returns:** _number_

---

### getSigIdxs

▸ **getSigIdxs**(): _[SigIdx](common_signature.sigidx)[]_

_Inherited from [Operation](api_avm_operations.operation).[getSigIdxs](api_avm_operations.operation#getsigidxs)_

_Defined in [src/apis/avm/ops.ts:123](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L123)_

Returns the array of [SigIdx](common_signature.sigidx) for this [Operation](api_avm_operations.operation)

**Returns:** _[SigIdx](common_signature.sigidx)[]_

---

### getTransferOutput

▸ **getTransferOutput**(): _[SECPTransferOutput](api_avm_outputs.secptransferoutput)_

_Defined in [src/apis/avm/ops.ts:398](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L398)_

Returns [SECPTransferOutput](api_evm_outputs.secptransferoutput) to be produced by this operation.

**Returns:** _[SECPTransferOutput](api_avm_outputs.secptransferoutput)_

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

_Overrides [Operation](api_avm_operations.operation).[serialize](api_avm_operations.operation#serialize)_

_Defined in [src/apis/avm/ops.ts:332](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L332)_

**Parameters:**

| Name       | Type                                                                    | Default |
| ---------- | ----------------------------------------------------------------------- | ------- |
| `encoding` | [SerializedEncoding](../modules/utils_serialization#serializedencoding) | "hex"   |

**Returns:** _object_

---

### setCodecID

▸ **setCodecID**(`codecID`: number): _void_

_Defined in [src/apis/avm/ops.ts:356](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L356)_

Set the codecID

**Parameters:**

| Name      | Type   | Description        |
| --------- | ------ | ------------------ |
| `codecID` | number | The codecID to set |

**Returns:** _void_

---

### toBuffer

▸ **toBuffer**(): _Buffer_

_Overrides [Operation](api_avm_operations.operation).[toBuffer](api_avm_operations.operation#tobuffer)_

_Defined in [src/apis/avm/ops.ts:417](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L417)_

Returns the buffer representing the [SECPMintOperation](api_avm_operations.secpmintoperation) instance.

**Returns:** _Buffer_

---

### toString

▸ **toString**(): _string_

_Inherited from [Operation](api_avm_operations.operation).[toString](api_avm_operations.operation#tostring)_

_Defined in [src/apis/avm/ops.ts:176](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L176)_

Returns a base-58 string representing the [NFTMintOperation](api_avm_operations.nftmintoperation).

**Returns:** _string_

---

### `Static` comparator

▸ **comparator**(): _function_

_Inherited from [Operation](api_avm_operations.operation).[comparator](api_avm_operations.operation#static-comparator)_

_Defined in [src/apis/avm/ops.ts:96](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L96)_

**Returns:** _function_

▸ (`a`: [Operation](api_avm_operations.operation), `b`: [Operation](api_avm_operations.operation)): _1 | -1 | 0_

**Parameters:**

| Name | Type                                      |
| ---- | ----------------------------------------- |
| `a`  | [Operation](api_avm_operations.operation) |
| `b`  | [Operation](api_avm_operations.operation) |
