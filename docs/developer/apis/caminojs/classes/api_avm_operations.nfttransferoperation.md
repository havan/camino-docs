# Class: NFTTransferOperation

A [Operation](api_avm_operations.operation) class which specifies a NFT Transfer Op.

## Hierarchy

↳ [Operation](api_avm_operations.operation)

↳ **NFTTransferOperation**

## Index

### Constructors

- [constructor](api_avm_operations.nfttransferoperation#constructor)

### Properties

- [\_codecID](api_avm_operations.nfttransferoperation#protected-_codecid)
- [\_typeID](api_avm_operations.nfttransferoperation#protected-_typeid)
- [\_typeName](api_avm_operations.nfttransferoperation#protected-_typename)
- [output](api_avm_operations.nfttransferoperation#protected-output)
- [sigCount](api_avm_operations.nfttransferoperation#protected-sigcount)
- [sigIdxs](api_avm_operations.nfttransferoperation#protected-sigidxs)

### Methods

- [addSignatureIdx](api_avm_operations.nfttransferoperation#addsignatureidx)
- [deserialize](api_avm_operations.nfttransferoperation#deserialize)
- [fromBuffer](api_avm_operations.nfttransferoperation#frombuffer)
- [getCodecID](api_avm_operations.nfttransferoperation#getcodecid)
- [getCredentialID](api_avm_operations.nfttransferoperation#getcredentialid)
- [getOperationID](api_avm_operations.nfttransferoperation#getoperationid)
- [getOutput](api_avm_operations.nfttransferoperation#getoutput)
- [getSigIdxs](api_avm_operations.nfttransferoperation#getsigidxs)
- [getTypeID](api_avm_operations.nfttransferoperation#gettypeid)
- [getTypeName](api_avm_operations.nfttransferoperation#gettypename)
- [sanitizeObject](api_avm_operations.nfttransferoperation#sanitizeobject)
- [serialize](api_avm_operations.nfttransferoperation#serialize)
- [setCodecID](api_avm_operations.nfttransferoperation#setcodecid)
- [toBuffer](api_avm_operations.nfttransferoperation#tobuffer)
- [toString](api_avm_operations.nfttransferoperation#tostring)
- [comparator](api_avm_operations.nfttransferoperation#static-comparator)

## Constructors

### constructor

\+ **new NFTTransferOperation**(`output`: [NFTTransferOutput](api_avm_outputs.nfttransferoutput)): _[NFTTransferOperation](api_avm_operations.nfttransferoperation)_

_Defined in [src/apis/avm/ops.ts:758](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L758)_

An [Operation](api_avm_operations.operation) class which contains an NFT on an assetID.

**Parameters:**

| Name     | Type                                                   | Default   | Description                                               |
| -------- | ------------------------------------------------------ | --------- | --------------------------------------------------------- |
| `output` | [NFTTransferOutput](api_avm_outputs.nfttransferoutput) | undefined | An [NFTTransferOutput](api_avm_outputs.nfttransferoutput) |

**Returns:** _[NFTTransferOperation](api_avm_operations.nfttransferoperation)_

## Properties

### `Protected` \_codecID

• **\_codecID**: _number_ = AVMConstants.LATESTCODEC

_Overrides [SigIdx](common_signature.sigidx).[\_codecID](common_signature.sigidx#protected-_codecid)_

_Defined in [src/apis/avm/ops.ts:673](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L673)_

---

### `Protected` \_typeID

• **\_typeID**: _number_ = this.\_codecID === 0
? AVMConstants.NFTXFEROPID
: AVMConstants.NFTXFEROPID_CODECONE

_Overrides [Operation](api_avm_operations.operation).[\_typeID](api_avm_operations.operation#protected-_typeid)_

_Defined in [src/apis/avm/ops.ts:674](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L674)_

---

### `Protected` \_typeName

• **\_typeName**: _string_ = "NFTTransferOperation"

_Overrides [Operation](api_avm_operations.operation).[\_typeName](api_avm_operations.operation#protected-_typename)_

_Defined in [src/apis/avm/ops.ts:672](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L672)_

---

### `Protected` output

• **output**: _[NFTTransferOutput](api_avm_outputs.nfttransferoutput)_

_Defined in [src/apis/avm/ops.ts:692](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L692)_

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

_Defined in [src/apis/avm/ops.ts:686](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L686)_

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

_Defined in [src/apis/avm/ops.ts:736](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L736)_

Popuates the instance from a [Buffer](https://github.com/feross/buffer) representing the [NFTTransferOperation](api_avm_operations.nfttransferoperation) and returns the updated offset.

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

_Defined in [src/apis/avm/ops.ts:723](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L723)_

Returns the credential ID.

**Returns:** _number_

---

### getOperationID

▸ **getOperationID**(): _number_

_Overrides [Operation](api_avm_operations.operation).[getOperationID](api_avm_operations.operation#abstract-getoperationid)_

_Defined in [src/apis/avm/ops.ts:716](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L716)_

Returns the operation ID.

**Returns:** _number_

---

### getOutput

▸ **getOutput**(): _[NFTTransferOutput](api_avm_outputs.nfttransferoutput)_

_Defined in [src/apis/avm/ops.ts:731](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L731)_

**Returns:** _[NFTTransferOutput](api_avm_outputs.nfttransferoutput)_

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

_Defined in [src/apis/avm/ops.ts:679](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L679)_

**Parameters:**

| Name       | Type                                                                    | Default |
| ---------- | ----------------------------------------------------------------------- | ------- |
| `encoding` | [SerializedEncoding](../modules/utils_serialization#serializedencoding) | "hex"   |

**Returns:** _object_

---

### setCodecID

▸ **setCodecID**(`codecID`: number): _void_

_Defined in [src/apis/avm/ops.ts:699](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L699)_

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

_Defined in [src/apis/avm/ops.ts:745](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L745)_

Returns the buffer representing the [NFTTransferOperation](api_avm_operations.nfttransferoperation) instance.

**Returns:** _Buffer_

---

### toString

▸ **toString**(): _string_

_Overrides [Operation](api_avm_operations.operation).[toString](api_avm_operations.operation#tostring)_

_Defined in [src/apis/avm/ops.ts:756](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L756)_

Returns a base-58 string representing the [NFTTransferOperation](api_avm_operations.nfttransferoperation).

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
