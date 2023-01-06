# Class: ImportTx

Class representing an unsigned Import transaction.

## Hierarchy

↳ [BaseTx](api_platformvm_basetx.basetx)

↳ **ImportTx**

## Index

### Constructors

- [constructor](api_platformvm_importtx.importtx#constructor)

### Properties

- [\_codecID](api_platformvm_importtx.importtx#protected-_codecid)
- [\_typeID](api_platformvm_importtx.importtx#protected-_typeid)
- [\_typeName](api_platformvm_importtx.importtx#protected-_typename)
- [blockchainID](api_platformvm_importtx.importtx#protected-blockchainid)
- [importIns](api_platformvm_importtx.importtx#protected-importins)
- [ins](api_platformvm_importtx.importtx#protected-ins)
- [memo](api_platformvm_importtx.importtx#protected-memo)
- [networkID](api_platformvm_importtx.importtx#protected-networkid)
- [numIns](api_platformvm_importtx.importtx#protected-numins)
- [numins](api_platformvm_importtx.importtx#protected-numins)
- [numouts](api_platformvm_importtx.importtx#protected-numouts)
- [outs](api_platformvm_importtx.importtx#protected-outs)
- [sourceChain](api_platformvm_importtx.importtx#protected-sourcechain)

### Methods

- [clone](api_platformvm_importtx.importtx#clone)
- [create](api_platformvm_importtx.importtx#create)
- [deserialize](api_platformvm_importtx.importtx#deserialize)
- [fromBuffer](api_platformvm_importtx.importtx#frombuffer)
- [getBlockchainID](api_platformvm_importtx.importtx#getblockchainid)
- [getCodecID](api_platformvm_importtx.importtx#getcodecid)
- [getImportInputs](api_platformvm_importtx.importtx#getimportinputs)
- [getIns](api_platformvm_importtx.importtx#getins)
- [getMemo](api_platformvm_importtx.importtx#getmemo)
- [getNetworkID](api_platformvm_importtx.importtx#getnetworkid)
- [getOuts](api_platformvm_importtx.importtx#getouts)
- [getSourceChain](api_platformvm_importtx.importtx#getsourcechain)
- [getTotalOuts](api_platformvm_importtx.importtx#gettotalouts)
- [getTxType](api_platformvm_importtx.importtx#gettxtype)
- [getTypeID](api_platformvm_importtx.importtx#gettypeid)
- [getTypeName](api_platformvm_importtx.importtx#gettypename)
- [sanitizeObject](api_platformvm_importtx.importtx#sanitizeobject)
- [select](api_platformvm_importtx.importtx#select)
- [serialize](api_platformvm_importtx.importtx#serialize)
- [sign](api_platformvm_importtx.importtx#sign)
- [toBuffer](api_platformvm_importtx.importtx#tobuffer)
- [toString](api_platformvm_importtx.importtx#tostring)
- [toStringHex](api_platformvm_importtx.importtx#tostringhex)

## Constructors

### constructor

\+ **new ImportTx**(`networkID`: number, `blockchainID`: Buffer, `outs`: [TransferableOutput](api_platformvm_outputs.transferableoutput)[], `ins`: [TransferableInput](api_platformvm_inputs.transferableinput)[], `memo`: Buffer, `sourceChain`: Buffer, `importIns`: [TransferableInput](api_platformvm_inputs.transferableinput)[]): _[ImportTx](api_platformvm_importtx.importtx)_

_Overrides [BaseTx](api_platformvm_basetx.basetx).[constructor](api_platformvm_basetx.basetx#constructor)_

_Defined in [src/apis/platformvm/importtx.ts:163](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/importtx.ts#L163)_

Class representing an unsigned Import transaction.

**Parameters:**

| Name           | Type                                                              | Default              | Description                                                                               |
| -------------- | ----------------------------------------------------------------- | -------------------- | ----------------------------------------------------------------------------------------- |
| `networkID`    | number                                                            | DefaultNetworkID     | Optional networkID, [DefaultNetworkID](../modules/utils_constants#const-defaultnetworkid) |
| `blockchainID` | Buffer                                                            | Buffer.alloc(32, 16) | Optional blockchainID, default Buffer.alloc(32, 16)                                       |
| `outs`         | [TransferableOutput](api_platformvm_outputs.transferableoutput)[] | undefined            | Optional array of the [TransferableOutput](api_evm_outputs.transferableoutput)s           |
| `ins`          | [TransferableInput](api_platformvm_inputs.transferableinput)[]    | undefined            | Optional array of the [TransferableInput](api_evm_inputs.transferableinput)s              |
| `memo`         | Buffer                                                            | undefined            | Optional [Buffer](https://github.com/feross/buffer) for the memo field                    |
| `sourceChain`  | Buffer                                                            | undefined            | Optiona chainid for the source inputs to import. Default platform chainid.                |
| `importIns`    | [TransferableInput](api_platformvm_inputs.transferableinput)[]    | undefined            | Array of [TransferableInput](api_evm_inputs.transferableinput)s used in the transaction   |

**Returns:** _[ImportTx](api_platformvm_importtx.importtx)_

## Properties

### `Protected` \_codecID

• **\_codecID**: _number_ = undefined

_Inherited from [SigIdx](common_signature.sigidx).[\_codecID](common_signature.sigidx#protected-_codecid)_

_Defined in [src/utils/serialization.ts:51](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/serialization.ts#L51)_

---

### `Protected` \_typeID

• **\_typeID**: _number_ = PlatformVMConstants.IMPORTTX

_Overrides [BaseTx](api_platformvm_basetx.basetx).[\_typeID](api_platformvm_basetx.basetx#protected-_typeid)_

_Defined in [src/apis/platformvm/importtx.ts:29](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/importtx.ts#L29)_

---

### `Protected` \_typeName

• **\_typeName**: _string_ = "ImportTx"

_Overrides [BaseTx](api_platformvm_basetx.basetx).[\_typeName](api_platformvm_basetx.basetx#protected-_typename)_

_Defined in [src/apis/platformvm/importtx.ts:28](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/importtx.ts#L28)_

---

### `Protected` blockchainID

• **blockchainID**: _Buffer_ = Buffer.alloc(32)

_Inherited from [StandardBaseTx](common_transactions.standardbasetx).[blockchainID](common_transactions.standardbasetx#protected-blockchainid)_

_Defined in [src/common/tx.ts:82](https://github.com/chain4travel/caminojs/blob/3883166/src/common/tx.ts#L82)_

---

### `Protected` importIns

• **importIns**: _[TransferableInput](api_platformvm_inputs.transferableinput)[]_ = []

_Defined in [src/apis/platformvm/importtx.ts:64](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/importtx.ts#L64)_

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

### `Protected` numIns

• **numIns**: _Buffer_ = Buffer.alloc(4)

_Defined in [src/apis/platformvm/importtx.ts:63](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/importtx.ts#L63)_

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

### `Protected` sourceChain

• **sourceChain**: _Buffer_ = Buffer.alloc(32)

_Defined in [src/apis/platformvm/importtx.ts:62](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/importtx.ts#L62)_

## Methods

### clone

▸ **clone**(): _this_

_Overrides [ValidatorTx](api_platformvm_validationtx.validatortx).[clone](api_platformvm_validationtx.validatortx#clone)_

_Defined in [src/apis/platformvm/importtx.ts:155](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/importtx.ts#L155)_

**Returns:** _this_

---

### create

▸ **create**(...`args`: any[]): _this_

_Overrides [ValidatorTx](api_platformvm_validationtx.validatortx).[create](api_platformvm_validationtx.validatortx#create)_

_Defined in [src/apis/platformvm/importtx.ts:161](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/importtx.ts#L161)_

**Parameters:**

| Name      | Type  |
| --------- | ----- |
| `...args` | any[] |

**Returns:** _this_

---

### deserialize

▸ **deserialize**(`fields`: object, `encoding`: [SerializedEncoding](../modules/utils_serialization#serializedencoding)): _void_

_Overrides [BaseTx](api_platformvm_basetx.basetx).[deserialize](api_platformvm_basetx.basetx#deserialize)_

_Defined in [src/apis/platformvm/importtx.ts:44](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/importtx.ts#L44)_

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

_Defined in [src/apis/platformvm/importtx.ts:82](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/importtx.ts#L82)_

Takes a [Buffer](https://github.com/feross/buffer) containing an [ImportTx](api_platformvm_importtx.importtx), parses it, populates the class, and returns the length of the [ImportTx](api_platformvm_importtx.importtx) in bytes.

**`remarks`** assume not-checksummed

**Parameters:**

| Name     | Type   | Default | Description                                                                                                |
| -------- | ------ | ------- | ---------------------------------------------------------------------------------------------------------- |
| `bytes`  | Buffer | -       | A [Buffer](https://github.com/feross/buffer) containing a raw [ImportTx](api_platformvm_importtx.importtx) |
| `offset` | number | 0       | -                                                                                                          |

**Returns:** _number_

The length of the raw [ImportTx](api_platformvm_importtx.importtx)

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

### getImportInputs

▸ **getImportInputs**(): _[TransferableInput](api_platformvm_inputs.transferableinput)[]_

_Defined in [src/apis/platformvm/importtx.ts:117](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/importtx.ts#L117)_

Returns an array of [TransferableInput](api_evm_inputs.transferableinput)s in this transaction.

**Returns:** _[TransferableInput](api_platformvm_inputs.transferableinput)[]_

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

### getSourceChain

▸ **getSourceChain**(): _Buffer_

_Defined in [src/apis/platformvm/importtx.ts:124](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/importtx.ts#L124)_

Returns a [Buffer](https://github.com/feross/buffer) for the source chainid.

**Returns:** _Buffer_

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

_Defined in [src/apis/platformvm/importtx.ts:69](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/importtx.ts#L69)_

Returns the id of the [ImportTx](api_platformvm_importtx.importtx)

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

_Defined in [src/apis/platformvm/importtx.ts:31](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/importtx.ts#L31)_

**Parameters:**

| Name       | Type                                                                    | Default |
| ---------- | ----------------------------------------------------------------------- | ------- |
| `encoding` | [SerializedEncoding](../modules/utils_serialization#serializedencoding) | "hex"   |

**Returns:** _object_

---

### sign

▸ **sign**(`msg`: Buffer, `kc`: [KeyChain](api_platformvm_keychain.keychain)): _[Credential](common_signature.credential)[]_

_Overrides [ExportTx](api_platformvm_exporttx.exporttx).[sign](api_platformvm_exporttx.exporttx#sign)_

_Defined in [src/apis/platformvm/importtx.ts:136](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/importtx.ts#L136)_

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

_Defined in [src/apis/platformvm/importtx.ts:100](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/importtx.ts#L100)_

Returns a [Buffer](https://github.com/feross/buffer) representation of the [ImportTx](api_platformvm_importtx.importtx).

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