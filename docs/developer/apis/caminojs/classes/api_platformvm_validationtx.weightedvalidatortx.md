# Class: WeightedValidatorTx

## Hierarchy

↳ [ValidatorTx](api_platformvm_validationtx.validatortx)

↳ **WeightedValidatorTx**

↳ [AddDelegatorTx](api_platformvm_validationtx.adddelegatortx)

## Index

### Constructors

- [constructor](api_platformvm_validationtx.weightedvalidatortx#constructor)

### Properties

- [\_codecID](api_platformvm_validationtx.weightedvalidatortx#protected-_codecid)
- [\_typeID](api_platformvm_validationtx.weightedvalidatortx#protected-_typeid)
- [\_typeName](api_platformvm_validationtx.weightedvalidatortx#protected-_typename)
- [blockchainID](api_platformvm_validationtx.weightedvalidatortx#protected-blockchainid)
- [endTime](api_platformvm_validationtx.weightedvalidatortx#protected-endtime)
- [ins](api_platformvm_validationtx.weightedvalidatortx#protected-ins)
- [memo](api_platformvm_validationtx.weightedvalidatortx#protected-memo)
- [networkID](api_platformvm_validationtx.weightedvalidatortx#protected-networkid)
- [nodeID](api_platformvm_validationtx.weightedvalidatortx#protected-nodeid)
- [numins](api_platformvm_validationtx.weightedvalidatortx#protected-numins)
- [numouts](api_platformvm_validationtx.weightedvalidatortx#protected-numouts)
- [outs](api_platformvm_validationtx.weightedvalidatortx#protected-outs)
- [startTime](api_platformvm_validationtx.weightedvalidatortx#protected-starttime)
- [weight](api_platformvm_validationtx.weightedvalidatortx#protected-weight)

### Methods

- [clone](api_platformvm_validationtx.weightedvalidatortx#clone)
- [create](api_platformvm_validationtx.weightedvalidatortx#create)
- [deserialize](api_platformvm_validationtx.weightedvalidatortx#deserialize)
- [fromBuffer](api_platformvm_validationtx.weightedvalidatortx#frombuffer)
- [getBlockchainID](api_platformvm_validationtx.weightedvalidatortx#getblockchainid)
- [getCodecID](api_platformvm_validationtx.weightedvalidatortx#getcodecid)
- [getEndTime](api_platformvm_validationtx.weightedvalidatortx#getendtime)
- [getIns](api_platformvm_validationtx.weightedvalidatortx#getins)
- [getMemo](api_platformvm_validationtx.weightedvalidatortx#getmemo)
- [getNetworkID](api_platformvm_validationtx.weightedvalidatortx#getnetworkid)
- [getNodeID](api_platformvm_validationtx.weightedvalidatortx#getnodeid)
- [getNodeIDString](api_platformvm_validationtx.weightedvalidatortx#getnodeidstring)
- [getOuts](api_platformvm_validationtx.weightedvalidatortx#getouts)
- [getStartTime](api_platformvm_validationtx.weightedvalidatortx#getstarttime)
- [getTotalOuts](api_platformvm_validationtx.weightedvalidatortx#gettotalouts)
- [getTxType](api_platformvm_validationtx.weightedvalidatortx#gettxtype)
- [getTypeID](api_platformvm_validationtx.weightedvalidatortx#gettypeid)
- [getTypeName](api_platformvm_validationtx.weightedvalidatortx#gettypename)
- [getWeight](api_platformvm_validationtx.weightedvalidatortx#getweight)
- [getWeightBuffer](api_platformvm_validationtx.weightedvalidatortx#getweightbuffer)
- [sanitizeObject](api_platformvm_validationtx.weightedvalidatortx#sanitizeobject)
- [select](api_platformvm_validationtx.weightedvalidatortx#select)
- [serialize](api_platformvm_validationtx.weightedvalidatortx#serialize)
- [sign](api_platformvm_validationtx.weightedvalidatortx#sign)
- [toBuffer](api_platformvm_validationtx.weightedvalidatortx#tobuffer)
- [toString](api_platformvm_validationtx.weightedvalidatortx#tostring)
- [toStringHex](api_platformvm_validationtx.weightedvalidatortx#tostringhex)

## Constructors

### constructor

\+ **new WeightedValidatorTx**(`networkID`: number, `blockchainID`: Buffer, `outs`: [TransferableOutput](api_platformvm_outputs.transferableoutput)[], `ins`: [TransferableInput](api_platformvm_inputs.transferableinput)[], `memo`: Buffer, `nodeID`: Buffer, `startTime`: BN, `endTime`: BN, `weight`: BN): _[WeightedValidatorTx](api_platformvm_validationtx.weightedvalidatortx)_

_Overrides [ValidatorTx](api_platformvm_validationtx.validatortx).[constructor](api_platformvm_validationtx.validatortx#constructor)_

_Defined in [src/apis/platformvm/validationtx.ts:207](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/validationtx.ts#L207)_

Class representing an unsigned AddSubnetValidatorTx transaction.

**Parameters:**

| Name           | Type                                                              | Default              | Description                                                                                                    |
| -------------- | ----------------------------------------------------------------- | -------------------- | -------------------------------------------------------------------------------------------------------------- |
| `networkID`    | number                                                            | DefaultNetworkID     | Optional. Networkid, [DefaultNetworkID](../modules/utils_constants#const-defaultnetworkid)                     |
| `blockchainID` | Buffer                                                            | Buffer.alloc(32, 16) | Optional. Blockchainid, default Buffer.alloc(32, 16)                                                           |
| `outs`         | [TransferableOutput](api_platformvm_outputs.transferableoutput)[] | undefined            | Optional. Array of the [TransferableOutput](api_evm_outputs.transferableoutput)s                               |
| `ins`          | [TransferableInput](api_platformvm_inputs.transferableinput)[]    | undefined            | Optional. Array of the [TransferableInput](api_evm_inputs.transferableinput)s                                  |
| `memo`         | Buffer                                                            | undefined            | Optional. [Buffer](https://github.com/feross/buffer) for the memo field                                        |
| `nodeID`       | Buffer                                                            | undefined            | Optional. The node ID of the validator being added.                                                            |
| `startTime`    | BN                                                                | undefined            | Optional. The Unix time when the validator starts validating the Primary Network.                              |
| `endTime`      | BN                                                                | undefined            | Optional. The Unix time when the validator stops validating the Primary Network (and staked AVAX is returned). |
| `weight`       | BN                                                                | undefined            | Optional. The amount of nAVAX the validator is staking.                                                        |

**Returns:** _[WeightedValidatorTx](api_platformvm_validationtx.weightedvalidatortx)_

## Properties

### `Protected` \_codecID

• **\_codecID**: _number_ = undefined

_Inherited from [SigIdx](common_signature.sigidx).[\_codecID](common_signature.sigidx#protected-_codecid)_

_Defined in [src/utils/serialization.ts:51](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/serialization.ts#L51)_

---

### `Protected` \_typeID

• **\_typeID**: _any_ = undefined

_Overrides [ValidatorTx](api_platformvm_validationtx.validatortx).[\_typeID](api_platformvm_validationtx.validatortx#protected-_typeid)_

_Defined in [src/apis/platformvm/validationtx.ts:153](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/validationtx.ts#L153)_

---

### `Protected` \_typeName

• **\_typeName**: _string_ = "WeightedValidatorTx"

_Overrides [ValidatorTx](api_platformvm_validationtx.validatortx).[\_typeName](api_platformvm_validationtx.validatortx#protected-_typename)_

_Defined in [src/apis/platformvm/validationtx.ts:152](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/validationtx.ts#L152)_

---

### `Protected` blockchainID

• **blockchainID**: _Buffer_ = Buffer.alloc(32)

_Inherited from [StandardBaseTx](common_transactions.standardbasetx).[blockchainID](common_transactions.standardbasetx#protected-blockchainid)_

_Defined in [src/common/tx.ts:82](https://github.com/chain4travel/caminojs/blob/3883166/src/common/tx.ts#L82)_

---

### `Protected` endTime

• **endTime**: _Buffer_ = Buffer.alloc(8)

_Inherited from [ValidatorTx](api_platformvm_validationtx.validatortx).[endTime](api_platformvm_validationtx.validatortx#protected-endtime)_

_Defined in [src/apis/platformvm/validationtx.ts:78](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/validationtx.ts#L78)_

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

_Inherited from [ValidatorTx](api_platformvm_validationtx.validatortx).[nodeID](api_platformvm_validationtx.validatortx#protected-nodeid)_

_Defined in [src/apis/platformvm/validationtx.ts:76](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/validationtx.ts#L76)_

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

### `Protected` startTime

• **startTime**: _Buffer_ = Buffer.alloc(8)

_Inherited from [ValidatorTx](api_platformvm_validationtx.validatortx).[startTime](api_platformvm_validationtx.validatortx#protected-starttime)_

_Defined in [src/apis/platformvm/validationtx.ts:77](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/validationtx.ts#L77)_

---

### `Protected` weight

• **weight**: _Buffer_ = Buffer.alloc(8)

_Defined in [src/apis/platformvm/validationtx.ts:178](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/validationtx.ts#L178)_

## Methods

### clone

▸ **clone**(): _this_

_Inherited from [ValidatorTx](api_platformvm_validationtx.validatortx).[clone](api_platformvm_validationtx.validatortx#clone)_

_Overrides [StandardBaseTx](common_transactions.standardbasetx).[clone](common_transactions.standardbasetx#abstract-clone)_

_Defined in [src/apis/platformvm/basetx.ts:136](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/basetx.ts#L136)_

**Returns:** _this_

---

### create

▸ **create**(...`args`: any[]): _this_

_Inherited from [ValidatorTx](api_platformvm_validationtx.validatortx).[create](api_platformvm_validationtx.validatortx#create)_

_Overrides [StandardBaseTx](common_transactions.standardbasetx).[create](common_transactions.standardbasetx#abstract-create)_

_Defined in [src/apis/platformvm/basetx.ts:142](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/basetx.ts#L142)_

**Parameters:**

| Name      | Type  |
| --------- | ----- |
| `...args` | any[] |

**Returns:** _this_

---

### deserialize

▸ **deserialize**(`fields`: object, `encoding`: [SerializedEncoding](../modules/utils_serialization#serializedencoding)): _void_

_Overrides [ValidatorTx](api_platformvm_validationtx.validatortx).[deserialize](api_platformvm_validationtx.validatortx#deserialize)_

_Defined in [src/apis/platformvm/validationtx.ts:167](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/validationtx.ts#L167)_

**Parameters:**

| Name       | Type                                                                    | Default |
| ---------- | ----------------------------------------------------------------------- | ------- |
| `fields`   | object                                                                  | -       |
| `encoding` | [SerializedEncoding](../modules/utils_serialization#serializedencoding) | "hex"   |

**Returns:** _void_

---

### fromBuffer

▸ **fromBuffer**(`bytes`: Buffer, `offset`: number): _number_

_Overrides [ValidatorTx](api_platformvm_validationtx.validatortx).[fromBuffer](api_platformvm_validationtx.validatortx#frombuffer)_

_Defined in [src/apis/platformvm/validationtx.ts:194](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/validationtx.ts#L194)_

**Parameters:**

| Name     | Type   | Default |
| -------- | ------ | ------- |
| `bytes`  | Buffer | -       |
| `offset` | number | 0       |

**Returns:** _number_

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

### getEndTime

▸ **getEndTime**(): _BN‹›_

_Inherited from [ValidatorTx](api_platformvm_validationtx.validatortx).[getEndTime](api_platformvm_validationtx.validatortx#getendtime)_

_Defined in [src/apis/platformvm/validationtx.ts:103](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/validationtx.ts#L103)_

Returns a [BN](https://github.com/indutny/bn.js/) for the stake amount.

**Returns:** _BN‹›_

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

_Inherited from [ValidatorTx](api_platformvm_validationtx.validatortx).[getNodeID](api_platformvm_validationtx.validatortx#getnodeid)_

_Defined in [src/apis/platformvm/validationtx.ts:83](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/validationtx.ts#L83)_

Returns a [Buffer](https://github.com/feross/buffer) for the stake amount.

**Returns:** _Buffer_

---

### getNodeIDString

▸ **getNodeIDString**(): _string_

_Inherited from [ValidatorTx](api_platformvm_validationtx.validatortx).[getNodeIDString](api_platformvm_validationtx.validatortx#getnodeidstring)_

_Defined in [src/apis/platformvm/validationtx.ts:90](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/validationtx.ts#L90)_

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

### getStartTime

▸ **getStartTime**(): _BN‹›_

_Inherited from [ValidatorTx](api_platformvm_validationtx.validatortx).[getStartTime](api_platformvm_validationtx.validatortx#getstarttime)_

_Defined in [src/apis/platformvm/validationtx.ts:96](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/validationtx.ts#L96)_

Returns a [BN](https://github.com/indutny/bn.js/) for the stake amount.

**Returns:** _BN‹›_

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

_Inherited from [ValidatorTx](api_platformvm_validationtx.validatortx).[getTxType](api_platformvm_validationtx.validatortx#gettxtype)_

_Overrides [StandardBaseTx](common_transactions.standardbasetx).[getTxType](common_transactions.standardbasetx#abstract-gettxtype)_

_Defined in [src/apis/platformvm/basetx.ts:63](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/basetx.ts#L63)_

Returns the id of the [BaseTx](api_avm_basetx.basetx)

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

_Defined in [src/apis/platformvm/validationtx.ts:183](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/validationtx.ts#L183)_

Returns a [BN](https://github.com/indutny/bn.js/) for the stake amount.

**Returns:** _BN_

---

### getWeightBuffer

▸ **getWeightBuffer**(): _Buffer_

_Defined in [src/apis/platformvm/validationtx.ts:190](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/validationtx.ts#L190)_

Returns a [Buffer](https://github.com/feross/buffer) for the stake amount.

**Returns:** _Buffer_

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

_Overrides [ValidatorTx](api_platformvm_validationtx.validatortx).[serialize](api_platformvm_validationtx.validatortx#serialize)_

_Defined in [src/apis/platformvm/validationtx.ts:155](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/validationtx.ts#L155)_

**Parameters:**

| Name       | Type                                                                    | Default |
| ---------- | ----------------------------------------------------------------------- | ------- |
| `encoding` | [SerializedEncoding](../modules/utils_serialization#serializedencoding) | "hex"   |

**Returns:** _object_

---

### sign

▸ **sign**(`msg`: Buffer, `kc`: [KeyChain](api_platformvm_keychain.keychain)): _[Credential](common_signature.credential)[]_

_Inherited from [ExportTx](api_platformvm_exporttx.exporttx).[sign](api_platformvm_exporttx.exporttx#sign)_

_Overrides [StandardBaseTx](common_transactions.standardbasetx).[sign](common_transactions.standardbasetx#abstract-sign)_

_Defined in [src/apis/platformvm/basetx.ts:117](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/basetx.ts#L117)_

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

_Overrides [ValidatorTx](api_platformvm_validationtx.validatortx).[toBuffer](api_platformvm_validationtx.validatortx#tobuffer)_

_Defined in [src/apis/platformvm/validationtx.ts:204](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/validationtx.ts#L204)_

Returns a [Buffer](https://github.com/feross/buffer) representation of the [AddSubnetValidatorTx](../modules/src_apis_platformvm#addsubnetvalidatortx).

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
