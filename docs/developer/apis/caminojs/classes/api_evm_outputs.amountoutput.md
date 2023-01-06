# Class: AmountOutput

## Hierarchy

↳ [StandardAmountOutput](common_output.standardamountoutput)

↳ **AmountOutput**

↳ [SECPTransferOutput](api_evm_outputs.secptransferoutput)

## Index

### Constructors

- [constructor](api_evm_outputs.amountoutput#constructor)

### Properties

- [\_codecID](api_evm_outputs.amountoutput#protected-_codecid)
- [\_typeID](api_evm_outputs.amountoutput#protected-_typeid)
- [\_typeName](api_evm_outputs.amountoutput#protected-_typename)
- [addresses](api_evm_outputs.amountoutput#protected-addresses)
- [amount](api_evm_outputs.amountoutput#protected-amount)
- [amountValue](api_evm_outputs.amountoutput#protected-amountvalue)
- [locktime](api_evm_outputs.amountoutput#protected-locktime)
- [numaddrs](api_evm_outputs.amountoutput#protected-numaddrs)
- [threshold](api_evm_outputs.amountoutput#protected-threshold)

### Methods

- [clone](api_evm_outputs.amountoutput#abstract-clone)
- [create](api_evm_outputs.amountoutput#abstract-create)
- [deserialize](api_evm_outputs.amountoutput#deserialize)
- [fromBuffer](api_evm_outputs.amountoutput#frombuffer)
- [getAddress](api_evm_outputs.amountoutput#getaddress)
- [getAddressIdx](api_evm_outputs.amountoutput#getaddressidx)
- [getAddresses](api_evm_outputs.amountoutput#getaddresses)
- [getAmount](api_evm_outputs.amountoutput#getamount)
- [getCodecID](api_evm_outputs.amountoutput#getcodecid)
- [getLocktime](api_evm_outputs.amountoutput#getlocktime)
- [getOutputID](api_evm_outputs.amountoutput#abstract-getoutputid)
- [getSpenders](api_evm_outputs.amountoutput#getspenders)
- [getThreshold](api_evm_outputs.amountoutput#getthreshold)
- [getTypeID](api_evm_outputs.amountoutput#gettypeid)
- [getTypeName](api_evm_outputs.amountoutput#gettypename)
- [makeTransferable](api_evm_outputs.amountoutput#maketransferable)
- [meetsThreshold](api_evm_outputs.amountoutput#meetsthreshold)
- [sanitizeObject](api_evm_outputs.amountoutput#sanitizeobject)
- [select](api_evm_outputs.amountoutput#select)
- [serialize](api_evm_outputs.amountoutput#serialize)
- [toBuffer](api_evm_outputs.amountoutput#tobuffer)
- [toString](api_evm_outputs.amountoutput#tostring)
- [comparator](api_evm_outputs.amountoutput#static-comparator)

## Constructors

### constructor

\+ **new AmountOutput**(`amount`: BN, `addresses`: Buffer[], `locktime`: BN, `threshold`: number): _[AmountOutput](api_evm_outputs.amountoutput)_

_Inherited from [StandardAmountOutput](common_output.standardamountoutput).[constructor](common_output.standardamountoutput#constructor)_

_Overrides [OutputOwners](common_output.outputowners).[constructor](common_output.outputowners#constructor)_

_Defined in [src/common/output.ts:563](https://github.com/chain4travel/caminojs/blob/3883166/src/common/output.ts#L563)_

A [StandardAmountOutput](../modules/src_common#standardamountoutput) class which issues a payment on an assetID.

**Parameters:**

| Name        | Type     | Default   | Description                                                                                |
| ----------- | -------- | --------- | ------------------------------------------------------------------------------------------ |
| `amount`    | BN       | undefined | A [BN](https://github.com/indutny/bn.js/) representing the amount in the output            |
| `addresses` | Buffer[] | undefined | An array of [Buffer](https://github.com/feross/buffer)s representing addresses             |
| `locktime`  | BN       | undefined | A [BN](https://github.com/indutny/bn.js/) representing the locktime                        |
| `threshold` | number   | undefined | A number representing the the threshold number of signers required to sign the transaction |

**Returns:** _[AmountOutput](api_evm_outputs.amountoutput)_

## Properties

### `Protected` \_codecID

• **\_codecID**: _number_ = undefined

_Inherited from [SigIdx](common_signature.sigidx).[\_codecID](common_signature.sigidx#protected-_codecid)_

_Defined in [src/utils/serialization.ts:51](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/serialization.ts#L51)_

---

### `Protected` \_typeID

• **\_typeID**: _any_ = undefined

_Overrides [StandardAmountOutput](common_output.standardamountoutput).[\_typeID](common_output.standardamountoutput#protected-_typeid)_

_Defined in [src/apis/evm/outputs.ts:64](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/outputs.ts#L64)_

---

### `Protected` \_typeName

• **\_typeName**: _string_ = "AmountOutput"

_Overrides [StandardAmountOutput](common_output.standardamountoutput).[\_typeName](common_output.standardamountoutput#protected-_typename)_

_Defined in [src/apis/evm/outputs.ts:63](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/outputs.ts#L63)_

---

### `Protected` addresses

• **addresses**: _[Address](common_output.address)[]_ = []

_Inherited from [OutputOwners](common_output.outputowners).[addresses](common_output.outputowners#protected-addresses)_

_Defined in [src/common/output.ts:158](https://github.com/chain4travel/caminojs/blob/3883166/src/common/output.ts#L158)_

---

### `Protected` amount

• **amount**: _Buffer_ = Buffer.alloc(8)

_Inherited from [StandardAmountOutput](common_output.standardamountoutput).[amount](common_output.standardamountoutput#protected-amount)_

_Defined in [src/common/output.ts:534](https://github.com/chain4travel/caminojs/blob/3883166/src/common/output.ts#L534)_

---

### `Protected` amountValue

• **amountValue**: _BN_ = new BN(0)

_Inherited from [StandardAmountOutput](common_output.standardamountoutput).[amountValue](common_output.standardamountoutput#protected-amountvalue)_

_Defined in [src/common/output.ts:535](https://github.com/chain4travel/caminojs/blob/3883166/src/common/output.ts#L535)_

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

### `Abstract` clone

▸ **clone**(): _this_

_Inherited from [Output](common_output.output).[clone](common_output.output#abstract-clone)_

_Defined in [src/common/output.ts:384](https://github.com/chain4travel/caminojs/blob/3883166/src/common/output.ts#L384)_

**Returns:** _this_

---

### `Abstract` create

▸ **create**(...`args`: any[]): _this_

_Inherited from [Output](common_output.output).[create](common_output.output#abstract-create)_

_Defined in [src/common/output.ts:386](https://github.com/chain4travel/caminojs/blob/3883166/src/common/output.ts#L386)_

**Parameters:**

| Name      | Type  |
| --------- | ----- |
| `...args` | any[] |

**Returns:** _this_

---

### deserialize

▸ **deserialize**(`fields`: object, `encoding`: [SerializedEncoding](../modules/utils_serialization#serializedencoding)): _void_

_Inherited from [StandardAmountOutput](common_output.standardamountoutput).[deserialize](common_output.standardamountoutput#deserialize)_

_Overrides [OutputOwners](common_output.outputowners).[deserialize](common_output.outputowners#deserialize)_

_Defined in [src/common/output.ts:522](https://github.com/chain4travel/caminojs/blob/3883166/src/common/output.ts#L522)_

**Parameters:**

| Name       | Type                                                                    | Default |
| ---------- | ----------------------------------------------------------------------- | ------- |
| `fields`   | object                                                                  | -       |
| `encoding` | [SerializedEncoding](../modules/utils_serialization#serializedencoding) | "hex"   |

**Returns:** _void_

---

### fromBuffer

▸ **fromBuffer**(`outbuff`: Buffer, `offset`: number): _number_

_Inherited from [StandardAmountOutput](common_output.standardamountoutput).[fromBuffer](common_output.standardamountoutput#frombuffer)_

_Overrides [OutputOwners](common_output.outputowners).[fromBuffer](common_output.outputowners#frombuffer)_

_Defined in [src/common/output.ts:547](https://github.com/chain4travel/caminojs/blob/3883166/src/common/output.ts#L547)_

Popuates the instance from a [Buffer](https://github.com/feross/buffer) representing the [StandardAmountOutput](../modules/src_common#standardamountoutput) and returns the size of the output.

**Parameters:**

| Name      | Type   | Default |
| --------- | ------ | ------- |
| `outbuff` | Buffer | -       |
| `offset`  | number | 0       |

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

### getAmount

▸ **getAmount**(): _BN_

_Inherited from [StandardAmountOutput](common_output.standardamountoutput).[getAmount](common_output.standardamountoutput#getamount)_

_Defined in [src/common/output.ts:540](https://github.com/chain4travel/caminojs/blob/3883166/src/common/output.ts#L540)_

Returns the amount as a [BN](https://github.com/indutny/bn.js/).

**Returns:** _BN_

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

### `Abstract` getOutputID

▸ **getOutputID**(): _number_

_Inherited from [Output](common_output.output).[getOutputID](common_output.output#abstract-getoutputid)_

_Defined in [src/common/output.ts:382](https://github.com/chain4travel/caminojs/blob/3883166/src/common/output.ts#L382)_

Returns the outputID for the output which tells parsers what type it is

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

▸ **makeTransferable**(`assetID`: Buffer): _[TransferableOutput](api_evm_outputs.transferableoutput)_

_Overrides [Output](common_output.output).[makeTransferable](common_output.output#abstract-maketransferable)_

_Defined in [src/apis/evm/outputs.ts:72](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/outputs.ts#L72)_

**Parameters:**

| Name      | Type   | Description                                                 |
| --------- | ------ | ----------------------------------------------------------- |
| `assetID` | Buffer | An assetID which is wrapped around the Buffer of the Output |

**Returns:** _[TransferableOutput](api_evm_outputs.transferableoutput)_

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

_Defined in [src/apis/evm/outputs.ts:76](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/outputs.ts#L76)_

**Parameters:**

| Name      | Type   |
| --------- | ------ |
| `id`      | number |
| `...args` | any[]  |

**Returns:** _[Output](common_output.output)_

---

### serialize

▸ **serialize**(`encoding`: [SerializedEncoding](../modules/utils_serialization#serializedencoding)): _object_

_Inherited from [StandardAmountOutput](common_output.standardamountoutput).[serialize](common_output.standardamountoutput#serialize)_

_Overrides [OutputOwners](common_output.outputowners).[serialize](common_output.outputowners#serialize)_

_Defined in [src/common/output.ts:509](https://github.com/chain4travel/caminojs/blob/3883166/src/common/output.ts#L509)_

**Parameters:**

| Name       | Type                                                                    | Default |
| ---------- | ----------------------------------------------------------------------- | ------- |
| `encoding` | [SerializedEncoding](../modules/utils_serialization#serializedencoding) | "hex"   |

**Returns:** _object_

---

### toBuffer

▸ **toBuffer**(): _Buffer_

_Inherited from [StandardAmountOutput](common_output.standardamountoutput).[toBuffer](common_output.standardamountoutput#tobuffer)_

_Overrides [OutputOwners](common_output.outputowners).[toBuffer](common_output.outputowners#tobuffer)_

_Defined in [src/common/output.ts:557](https://github.com/chain4travel/caminojs/blob/3883166/src/common/output.ts#L557)_

Returns the buffer representing the [StandardAmountOutput](../modules/src_common#standardamountoutput) instance.

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
