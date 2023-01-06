# Class: BaseTx

Class representing a base for all transactions.

## Hierarchy

↳ [StandardBaseTx](common_transactions.standardbasetx)‹[KeyPair](api_avm_keychain.keypair), [KeyChain](api_avm_keychain.keychain)›

↳ **BaseTx**

↳ [CreateAssetTx](api_avm_createassettx.createassettx)

↳ [OperationTx](api_avm_operationtx.operationtx)

↳ [ImportTx](api_avm_importtx.importtx)

↳ [ExportTx](api_avm_exporttx.exporttx)

## Index

### Constructors

- [constructor](api_avm_basetx.basetx#constructor)

### Properties

- [\_codecID](api_avm_basetx.basetx#protected-_codecid)
- [\_typeID](api_avm_basetx.basetx#protected-_typeid)
- [\_typeName](api_avm_basetx.basetx#protected-_typename)
- [blockchainID](api_avm_basetx.basetx#protected-blockchainid)
- [ins](api_avm_basetx.basetx#protected-ins)
- [memo](api_avm_basetx.basetx#protected-memo)
- [networkID](api_avm_basetx.basetx#protected-networkid)
- [numins](api_avm_basetx.basetx#protected-numins)
- [numouts](api_avm_basetx.basetx#protected-numouts)
- [outs](api_avm_basetx.basetx#protected-outs)

### Methods

- [clone](api_avm_basetx.basetx#clone)
- [create](api_avm_basetx.basetx#create)
- [deserialize](api_avm_basetx.basetx#deserialize)
- [fromBuffer](api_avm_basetx.basetx#frombuffer)
- [getBlockchainID](api_avm_basetx.basetx#getblockchainid)
- [getCodecID](api_avm_basetx.basetx#getcodecid)
- [getIns](api_avm_basetx.basetx#getins)
- [getMemo](api_avm_basetx.basetx#getmemo)
- [getNetworkID](api_avm_basetx.basetx#getnetworkid)
- [getOuts](api_avm_basetx.basetx#getouts)
- [getTotalOuts](api_avm_basetx.basetx#gettotalouts)
- [getTxType](api_avm_basetx.basetx#gettxtype)
- [getTypeID](api_avm_basetx.basetx#gettypeid)
- [getTypeName](api_avm_basetx.basetx#gettypename)
- [sanitizeObject](api_avm_basetx.basetx#sanitizeobject)
- [select](api_avm_basetx.basetx#select)
- [serialize](api_avm_basetx.basetx#serialize)
- [setCodecID](api_avm_basetx.basetx#setcodecid)
- [sign](api_avm_basetx.basetx#sign)
- [toBuffer](api_avm_basetx.basetx#tobuffer)
- [toString](api_avm_basetx.basetx#tostring)
- [toStringHex](api_avm_basetx.basetx#tostringhex)

## Constructors

### constructor

\+ **new BaseTx**(`networkID`: number, `blockchainID`: Buffer, `outs`: [TransferableOutput](api_avm_outputs.transferableoutput)[], `ins`: [TransferableInput](api_avm_inputs.transferableinput)[], `memo`: Buffer): _[BaseTx](api_avm_basetx.basetx)_

_Overrides [StandardBaseTx](common_transactions.standardbasetx).[constructor](common_transactions.standardbasetx#constructor)_

_Defined in [src/apis/avm/basetx.ts:189](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/basetx.ts#L189)_

Class representing a BaseTx which is the foundation for all transactions.

**Parameters:**

| Name           | Type                                                       | Default              | Description                                                                               |
| -------------- | ---------------------------------------------------------- | -------------------- | ----------------------------------------------------------------------------------------- |
| `networkID`    | number                                                     | DefaultNetworkID     | Optional networkID, [DefaultNetworkID](../modules/utils_constants#const-defaultnetworkid) |
| `blockchainID` | Buffer                                                     | Buffer.alloc(32, 16) | Optional blockchainID, default Buffer.alloc(32, 16)                                       |
| `outs`         | [TransferableOutput](api_avm_outputs.transferableoutput)[] | undefined            | Optional array of the [TransferableOutput](api_evm_outputs.transferableoutput)s           |
| `ins`          | [TransferableInput](api_avm_inputs.transferableinput)[]    | undefined            | Optional array of the [TransferableInput](api_evm_inputs.transferableinput)s              |
| `memo`         | Buffer                                                     | undefined            | Optional [Buffer](https://github.com/feross/buffer) for the memo field                    |

**Returns:** _[BaseTx](api_avm_basetx.basetx)_

## Properties

### `Protected` \_codecID

• **\_codecID**: _number_ = AVMConstants.LATESTCODEC

_Overrides [SigIdx](common_signature.sigidx).[\_codecID](common_signature.sigidx#protected-_codecid)_

_Defined in [src/apis/avm/basetx.ts:37](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/basetx.ts#L37)_

---

### `Protected` \_typeID

• **\_typeID**: _number_ = this.\_codecID === 0 ? AVMConstants.BASETX : AVMConstants.BASETX_CODECONE

_Overrides [StandardBaseTx](common_transactions.standardbasetx).[\_typeID](common_transactions.standardbasetx#protected-_typeid)_

_Defined in [src/apis/avm/basetx.ts:38](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/basetx.ts#L38)_

---

### `Protected` \_typeName

• **\_typeName**: _string_ = "BaseTx"

_Overrides [StandardBaseTx](common_transactions.standardbasetx).[\_typeName](common_transactions.standardbasetx#protected-_typename)_

_Defined in [src/apis/avm/basetx.ts:36](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/basetx.ts#L36)_

---

### `Protected` blockchainID

• **blockchainID**: _Buffer_ = Buffer.alloc(32)

_Inherited from [StandardBaseTx](common_transactions.standardbasetx).[blockchainID](common_transactions.standardbasetx#protected-blockchainid)_

_Defined in [src/common/tx.ts:82](https://github.com/chain4travel/caminojs/blob/3883166/src/common/tx.ts#L82)_

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

_Overrides [StandardBaseTx](common_transactions.standardbasetx).[clone](common_transactions.standardbasetx#abstract-clone)_

_Defined in [src/apis/avm/basetx.ts:176](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/basetx.ts#L176)_

**Returns:** _this_

---

### create

▸ **create**(...`args`: any[]): _this_

_Overrides [StandardBaseTx](common_transactions.standardbasetx).[create](common_transactions.standardbasetx#abstract-create)_

_Defined in [src/apis/avm/basetx.ts:182](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/basetx.ts#L182)_

**Parameters:**

| Name      | Type  |
| --------- | ----- |
| `...args` | any[] |

**Returns:** _this_

---

### deserialize

▸ **deserialize**(`fields`: object, `encoding`: [SerializedEncoding](../modules/utils_serialization#serializedencoding)): _void_

_Overrides [StandardBaseTx](common_transactions.standardbasetx).[deserialize](common_transactions.standardbasetx#deserialize)_

_Defined in [src/apis/avm/basetx.ts:43](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/basetx.ts#L43)_

**Parameters:**

| Name       | Type                                                                    | Default |
| ---------- | ----------------------------------------------------------------------- | ------- |
| `fields`   | object                                                                  | -       |
| `encoding` | [SerializedEncoding](../modules/utils_serialization#serializedencoding) | "hex"   |

**Returns:** _void_

---

### fromBuffer

▸ **fromBuffer**(`bytes`: Buffer, `offset`: number): _number_

_Defined in [src/apis/avm/basetx.ts:116](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/basetx.ts#L116)_

Takes a [Buffer](https://github.com/feross/buffer) containing an [BaseTx](api_avm_basetx.basetx), parses it, populates the class, and returns the length of the BaseTx in bytes.

**`remarks`** assume not-checksummed

**Parameters:**

| Name     | Type   | Default | Description                                                                                   |
| -------- | ------ | ------- | --------------------------------------------------------------------------------------------- |
| `bytes`  | Buffer | -       | A [Buffer](https://github.com/feross/buffer) containing a raw [BaseTx](api_avm_basetx.basetx) |
| `offset` | number | 0       | -                                                                                             |

**Returns:** _number_

The length of the raw [BaseTx](api_avm_basetx.basetx)

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

### getIns

▸ **getIns**(): _[TransferableInput](api_avm_inputs.transferableinput)[]_

_Overrides [StandardBaseTx](common_transactions.standardbasetx).[getIns](common_transactions.standardbasetx#abstract-getins)_

_Defined in [src/apis/avm/basetx.ts:75](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/basetx.ts#L75)_

**Returns:** _[TransferableInput](api_avm_inputs.transferableinput)[]_

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

▸ **getOuts**(): _[TransferableOutput](api_avm_outputs.transferableoutput)[]_

_Overrides [StandardBaseTx](common_transactions.standardbasetx).[getOuts](common_transactions.standardbasetx#abstract-getouts)_

_Defined in [src/apis/avm/basetx.ts:71](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/basetx.ts#L71)_

**Returns:** _[TransferableOutput](api_avm_outputs.transferableoutput)[]_

---

### getTotalOuts

▸ **getTotalOuts**(): _[TransferableOutput](api_avm_outputs.transferableoutput)[]_

_Overrides [StandardBaseTx](common_transactions.standardbasetx).[getTotalOuts](common_transactions.standardbasetx#abstract-gettotalouts)_

_Defined in [src/apis/avm/basetx.ts:79](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/basetx.ts#L79)_

**Returns:** _[TransferableOutput](api_avm_outputs.transferableoutput)[]_

---

### getTxType

▸ **getTxType**(): _number_

_Overrides [StandardBaseTx](common_transactions.standardbasetx).[getTxType](common_transactions.standardbasetx#abstract-gettxtype)_

_Defined in [src/apis/avm/basetx.ts:103](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/basetx.ts#L103)_

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

_Overrides [StandardBaseTx](common_transactions.standardbasetx).[select](common_transactions.standardbasetx#abstract-select)_

_Defined in [src/apis/avm/basetx.ts:186](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/basetx.ts#L186)_

**Parameters:**

| Name      | Type   |
| --------- | ------ |
| `id`      | number |
| `...args` | any[]  |

**Returns:** _this_

---

### serialize

▸ **serialize**(`encoding`: [SerializedEncoding](../modules/utils_serialization#serializedencoding)): _object_

_Inherited from [StandardBaseTx](common_transactions.standardbasetx).[serialize](common_transactions.standardbasetx#serialize)_

_Overrides [Serializable](utils_serialization.serializable).[serialize](utils_serialization.serializable#serialize)_

_Defined in [src/common/tx.ts:40](https://github.com/chain4travel/caminojs/blob/3883166/src/common/tx.ts#L40)_

**Parameters:**

| Name       | Type                                                                    | Default |
| ---------- | ----------------------------------------------------------------------- | ------- |
| `encoding` | [SerializedEncoding](../modules/utils_serialization#serializedencoding) | "hex"   |

**Returns:** _object_

---

### setCodecID

▸ **setCodecID**(`codecID`: number): _void_

_Defined in [src/apis/avm/basetx.ts:88](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/basetx.ts#L88)_

Set the codecID

**Parameters:**

| Name      | Type   | Description        |
| --------- | ------ | ------------------ |
| `codecID` | number | The codecID to set |

**Returns:** _void_

---

### sign

▸ **sign**(`msg`: Buffer, `kc`: [KeyChain](api_avm_keychain.keychain)): _[Credential](common_signature.credential)[]_

_Overrides [StandardBaseTx](common_transactions.standardbasetx).[sign](common_transactions.standardbasetx#abstract-sign)_

_Defined in [src/apis/avm/basetx.ts:157](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/basetx.ts#L157)_

Takes the bytes of an [UnsignedTx](api_evm_transactions.unsignedtx) and returns an array of [Credential](common_signature.credential)s

**Parameters:**

| Name  | Type                                  | Description                                                    |
| ----- | ------------------------------------- | -------------------------------------------------------------- |
| `msg` | Buffer                                | A Buffer for the [UnsignedTx](api_evm_transactions.unsignedtx) |
| `kc`  | [KeyChain](api_avm_keychain.keychain) | An [KeyChain](api_evm_keychain.keychain) used in signing       |

**Returns:** _[Credential](common_signature.credential)[]_

An array of [Credential](common_signature.credential)s

---

### toBuffer

▸ **toBuffer**(): _Buffer_

_Inherited from [StandardBaseTx](common_transactions.standardbasetx).[toBuffer](common_transactions.standardbasetx#tobuffer)_

_Defined in [src/common/tx.ts:133](https://github.com/chain4travel/caminojs/blob/3883166/src/common/tx.ts#L133)_

Returns a [Buffer](https://github.com/feross/buffer) representation of the [StandardBaseTx](common_transactions.standardbasetx).

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
