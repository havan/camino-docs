# Class: NFTMintOutput

An [Output](../modules/src_common#output) class which specifies an Output that carries an NFT Mint and uses secp256k1 signature scheme.

## Hierarchy

↳ [NFTOutput](api_avm_outputs.nftoutput)

↳ **NFTMintOutput**

## Index

### Constructors

- [constructor](api_avm_outputs.nftmintoutput#constructor)

### Properties

- [\_codecID](api_avm_outputs.nftmintoutput#protected-_codecid)
- [\_typeID](api_avm_outputs.nftmintoutput#protected-_typeid)
- [\_typeName](api_avm_outputs.nftmintoutput#protected-_typename)
- [addresses](api_avm_outputs.nftmintoutput#protected-addresses)
- [groupID](api_avm_outputs.nftmintoutput#protected-groupid)
- [locktime](api_avm_outputs.nftmintoutput#protected-locktime)
- [numaddrs](api_avm_outputs.nftmintoutput#protected-numaddrs)
- [threshold](api_avm_outputs.nftmintoutput#protected-threshold)

### Methods

- [clone](api_avm_outputs.nftmintoutput#clone)
- [create](api_avm_outputs.nftmintoutput#create)
- [deserialize](api_avm_outputs.nftmintoutput#deserialize)
- [fromBuffer](api_avm_outputs.nftmintoutput#frombuffer)
- [getAddress](api_avm_outputs.nftmintoutput#getaddress)
- [getAddressIdx](api_avm_outputs.nftmintoutput#getaddressidx)
- [getAddresses](api_avm_outputs.nftmintoutput#getaddresses)
- [getCodecID](api_avm_outputs.nftmintoutput#getcodecid)
- [getGroupID](api_avm_outputs.nftmintoutput#getgroupid)
- [getLocktime](api_avm_outputs.nftmintoutput#getlocktime)
- [getOutputID](api_avm_outputs.nftmintoutput#getoutputid)
- [getSpenders](api_avm_outputs.nftmintoutput#getspenders)
- [getThreshold](api_avm_outputs.nftmintoutput#getthreshold)
- [getTypeID](api_avm_outputs.nftmintoutput#gettypeid)
- [getTypeName](api_avm_outputs.nftmintoutput#gettypename)
- [makeTransferable](api_avm_outputs.nftmintoutput#maketransferable)
- [meetsThreshold](api_avm_outputs.nftmintoutput#meetsthreshold)
- [sanitizeObject](api_avm_outputs.nftmintoutput#sanitizeobject)
- [select](api_avm_outputs.nftmintoutput#select)
- [serialize](api_avm_outputs.nftmintoutput#serialize)
- [setCodecID](api_avm_outputs.nftmintoutput#setcodecid)
- [toBuffer](api_avm_outputs.nftmintoutput#tobuffer)
- [toString](api_avm_outputs.nftmintoutput#tostring)
- [comparator](api_avm_outputs.nftmintoutput#static-comparator)

## Constructors

### constructor

\+ **new NFTMintOutput**(`groupID`: number, `addresses`: Buffer[], `locktime`: BN, `threshold`: number): _[NFTMintOutput](api_avm_outputs.nftmintoutput)_

_Overrides [OutputOwners](common_output.outputowners).[constructor](common_output.outputowners#constructor)_

_Defined in [src/apis/avm/outputs.ts:299](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/outputs.ts#L299)_

An [Output](../modules/src_common#output) class which contains an NFT mint for an assetID.

**Parameters:**

| Name        | Type     | Default   | Description                                                                                |
| ----------- | -------- | --------- | ------------------------------------------------------------------------------------------ |
| `groupID`   | number   | undefined | A number specifies the group this NFT is issued to                                         |
| `addresses` | Buffer[] | undefined | An array of [Buffer](https://github.com/feross/buffer)s representing addresses             |
| `locktime`  | BN       | undefined | A [BN](https://github.com/indutny/bn.js/) representing the locktime                        |
| `threshold` | number   | undefined | A number representing the the threshold number of signers required to sign the transaction |

**Returns:** _[NFTMintOutput](api_avm_outputs.nftmintoutput)_

## Properties

### `Protected` \_codecID

• **\_codecID**: _number_ = AVMConstants.LATESTCODEC

_Overrides [SigIdx](common_signature.sigidx).[\_codecID](common_signature.sigidx#protected-_codecid)_

_Defined in [src/apis/avm/outputs.ts:238](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/outputs.ts#L238)_

---

### `Protected` \_typeID

• **\_typeID**: _number_ = this.\_codecID === 0
? AVMConstants.NFTMINTOUTPUTID
: AVMConstants.NFTMINTOUTPUTID_CODECONE

_Overrides [NFTOutput](api_avm_outputs.nftoutput).[\_typeID](api_avm_outputs.nftoutput#protected-_typeid)_

_Defined in [src/apis/avm/outputs.ts:239](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/outputs.ts#L239)_

---

### `Protected` \_typeName

• **\_typeName**: _string_ = "NFTMintOutput"

_Overrides [NFTOutput](api_avm_outputs.nftoutput).[\_typeName](api_avm_outputs.nftoutput#protected-_typename)_

_Defined in [src/apis/avm/outputs.ts:237](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/outputs.ts#L237)_

---

### `Protected` addresses

• **addresses**: _[Address](common_output.address)[]_ = []

_Inherited from [OutputOwners](common_output.outputowners).[addresses](common_output.outputowners#protected-addresses)_

_Defined in [src/common/output.ts:158](https://github.com/chain4travel/caminojs/blob/3883166/src/common/output.ts#L158)_

---

### `Protected` groupID

• **groupID**: _Buffer_ = Buffer.alloc(4)

_Inherited from [BaseNFTOutput](common_output.basenftoutput).[groupID](common_output.basenftoutput#protected-groupid)_

_Defined in [src/common/output.ts:618](https://github.com/chain4travel/caminojs/blob/3883166/src/common/output.ts#L618)_

---

### `Protected` locktime

• **locktime**: _Buffer_ = Buffer.alloc(8)

_Inherited from [OutputOwners](common_output.outputowners).[locktime](common_output.outputowners#protected-locktime)_

_Defined in [src/common/output.ts:155](https://github.com/chain4travel/caminojs/blob/3883166/src/common/output.ts#L155)_

---

### `Protected` numaddrs

• **numaddrs**: _Buffer_ = Buffer.alloc(4)

_Inherited from [OutputOwners](common_output.outputowners).[numaddrs](common_output.outputowners#protected-numaddrs)_

_Defined in [src/common/output.ts:157](https://github.com/chain4travel/caminojs/blob/3883166/src/common/output.ts#L157)_

---

### `Protected` threshold

• **threshold**: _Buffer_ = Buffer.alloc(4)

_Inherited from [OutputOwners](common_output.outputowners).[threshold](common_output.outputowners#protected-threshold)_

_Defined in [src/common/output.ts:156](https://github.com/chain4travel/caminojs/blob/3883166/src/common/output.ts#L156)_

## Methods

### clone

▸ **clone**(): _this_

_Overrides [Output](common_output.output).[clone](common_output.output#abstract-clone)_

_Defined in [src/apis/avm/outputs.ts:295](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/outputs.ts#L295)_

**Returns:** _this_

---

### create

▸ **create**(...`args`: any[]): _this_

_Overrides [Output](common_output.output).[create](common_output.output#abstract-create)_

_Defined in [src/apis/avm/outputs.ts:291](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/outputs.ts#L291)_

**Parameters:**

| Name      | Type  |
| --------- | ----- |
| `...args` | any[] |

**Returns:** _this_

---

### deserialize

▸ **deserialize**(`fields`: object, `encoding`: [SerializedEncoding](../modules/utils_serialization#serializedencoding)): _void_

_Inherited from [BaseNFTOutput](common_output.basenftoutput).[deserialize](common_output.basenftoutput#deserialize)_

_Overrides [OutputOwners](common_output.outputowners).[deserialize](common_output.outputowners#deserialize)_

_Defined in [src/common/output.ts:607](https://github.com/chain4travel/caminojs/blob/3883166/src/common/output.ts#L607)_

**Parameters:**

| Name       | Type                                                                    | Default |
| ---------- | ----------------------------------------------------------------------- | ------- |
| `fields`   | object                                                                  | -       |
| `encoding` | [SerializedEncoding](../modules/utils_serialization#serializedencoding) | "hex"   |

**Returns:** _void_

---

### fromBuffer

▸ **fromBuffer**(`utxobuff`: Buffer, `offset`: number): _number_

_Overrides [OutputOwners](common_output.outputowners).[fromBuffer](common_output.outputowners#frombuffer)_

_Defined in [src/apis/avm/outputs.ts:275](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/outputs.ts#L275)_

Popuates the instance from a [Buffer](https://github.com/feross/buffer) representing the [NFTMintOutput](api_avm_outputs.nftmintoutput) and returns the size of the output.

**Parameters:**

| Name       | Type   | Default |
| ---------- | ------ | ------- |
| `utxobuff` | Buffer | -       |
| `offset`   | number | 0       |

**Returns:** _number_

---

### getAddress

▸ **getAddress**(`idx`: number): _Buffer_

_Inherited from [OutputOwners](common_output.outputowners).[getAddress](common_output.outputowners#getaddress)_

_Defined in [src/common/output.ts:208](https://github.com/chain4travel/caminojs/blob/3883166/src/common/output.ts#L208)_

Returns the address from the index provided.

**Parameters:**

| Name  | Type   | Description               |
| ----- | ------ | ------------------------- |
| `idx` | number | The index of the address. |

**Returns:** _Buffer_

Returns the string representing the address.

---

### getAddressIdx

▸ **getAddressIdx**(`address`: Buffer): _number_

_Inherited from [OutputOwners](common_output.outputowners).[getAddressIdx](common_output.outputowners#getaddressidx)_

_Defined in [src/common/output.ts:188](https://github.com/chain4travel/caminojs/blob/3883166/src/common/output.ts#L188)_

Returns the index of the address.

**Parameters:**

| Name      | Type   | Description                                                                                 |
| --------- | ------ | ------------------------------------------------------------------------------------------- |
| `address` | Buffer | A [Buffer](https://github.com/feross/buffer) of the address to look up to return its index. |

**Returns:** _number_

The index of the address.

---

### getAddresses

▸ **getAddresses**(): _Buffer[]_

_Inherited from [OutputOwners](common_output.outputowners).[getAddresses](common_output.outputowners#getaddresses)_

_Defined in [src/common/output.ts:173](https://github.com/chain4travel/caminojs/blob/3883166/src/common/output.ts#L173)_

Returns an array of [Buffer](https://github.com/feross/buffer)s for the addresses.

**Returns:** _Buffer[]_

---

### getCodecID

▸ **getCodecID**(): _number_

_Inherited from [SigIdx](common_signature.sigidx).[getCodecID](common_signature.sigidx#getcodecid)_

_Defined in [src/utils/serialization.ts:70](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/serialization.ts#L70)_

Used in serialization. Optional. TypeID is a number for the typeID of object being output.

**Returns:** _number_

---

### getGroupID

▸ **getGroupID**(): _number_

_Inherited from [BaseNFTOutput](common_output.basenftoutput).[getGroupID](common_output.basenftoutput#getgroupid)_

_Defined in [src/common/output.ts:623](https://github.com/chain4travel/caminojs/blob/3883166/src/common/output.ts#L623)_

Returns the groupID as a number.

**Returns:** _number_

---

### getLocktime

▸ **getLocktime**(): _BN_

_Inherited from [OutputOwners](common_output.outputowners).[getLocktime](common_output.outputowners#getlocktime)_

_Defined in [src/common/output.ts:168](https://github.com/chain4travel/caminojs/blob/3883166/src/common/output.ts#L168)_

Returns the a [BN](https://github.com/indutny/bn.js/) repersenting the UNIX Timestamp when the lock is made available.

**Returns:** _BN_

---

### getOutputID

▸ **getOutputID**(): _number_

_Overrides [Output](common_output.output).[getOutputID](common_output.output#abstract-getoutputid)_

_Defined in [src/apis/avm/outputs.ts:268](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/outputs.ts#L268)_

Returns the outputID for this output

**Returns:** _number_

---

### getSpenders

▸ **getSpenders**(`addresses`: Buffer[], `asOf`: BN): _Buffer[]_

_Inherited from [OutputOwners](common_output.outputowners).[getSpenders](common_output.outputowners#getspenders)_

_Defined in [src/common/output.ts:237](https://github.com/chain4travel/caminojs/blob/3883166/src/common/output.ts#L237)_

Given an array of addresses and an optional timestamp, select an array of address [Buffer](https://github.com/feross/buffer)s of qualified spenders for the output.

**Parameters:**

| Name        | Type     | Default   |
| ----------- | -------- | --------- |
| `addresses` | Buffer[] | -         |
| `asOf`      | BN       | undefined |

**Returns:** _Buffer[]_

---

### getThreshold

▸ **getThreshold**(): _number_

_Inherited from [OutputOwners](common_output.outputowners).[getThreshold](common_output.outputowners#getthreshold)_

_Defined in [src/common/output.ts:163](https://github.com/chain4travel/caminojs/blob/3883166/src/common/output.ts#L163)_

Returns the threshold of signers required to spend this output.

**Returns:** _number_

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

### makeTransferable

▸ **makeTransferable**(`assetID`: Buffer): _[TransferableOutput](api_avm_outputs.transferableoutput)_

_Inherited from [NFTOutput](api_avm_outputs.nftoutput).[makeTransferable](api_avm_outputs.nftoutput#maketransferable)_

_Overrides [Output](common_output.output).[makeTransferable](common_output.output#abstract-maketransferable)_

_Defined in [src/apis/avm/outputs.ts:112](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/outputs.ts#L112)_

**Parameters:**

| Name      | Type   | Description                                                 |
| --------- | ------ | ----------------------------------------------------------- |
| `assetID` | Buffer | An assetID which is wrapped around the Buffer of the Output |

**Returns:** _[TransferableOutput](api_avm_outputs.transferableoutput)_

---

### meetsThreshold

▸ **meetsThreshold**(`addresses`: Buffer[], `asOf`: BN): _boolean_

_Inherited from [OutputOwners](common_output.outputowners).[meetsThreshold](common_output.outputowners#meetsthreshold)_

_Defined in [src/common/output.ts:218](https://github.com/chain4travel/caminojs/blob/3883166/src/common/output.ts#L218)_

Given an array of address [Buffer](https://github.com/feross/buffer)s and an optional timestamp, returns true if the addresses meet the threshold required to spend the output.

**Parameters:**

| Name        | Type     | Default   |
| ----------- | -------- | --------- |
| `addresses` | Buffer[] | -         |
| `asOf`      | BN       | undefined |

**Returns:** _boolean_

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

### select

▸ **select**(`id`: number, ...`args`: any[]): _[Output](common_output.output)_

_Inherited from [NFTOutput](api_avm_outputs.nftoutput).[select](api_avm_outputs.nftoutput#select)_

_Overrides [Output](common_output.output).[select](common_output.output#abstract-select)_

_Defined in [src/apis/avm/outputs.ts:116](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/outputs.ts#L116)_

**Parameters:**

| Name      | Type   |
| --------- | ------ |
| `id`      | number |
| `...args` | any[]  |

**Returns:** _[Output](common_output.output)_

---

### serialize

▸ **serialize**(`encoding`: [SerializedEncoding](../modules/utils_serialization#serializedencoding)): _object_

_Inherited from [BaseNFTOutput](common_output.basenftoutput).[serialize](common_output.basenftoutput#serialize)_

_Overrides [OutputOwners](common_output.outputowners).[serialize](common_output.outputowners#serialize)_

_Defined in [src/common/output.ts:594](https://github.com/chain4travel/caminojs/blob/3883166/src/common/output.ts#L594)_

**Parameters:**

| Name       | Type                                                                    | Default |
| ---------- | ----------------------------------------------------------------------- | ------- |
| `encoding` | [SerializedEncoding](../modules/utils_serialization#serializedencoding) | "hex"   |

**Returns:** _object_

---

### setCodecID

▸ **setCodecID**(`codecID`: number): _void_

_Defined in [src/apis/avm/outputs.ts:251](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/outputs.ts#L251)_

Set the codecID

**Parameters:**

| Name      | Type   | Description        |
| --------- | ------ | ------------------ |
| `codecID` | number | The codecID to set |

**Returns:** _void_

---

### toBuffer

▸ **toBuffer**(): _Buffer_

_Overrides [OutputOwners](common_output.outputowners).[toBuffer](common_output.outputowners#tobuffer)_

_Defined in [src/apis/avm/outputs.ts:284](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/outputs.ts#L284)_

Returns the buffer representing the [NFTMintOutput](api_avm_outputs.nftmintoutput) instance.

**Returns:** _Buffer_

---

### toString

▸ **toString**(): _string_

_Inherited from [OutputOwners](common_output.outputowners).[toString](common_output.outputowners#tostring)_

_Defined in [src/common/output.ts:315](https://github.com/chain4travel/caminojs/blob/3883166/src/common/output.ts#L315)_

Returns a base-58 string representing the [Output](../modules/src_common#output).

**Returns:** _string_

---

### `Static` comparator

▸ **comparator**(): _function_

_Inherited from [OutputOwners](common_output.outputowners).[comparator](common_output.outputowners#static-comparator)_

_Defined in [src/common/output.ts:319](https://github.com/chain4travel/caminojs/blob/3883166/src/common/output.ts#L319)_

**Returns:** _function_

▸ (`a`: [Output](common_output.output), `b`: [Output](common_output.output)): _1 | -1 | 0_

**Parameters:**

| Name | Type                           |
| ---- | ------------------------------ |
| `a`  | [Output](common_output.output) |
| `b`  | [Output](common_output.output) |