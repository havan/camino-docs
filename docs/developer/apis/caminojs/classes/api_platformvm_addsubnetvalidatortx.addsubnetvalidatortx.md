# Class: AddSubnetValidatorTx

Class representing an unsigned AddSubnetValidatorTx transaction.

## Hierarchy

↳ [BaseTx](api_platformvm_basetx.basetx)

↳ **AddSubnetValidatorTx**

## Index

### Constructors

- [constructor](api_platformvm_addsubnetvalidatortx.addsubnetvalidatortx#constructor)

### Properties

- [\_codecID](api_platformvm_addsubnetvalidatortx.addsubnetvalidatortx#protected-_codecid)
- [\_typeID](api_platformvm_addsubnetvalidatortx.addsubnetvalidatortx#protected-_typeid)
- [\_typeName](api_platformvm_addsubnetvalidatortx.addsubnetvalidatortx#protected-_typename)
- [blockchainID](api_platformvm_addsubnetvalidatortx.addsubnetvalidatortx#protected-blockchainid)
- [endTime](api_platformvm_addsubnetvalidatortx.addsubnetvalidatortx#protected-endtime)
- [ins](api_platformvm_addsubnetvalidatortx.addsubnetvalidatortx#protected-ins)
- [memo](api_platformvm_addsubnetvalidatortx.addsubnetvalidatortx#protected-memo)
- [networkID](api_platformvm_addsubnetvalidatortx.addsubnetvalidatortx#protected-networkid)
- [nodeID](api_platformvm_addsubnetvalidatortx.addsubnetvalidatortx#protected-nodeid)
- [numins](api_platformvm_addsubnetvalidatortx.addsubnetvalidatortx#protected-numins)
- [numouts](api_platformvm_addsubnetvalidatortx.addsubnetvalidatortx#protected-numouts)
- [outs](api_platformvm_addsubnetvalidatortx.addsubnetvalidatortx#protected-outs)
- [sigCount](api_platformvm_addsubnetvalidatortx.addsubnetvalidatortx#protected-sigcount)
- [sigIdxs](api_platformvm_addsubnetvalidatortx.addsubnetvalidatortx#protected-sigidxs)
- [startTime](api_platformvm_addsubnetvalidatortx.addsubnetvalidatortx#protected-starttime)
- [subnetAuth](api_platformvm_addsubnetvalidatortx.addsubnetvalidatortx#protected-subnetauth)
- [subnetID](api_platformvm_addsubnetvalidatortx.addsubnetvalidatortx#protected-subnetid)
- [weight](api_platformvm_addsubnetvalidatortx.addsubnetvalidatortx#protected-weight)

### Methods

- [addSignatureIdx](api_platformvm_addsubnetvalidatortx.addsubnetvalidatortx#addsignatureidx)
- [clone](api_platformvm_addsubnetvalidatortx.addsubnetvalidatortx#clone)
- [create](api_platformvm_addsubnetvalidatortx.addsubnetvalidatortx#create)
- [deserialize](api_platformvm_addsubnetvalidatortx.addsubnetvalidatortx#deserialize)
- [fromBuffer](api_platformvm_addsubnetvalidatortx.addsubnetvalidatortx#frombuffer)
- [getBlockchainID](api_platformvm_addsubnetvalidatortx.addsubnetvalidatortx#getblockchainid)
- [getCodecID](api_platformvm_addsubnetvalidatortx.addsubnetvalidatortx#getcodecid)
- [getCredentialID](api_platformvm_addsubnetvalidatortx.addsubnetvalidatortx#getcredentialid)
- [getEndTime](api_platformvm_addsubnetvalidatortx.addsubnetvalidatortx#getendtime)
- [getIns](api_platformvm_addsubnetvalidatortx.addsubnetvalidatortx#getins)
- [getMemo](api_platformvm_addsubnetvalidatortx.addsubnetvalidatortx#getmemo)
- [getNetworkID](api_platformvm_addsubnetvalidatortx.addsubnetvalidatortx#getnetworkid)
- [getNodeID](api_platformvm_addsubnetvalidatortx.addsubnetvalidatortx#getnodeid)
- [getNodeIDString](api_platformvm_addsubnetvalidatortx.addsubnetvalidatortx#getnodeidstring)
- [getOuts](api_platformvm_addsubnetvalidatortx.addsubnetvalidatortx#getouts)
- [getSigIdxs](api_platformvm_addsubnetvalidatortx.addsubnetvalidatortx#getsigidxs)
- [getStartTime](api_platformvm_addsubnetvalidatortx.addsubnetvalidatortx#getstarttime)
- [getSubnetAuth](api_platformvm_addsubnetvalidatortx.addsubnetvalidatortx#getsubnetauth)
- [getSubnetID](api_platformvm_addsubnetvalidatortx.addsubnetvalidatortx#getsubnetid)
- [getTotalOuts](api_platformvm_addsubnetvalidatortx.addsubnetvalidatortx#gettotalouts)
- [getTxType](api_platformvm_addsubnetvalidatortx.addsubnetvalidatortx#gettxtype)
- [getTypeID](api_platformvm_addsubnetvalidatortx.addsubnetvalidatortx#gettypeid)
- [getTypeName](api_platformvm_addsubnetvalidatortx.addsubnetvalidatortx#gettypename)
- [getWeight](api_platformvm_addsubnetvalidatortx.addsubnetvalidatortx#getweight)
- [sanitizeObject](api_platformvm_addsubnetvalidatortx.addsubnetvalidatortx#sanitizeobject)
- [select](api_platformvm_addsubnetvalidatortx.addsubnetvalidatortx#select)
- [serialize](api_platformvm_addsubnetvalidatortx.addsubnetvalidatortx#serialize)
- [sign](api_platformvm_addsubnetvalidatortx.addsubnetvalidatortx#sign)
- [toBuffer](api_platformvm_addsubnetvalidatortx.addsubnetvalidatortx#tobuffer)
- [toString](api_platformvm_addsubnetvalidatortx.addsubnetvalidatortx#tostring)
- [toStringHex](api_platformvm_addsubnetvalidatortx.addsubnetvalidatortx#tostringhex)

## Constructors

### constructor

\+ **new AddSubnetValidatorTx**(`networkID`: number, `blockchainID`: Buffer, `outs`: [TransferableOutput](api_platformvm_outputs.transferableoutput)[], `ins`: [TransferableInput](api_platformvm_inputs.transferableinput)[], `memo`: Buffer, `nodeID`: Buffer, `startTime`: BN, `endTime`: BN, `weight`: BN, `subnetID`: string | Buffer): _[AddSubnetValidatorTx](api_platformvm_addsubnetvalidatortx.addsubnetvalidatortx)_

_Overrides [BaseTx](api_platformvm_basetx.basetx).[constructor](api_platformvm_basetx.basetx#constructor)_

_Defined in [src/apis/platformvm/addsubnetvalidatortx.ts:244](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/addsubnetvalidatortx.ts#L244)_

Class representing an unsigned AddSubnetValidator transaction.

**Parameters:**

| Name           | Type                                                              | Default              | Description                                                                                                    |
| -------------- | ----------------------------------------------------------------- | -------------------- | -------------------------------------------------------------------------------------------------------------- |
| `networkID`    | number                                                            | DefaultNetworkID     | Optional networkID, [DefaultNetworkID](../modules/utils_constants#const-defaultnetworkid)                      |
| `blockchainID` | Buffer                                                            | Buffer.alloc(32, 16) | Optional blockchainID, default Buffer.alloc(32, 16)                                                            |
| `outs`         | [TransferableOutput](api_platformvm_outputs.transferableoutput)[] | undefined            | Optional array of the [TransferableOutput](api_evm_outputs.transferableoutput)s                                |
| `ins`          | [TransferableInput](api_platformvm_inputs.transferableinput)[]    | undefined            | Optional array of the [TransferableInput](api_evm_inputs.transferableinput)s                                   |
| `memo`         | Buffer                                                            | undefined            | Optional [Buffer](https://github.com/feross/buffer) for the memo field                                         |
| `nodeID`       | Buffer                                                            | undefined            | Optional. The node ID of the validator being added.                                                            |
| `startTime`    | BN                                                                | undefined            | Optional. The Unix time when the validator starts validating the Primary Network.                              |
| `endTime`      | BN                                                                | undefined            | Optional. The Unix time when the validator stops validating the Primary Network (and staked AVAX is returned). |
| `weight`       | BN                                                                | undefined            | Optional. Weight of this validator used when sampling                                                          |
| `subnetID`     | string &#124; Buffer                                              | undefined            | Optional. ID of the subnet this validator is validating                                                        |

**Returns:** _[AddSubnetValidatorTx](api_platformvm_addsubnetvalidatortx.addsubnetvalidatortx)_

## Properties

### `Protected` \_codecID

• **\_codecID**: _number_ = undefined

_Inherited from [SigIdx](common_signature.sigidx).[\_codecID](common_signature.sigidx#protected-_codecid)_

_Defined in [src/utils/serialization.ts:51](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/serialization.ts#L51)_

---

### `Protected` \_typeID

• **\_typeID**: _number_ = PlatformVMConstants.ADDSUBNETVALIDATORTX

_Overrides [BaseTx](api_platformvm_basetx.basetx).[\_typeID](api_platformvm_basetx.basetx#protected-_typeid)_

_Defined in [src/apis/platformvm/addsubnetvalidatortx.ts:30](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/addsubnetvalidatortx.ts#L30)_

---

### `Protected` \_typeName

• **\_typeName**: _string_ = "AddSubnetValidatorTx"

_Overrides [BaseTx](api_platformvm_basetx.basetx).[\_typeName](api_platformvm_basetx.basetx#protected-_typename)_

_Defined in [src/apis/platformvm/addsubnetvalidatortx.ts:29](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/addsubnetvalidatortx.ts#L29)_

---

### `Protected` blockchainID

• **blockchainID**: _Buffer_ = Buffer.alloc(32)

_Inherited from [StandardBaseTx](common_transactions.standardbasetx).[blockchainID](common_transactions.standardbasetx#protected-blockchainid)_

_Defined in [src/common/tx.ts:82](https://github.com/chain4travel/caminojs/blob/3883166/src/common/tx.ts#L82)_

---

### `Protected` endTime

• **endTime**: _Buffer_ = Buffer.alloc(8)

_Defined in [src/apis/platformvm/addsubnetvalidatortx.ts:58](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/addsubnetvalidatortx.ts#L58)_

---

### `Protected` ins

• **ins**: _[StandardTransferableInput](common_inputs.standardtransferableinput)[]_

_Inherited from [StandardBaseTx](common_transactions.standardbasetx).[ins](common_transactions.standardbasetx#protected-ins)_

_Defined in [src/common/tx.ts:86](https://github.com/chain4travel/caminojs/blob/3883166/src/common/tx.ts#L86)_

---

### `Protected` memo

• **memo**: _Buffer_ = Buffer.alloc(0)

_Inherited from [StandardBaseTx](common_transactions.standardbasetx).[memo](common_transactions.standardbasetx#protected-memo)_

_Defined in [src/common/tx.ts:87](https://github.com/chain4travel/caminojs/blob/3883166/src/common/tx.ts#L87)_

---

### `Protected` networkID

• **networkID**: _Buffer_ = Buffer.alloc(4)

_Inherited from [StandardBaseTx](common_transactions.standardbasetx).[networkID](common_transactions.standardbasetx#protected-networkid)_

_Defined in [src/common/tx.ts:81](https://github.com/chain4travel/caminojs/blob/3883166/src/common/tx.ts#L81)_

---

### `Protected` nodeID

• **nodeID**: _Buffer_ = Buffer.alloc(20)

_Defined in [src/apis/platformvm/addsubnetvalidatortx.ts:56](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/addsubnetvalidatortx.ts#L56)_

---

### `Protected` numins

• **numins**: _Buffer_ = Buffer.alloc(4)

_Inherited from [StandardBaseTx](common_transactions.standardbasetx).[numins](common_transactions.standardbasetx#protected-numins)_

_Defined in [src/common/tx.ts:85](https://github.com/chain4travel/caminojs/blob/3883166/src/common/tx.ts#L85)_

---

### `Protected` numouts

• **numouts**: _Buffer_ = Buffer.alloc(4)

_Inherited from [StandardBaseTx](common_transactions.standardbasetx).[numouts](common_transactions.standardbasetx#protected-numouts)_

_Defined in [src/common/tx.ts:83](https://github.com/chain4travel/caminojs/blob/3883166/src/common/tx.ts#L83)_

---

### `Protected` outs

• **outs**: _[StandardTransferableOutput](common_output.standardtransferableoutput)[]_

_Inherited from [StandardBaseTx](common_transactions.standardbasetx).[outs](common_transactions.standardbasetx#protected-outs)_

_Defined in [src/common/tx.ts:84](https://github.com/chain4travel/caminojs/blob/3883166/src/common/tx.ts#L84)_

---

### `Protected` sigCount

• **sigCount**: _Buffer_ = Buffer.alloc(4)

_Defined in [src/apis/platformvm/addsubnetvalidatortx.ts:62](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/addsubnetvalidatortx.ts#L62)_

---

### `Protected` sigIdxs

• **sigIdxs**: _[SigIdx](common_signature.sigidx)[]_ = []

_Defined in [src/apis/platformvm/addsubnetvalidatortx.ts:63](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/addsubnetvalidatortx.ts#L63)_

---

### `Protected` startTime

• **startTime**: _Buffer_ = Buffer.alloc(8)

_Defined in [src/apis/platformvm/addsubnetvalidatortx.ts:57](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/addsubnetvalidatortx.ts#L57)_

---

### `Protected` subnetAuth

• **subnetAuth**: _[SubnetAuth](api_platformvm_subnetauth.subnetauth)_

_Defined in [src/apis/platformvm/addsubnetvalidatortx.ts:61](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/addsubnetvalidatortx.ts#L61)_

---

### `Protected` subnetID

• **subnetID**: _Buffer_ = Buffer.alloc(32)

_Defined in [src/apis/platformvm/addsubnetvalidatortx.ts:60](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/addsubnetvalidatortx.ts#L60)_

---

### `Protected` weight

• **weight**: _Buffer_ = Buffer.alloc(8)

_Defined in [src/apis/platformvm/addsubnetvalidatortx.ts:59](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/addsubnetvalidatortx.ts#L59)_

## Methods

### addSignatureIdx

▸ **addSignatureIdx**(`addressIdx`: number, `address`: Buffer): _void_

_Defined in [src/apis/platformvm/addsubnetvalidatortx.ts:198](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/addsubnetvalidatortx.ts#L198)_

Creates and adds a [SigIdx](common_signature.sigidx) to the [AddSubnetValidatorTx](api_platformvm_addsubnetvalidatortx.addsubnetvalidatortx).

**Parameters:**

| Name         | Type   | Description                                             |
| ------------ | ------ | ------------------------------------------------------- |
| `addressIdx` | number | The index of the address to reference in the signatures |
| `address`    | Buffer | The address of the source of the signature              |

**Returns:** _void_

---

### clone

▸ **clone**(): _this_

_Overrides [ValidatorTx](api_platformvm_validationtx.validatortx).[clone](api_platformvm_validationtx.validatortx#clone)_

_Defined in [src/apis/platformvm/addsubnetvalidatortx.ts:181](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/addsubnetvalidatortx.ts#L181)_

**Returns:** _this_

---

### create

▸ **create**(...`args`: any[]): _this_

_Overrides [ValidatorTx](api_platformvm_validationtx.validatortx).[create](api_platformvm_validationtx.validatortx#create)_

_Defined in [src/apis/platformvm/addsubnetvalidatortx.ts:188](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/addsubnetvalidatortx.ts#L188)_

**Parameters:**

| Name      | Type  |
| --------- | ----- |
| `...args` | any[] |

**Returns:** _this_

---

### deserialize

▸ **deserialize**(`fields`: object, `encoding`: [SerializedEncoding](../modules/utils_serialization#serializedencoding)): _void_

_Overrides [BaseTx](api_platformvm_basetx.basetx).[deserialize](api_platformvm_basetx.basetx#deserialize)_

_Defined in [src/apis/platformvm/addsubnetvalidatortx.ts:40](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/addsubnetvalidatortx.ts#L40)_

**Parameters:**

| Name       | Type                                                                    | Default |
| ---------- | ----------------------------------------------------------------------- | ------- |
| `fields`   | object                                                                  | -       |
| `encoding` | [SerializedEncoding](../modules/utils_serialization#serializedencoding) | "hex"   |

**Returns:** _void_

---

### fromBuffer

▸ **fromBuffer**(`bytes`: Buffer, `offset`: number): _number_

_Overrides [BaseTx](api_platformvm_basetx.basetx).[fromBuffer](api_platformvm_basetx.basetx#frombuffer)_

_Defined in [src/apis/platformvm/addsubnetvalidatortx.ts:129](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/addsubnetvalidatortx.ts#L129)_

Takes a [Buffer](https://github.com/feross/buffer) containing an [AddSubnetValidatorTx](api_platformvm_addsubnetvalidatortx.addsubnetvalidatortx), parses it, populates the class, and returns the length of the [CreateChainTx](api_platformvm_createchaintx.createchaintx) in bytes.

**`remarks`** assume not-checksummed

**Parameters:**

| Name     | Type   | Default | Description                                                                                                                                    |
| -------- | ------ | ------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| `bytes`  | Buffer | -       | A [Buffer](https://github.com/feross/buffer) containing a raw [AddSubnetValidatorTx](api_platformvm_addsubnetvalidatortx.addsubnetvalidatortx) |
| `offset` | number | 0       | -                                                                                                                                              |

**Returns:** _number_

The length of the raw [AddSubnetValidatorTx](api_platformvm_addsubnetvalidatortx.addsubnetvalidatortx)

---

### getBlockchainID

▸ **getBlockchainID**(): _Buffer_

_Inherited from [StandardBaseTx](common_transactions.standardbasetx).[getBlockchainID](common_transactions.standardbasetx#getblockchainid)_

_Defined in [src/common/tx.ts:104](https://github.com/chain4travel/caminojs/blob/3883166/src/common/tx.ts#L104)_

Returns the Buffer representation of the BlockchainID

**Returns:** _Buffer_

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

_Defined in [src/apis/platformvm/addsubnetvalidatortx.ts:219](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/addsubnetvalidatortx.ts#L219)_

**Returns:** _number_

---

### getEndTime

▸ **getEndTime**(): _BN_

_Defined in [src/apis/platformvm/addsubnetvalidatortx.ts:96](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/addsubnetvalidatortx.ts#L96)_

Returns a [BN](https://github.com/indutny/bn.js/) for the endTime.

**Returns:** _BN_

---

### getIns

▸ **getIns**(): _[TransferableInput](api_platformvm_inputs.transferableinput)[]_

_Inherited from [ImportTx](api_platformvm_importtx.importtx).[getIns](api_platformvm_importtx.importtx#getins)_

_Overrides [StandardBaseTx](common_transactions.standardbasetx).[getIns](common_transactions.standardbasetx#abstract-getins)_

_Defined in [src/apis/platformvm/basetx.ts:52](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/basetx.ts#L52)_

**Returns:** _[TransferableInput](api_platformvm_inputs.transferableinput)[]_

---

### getMemo

▸ **getMemo**(): _Buffer_

_Inherited from [StandardBaseTx](common_transactions.standardbasetx).[getMemo](common_transactions.standardbasetx#getmemo)_

_Defined in [src/common/tx.ts:126](https://github.com/chain4travel/caminojs/blob/3883166/src/common/tx.ts#L126)_

Returns the [Buffer](https://github.com/feross/buffer) representation of the memo

**Returns:** _Buffer_

---

### getNetworkID

▸ **getNetworkID**(): _number_

_Inherited from [StandardBaseTx](common_transactions.standardbasetx).[getNetworkID](common_transactions.standardbasetx#getnetworkid)_

_Defined in [src/common/tx.ts:97](https://github.com/chain4travel/caminojs/blob/3883166/src/common/tx.ts#L97)_

Returns the NetworkID as a number

**Returns:** _number_

---

### getNodeID

▸ **getNodeID**(): _Buffer_

_Defined in [src/apis/platformvm/addsubnetvalidatortx.ts:75](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/addsubnetvalidatortx.ts#L75)_

Returns a [Buffer](https://github.com/feross/buffer) for the stake amount.

**Returns:** _Buffer_

---

### getNodeIDString

▸ **getNodeIDString**(): _string_

_Defined in [src/apis/platformvm/addsubnetvalidatortx.ts:82](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/addsubnetvalidatortx.ts#L82)_

Returns a string for the nodeID amount.

**Returns:** _string_

---

### getOuts

▸ **getOuts**(): _[TransferableOutput](api_platformvm_outputs.transferableoutput)[]_

_Inherited from [ImportTx](api_platformvm_importtx.importtx).[getOuts](api_platformvm_importtx.importtx#getouts)_

_Overrides [StandardBaseTx](common_transactions.standardbasetx).[getOuts](common_transactions.standardbasetx#abstract-getouts)_

_Defined in [src/apis/platformvm/basetx.ts:48](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/basetx.ts#L48)_

**Returns:** _[TransferableOutput](api_platformvm_outputs.transferableoutput)[]_

---

### getSigIdxs

▸ **getSigIdxs**(): _[SigIdx](common_signature.sigidx)[]_

_Defined in [src/apis/platformvm/addsubnetvalidatortx.ts:215](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/addsubnetvalidatortx.ts#L215)_

Returns the array of [SigIdx](common_signature.sigidx) for this [Input](common_inputs.input)

**Returns:** _[SigIdx](common_signature.sigidx)[]_

---

### getStartTime

▸ **getStartTime**(): _BN_

_Defined in [src/apis/platformvm/addsubnetvalidatortx.ts:89](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/addsubnetvalidatortx.ts#L89)_

Returns a [BN](https://github.com/indutny/bn.js/) for the startTime.

**Returns:** _BN_

---

### getSubnetAuth

▸ **getSubnetAuth**(): _[SubnetAuth](api_platformvm_subnetauth.subnetauth)_

_Defined in [src/apis/platformvm/addsubnetvalidatortx.ts:116](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/addsubnetvalidatortx.ts#L116)_

Returns the subnetAuth

**Returns:** _[SubnetAuth](api_platformvm_subnetauth.subnetauth)_

---

### getSubnetID

▸ **getSubnetID**(): _string_

_Defined in [src/apis/platformvm/addsubnetvalidatortx.ts:110](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/addsubnetvalidatortx.ts#L110)_

Returns the subnetID as a string

**Returns:** _string_

---

### getTotalOuts

▸ **getTotalOuts**(): _[TransferableOutput](api_platformvm_outputs.transferableoutput)[]_

_Inherited from [ImportTx](api_platformvm_importtx.importtx).[getTotalOuts](api_platformvm_importtx.importtx#gettotalouts)_

_Overrides [StandardBaseTx](common_transactions.standardbasetx).[getTotalOuts](common_transactions.standardbasetx#abstract-gettotalouts)_

_Defined in [src/apis/platformvm/basetx.ts:56](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/basetx.ts#L56)_

**Returns:** _[TransferableOutput](api_platformvm_outputs.transferableoutput)[]_

---

### getTxType

▸ **getTxType**(): _number_

_Overrides [ValidatorTx](api_platformvm_validationtx.validatortx).[getTxType](api_platformvm_validationtx.validatortx#gettxtype)_

_Defined in [src/apis/platformvm/addsubnetvalidatortx.ts:68](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/addsubnetvalidatortx.ts#L68)_

Returns the id of the [AddSubnetValidatorTx](api_platformvm_addsubnetvalidatortx.addsubnetvalidatortx)

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

### getWeight

▸ **getWeight**(): _BN_

_Defined in [src/apis/platformvm/addsubnetvalidatortx.ts:103](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/addsubnetvalidatortx.ts#L103)_

Returns a [BN](https://github.com/indutny/bn.js/) for the weight

**Returns:** _BN_

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

▸ **select**(`id`: number, ...`args`: any[]): _this_

_Inherited from [ImportTx](api_platformvm_importtx.importtx).[select](api_platformvm_importtx.importtx#select)_

_Overrides [StandardBaseTx](common_transactions.standardbasetx).[select](common_transactions.standardbasetx#abstract-select)_

_Defined in [src/apis/platformvm/basetx.ts:146](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/basetx.ts#L146)_

**Parameters:**

| Name      | Type   |
| --------- | ------ |
| `id`      | number |
| `...args` | any[]  |

**Returns:** _this_

---

### serialize

▸ **serialize**(`encoding`: [SerializedEncoding](../modules/utils_serialization#serializedencoding)): _object_

_Overrides [StandardBaseTx](common_transactions.standardbasetx).[serialize](common_transactions.standardbasetx#serialize)_

_Defined in [src/apis/platformvm/addsubnetvalidatortx.ts:32](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/addsubnetvalidatortx.ts#L32)_

**Parameters:**

| Name       | Type                                                                    | Default |
| ---------- | ----------------------------------------------------------------------- | ------- |
| `encoding` | [SerializedEncoding](../modules/utils_serialization#serializedencoding) | "hex"   |

**Returns:** _object_

---

### sign

▸ **sign**(`msg`: Buffer, `kc`: [KeyChain](api_platformvm_keychain.keychain)): _[Credential](common_signature.credential)[]_

_Overrides [ExportTx](api_platformvm_exporttx.exporttx).[sign](api_platformvm_exporttx.exporttx#sign)_

_Defined in [src/apis/platformvm/addsubnetvalidatortx.ts:231](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/addsubnetvalidatortx.ts#L231)_

Takes the bytes of an [UnsignedTx](api_evm_transactions.unsignedtx) and returns an array of [Credential](common_signature.credential)s

**Parameters:**

| Name  | Type                                         | Description                                                    |
| ----- | -------------------------------------------- | -------------------------------------------------------------- |
| `msg` | Buffer                                       | A Buffer for the [UnsignedTx](api_evm_transactions.unsignedtx) |
| `kc`  | [KeyChain](api_platformvm_keychain.keychain) | An [KeyChain](api_evm_keychain.keychain) used in signing       |

**Returns:** _[Credential](common_signature.credential)[]_

An array of [Credential](common_signature.credential)s

---

### toBuffer

▸ **toBuffer**(): _Buffer_

_Overrides [StandardBaseTx](common_transactions.standardbasetx).[toBuffer](common_transactions.standardbasetx#tobuffer)_

_Defined in [src/apis/platformvm/addsubnetvalidatortx.ts:157](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/addsubnetvalidatortx.ts#L157)_

Returns a [Buffer](https://github.com/feross/buffer) representation of the [CreateChainTx](api_platformvm_createchaintx.createchaintx).

**Returns:** _Buffer_

---

### toString

▸ **toString**(): _string_

_Inherited from [StandardBaseTx](common_transactions.standardbasetx).[toString](common_transactions.standardbasetx#tostring)_

_Defined in [src/common/tx.ts:166](https://github.com/chain4travel/caminojs/blob/3883166/src/common/tx.ts#L166)_

Returns a base-58 representation of the [StandardBaseTx](common_transactions.standardbasetx).

**Returns:** _string_

---

### toStringHex

▸ **toStringHex**(): _string_

_Inherited from [StandardBaseTx](common_transactions.standardbasetx).[toStringHex](common_transactions.standardbasetx#tostringhex)_

_Defined in [src/common/tx.ts:170](https://github.com/chain4travel/caminojs/blob/3883166/src/common/tx.ts#L170)_

**Returns:** _string_
