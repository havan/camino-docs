# Class: ExportTx

Class representing an unsigned Export transaction.

## Hierarchy

↳ [BaseTx](api_platformvm_basetx.basetx)

↳ **ExportTx**

## Index

### Constructors

- [constructor](api_platformvm_exporttx.exporttx#constructor)

### Properties

- [\_codecID](api_platformvm_exporttx.exporttx#protected-_codecid)
- [\_typeID](api_platformvm_exporttx.exporttx#protected-_typeid)
- [\_typeName](api_platformvm_exporttx.exporttx#protected-_typename)
- [blockchainID](api_platformvm_exporttx.exporttx#protected-blockchainid)
- [destinationChain](api_platformvm_exporttx.exporttx#protected-destinationchain)
- [exportOuts](api_platformvm_exporttx.exporttx#protected-exportouts)
- [ins](api_platformvm_exporttx.exporttx#protected-ins)
- [memo](api_platformvm_exporttx.exporttx#protected-memo)
- [networkID](api_platformvm_exporttx.exporttx#protected-networkid)
- [numOuts](api_platformvm_exporttx.exporttx#protected-numouts)
- [numins](api_platformvm_exporttx.exporttx#protected-numins)
- [numouts](api_platformvm_exporttx.exporttx#protected-numouts)
- [outs](api_platformvm_exporttx.exporttx#protected-outs)

### Methods

- [clone](api_platformvm_exporttx.exporttx#clone)
- [create](api_platformvm_exporttx.exporttx#create)
- [deserialize](api_platformvm_exporttx.exporttx#deserialize)
- [fromBuffer](api_platformvm_exporttx.exporttx#frombuffer)
- [getBlockchainID](api_platformvm_exporttx.exporttx#getblockchainid)
- [getCodecID](api_platformvm_exporttx.exporttx#getcodecid)
- [getDestinationChain](api_platformvm_exporttx.exporttx#getdestinationchain)
- [getExportOutputs](api_platformvm_exporttx.exporttx#getexportoutputs)
- [getExportTotal](api_platformvm_exporttx.exporttx#getexporttotal)
- [getIns](api_platformvm_exporttx.exporttx#getins)
- [getMemo](api_platformvm_exporttx.exporttx#getmemo)
- [getNetworkID](api_platformvm_exporttx.exporttx#getnetworkid)
- [getOuts](api_platformvm_exporttx.exporttx#getouts)
- [getTotalOuts](api_platformvm_exporttx.exporttx#gettotalouts)
- [getTxType](api_platformvm_exporttx.exporttx#gettxtype)
- [getTypeID](api_platformvm_exporttx.exporttx#gettypeid)
- [getTypeName](api_platformvm_exporttx.exporttx#gettypename)
- [sanitizeObject](api_platformvm_exporttx.exporttx#sanitizeobject)
- [select](api_platformvm_exporttx.exporttx#select)
- [serialize](api_platformvm_exporttx.exporttx#serialize)
- [sign](api_platformvm_exporttx.exporttx#sign)
- [toBuffer](api_platformvm_exporttx.exporttx#tobuffer)
- [toString](api_platformvm_exporttx.exporttx#tostring)
- [toStringHex](api_platformvm_exporttx.exporttx#tostringhex)

## Constructors

### constructor

\+ **new ExportTx**(`networkID`: number, `blockchainID`: Buffer, `outs`: [TransferableOutput](api_platformvm_outputs.transferableoutput)[], `ins`: [TransferableInput](api_platformvm_inputs.transferableinput)[], `memo`: Buffer, `destinationChain`: Buffer, `exportOuts`: [TransferableOutput](api_platformvm_outputs.transferableoutput)[]): _[ExportTx](api_platformvm_exporttx.exporttx)_

_Overrides [BaseTx](api_platformvm_basetx.basetx).[constructor](api_platformvm_basetx.basetx#constructor)_

_Defined in [src/apis/platformvm/exporttx.ts:156](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/exporttx.ts#L156)_

Class representing an unsigned Export transaction.

**Parameters:**

| Name               | Type                                                              | Default              | Description                                                                               |
| ------------------ | ----------------------------------------------------------------- | -------------------- | ----------------------------------------------------------------------------------------- |
| `networkID`        | number                                                            | DefaultNetworkID     | Optional networkID, [DefaultNetworkID](../modules/utils_constants#const-defaultnetworkid) |
| `blockchainID`     | Buffer                                                            | Buffer.alloc(32, 16) | Optional blockchainID, default Buffer.alloc(32, 16)                                       |
| `outs`             | [TransferableOutput](api_platformvm_outputs.transferableoutput)[] | undefined            | Optional array of the [TransferableOutput](api_evm_outputs.transferableoutput)s           |
| `ins`              | [TransferableInput](api_platformvm_inputs.transferableinput)[]    | undefined            | Optional array of the [TransferableInput](api_evm_inputs.transferableinput)s              |
| `memo`             | Buffer                                                            | undefined            | Optional [Buffer](https://github.com/feross/buffer) for the memo field                    |
| `destinationChain` | Buffer                                                            | undefined            | Optional chainid which identifies where the funds will send to.                           |
| `exportOuts`       | [TransferableOutput](api_platformvm_outputs.transferableoutput)[] | undefined            | Array of [[TransferableOutputs]]s used in the transaction                                 |

**Returns:** _[ExportTx](api_platformvm_exporttx.exporttx)_

## Properties

### `Protected` \_codecID

• **\_codecID**: _number_ = undefined

_Inherited from [SigIdx](common_signature.sigidx).[\_codecID](common_signature.sigidx#protected-_codecid)_

_Defined in [src/utils/serialization.ts:51](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/serialization.ts#L51)_

---

### `Protected` \_typeID

• **\_typeID**: _number_ = PlatformVMConstants.EXPORTTX

_Overrides [BaseTx](api_platformvm_basetx.basetx).[\_typeID](api_platformvm_basetx.basetx#protected-_typeid)_

_Defined in [src/apis/platformvm/exporttx.ts:28](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/exporttx.ts#L28)_

---

### `Protected` \_typeName

• **\_typeName**: _string_ = "ExportTx"

_Overrides [BaseTx](api_platformvm_basetx.basetx).[\_typeName](api_platformvm_basetx.basetx#protected-_typename)_

_Defined in [src/apis/platformvm/exporttx.ts:27](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/exporttx.ts#L27)_

---

### `Protected` blockchainID

• **blockchainID**: _Buffer_ = Buffer.alloc(32)

_Inherited from [StandardBaseTx](common_transactions.standardbasetx).[blockchainID](common_transactions.standardbasetx#protected-blockchainid)_

_Defined in [src/common/tx.ts:82](https://github.com/chain4travel/caminojs/blob/3883166/src/common/tx.ts#L82)_

---

### `Protected` destinationChain

• **destinationChain**: _Buffer_ = Buffer.alloc(32)

_Defined in [src/apis/platformvm/exporttx.ts:61](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/exporttx.ts#L61)_

---

### `Protected` exportOuts

• **exportOuts**: _[TransferableOutput](api_platformvm_outputs.transferableoutput)[]_ = []

_Defined in [src/apis/platformvm/exporttx.ts:63](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/exporttx.ts#L63)_

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

### `Protected` numOuts

• **numOuts**: _Buffer_ = Buffer.alloc(4)

_Defined in [src/apis/platformvm/exporttx.ts:62](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/exporttx.ts#L62)_

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

## Methods

### clone

▸ **clone**(): _this_

_Overrides [ValidatorTx](api_platformvm_validationtx.validatortx).[clone](api_platformvm_validationtx.validatortx#clone)_

_Defined in [src/apis/platformvm/exporttx.ts:148](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/exporttx.ts#L148)_

**Returns:** _this_

---

### create

▸ **create**(...`args`: any[]): _this_

_Overrides [ValidatorTx](api_platformvm_validationtx.validatortx).[create](api_platformvm_validationtx.validatortx#create)_

_Defined in [src/apis/platformvm/exporttx.ts:154](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/exporttx.ts#L154)_

**Parameters:**

| Name      | Type  |
| --------- | ----- |
| `...args` | any[] |

**Returns:** _this_

---

### deserialize

▸ **deserialize**(`fields`: object, `encoding`: [SerializedEncoding](../modules/utils_serialization#serializedencoding)): _void_

_Overrides [BaseTx](api_platformvm_basetx.basetx).[deserialize](api_platformvm_basetx.basetx#deserialize)_

_Defined in [src/apis/platformvm/exporttx.ts:43](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/exporttx.ts#L43)_

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

_Defined in [src/apis/platformvm/exporttx.ts:115](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/exporttx.ts#L115)_

Takes a [Buffer](https://github.com/feross/buffer) containing an [ExportTx](api_platformvm_exporttx.exporttx), parses it, populates the class, and returns the length of the [ExportTx](api_platformvm_exporttx.exporttx) in bytes.

**`remarks`** assume not-checksummed

**Parameters:**

| Name     | Type   | Default | Description                                                                                                |
| -------- | ------ | ------- | ---------------------------------------------------------------------------------------------------------- |
| `bytes`  | Buffer | -       | A [Buffer](https://github.com/feross/buffer) containing a raw [ExportTx](api_platformvm_exporttx.exporttx) |
| `offset` | number | 0       | -                                                                                                          |

**Returns:** _number_

The length of the raw [ExportTx](api_platformvm_exporttx.exporttx)

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

### getDestinationChain

▸ **getDestinationChain**(): _Buffer_

_Defined in [src/apis/platformvm/exporttx.ts:102](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/exporttx.ts#L102)_

Returns the destinationChain as a [Buffer](https://github.com/feross/buffer)

**Returns:** _Buffer_

---

### getExportOutputs

▸ **getExportOutputs**(): _[TransferableOutput](api_platformvm_outputs.transferableoutput)[]_

_Defined in [src/apis/platformvm/exporttx.ts:75](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/exporttx.ts#L75)_

Returns an array of [TransferableOutput](api_evm_outputs.transferableoutput)s in this transaction.

**Returns:** _[TransferableOutput](api_platformvm_outputs.transferableoutput)[]_

---

### getExportTotal

▸ **getExportTotal**(): _BN_

_Defined in [src/apis/platformvm/exporttx.ts:82](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/exporttx.ts#L82)_

Returns the total exported amount as a [BN](https://github.com/indutny/bn.js/).

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

### getOuts

▸ **getOuts**(): _[TransferableOutput](api_platformvm_outputs.transferableoutput)[]_

_Inherited from [ImportTx](api_platformvm_importtx.importtx).[getOuts](api_platformvm_importtx.importtx#getouts)_

_Overrides [StandardBaseTx](common_transactions.standardbasetx).[getOuts](common_transactions.standardbasetx#abstract-getouts)_

_Defined in [src/apis/platformvm/basetx.ts:48](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/basetx.ts#L48)_

**Returns:** _[TransferableOutput](api_platformvm_outputs.transferableoutput)[]_

---

### getTotalOuts

▸ **getTotalOuts**(): _[TransferableOutput](api_platformvm_outputs.transferableoutput)[]_

_Overrides [ImportTx](api_platformvm_importtx.importtx).[getTotalOuts](api_platformvm_importtx.importtx#gettotalouts)_

_Defined in [src/apis/platformvm/exporttx.ts:92](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/exporttx.ts#L92)_

**Returns:** _[TransferableOutput](api_platformvm_outputs.transferableoutput)[]_

---

### getTxType

▸ **getTxType**(): _number_

_Overrides [ValidatorTx](api_platformvm_validationtx.validatortx).[getTxType](api_platformvm_validationtx.validatortx#gettxtype)_

_Defined in [src/apis/platformvm/exporttx.ts:68](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/exporttx.ts#L68)_

Returns the id of the [ExportTx](api_platformvm_exporttx.exporttx)

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

_Defined in [src/apis/platformvm/exporttx.ts:30](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/exporttx.ts#L30)_

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

_Overrides [StandardBaseTx](common_transactions.standardbasetx).[toBuffer](common_transactions.standardbasetx#tobuffer)_

_Defined in [src/apis/platformvm/exporttx.ts:133](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/exporttx.ts#L133)_

Returns a [Buffer](https://github.com/feross/buffer) representation of the [ExportTx](api_platformvm_exporttx.exporttx).

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
