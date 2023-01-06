# Class: SECPMintOutput

An [Output](../modules/src_common#output) class which specifies an Output that carries an ammount for an assetID and uses secp256k1 signature scheme.

## Hierarchy

↳ [Output](common_output.output)

↳ **SECPMintOutput**

## Index

### Constructors

- [constructor](api_avm_outputs.secpmintoutput#constructor)

### Properties

- [\_codecID](api_avm_outputs.secpmintoutput#protected-_codecid)
- [\_typeID](api_avm_outputs.secpmintoutput#protected-_typeid)
- [\_typeName](api_avm_outputs.secpmintoutput#protected-_typename)
- [addresses](api_avm_outputs.secpmintoutput#protected-addresses)
- [locktime](api_avm_outputs.secpmintoutput#protected-locktime)
- [numaddrs](api_avm_outputs.secpmintoutput#protected-numaddrs)
- [threshold](api_avm_outputs.secpmintoutput#protected-threshold)

### Methods

- [clone](api_avm_outputs.secpmintoutput#clone)
- [create](api_avm_outputs.secpmintoutput#create)
- [deserialize](api_avm_outputs.secpmintoutput#deserialize)
- [fromBuffer](api_avm_outputs.secpmintoutput#frombuffer)
- [getAddress](api_avm_outputs.secpmintoutput#getaddress)
- [getAddressIdx](api_avm_outputs.secpmintoutput#getaddressidx)
- [getAddresses](api_avm_outputs.secpmintoutput#getaddresses)
- [getCodecID](api_avm_outputs.secpmintoutput#getcodecid)
- [getLocktime](api_avm_outputs.secpmintoutput#getlocktime)
- [getOutputID](api_avm_outputs.secpmintoutput#getoutputid)
- [getSpenders](api_avm_outputs.secpmintoutput#getspenders)
- [getThreshold](api_avm_outputs.secpmintoutput#getthreshold)
- [getTypeID](api_avm_outputs.secpmintoutput#gettypeid)
- [getTypeName](api_avm_outputs.secpmintoutput#gettypename)
- [makeTransferable](api_avm_outputs.secpmintoutput#maketransferable)
- [meetsThreshold](api_avm_outputs.secpmintoutput#meetsthreshold)
- [sanitizeObject](api_avm_outputs.secpmintoutput#sanitizeobject)
- [select](api_avm_outputs.secpmintoutput#select)
- [serialize](api_avm_outputs.secpmintoutput#serialize)
- [setCodecID](api_avm_outputs.secpmintoutput#setcodecid)
- [toBuffer](api_avm_outputs.secpmintoutput#tobuffer)
- [toString](api_avm_outputs.secpmintoutput#tostring)
- [comparator](api_avm_outputs.secpmintoutput#static-comparator)

## Constructors

### constructor

\+ **new SECPMintOutput**(`addresses`: Buffer[], `locktime`: BN, `threshold`: number): _[SECPMintOutput](api_avm_outputs.secpmintoutput)_

_Inherited from [OutputOwners](common_output.outputowners).[constructor](common_output.outputowners#constructor)_

_Defined in [src/common/output.ts:339](https://github.com/chain4travel/caminojs/blob/3883166/src/common/output.ts#L339)_

An [Output](../modules/src_common#output) class which contains addresses, locktimes, and thresholds.

**Parameters:**

| Name        | Type     | Default   | Description                                                                                   |
| ----------- | -------- | --------- | --------------------------------------------------------------------------------------------- |
| `addresses` | Buffer[] | undefined | An array of [Buffer](https://github.com/feross/buffer)s representing output owner's addresses |
| `locktime`  | BN       | undefined | A [BN](https://github.com/indutny/bn.js/) representing the locktime                           |
| `threshold` | number   | undefined | A number representing the the threshold number of signers required to sign the transaction    |

**Returns:** _[SECPMintOutput](api_avm_outputs.secpmintoutput)_

## Properties

### `Protected` \_codecID

• **\_codecID**: _number_ = AVMConstants.LATESTCODEC

_Overrides [SigIdx](common_signature.sigidx).[\_codecID](common_signature.sigidx#protected-_codecid)_

_Defined in [src/apis/avm/outputs.ts:176](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/outputs.ts#L176)_

---

### `Protected` \_typeID

• **\_typeID**: _number_ = this.\_codecID === 0
? AVMConstants.SECPMINTOUTPUTID
: AVMConstants.SECPMINTOUTPUTID_CODECONE

_Overrides [Output](common_output.output).[\_typeID](common_output.output#protected-_typeid)_

_Defined in [src/apis/avm/outputs.ts:177](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/outputs.ts#L177)_

---

### `Protected` \_typeName

• **\_typeName**: _string_ = "SECPMintOutput"

_Overrides [Output](common_output.output).[\_typeName](common_output.output#protected-_typename)_

_Defined in [src/apis/avm/outputs.ts:175](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/outputs.ts#L175)_

---

### `Protected` addresses

• **addresses**: _[Address](common_output.address)[]_ = []

_Inherited from [OutputOwners](common_output.outputowners).[addresses](common_output.outputowners#protected-addresses)_

_Defined in [src/common/output.ts:158](https://github.com/chain4travel/caminojs/blob/3883166/src/common/output.ts#L158)_

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

_Defined in [src/apis/avm/outputs.ts:222](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/outputs.ts#L222)_

**Returns:** _this_

---

### create

▸ **create**(...`args`: any[]): _this_

_Overrides [Output](common_output.output).[create](common_output.output#abstract-create)_

_Defined in [src/apis/avm/outputs.ts:218](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/outputs.ts#L218)_

**Parameters:**

| Name      | Type  |
| --------- | ----- |
| `...args` | any[] |

**Returns:** _this_

---

### deserialize

▸ **deserialize**(`fields`: object, `encoding`: [SerializedEncoding](../modules/utils_serialization#serializedencoding)): _void_

_Inherited from [OutputOwners](common_output.outputowners).[deserialize](common_output.outputowners#deserialize)_

_Overrides [StandardParseableInput](common_inputs.standardparseableinput).[deserialize](common_inputs.standardparseableinput#deserialize)_

_Defined in [src/common/output.ts:130](https://github.com/chain4travel/caminojs/blob/3883166/src/common/output.ts#L130)_

**Parameters:**

| Name       | Type                                                                    | Default |
| ---------- | ----------------------------------------------------------------------- | ------- |
| `fields`   | object                                                                  | -       |
| `encoding` | [SerializedEncoding](../modules/utils_serialization#serializedencoding) | "hex"   |

**Returns:** _void_

---

### fromBuffer

▸ **fromBuffer**(`bytes`: Buffer, `offset`: number): _number_

_Inherited from [OutputOwners](common_output.outputowners).[fromBuffer](common_output.outputowners#frombuffer)_

_Defined in [src/common/output.ts:277](https://github.com/chain4travel/caminojs/blob/3883166/src/common/output.ts#L277)_

Returns a base-58 string representing the [Output](../modules/src_common#output).

**Parameters:**

| Name     | Type   | Default |
| -------- | ------ | ------- |
| `bytes`  | Buffer | -       |
| `offset` | number | 0       |

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

_Defined in [src/apis/avm/outputs.ts:206](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/outputs.ts#L206)_

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

_Overrides [Output](common_output.output).[makeTransferable](common_output.output#abstract-maketransferable)_

_Defined in [src/apis/avm/outputs.ts:214](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/outputs.ts#L214)_

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

_Overrides [Output](common_output.output).[select](common_output.output#abstract-select)_

_Defined in [src/apis/avm/outputs.ts:228](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/outputs.ts#L228)_

**Parameters:**

| Name      | Type   |
| --------- | ------ |
| `id`      | number |
| `...args` | any[]  |

**Returns:** _[Output](common_output.output)_

---

### serialize

▸ **serialize**(`encoding`: [SerializedEncoding](../modules/utils_serialization#serializedencoding)): _object_

_Inherited from [OutputOwners](common_output.outputowners).[serialize](common_output.outputowners#serialize)_

_Overrides [Serializable](utils_serialization.serializable).[serialize](utils_serialization.serializable#serialize)_

_Defined in [src/common/output.ts:107](https://github.com/chain4travel/caminojs/blob/3883166/src/common/output.ts#L107)_

**Parameters:**

| Name       | Type                                                                    | Default |
| ---------- | ----------------------------------------------------------------------- | ------- |
| `encoding` | [SerializedEncoding](../modules/utils_serialization#serializedencoding) | "hex"   |

**Returns:** _object_

---

### setCodecID

▸ **setCodecID**(`codecID`: number): _void_

_Defined in [src/apis/avm/outputs.ts:189](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/outputs.ts#L189)_

Set the codecID

**Parameters:**

| Name      | Type   | Description        |
| --------- | ------ | ------------------ |
| `codecID` | number | The codecID to set |

**Returns:** _void_

---

### toBuffer

▸ **toBuffer**(): _Buffer_

_Inherited from [OutputOwners](common_output.outputowners).[toBuffer](common_output.outputowners#tobuffer)_

_Defined in [src/common/output.ts:298](https://github.com/chain4travel/caminojs/blob/3883166/src/common/output.ts#L298)_

Returns the buffer representing the [Output](../modules/src_common#output) instance.

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
