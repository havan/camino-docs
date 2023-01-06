# Class: StakeableLockOut

An [Output](../modules/src_common#output) class which specifies an input that has a locktime which can also enable staking of the value held, preventing transfers but not validation.

## Hierarchy

↳ [AmountOutput](api_platformvm_outputs.amountoutput)

↳ **StakeableLockOut**

## Index

### Constructors

- [constructor](api_platformvm_outputs.stakeablelockout#constructor)

### Properties

- [\_codecID](api_platformvm_outputs.stakeablelockout#protected-_codecid)
- [\_typeID](api_platformvm_outputs.stakeablelockout#protected-_typeid)
- [\_typeName](api_platformvm_outputs.stakeablelockout#protected-_typename)
- [addresses](api_platformvm_outputs.stakeablelockout#protected-addresses)
- [amount](api_platformvm_outputs.stakeablelockout#protected-amount)
- [amountValue](api_platformvm_outputs.stakeablelockout#protected-amountvalue)
- [locktime](api_platformvm_outputs.stakeablelockout#protected-locktime)
- [numaddrs](api_platformvm_outputs.stakeablelockout#protected-numaddrs)
- [stakeableLocktime](api_platformvm_outputs.stakeablelockout#protected-stakeablelocktime)
- [threshold](api_platformvm_outputs.stakeablelockout#protected-threshold)
- [transferableOutput](api_platformvm_outputs.stakeablelockout#protected-transferableoutput)

### Methods

- [clone](api_platformvm_outputs.stakeablelockout#clone)
- [create](api_platformvm_outputs.stakeablelockout#create)
- [deserialize](api_platformvm_outputs.stakeablelockout#deserialize)
- [fromBuffer](api_platformvm_outputs.stakeablelockout#frombuffer)
- [getAddress](api_platformvm_outputs.stakeablelockout#getaddress)
- [getAddressIdx](api_platformvm_outputs.stakeablelockout#getaddressidx)
- [getAddresses](api_platformvm_outputs.stakeablelockout#getaddresses)
- [getAmount](api_platformvm_outputs.stakeablelockout#getamount)
- [getCodecID](api_platformvm_outputs.stakeablelockout#getcodecid)
- [getLocktime](api_platformvm_outputs.stakeablelockout#getlocktime)
- [getOutputID](api_platformvm_outputs.stakeablelockout#getoutputid)
- [getSpenders](api_platformvm_outputs.stakeablelockout#getspenders)
- [getStakeableLocktime](api_platformvm_outputs.stakeablelockout#getstakeablelocktime)
- [getThreshold](api_platformvm_outputs.stakeablelockout#getthreshold)
- [getTransferableOutput](api_platformvm_outputs.stakeablelockout#gettransferableoutput)
- [getTypeID](api_platformvm_outputs.stakeablelockout#gettypeid)
- [getTypeName](api_platformvm_outputs.stakeablelockout#gettypename)
- [makeTransferable](api_platformvm_outputs.stakeablelockout#maketransferable)
- [meetsThreshold](api_platformvm_outputs.stakeablelockout#meetsthreshold)
- [sanitizeObject](api_platformvm_outputs.stakeablelockout#sanitizeobject)
- [select](api_platformvm_outputs.stakeablelockout#select)
- [serialize](api_platformvm_outputs.stakeablelockout#serialize)
- [synchronize](api_platformvm_outputs.stakeablelockout#private-synchronize)
- [toBuffer](api_platformvm_outputs.stakeablelockout#tobuffer)
- [toString](api_platformvm_outputs.stakeablelockout#tostring)
- [comparator](api_platformvm_outputs.stakeablelockout#static-comparator)

## Constructors

### constructor

\+ **new StakeableLockOut**(`amount`: BN, `addresses`: Buffer[], `locktime`: BN, `threshold`: number, `stakeableLocktime`: BN, `transferableOutput`: [ParseableOutput](api_platformvm_outputs.parseableoutput)): _[StakeableLockOut](api_platformvm_outputs.stakeablelockout)_

_Overrides [StandardAmountOutput](common_output.standardamountoutput).[constructor](common_output.standardamountoutput#constructor)_

_Defined in [src/apis/platformvm/outputs.ts:260](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/outputs.ts#L260)_

A [Output](../modules/src_common#output) class which specifies a [ParseableOutput](api_platformvm_outputs.parseableoutput) that has a locktime which can also enable staking of the value held, preventing transfers but not validation.

**Parameters:**

| Name                 | Type                                                      | Default   | Description                                                                                     |
| -------------------- | --------------------------------------------------------- | --------- | ----------------------------------------------------------------------------------------------- |
| `amount`             | BN                                                        | undefined | A [BN](https://github.com/indutny/bn.js/) representing the amount in the output                 |
| `addresses`          | Buffer[]                                                  | undefined | An array of [Buffer](https://github.com/feross/buffer)s representing addresses                  |
| `locktime`           | BN                                                        | undefined | A [BN](https://github.com/indutny/bn.js/) representing the locktime                             |
| `threshold`          | number                                                    | undefined | A number representing the the threshold number of signers required to sign the transaction      |
| `stakeableLocktime`  | BN                                                        | undefined | A [BN](https://github.com/indutny/bn.js/) representing the stakeable locktime                   |
| `transferableOutput` | [ParseableOutput](api_platformvm_outputs.parseableoutput) | undefined | A [ParseableOutput](api_platformvm_outputs.parseableoutput) which is embedded into this output. |

**Returns:** _[StakeableLockOut](api_platformvm_outputs.stakeablelockout)_

## Properties

### `Protected` \_codecID

• **\_codecID**: _number_ = undefined

_Inherited from [SigIdx](common_signature.sigidx).[\_codecID](common_signature.sigidx#protected-_codecid)_

_Defined in [src/utils/serialization.ts:51](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/serialization.ts#L51)_

---

### `Protected` \_typeID

• **\_typeID**: _number_ = PlatformVMConstants.STAKEABLELOCKOUTID

_Overrides [AmountOutput](api_platformvm_outputs.amountoutput).[\_typeID](api_platformvm_outputs.amountoutput#protected-_typeid)_

_Defined in [src/apis/platformvm/outputs.ts:142](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/outputs.ts#L142)_

---

### `Protected` \_typeName

• **\_typeName**: _string_ = "StakeableLockOut"

_Overrides [AmountOutput](api_platformvm_outputs.amountoutput).[\_typeName](api_platformvm_outputs.amountoutput#protected-_typename)_

_Defined in [src/apis/platformvm/outputs.ts:141](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/outputs.ts#L141)_

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

### `Protected` stakeableLocktime

• **stakeableLocktime**: _Buffer_

_Defined in [src/apis/platformvm/outputs.ts:183](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/outputs.ts#L183)_

---

### `Protected` threshold

• **threshold**: _Buffer_ = Buffer.alloc(4)

_Inherited from [OutputOwners](common_output.outputowners).[threshold](common_output.outputowners#protected-threshold)_

_Defined in [src/common/output.ts:156](https://github.com/chain4travel/caminojs/blob/3883166/src/common/output.ts#L156)_

---

### `Protected` transferableOutput

• **transferableOutput**: _[ParseableOutput](api_platformvm_outputs.parseableoutput)_

_Defined in [src/apis/platformvm/outputs.ts:184](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/outputs.ts#L184)_

## Methods

### clone

▸ **clone**(): _this_

_Overrides [Output](common_output.output).[clone](common_output.output#abstract-clone)_

_Defined in [src/apis/platformvm/outputs.ts:256](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/outputs.ts#L256)_

**Returns:** _this_

---

### create

▸ **create**(...`args`: any[]): _this_

_Overrides [Output](common_output.output).[create](common_output.output#abstract-create)_

_Defined in [src/apis/platformvm/outputs.ts:252](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/outputs.ts#L252)_

**Parameters:**

| Name      | Type  |
| --------- | ----- |
| `...args` | any[] |

**Returns:** _this_

---

### deserialize

▸ **deserialize**(`fields`: object, `encoding`: [SerializedEncoding](../modules/utils_serialization#serializedencoding)): _void_

_Overrides [StandardAmountOutput](common_output.standardamountoutput).[deserialize](common_output.standardamountoutput#deserialize)_

_Defined in [src/apis/platformvm/outputs.ts:165](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/outputs.ts#L165)_

**Parameters:**

| Name       | Type                                                                    | Default |
| ---------- | ----------------------------------------------------------------------- | ------- |
| `fields`   | object                                                                  | -       |
| `encoding` | [SerializedEncoding](../modules/utils_serialization#serializedencoding) | "hex"   |

**Returns:** _void_

---

### fromBuffer

▸ **fromBuffer**(`outbuff`: Buffer, `offset`: number): _number_

_Overrides [StandardAmountOutput](common_output.standardamountoutput).[fromBuffer](common_output.standardamountoutput#frombuffer)_

_Defined in [src/apis/platformvm/outputs.ts:226](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/outputs.ts#L226)_

Popuates the instance from a [Buffer](https://github.com/feross/buffer) representing the [StakeableLockOut](api_platformvm_outputs.stakeablelockout) and returns the size of the output.

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

### getOutputID

▸ **getOutputID**(): _number_

_Overrides [Output](common_output.output).[getOutputID](common_output.output#abstract-getoutputid)_

_Defined in [src/apis/platformvm/outputs.ts:248](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/outputs.ts#L248)_

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

### getStakeableLocktime

▸ **getStakeableLocktime**(): _BN_

_Defined in [src/apis/platformvm/outputs.ts:204](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/outputs.ts#L204)_

**Returns:** _BN_

---

### getThreshold

▸ **getThreshold**(): _number_

_Inherited from [OutputOwners](common_output.outputowners).[getThreshold](common_output.outputowners#getthreshold)_

_Defined in [src/common/output.ts:163](https://github.com/chain4travel/caminojs/blob/3883166/src/common/output.ts#L163)_

Returns the threshold of signers required to spend this output.

**Returns:** _number_

---

### getTransferableOutput

▸ **getTransferableOutput**(): _[ParseableOutput](api_platformvm_outputs.parseableoutput)_

_Defined in [src/apis/platformvm/outputs.ts:208](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/outputs.ts#L208)_

**Returns:** _[ParseableOutput](api_platformvm_outputs.parseableoutput)_

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

▸ **makeTransferable**(`assetID`: Buffer): _[TransferableOutput](api_platformvm_outputs.transferableoutput)_

_Overrides [AmountOutput](api_platformvm_outputs.amountoutput).[makeTransferable](api_platformvm_outputs.amountoutput#maketransferable)_

_Defined in [src/apis/platformvm/outputs.ts:215](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/outputs.ts#L215)_

**Parameters:**

| Name      | Type   | Description                                                 |
| --------- | ------ | ----------------------------------------------------------- |
| `assetID` | Buffer | An assetID which is wrapped around the Buffer of the Output |

**Returns:** _[TransferableOutput](api_platformvm_outputs.transferableoutput)_

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

_Overrides [AmountOutput](api_platformvm_outputs.amountoutput).[select](api_platformvm_outputs.amountoutput#select)_

_Defined in [src/apis/platformvm/outputs.ts:219](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/outputs.ts#L219)_

**Parameters:**

| Name      | Type   |
| --------- | ------ |
| `id`      | number |
| `...args` | any[]  |

**Returns:** _[Output](common_output.output)_

---

### serialize

▸ **serialize**(`encoding`: [SerializedEncoding](../modules/utils_serialization#serializedencoding)): _object_

_Overrides [StandardAmountOutput](common_output.standardamountoutput).[serialize](common_output.standardamountoutput#serialize)_

_Defined in [src/apis/platformvm/outputs.ts:146](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/outputs.ts#L146)_

**Parameters:**

| Name       | Type                                                                    | Default |
| ---------- | ----------------------------------------------------------------------- | ------- |
| `encoding` | [SerializedEncoding](../modules/utils_serialization#serializedencoding) | "hex"   |

**Returns:** _object_

---

### `Private` synchronize

▸ **synchronize**(): _void_

_Defined in [src/apis/platformvm/outputs.ts:187](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/outputs.ts#L187)_

**Returns:** _void_

---

### toBuffer

▸ **toBuffer**(): _Buffer_

_Overrides [StandardAmountOutput](common_output.standardamountoutput).[toBuffer](common_output.standardamountoutput#tobuffer)_

_Defined in [src/apis/platformvm/outputs.ts:238](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/outputs.ts#L238)_

Returns the buffer representing the [StakeableLockOut](api_platformvm_outputs.stakeablelockout) instance.

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
