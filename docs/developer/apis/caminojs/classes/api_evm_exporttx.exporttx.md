# Class: ExportTx

## Hierarchy

↳ [EVMBaseTx](api_evm_basetx.evmbasetx)

↳ **ExportTx**

## Index

### Constructors

- [constructor](api_evm_exporttx.exporttx#constructor)

### Properties

- [\_codecID](api_evm_exporttx.exporttx#protected-_codecid)
- [\_typeID](api_evm_exporttx.exporttx#protected-_typeid)
- [\_typeName](api_evm_exporttx.exporttx#protected-_typename)
- [blockchainID](api_evm_exporttx.exporttx#protected-blockchainid)
- [destinationChain](api_evm_exporttx.exporttx#protected-destinationchain)
- [exportedOutputs](api_evm_exporttx.exporttx#protected-exportedoutputs)
- [inputs](api_evm_exporttx.exporttx#protected-inputs)
- [networkID](api_evm_exporttx.exporttx#protected-networkid)
- [numExportedOutputs](api_evm_exporttx.exporttx#protected-numexportedoutputs)
- [numInputs](api_evm_exporttx.exporttx#protected-numinputs)

### Methods

- [clone](api_evm_exporttx.exporttx#clone)
- [create](api_evm_exporttx.exporttx#create)
- [deserialize](api_evm_exporttx.exporttx#deserialize)
- [fromBuffer](api_evm_exporttx.exporttx#frombuffer)
- [getBlockchainID](api_evm_exporttx.exporttx#getblockchainid)
- [getCodecID](api_evm_exporttx.exporttx#getcodecid)
- [getDestinationChain](api_evm_exporttx.exporttx#getdestinationchain)
- [getExportedOutputs](api_evm_exporttx.exporttx#getexportedoutputs)
- [getInputs](api_evm_exporttx.exporttx#getinputs)
- [getNetworkID](api_evm_exporttx.exporttx#getnetworkid)
- [getTxType](api_evm_exporttx.exporttx#gettxtype)
- [getTypeID](api_evm_exporttx.exporttx#gettypeid)
- [getTypeName](api_evm_exporttx.exporttx#gettypename)
- [sanitizeObject](api_evm_exporttx.exporttx#sanitizeobject)
- [select](api_evm_exporttx.exporttx#select)
- [serialize](api_evm_exporttx.exporttx#serialize)
- [sign](api_evm_exporttx.exporttx#sign)
- [toBuffer](api_evm_exporttx.exporttx#tobuffer)
- [toString](api_evm_exporttx.exporttx#tostring)

## Constructors

### constructor

\+ **new ExportTx**(`networkID`: number, `blockchainID`: Buffer, `destinationChain`: Buffer, `inputs`: [EVMInput](api_evm_inputs.evminput)[], `exportedOutputs`: [TransferableOutput](api_evm_outputs.transferableoutput)[]): _[ExportTx](api_evm_exporttx.exporttx)_

_Overrides [EVMBaseTx](api_evm_basetx.evmbasetx).[constructor](api_evm_basetx.evmbasetx#constructor)_

_Defined in [src/apis/evm/exporttx.ts:179](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/exporttx.ts#L179)_

Class representing a ExportTx.

**Parameters:**

| Name               | Type                                                       | Default              | Description                                             |
| ------------------ | ---------------------------------------------------------- | -------------------- | ------------------------------------------------------- |
| `networkID`        | number                                                     | undefined            | Optional networkID                                      |
| `blockchainID`     | Buffer                                                     | Buffer.alloc(32, 16) | Optional blockchainID, default Buffer.alloc(32, 16)     |
| `destinationChain` | Buffer                                                     | Buffer.alloc(32, 16) | Optional destinationChain, default Buffer.alloc(32, 16) |
| `inputs`           | [EVMInput](api_evm_inputs.evminput)[]                      | undefined            | Optional array of the [[EVMInputs]]s                    |
| `exportedOutputs`  | [TransferableOutput](api_evm_outputs.transferableoutput)[] | undefined            | Optional array of the [[EVMOutputs]]s                   |

**Returns:** _[ExportTx](api_evm_exporttx.exporttx)_

## Properties

### `Protected` \_codecID

• **\_codecID**: _number_ = undefined

_Inherited from [SigIdx](common_signature.sigidx).[\_codecID](common_signature.sigidx#protected-_codecid)_

_Defined in [src/utils/serialization.ts:51](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/serialization.ts#L51)_

---

### `Protected` \_typeID

• **\_typeID**: _number_ = EVMConstants.EXPORTTX

_Overrides [EVMBaseTx](api_evm_basetx.evmbasetx).[\_typeID](api_evm_basetx.evmbasetx#protected-_typeid)_

_Defined in [src/apis/evm/exporttx.ts:30](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/exporttx.ts#L30)_

---

### `Protected` \_typeName

• **\_typeName**: _string_ = "ExportTx"

_Overrides [EVMBaseTx](api_evm_basetx.evmbasetx).[\_typeName](api_evm_basetx.evmbasetx#protected-_typename)_

_Defined in [src/apis/evm/exporttx.ts:29](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/exporttx.ts#L29)_

---

### `Protected` blockchainID

• **blockchainID**: _Buffer_ = Buffer.alloc(32)

_Inherited from [EVMStandardBaseTx](common_transactions.evmstandardbasetx).[blockchainID](common_transactions.evmstandardbasetx#protected-blockchainid)_

_Defined in [src/common/evmtx.ts:74](https://github.com/chain4travel/caminojs/blob/3883166/src/common/evmtx.ts#L74)_

---

### `Protected` destinationChain

• **destinationChain**: _Buffer_ = Buffer.alloc(32)

_Defined in [src/apis/evm/exporttx.ts:63](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/exporttx.ts#L63)_

---

### `Protected` exportedOutputs

• **exportedOutputs**: _[TransferableOutput](api_evm_outputs.transferableoutput)[]_ = []

_Defined in [src/apis/evm/exporttx.ts:67](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/exporttx.ts#L67)_

---

### `Protected` inputs

• **inputs**: _[EVMInput](api_evm_inputs.evminput)[]_ = []

_Defined in [src/apis/evm/exporttx.ts:65](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/exporttx.ts#L65)_

---

### `Protected` networkID

• **networkID**: _Buffer_ = Buffer.alloc(4)

_Inherited from [EVMStandardBaseTx](common_transactions.evmstandardbasetx).[networkID](common_transactions.evmstandardbasetx#protected-networkid)_

_Defined in [src/common/evmtx.ts:73](https://github.com/chain4travel/caminojs/blob/3883166/src/common/evmtx.ts#L73)_

---

### `Protected` numExportedOutputs

• **numExportedOutputs**: _Buffer_ = Buffer.alloc(4)

_Defined in [src/apis/evm/exporttx.ts:66](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/exporttx.ts#L66)_

---

### `Protected` numInputs

• **numInputs**: _Buffer_ = Buffer.alloc(4)

_Defined in [src/apis/evm/exporttx.ts:64](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/exporttx.ts#L64)_

## Methods

### clone

▸ **clone**(): _this_

_Inherited from [EVMBaseTx](api_evm_basetx.evmbasetx).[clone](api_evm_basetx.evmbasetx#clone)_

_Overrides [EVMStandardBaseTx](common_transactions.evmstandardbasetx).[clone](common_transactions.evmstandardbasetx#abstract-clone)_

_Defined in [src/apis/evm/basetx.ts:70](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/basetx.ts#L70)_

**Returns:** _this_

---

### create

▸ **create**(...`args`: any[]): _this_

_Inherited from [EVMBaseTx](api_evm_basetx.evmbasetx).[create](api_evm_basetx.evmbasetx#create)_

_Overrides [EVMStandardBaseTx](common_transactions.evmstandardbasetx).[create](common_transactions.evmstandardbasetx#abstract-create)_

_Defined in [src/apis/evm/basetx.ts:76](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/basetx.ts#L76)_

**Parameters:**

| Name      | Type  |
| --------- | ----- |
| `...args` | any[] |

**Returns:** _this_

---

### deserialize

▸ **deserialize**(`fields`: object, `encoding`: [SerializedEncoding](../modules/utils_serialization#serializedencoding)): _void_

_Overrides [EVMBaseTx](api_evm_basetx.evmbasetx).[deserialize](api_evm_basetx.evmbasetx#deserialize)_

_Defined in [src/apis/evm/exporttx.ts:45](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/exporttx.ts#L45)_

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

_Defined in [src/apis/evm/exporttx.ts:126](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/exporttx.ts#L126)_

Decodes the [ExportTx](api_evm_exporttx.exporttx) as a [Buffer](https://github.com/feross/buffer) and returns the size.

**Parameters:**

| Name     | Type   | Default |
| -------- | ------ | ------- |
| `bytes`  | Buffer | -       |
| `offset` | number | 0       |

**Returns:** _number_

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

### getDestinationChain

▸ **getDestinationChain**(): _Buffer_

_Defined in [src/apis/evm/exporttx.ts:72](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/exporttx.ts#L72)_

Returns the destinationChain as a [Buffer](https://github.com/feross/buffer)

**Returns:** _Buffer_

---

### getExportedOutputs

▸ **getExportedOutputs**(): _[TransferableOutput](api_evm_outputs.transferableoutput)[]_

_Defined in [src/apis/evm/exporttx.ts:86](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/exporttx.ts#L86)_

Returns the outs as an array of [[EVMOutputs]]

**Returns:** _[TransferableOutput](api_evm_outputs.transferableoutput)[]_

---

### getInputs

▸ **getInputs**(): _[EVMInput](api_evm_inputs.evminput)[]_

_Defined in [src/apis/evm/exporttx.ts:79](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/exporttx.ts#L79)_

Returns the inputs as an array of [[EVMInputs]]

**Returns:** _[EVMInput](api_evm_inputs.evminput)[]_

---

### getNetworkID

▸ **getNetworkID**(): _number_

_Inherited from [EVMStandardBaseTx](common_transactions.evmstandardbasetx).[getNetworkID](common_transactions.evmstandardbasetx#getnetworkid)_

_Defined in [src/common/evmtx.ts:84](https://github.com/chain4travel/caminojs/blob/3883166/src/common/evmtx.ts#L84)_

Returns the NetworkID as a number

**Returns:** _number_

---

### getTxType

▸ **getTxType**(): _number_

_Inherited from [EVMBaseTx](api_evm_basetx.evmbasetx).[getTxType](api_evm_basetx.evmbasetx#gettxtype)_

_Overrides [EVMStandardBaseTx](common_transactions.evmstandardbasetx).[getTxType](common_transactions.evmstandardbasetx#abstract-gettxtype)_

_Defined in [src/apis/evm/basetx.ts:36](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/basetx.ts#L36)_

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

_Defined in [src/apis/evm/exporttx.ts:32](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/exporttx.ts#L32)_

**Parameters:**

| Name       | Type                                                                    | Default |
| ---------- | ----------------------------------------------------------------------- | ------- |
| `encoding` | [SerializedEncoding](../modules/utils_serialization#serializedencoding) | "hex"   |

**Returns:** _object_

---

### sign

▸ **sign**(`msg`: Buffer, `kc`: [KeyChain](api_evm_keychain.keychain)): _[Credential](common_signature.credential)[]_

_Overrides [EVMBaseTx](api_evm_basetx.evmbasetx).[sign](api_evm_basetx.evmbasetx#sign)_

_Defined in [src/apis/evm/exporttx.ts:164](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/exporttx.ts#L164)_

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

_Defined in [src/apis/evm/exporttx.ts:93](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/exporttx.ts#L93)_

Returns a [Buffer](https://github.com/feross/buffer) representation of the [ExportTx](api_evm_exporttx.exporttx).

**Returns:** _Buffer_

---

### toString

▸ **toString**(): _string_

_Overrides [EVMStandardBaseTx](common_transactions.evmstandardbasetx).[toString](common_transactions.evmstandardbasetx#tostring)_

_Defined in [src/apis/evm/exporttx.ts:152](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/exporttx.ts#L152)_

Returns a base-58 representation of the [ExportTx](api_evm_exporttx.exporttx).

**Returns:** _string_
