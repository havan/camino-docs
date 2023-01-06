# Class: CreateChainTx

Class representing an unsigned CreateChainTx transaction.

## Hierarchy

↳ [BaseTx](api_platformvm_basetx.basetx)

↳ **CreateChainTx**

## Index

### Constructors

- [constructor](api_platformvm_createchaintx.createchaintx#constructor)

### Properties

- [\_codecID](api_platformvm_createchaintx.createchaintx#protected-_codecid)
- [\_typeID](api_platformvm_createchaintx.createchaintx#protected-_typeid)
- [\_typeName](api_platformvm_createchaintx.createchaintx#protected-_typename)
- [blockchainID](api_platformvm_createchaintx.createchaintx#protected-blockchainid)
- [chainName](api_platformvm_createchaintx.createchaintx#protected-chainname)
- [fxIDs](api_platformvm_createchaintx.createchaintx#protected-fxids)
- [genesisData](api_platformvm_createchaintx.createchaintx#protected-genesisdata)
- [ins](api_platformvm_createchaintx.createchaintx#protected-ins)
- [memo](api_platformvm_createchaintx.createchaintx#protected-memo)
- [networkID](api_platformvm_createchaintx.createchaintx#protected-networkid)
- [numFXIDs](api_platformvm_createchaintx.createchaintx#protected-numfxids)
- [numins](api_platformvm_createchaintx.createchaintx#protected-numins)
- [numouts](api_platformvm_createchaintx.createchaintx#protected-numouts)
- [outs](api_platformvm_createchaintx.createchaintx#protected-outs)
- [sigCount](api_platformvm_createchaintx.createchaintx#protected-sigcount)
- [sigIdxs](api_platformvm_createchaintx.createchaintx#protected-sigidxs)
- [subnetAuth](api_platformvm_createchaintx.createchaintx#protected-subnetauth)
- [subnetID](api_platformvm_createchaintx.createchaintx#protected-subnetid)
- [vmID](api_platformvm_createchaintx.createchaintx#protected-vmid)

### Methods

- [addSignatureIdx](api_platformvm_createchaintx.createchaintx#addsignatureidx)
- [clone](api_platformvm_createchaintx.createchaintx#clone)
- [create](api_platformvm_createchaintx.createchaintx#create)
- [deserialize](api_platformvm_createchaintx.createchaintx#deserialize)
- [fromBuffer](api_platformvm_createchaintx.createchaintx#frombuffer)
- [getBlockchainID](api_platformvm_createchaintx.createchaintx#getblockchainid)
- [getChainName](api_platformvm_createchaintx.createchaintx#getchainname)
- [getCodecID](api_platformvm_createchaintx.createchaintx#getcodecid)
- [getCredentialID](api_platformvm_createchaintx.createchaintx#getcredentialid)
- [getFXIDs](api_platformvm_createchaintx.createchaintx#getfxids)
- [getGenesisData](api_platformvm_createchaintx.createchaintx#getgenesisdata)
- [getIns](api_platformvm_createchaintx.createchaintx#getins)
- [getMemo](api_platformvm_createchaintx.createchaintx#getmemo)
- [getNetworkID](api_platformvm_createchaintx.createchaintx#getnetworkid)
- [getOuts](api_platformvm_createchaintx.createchaintx#getouts)
- [getSigIdxs](api_platformvm_createchaintx.createchaintx#getsigidxs)
- [getSubnetAuth](api_platformvm_createchaintx.createchaintx#getsubnetauth)
- [getSubnetID](api_platformvm_createchaintx.createchaintx#getsubnetid)
- [getTotalOuts](api_platformvm_createchaintx.createchaintx#gettotalouts)
- [getTxType](api_platformvm_createchaintx.createchaintx#gettxtype)
- [getTypeID](api_platformvm_createchaintx.createchaintx#gettypeid)
- [getTypeName](api_platformvm_createchaintx.createchaintx#gettypename)
- [getVMID](api_platformvm_createchaintx.createchaintx#getvmid)
- [sanitizeObject](api_platformvm_createchaintx.createchaintx#sanitizeobject)
- [select](api_platformvm_createchaintx.createchaintx#select)
- [serialize](api_platformvm_createchaintx.createchaintx#serialize)
- [sign](api_platformvm_createchaintx.createchaintx#sign)
- [toBuffer](api_platformvm_createchaintx.createchaintx#tobuffer)
- [toString](api_platformvm_createchaintx.createchaintx#tostring)
- [toStringHex](api_platformvm_createchaintx.createchaintx#tostringhex)

## Constructors

### constructor

\+ **new CreateChainTx**(`networkID`: number, `blockchainID`: Buffer, `outs`: [TransferableOutput](api_platformvm_outputs.transferableoutput)[], `ins`: [TransferableInput](api_platformvm_inputs.transferableinput)[], `memo`: Buffer, `subnetID`: string | Buffer, `chainName`: string, `vmID`: string, `fxIDs`: string[], `genesisData`: string | [GenesisData](api_avm_genesisdata.genesisdata)): _[CreateChainTx](api_platformvm_createchaintx.createchaintx)_

_Overrides [BaseTx](api_platformvm_basetx.basetx).[constructor](api_platformvm_basetx.basetx#constructor)_

_Defined in [src/apis/platformvm/createchaintx.ts:279](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/createchaintx.ts#L279)_

Class representing an unsigned CreateChain transaction.

**Parameters:**

| Name           | Type                                                              | Default              | Description                                                                               |
| -------------- | ----------------------------------------------------------------- | -------------------- | ----------------------------------------------------------------------------------------- |
| `networkID`    | number                                                            | DefaultNetworkID     | Optional networkID, [DefaultNetworkID](../modules/utils_constants#const-defaultnetworkid) |
| `blockchainID` | Buffer                                                            | Buffer.alloc(32, 16) | Optional blockchainID, default Buffer.alloc(32, 16)                                       |
| `outs`         | [TransferableOutput](api_platformvm_outputs.transferableoutput)[] | undefined            | Optional array of the [TransferableOutput](api_evm_outputs.transferableoutput)s           |
| `ins`          | [TransferableInput](api_platformvm_inputs.transferableinput)[]    | undefined            | Optional array of the [TransferableInput](api_evm_inputs.transferableinput)s              |
| `memo`         | Buffer                                                            | undefined            | Optional [Buffer](https://github.com/feross/buffer) for the memo field                    |
| `subnetID`     | string &#124; Buffer                                              | undefined            | Optional ID of the Subnet that validates this blockchain.                                 |
| `chainName`    | string                                                            | undefined            | Optional A human readable name for the chain; need not be unique                          |
| `vmID`         | string                                                            | undefined            | Optional ID of the VM running on the new chain                                            |
| `fxIDs`        | string[]                                                          | undefined            | Optional IDs of the feature extensions running on the new chain                           |
| `genesisData`  | string &#124; [GenesisData](api_avm_genesisdata.genesisdata)      | undefined            | Optional Byte representation of genesis state of the new chain                            |

**Returns:** _[CreateChainTx](api_platformvm_createchaintx.createchaintx)_

## Properties

### `Protected` \_codecID

• **\_codecID**: _number_ = undefined

_Inherited from [SigIdx](common_signature.sigidx).[\_codecID](common_signature.sigidx#protected-_codecid)_

_Defined in [src/utils/serialization.ts:51](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/serialization.ts#L51)_

---

### `Protected` \_typeID

• **\_typeID**: _number_ = PlatformVMConstants.CREATECHAINTX

_Overrides [BaseTx](api_platformvm_basetx.basetx).[\_typeID](api_platformvm_basetx.basetx#protected-_typeid)_

_Defined in [src/apis/platformvm/createchaintx.ts:29](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/createchaintx.ts#L29)_

---

### `Protected` \_typeName

• **\_typeName**: _string_ = "CreateChainTx"

_Overrides [BaseTx](api_platformvm_basetx.basetx).[\_typeName](api_platformvm_basetx.basetx#protected-_typename)_

_Defined in [src/apis/platformvm/createchaintx.ts:28](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/createchaintx.ts#L28)_

---

### `Protected` blockchainID

• **blockchainID**: _Buffer_ = Buffer.alloc(32)

_Inherited from [StandardBaseTx](common_transactions.standardbasetx).[blockchainID](common_transactions.standardbasetx#protected-blockchainid)_

_Defined in [src/common/tx.ts:82](https://github.com/chain4travel/caminojs/blob/3883166/src/common/tx.ts#L82)_

---

### `Protected` chainName

• **chainName**: _string_ = ""

_Defined in [src/apis/platformvm/createchaintx.ts:56](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/createchaintx.ts#L56)_

---

### `Protected` fxIDs

• **fxIDs**: _Buffer[]_ = []

_Defined in [src/apis/platformvm/createchaintx.ts:59](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/createchaintx.ts#L59)_

---

### `Protected` genesisData

• **genesisData**: _Buffer_ = Buffer.alloc(32)

_Defined in [src/apis/platformvm/createchaintx.ts:60](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/createchaintx.ts#L60)_

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

### `Protected` numFXIDs

• **numFXIDs**: _Buffer_ = Buffer.alloc(4)

_Defined in [src/apis/platformvm/createchaintx.ts:58](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/createchaintx.ts#L58)_

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

_Defined in [src/apis/platformvm/createchaintx.ts:62](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/createchaintx.ts#L62)_

---

### `Protected` sigIdxs

• **sigIdxs**: _[SigIdx](common_signature.sigidx)[]_ = []

_Defined in [src/apis/platformvm/createchaintx.ts:63](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/createchaintx.ts#L63)_

---

### `Protected` subnetAuth

• **subnetAuth**: _[SubnetAuth](api_platformvm_subnetauth.subnetauth)_

_Defined in [src/apis/platformvm/createchaintx.ts:61](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/createchaintx.ts#L61)_

---

### `Protected` subnetID

• **subnetID**: _Buffer_ = Buffer.alloc(32)

_Defined in [src/apis/platformvm/createchaintx.ts:55](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/createchaintx.ts#L55)_

---

### `Protected` vmID

• **vmID**: _Buffer_ = Buffer.alloc(32)

_Defined in [src/apis/platformvm/createchaintx.ts:57](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/createchaintx.ts#L57)_

## Methods

### addSignatureIdx

▸ **addSignatureIdx**(`addressIdx`: number, `address`: Buffer): _void_

_Defined in [src/apis/platformvm/createchaintx.ts:233](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/createchaintx.ts#L233)_

Creates and adds a [SigIdx](common_signature.sigidx) to the [AddSubnetValidatorTx](../modules/src_apis_platformvm#addsubnetvalidatortx).

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

_Defined in [src/apis/platformvm/createchaintx.ts:217](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/createchaintx.ts#L217)_

**Returns:** _this_

---

### create

▸ **create**(...`args`: any[]): _this_

_Overrides [ValidatorTx](api_platformvm_validationtx.validatortx).[create](api_platformvm_validationtx.validatortx#create)_

_Defined in [src/apis/platformvm/createchaintx.ts:223](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/createchaintx.ts#L223)_

**Parameters:**

| Name      | Type  |
| --------- | ----- |
| `...args` | any[] |

**Returns:** _this_

---

### deserialize

▸ **deserialize**(`fields`: object, `encoding`: [SerializedEncoding](../modules/utils_serialization#serializedencoding)): _void_

_Overrides [BaseTx](api_platformvm_basetx.basetx).[deserialize](api_platformvm_basetx.basetx#deserialize)_

_Defined in [src/apis/platformvm/createchaintx.ts:39](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/createchaintx.ts#L39)_

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

_Defined in [src/apis/platformvm/createchaintx.ts:123](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/createchaintx.ts#L123)_

Takes a [Buffer](https://github.com/feross/buffer) containing an [CreateChainTx](api_platformvm_createchaintx.createchaintx), parses it, populates the class, and returns the length of the [CreateChainTx](api_platformvm_createchaintx.createchaintx) in bytes.

**`remarks`** assume not-checksummed

**Parameters:**

| Name     | Type   | Default | Description                                                                                                               |
| -------- | ------ | ------- | ------------------------------------------------------------------------------------------------------------------------- |
| `bytes`  | Buffer | -       | A [Buffer](https://github.com/feross/buffer) containing a raw [CreateChainTx](api_platformvm_createchaintx.createchaintx) |
| `offset` | number | 0       | -                                                                                                                         |

**Returns:** _number_

The length of the raw [CreateChainTx](api_platformvm_createchaintx.createchaintx)

---

### getBlockchainID

▸ **getBlockchainID**(): _Buffer_

_Inherited from [StandardBaseTx](common_transactions.standardbasetx).[getBlockchainID](common_transactions.standardbasetx#getblockchainid)_

_Defined in [src/common/tx.ts:104](https://github.com/chain4travel/caminojs/blob/3883166/src/common/tx.ts#L104)_

Returns the Buffer representation of the BlockchainID

**Returns:** _Buffer_

---

### getChainName

▸ **getChainName**(): _string_

_Defined in [src/apis/platformvm/createchaintx.ts:89](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/createchaintx.ts#L89)_

Returns a string of the chainName

**Returns:** _string_

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

_Defined in [src/apis/platformvm/createchaintx.ts:254](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/createchaintx.ts#L254)_

**Returns:** _number_

---

### getFXIDs

▸ **getFXIDs**(): _Buffer[]_

_Defined in [src/apis/platformvm/createchaintx.ts:103](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/createchaintx.ts#L103)_

Returns an array of fxIDs as Buffers

**Returns:** _Buffer[]_

---

### getGenesisData

▸ **getGenesisData**(): _string_

_Defined in [src/apis/platformvm/createchaintx.ts:110](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/createchaintx.ts#L110)_

Returns a string of the genesisData

**Returns:** _string_

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

### getSigIdxs

▸ **getSigIdxs**(): _[SigIdx](common_signature.sigidx)[]_

_Defined in [src/apis/platformvm/createchaintx.ts:250](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/createchaintx.ts#L250)_

Returns the array of [SigIdx](common_signature.sigidx) for this [Input](common_inputs.input)

**Returns:** _[SigIdx](common_signature.sigidx)[]_

---

### getSubnetAuth

▸ **getSubnetAuth**(): _[SubnetAuth](api_platformvm_subnetauth.subnetauth)_

_Defined in [src/apis/platformvm/createchaintx.ts:75](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/createchaintx.ts#L75)_

Returns the subnetAuth

**Returns:** _[SubnetAuth](api_platformvm_subnetauth.subnetauth)_

---

### getSubnetID

▸ **getSubnetID**(): _string_

_Defined in [src/apis/platformvm/createchaintx.ts:82](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/createchaintx.ts#L82)_

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

_Defined in [src/apis/platformvm/createchaintx.ts:68](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/createchaintx.ts#L68)_

Returns the id of the [CreateChainTx](api_platformvm_createchaintx.createchaintx)

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

### getVMID

▸ **getVMID**(): _Buffer_

_Defined in [src/apis/platformvm/createchaintx.ts:96](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/createchaintx.ts#L96)_

Returns a Buffer of the vmID

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

_Overrides [StandardBaseTx](common_transactions.standardbasetx).[serialize](common_transactions.standardbasetx#serialize)_

_Defined in [src/apis/platformvm/createchaintx.ts:31](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/createchaintx.ts#L31)_

**Parameters:**

| Name       | Type                                                                    | Default |
| ---------- | ----------------------------------------------------------------------- | ------- |
| `encoding` | [SerializedEncoding](../modules/utils_serialization#serializedencoding) | "hex"   |

**Returns:** _object_

---

### sign

▸ **sign**(`msg`: Buffer, `kc`: [KeyChain](api_platformvm_keychain.keychain)): _[Credential](common_signature.credential)[]_

_Overrides [ExportTx](api_platformvm_exporttx.exporttx).[sign](api_platformvm_exporttx.exporttx#sign)_

_Defined in [src/apis/platformvm/createchaintx.ts:266](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/createchaintx.ts#L266)_

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

_Defined in [src/apis/platformvm/createchaintx.ts:174](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/createchaintx.ts#L174)_

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
