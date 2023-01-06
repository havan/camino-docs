# Class: NFTMintOperation

An [Operation](api_avm_operations.operation) class which specifies a NFT Mint Op.

## Hierarchy

↳ [Operation](api_avm_operations.operation)

↳ **NFTMintOperation**

## Index

### Constructors

- [constructor](api_avm_operations.nftmintoperation#constructor)

### Properties

- [\_codecID](api_avm_operations.nftmintoperation#protected-_codecid)
- [\_typeID](api_avm_operations.nftmintoperation#protected-_typeid)
- [\_typeName](api_avm_operations.nftmintoperation#protected-_typename)
- [groupID](api_avm_operations.nftmintoperation#protected-groupid)
- [outputOwners](api_avm_operations.nftmintoperation#protected-outputowners)
- [payload](api_avm_operations.nftmintoperation#protected-payload)
- [sigCount](api_avm_operations.nftmintoperation#protected-sigcount)
- [sigIdxs](api_avm_operations.nftmintoperation#protected-sigidxs)

### Methods

- [addSignatureIdx](api_avm_operations.nftmintoperation#addsignatureidx)
- [deserialize](api_avm_operations.nftmintoperation#deserialize)
- [fromBuffer](api_avm_operations.nftmintoperation#frombuffer)
- [getCodecID](api_avm_operations.nftmintoperation#getcodecid)
- [getCredentialID](api_avm_operations.nftmintoperation#getcredentialid)
- [getGroupID](api_avm_operations.nftmintoperation#getgroupid)
- [getOperationID](api_avm_operations.nftmintoperation#getoperationid)
- [getOutputOwners](api_avm_operations.nftmintoperation#getoutputowners)
- [getPayload](api_avm_operations.nftmintoperation#getpayload)
- [getPayloadBuffer](api_avm_operations.nftmintoperation#getpayloadbuffer)
- [getSigIdxs](api_avm_operations.nftmintoperation#getsigidxs)
- [getTypeID](api_avm_operations.nftmintoperation#gettypeid)
- [getTypeName](api_avm_operations.nftmintoperation#gettypename)
- [sanitizeObject](api_avm_operations.nftmintoperation#sanitizeobject)
- [serialize](api_avm_operations.nftmintoperation#serialize)
- [setCodecID](api_avm_operations.nftmintoperation#setcodecid)
- [toBuffer](api_avm_operations.nftmintoperation#tobuffer)
- [toString](api_avm_operations.nftmintoperation#tostring)
- [comparator](api_avm_operations.nftmintoperation#static-comparator)

## Constructors

### constructor

\+ **new NFTMintOperation**(`groupID`: number, `payload`: Buffer, `outputOwners`: [OutputOwners](common_output.outputowners)[]): _[NFTMintOperation](api_avm_operations.nftmintoperation)_

_Defined in [src/apis/avm/ops.ts:641](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L641)_

An [Operation](api_avm_operations.operation) class which contains an NFT on an assetID.

**Parameters:**

| Name           | Type                                         | Default   | Description                                                     |
| -------------- | -------------------------------------------- | --------- | --------------------------------------------------------------- |
| `groupID`      | number                                       | undefined | The group to which to issue the NFT Output                      |
| `payload`      | Buffer                                       | undefined | A [Buffer](https://github.com/feross/buffer) of the NFT payload |
| `outputOwners` | [OutputOwners](common_output.outputowners)[] | undefined | An array of outputOwners                                        |

**Returns:** _[NFTMintOperation](api_avm_operations.nftmintoperation)_

## Properties

### `Protected` \_codecID

• **\_codecID**: _number_ = AVMConstants.LATESTCODEC

_Overrides [SigIdx](common_signature.sigidx).[\_codecID](common_signature.sigidx#protected-_codecid)_

_Defined in [src/apis/avm/ops.ts:454](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L454)_

---

### `Protected` \_typeID

• **\_typeID**: _number_ = this.\_codecID === 0
? AVMConstants.NFTMINTOPID
: AVMConstants.NFTMINTOPID_CODECONE

_Overrides [Operation](api_avm_operations.operation).[\_typeID](api_avm_operations.operation#protected-_typeid)_

_Defined in [src/apis/avm/ops.ts:455](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L455)_

---

### `Protected` \_typeName

• **\_typeName**: _string_ = "NFTMintOperation"

_Overrides [Operation](api_avm_operations.operation).[\_typeName](api_avm_operations.operation#protected-_typename)_

_Defined in [src/apis/avm/ops.ts:453](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L453)_

---

### `Protected` groupID

• **groupID**: _Buffer_ = Buffer.alloc(4)

_Defined in [src/apis/avm/ops.ts:504](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L504)_

---

### `Protected` outputOwners

• **outputOwners**: _[OutputOwners](common_output.outputowners)[]_ = []

_Defined in [src/apis/avm/ops.ts:506](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L506)_

---

### `Protected` payload

• **payload**: _Buffer_

_Defined in [src/apis/avm/ops.ts:505](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L505)_

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

_Defined in [src/apis/avm/ops.ts:475](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L475)_

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

_Defined in [src/apis/avm/ops.ts:578](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L578)_

Popuates the instance from a [Buffer](https://github.com/feross/buffer) representing the [NFTMintOperation](api_avm_operations.nftmintoperation) and returns the updated offset.

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

_Defined in [src/apis/avm/ops.ts:537](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L537)_

Returns the credential ID.

**Returns:** _number_

---

### getGroupID

▸ **getGroupID**(): _Buffer_

_Defined in [src/apis/avm/ops.ts:548](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L548)_

Returns the payload.

**Returns:** _Buffer_

---

### getOperationID

▸ **getOperationID**(): _number_

_Overrides [Operation](api_avm_operations.operation).[getOperationID](api_avm_operations.operation#abstract-getoperationid)_

_Defined in [src/apis/avm/ops.ts:530](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L530)_

Returns the operation ID.

**Returns:** _number_

---

### getOutputOwners

▸ **getOutputOwners**(): _[OutputOwners](common_output.outputowners)[]_

_Defined in [src/apis/avm/ops.ts:571](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L571)_

Returns the outputOwners.

**Returns:** _[OutputOwners](common_output.outputowners)[]_

---

### getPayload

▸ **getPayload**(): _Buffer_

_Defined in [src/apis/avm/ops.ts:555](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L555)_

Returns the payload.

**Returns:** _Buffer_

---

### getPayloadBuffer

▸ **getPayloadBuffer**(): _Buffer_

_Defined in [src/apis/avm/ops.ts:562](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L562)_

Returns the payload's raw [Buffer](https://github.com/feross/buffer) with length prepended, for use with [PayloadBase](utils_payload.payloadbase)'s fromBuffer

**Returns:** _Buffer_

---

### getSigIdxs

▸ **getSigIdxs**(): _[SigIdx](common_signature.sigidx)[]_

_Inherited from [Operation](api_avm_operations.operation).[getSigIdxs](api_avm_operations.operation#getsigidxs)_

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

_Overrides [Operation](api_avm_operations.operation).[serialize](api_avm_operations.operation#serialize)_

_Defined in [src/apis/avm/ops.ts:460](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L460)_

**Parameters:**

| Name       | Type                                                                    | Default |
| ---------- | ----------------------------------------------------------------------- | ------- |
| `encoding` | [SerializedEncoding](../modules/utils_serialization#serializedencoding) | "hex"   |

**Returns:** _object_

---

### setCodecID

▸ **setCodecID**(`codecID`: number): _void_

_Defined in [src/apis/avm/ops.ts:513](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L513)_

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

_Defined in [src/apis/avm/ops.ts:604](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L604)_

Returns the buffer representing the [NFTMintOperation](api_avm_operations.nftmintoperation) instance.

**Returns:** _Buffer_

---

### toString

▸ **toString**(): _string_

_Overrides [Operation](api_avm_operations.operation).[toString](api_avm_operations.operation#tostring)_

_Defined in [src/apis/avm/ops.ts:639](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L639)_

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
