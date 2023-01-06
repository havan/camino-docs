# Class: ImportTx

Class representing an unsigned Import transaction.

## Hierarchy

↳ [EVMBaseTx](api_evm_basetx.evmbasetx)

↳ **ImportTx**

## Index

### Constructors

- [constructor](api_evm_importtx.importtx#constructor)

### Properties

- [\_codecID](api_evm_importtx.importtx#protected-_codecid)
- [\_typeID](api_evm_importtx.importtx#protected-_typeid)
- [\_typeName](api_evm_importtx.importtx#protected-_typename)
- [blockchainID](api_evm_importtx.importtx#protected-blockchainid)
- [importIns](api_evm_importtx.importtx#protected-importins)
- [networkID](api_evm_importtx.importtx#protected-networkid)
- [numIns](api_evm_importtx.importtx#protected-numins)
- [numOuts](api_evm_importtx.importtx#protected-numouts)
- [outs](api_evm_importtx.importtx#protected-outs)
- [sourceChain](api_evm_importtx.importtx#protected-sourcechain)

### Methods

- [clone](api_evm_importtx.importtx#clone)
- [create](api_evm_importtx.importtx#create)
- [deserialize](api_evm_importtx.importtx#deserialize)
- [fromBuffer](api_evm_importtx.importtx#frombuffer)
- [getBlockchainID](api_evm_importtx.importtx#getblockchainid)
- [getCodecID](api_evm_importtx.importtx#getcodecid)
- [getImportInputs](api_evm_importtx.importtx#getimportinputs)
- [getNetworkID](api_evm_importtx.importtx#getnetworkid)
- [getOuts](api_evm_importtx.importtx#getouts)
- [getSourceChain](api_evm_importtx.importtx#getsourcechain)
- [getTxType](api_evm_importtx.importtx#gettxtype)
- [getTypeID](api_evm_importtx.importtx#gettypeid)
- [getTypeName](api_evm_importtx.importtx#gettypename)
- [sanitizeObject](api_evm_importtx.importtx#sanitizeobject)
- [select](api_evm_importtx.importtx#select)
- [serialize](api_evm_importtx.importtx#serialize)
- [sign](api_evm_importtx.importtx#sign)
- [toBuffer](api_evm_importtx.importtx#tobuffer)
- [toString](api_evm_importtx.importtx#tostring)
- [validateOuts](api_evm_importtx.importtx#private-validateouts)

## Constructors

### constructor

\+ **new ImportTx**(`networkID`: number, `blockchainID`: Buffer, `sourceChainID`: Buffer, `importIns`: [TransferableInput](api_evm_inputs.transferableinput)[], `outs`: [EVMOutput](api_evm_outputs.evmoutput)[], `fee`: BN): _[ImportTx](api_evm_importtx.importtx)_

_Overrides [EVMBaseTx](api_evm_basetx.evmbasetx).[constructor](api_evm_basetx.evmbasetx#constructor)_

_Defined in [src/apis/evm/importtx.ts:202](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/importtx.ts#L202)_

Class representing an unsigned Import transaction.

**Parameters:**

| Name            | Type                                                    | Default              | Description                                                                                      |
| --------------- | ------------------------------------------------------- | -------------------- | ------------------------------------------------------------------------------------------------ |
| `networkID`     | number                                                  | DefaultNetworkID     | Optional networkID, [DefaultNetworkID](../modules/utils_constants#const-defaultnetworkid)        |
| `blockchainID`  | Buffer                                                  | Buffer.alloc(32, 16) | Optional blockchainID, default Buffer.alloc(32, 16)                                              |
| `sourceChainID` | Buffer                                                  | Buffer.alloc(32, 16) | Optional chainID for the source inputs to import. Default Buffer.alloc(32, 16)                   |
| `importIns`     | [TransferableInput](api_evm_inputs.transferableinput)[] | undefined            | Optional array of [TransferableInput](api_evm_inputs.transferableinput)s used in the transaction |
| `outs`          | [EVMOutput](api_evm_outputs.evmoutput)[]                | undefined            | Optional array of the [EVMOutput](api_evm_outputs.evmoutput)s                                    |
| `fee`           | BN                                                      | new BN(0)            | Optional the fee as a BN                                                                         |

**Returns:** _[ImportTx](api_evm_importtx.importtx)_

## Properties

### `Protected` \_codecID

• **\_codecID**: _number_ = undefined

_Inherited from [SigIdx](common_signature.sigidx).[\_codecID](common_signature.sigidx#protected-_codecid)_

_Defined in [src/utils/serialization.ts:51](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/serialization.ts#L51)_

---

### `Protected` \_typeID

• **\_typeID**: _number_ = EVMConstants.IMPORTTX

_Overrides [EVMBaseTx](api_evm_basetx.evmbasetx).[\_typeID](api_evm_basetx.evmbasetx#protected-_typeid)_

_Defined in [src/apis/evm/importtx.ts:38](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/importtx.ts#L38)_

---

### `Protected` \_typeName

• **\_typeName**: _string_ = "ImportTx"

_Overrides [EVMBaseTx](api_evm_basetx.evmbasetx).[\_typeName](api_evm_basetx.evmbasetx#protected-_typename)_

_Defined in [src/apis/evm/importtx.ts:37](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/importtx.ts#L37)_

---

### `Protected` blockchainID

• **blockchainID**: _Buffer_ = Buffer.alloc(32)

_Inherited from [EVMStandardBaseTx](common_transactions.evmstandardbasetx).[blockchainID](common_transactions.evmstandardbasetx#protected-blockchainid)_

_Defined in [src/common/evmtx.ts:74](https://github.com/chain4travel/caminojs/blob/3883166/src/common/evmtx.ts#L74)_

---

### `Protected` importIns

• **importIns**: _[TransferableInput](api_evm_inputs.transferableinput)[]_ = []

_Defined in [src/apis/evm/importtx.ts:73](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/importtx.ts#L73)_

---

### `Protected` networkID

• **networkID**: _Buffer_ = Buffer.alloc(4)

_Inherited from [EVMStandardBaseTx](common_transactions.evmstandardbasetx).[networkID](common_transactions.evmstandardbasetx#protected-networkid)_

_Defined in [src/common/evmtx.ts:73](https://github.com/chain4travel/caminojs/blob/3883166/src/common/evmtx.ts#L73)_

---

### `Protected` numIns

• **numIns**: _Buffer_ = Buffer.alloc(4)

_Defined in [src/apis/evm/importtx.ts:72](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/importtx.ts#L72)_

---

### `Protected` numOuts

• **numOuts**: _Buffer_ = Buffer.alloc(4)

_Defined in [src/apis/evm/importtx.ts:74](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/importtx.ts#L74)_

---

### `Protected` outs

• **outs**: _[EVMOutput](api_evm_outputs.evmoutput)[]_ = []

_Defined in [src/apis/evm/importtx.ts:75](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/importtx.ts#L75)_

---

### `Protected` sourceChain

• **sourceChain**: _Buffer_ = Buffer.alloc(32)

_Defined in [src/apis/evm/importtx.ts:71](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/importtx.ts#L71)_

## Methods

### clone

▸ **clone**(): _this_

_Overrides [EVMBaseTx](api_evm_basetx.evmbasetx).[clone](api_evm_basetx.evmbasetx#clone)_

_Defined in [src/apis/evm/importtx.ts:167](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/importtx.ts#L167)_

**Returns:** _this_

---

### create

▸ **create**(...`args`: any[]): _this_

_Overrides [EVMBaseTx](api_evm_basetx.evmbasetx).[create](api_evm_basetx.evmbasetx#create)_

_Defined in [src/apis/evm/importtx.ts:173](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/importtx.ts#L173)_

**Parameters:**

| Name      | Type  |
| --------- | ----- |
| `...args` | any[] |

**Returns:** _this_

---

### deserialize

▸ **deserialize**(`fields`: object, `encoding`: [SerializedEncoding](../modules/utils_serialization#serializedencoding)): _void_

_Overrides [EVMBaseTx](api_evm_basetx.evmbasetx).[deserialize](api_evm_basetx.evmbasetx#deserialize)_

_Defined in [src/apis/evm/importtx.ts:53](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/importtx.ts#L53)_

**Parameters:**

| Name       | Type                                                                    | Default |
| ---------- | ----------------------------------------------------------------------- | ------- |
| `fields`   | object                                                                  | -       |
| `encoding` | [SerializedEncoding](../modules/utils_serialization#serializedencoding) | "hex"   |

**Returns:** _void_

---

### fromBuffer

▸ **fromBuffer**(`bytes`: Buffer, `offset`: number): _number_

_Overrides [EVMBaseTx](api_evm_basetx.evmbasetx).[fromBuffer](api_evm_basetx.evmbasetx#frombuffer)_

_Defined in [src/apis/evm/importtx.ts:102](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/importtx.ts#L102)_

Takes a [Buffer](https://github.com/feross/buffer) containing an [ImportTx](api_evm_importtx.importtx), parses it,
populates the class, and returns the length of the [ImportTx](api_evm_importtx.importtx) in bytes.

**`remarks`** assume not-checksummed

**Parameters:**

| Name     | Type   | Default | Description                                                                                         |
| -------- | ------ | ------- | --------------------------------------------------------------------------------------------------- |
| `bytes`  | Buffer | -       | A [Buffer](https://github.com/feross/buffer) containing a raw [ImportTx](api_evm_importtx.importtx) |
| `offset` | number | 0       | A number representing the byte offset. Defaults to 0.                                               |

**Returns:** _number_

The length of the raw [ImportTx](api_evm_importtx.importtx)

---

### getBlockchainID

▸ **getBlockchainID**(): _Buffer_

_Inherited from [EVMStandardBaseTx](common_transactions.evmstandardbasetx).[getBlockchainID](common_transactions.evmstandardbasetx#getblockchainid)_

_Defined in [src/common/evmtx.ts:91](https://github.com/chain4travel/caminojs/blob/3883166/src/common/evmtx.ts#L91)_

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

▸ **getImportInputs**(): _[TransferableInput](api_evm_inputs.transferableinput)[]_

_Defined in [src/apis/evm/importtx.ts:156](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/importtx.ts#L156)_

Returns an array of [TransferableInput](api_evm_inputs.transferableinput)s in this transaction.

**Returns:** _[TransferableInput](api_evm_inputs.transferableinput)[]_

---

### getNetworkID

▸ **getNetworkID**(): _number_

_Inherited from [EVMStandardBaseTx](common_transactions.evmstandardbasetx).[getNetworkID](common_transactions.evmstandardbasetx#getnetworkid)_

_Defined in [src/common/evmtx.ts:84](https://github.com/chain4travel/caminojs/blob/3883166/src/common/evmtx.ts#L84)_

Returns the NetworkID as a number

**Returns:** _number_

---

### getOuts

▸ **getOuts**(): _[EVMOutput](api_evm_outputs.evmoutput)[]_

_Defined in [src/apis/evm/importtx.ts:163](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/importtx.ts#L163)_

Returns an array of [EVMOutput](api_evm_outputs.evmoutput)s in this transaction.

**Returns:** _[EVMOutput](api_evm_outputs.evmoutput)[]_

---

### getSourceChain

▸ **getSourceChain**(): _Buffer_

_Defined in [src/apis/evm/importtx.ts:87](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/importtx.ts#L87)_

Returns a [Buffer](https://github.com/feross/buffer) for the source chainid.

**Returns:** _Buffer_

---

### getTxType

▸ **getTxType**(): _number_

_Overrides [EVMBaseTx](api_evm_basetx.evmbasetx).[getTxType](api_evm_basetx.evmbasetx#gettxtype)_

_Defined in [src/apis/evm/importtx.ts:80](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/importtx.ts#L80)_

Returns the id of the [ImportTx](api_evm_importtx.importtx)

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

_Inherited from [EVMBaseTx](api_evm_basetx.evmbasetx).[select](api_evm_basetx.evmbasetx#select)_

_Overrides [EVMStandardBaseTx](common_transactions.evmstandardbasetx).[select](common_transactions.evmstandardbasetx#abstract-select)_

_Defined in [src/apis/evm/basetx.ts:80](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/basetx.ts#L80)_

**Parameters:**

| Name      | Type   |
| --------- | ------ |
| `id`      | number |
| `...args` | any[]  |

**Returns:** _this_

---

### serialize

▸ **serialize**(`encoding`: [SerializedEncoding](../modules/utils_serialization#serializedencoding)): _object_

_Overrides [EVMStandardBaseTx](common_transactions.evmstandardbasetx).[serialize](common_transactions.evmstandardbasetx#serialize)_

_Defined in [src/apis/evm/importtx.ts:40](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/importtx.ts#L40)_

**Parameters:**

| Name       | Type                                                                    | Default |
| ---------- | ----------------------------------------------------------------------- | ------- |
| `encoding` | [SerializedEncoding](../modules/utils_serialization#serializedencoding) | "hex"   |

**Returns:** _object_

---

### sign

▸ **sign**(`msg`: Buffer, `kc`: [KeyChain](api_evm_keychain.keychain)): _[Credential](common_signature.credential)[]_

_Overrides [EVMBaseTx](api_evm_basetx.evmbasetx).[sign](api_evm_basetx.evmbasetx#sign)_

_Defined in [src/apis/evm/importtx.ts:185](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/importtx.ts#L185)_

Takes the bytes of an [UnsignedTx](api_evm_transactions.unsignedtx) and returns an array of [Credential](common_signature.credential)s

**Parameters:**

| Name  | Type                                  | Description                                                    |
| ----- | ------------------------------------- | -------------------------------------------------------------- |
| `msg` | Buffer                                | A Buffer for the [UnsignedTx](api_evm_transactions.unsignedtx) |
| `kc`  | [KeyChain](api_evm_keychain.keychain) | An [KeyChain](api_evm_keychain.keychain) used in signing       |

**Returns:** _[Credential](common_signature.credential)[]_

An array of [Credential](common_signature.credential)s

---

### toBuffer

▸ **toBuffer**(): _Buffer_

_Overrides [EVMStandardBaseTx](common_transactions.evmstandardbasetx).[toBuffer](common_transactions.evmstandardbasetx#tobuffer)_

_Defined in [src/apis/evm/importtx.ts:128](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/importtx.ts#L128)_

Returns a [Buffer](https://github.com/feross/buffer) representation of the [ImportTx](api_evm_importtx.importtx).

**Returns:** _Buffer_

---

### toString

▸ **toString**(): _string_

_Inherited from [EVMStandardBaseTx](common_transactions.evmstandardbasetx).[toString](common_transactions.evmstandardbasetx#tostring)_

_Defined in [src/common/evmtx.ts:108](https://github.com/chain4travel/caminojs/blob/3883166/src/common/evmtx.ts#L108)_

Returns a base-58 representation of the [StandardBaseTx](common_transactions.standardbasetx).

**Returns:** _string_

---

### `Private` validateOuts

▸ **validateOuts**(`fee`: BN): _void_

_Defined in [src/apis/evm/importtx.ts:260](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/importtx.ts#L260)_

**Parameters:**

| Name  | Type |
| ----- | ---- |
| `fee` | BN   |

**Returns:** _void_
