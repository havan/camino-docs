# Class: EVMBaseTx

Class representing a base for all transactions.

## Hierarchy

↳ [EVMStandardBaseTx](common_transactions.evmstandardbasetx)‹[KeyPair](api_evm_keychain.keypair), [KeyChain](api_evm_keychain.keychain)›

↳ **EVMBaseTx**

↳ [ImportTx](api_evm_importtx.importtx)

↳ [ExportTx](api_evm_exporttx.exporttx)

## Index

### Constructors

- [constructor](api_evm_basetx.evmbasetx#constructor)

### Properties

- [\_codecID](api_evm_basetx.evmbasetx#protected-_codecid)
- [\_typeID](api_evm_basetx.evmbasetx#protected-_typeid)
- [\_typeName](api_evm_basetx.evmbasetx#protected-_typename)
- [blockchainID](api_evm_basetx.evmbasetx#protected-blockchainid)
- [networkID](api_evm_basetx.evmbasetx#protected-networkid)

### Methods

- [clone](api_evm_basetx.evmbasetx#clone)
- [create](api_evm_basetx.evmbasetx#create)
- [deserialize](api_evm_basetx.evmbasetx#deserialize)
- [fromBuffer](api_evm_basetx.evmbasetx#frombuffer)
- [getBlockchainID](api_evm_basetx.evmbasetx#getblockchainid)
- [getCodecID](api_evm_basetx.evmbasetx#getcodecid)
- [getNetworkID](api_evm_basetx.evmbasetx#getnetworkid)
- [getTxType](api_evm_basetx.evmbasetx#gettxtype)
- [getTypeID](api_evm_basetx.evmbasetx#gettypeid)
- [getTypeName](api_evm_basetx.evmbasetx#gettypename)
- [sanitizeObject](api_evm_basetx.evmbasetx#sanitizeobject)
- [select](api_evm_basetx.evmbasetx#select)
- [serialize](api_evm_basetx.evmbasetx#serialize)
- [sign](api_evm_basetx.evmbasetx#sign)
- [toBuffer](api_evm_basetx.evmbasetx#tobuffer)
- [toString](api_evm_basetx.evmbasetx#tostring)

## Constructors

### constructor

\+ **new EVMBaseTx**(`networkID`: number, `blockchainID`: Buffer): _[EVMBaseTx](api_evm_basetx.evmbasetx)_

_Overrides [EVMStandardBaseTx](common_transactions.evmstandardbasetx).[constructor](common_transactions.evmstandardbasetx#constructor)_

_Defined in [src/apis/evm/basetx.ts:83](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/basetx.ts#L83)_

Class representing an EVMBaseTx which is the foundation for all EVM transactions.

**Parameters:**

| Name           | Type   | Default              | Description                                                                               |
| -------------- | ------ | -------------------- | ----------------------------------------------------------------------------------------- |
| `networkID`    | number | DefaultNetworkID     | Optional networkID, [DefaultNetworkID](../modules/utils_constants#const-defaultnetworkid) |
| `blockchainID` | Buffer | Buffer.alloc(32, 16) | Optional blockchainID, default Buffer.alloc(32, 16)                                       |

**Returns:** _[EVMBaseTx](api_evm_basetx.evmbasetx)_

## Properties

### `Protected` \_codecID

• **\_codecID**: _number_ = undefined

_Inherited from [SigIdx](common_signature.sigidx).[\_codecID](common_signature.sigidx#protected-_codecid)_

_Defined in [src/utils/serialization.ts:51](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/serialization.ts#L51)_

---

### `Protected` \_typeID

• **\_typeID**: _any_ = undefined

_Overrides [EVMStandardBaseTx](common_transactions.evmstandardbasetx).[\_typeID](common_transactions.evmstandardbasetx#protected-_typeid)_

_Defined in [src/apis/evm/basetx.ts:25](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/basetx.ts#L25)_

---

### `Protected` \_typeName

• **\_typeName**: _string_ = "BaseTx"

_Overrides [EVMStandardBaseTx](common_transactions.evmstandardbasetx).[\_typeName](common_transactions.evmstandardbasetx#protected-_typename)_

_Defined in [src/apis/evm/basetx.ts:24](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/basetx.ts#L24)_

---

### `Protected` blockchainID

• **blockchainID**: _Buffer_ = Buffer.alloc(32)

_Inherited from [EVMStandardBaseTx](common_transactions.evmstandardbasetx).[blockchainID](common_transactions.evmstandardbasetx#protected-blockchainid)_

_Defined in [src/common/evmtx.ts:74](https://github.com/chain4travel/caminojs/blob/3883166/src/common/evmtx.ts#L74)_

---

### `Protected` networkID

• **networkID**: _Buffer_ = Buffer.alloc(4)

_Inherited from [EVMStandardBaseTx](common_transactions.evmstandardbasetx).[networkID](common_transactions.evmstandardbasetx#protected-networkid)_

_Defined in [src/common/evmtx.ts:73](https://github.com/chain4travel/caminojs/blob/3883166/src/common/evmtx.ts#L73)_

## Methods

### clone

▸ **clone**(): _this_

_Overrides [EVMStandardBaseTx](common_transactions.evmstandardbasetx).[clone](common_transactions.evmstandardbasetx#abstract-clone)_

_Defined in [src/apis/evm/basetx.ts:70](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/basetx.ts#L70)_

**Returns:** _this_

---

### create

▸ **create**(...`args`: any[]): _this_

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

_Overrides [EVMStandardBaseTx](common_transactions.evmstandardbasetx).[deserialize](common_transactions.evmstandardbasetx#deserialize)_

_Defined in [src/apis/evm/basetx.ts:29](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/basetx.ts#L29)_

**Parameters:**

| Name       | Type                                                                    | Default |
| ---------- | ----------------------------------------------------------------------- | ------- |
| `fields`   | object                                                                  | -       |
| `encoding` | [SerializedEncoding](../modules/utils_serialization#serializedencoding) | "hex"   |

**Returns:** _void_

---

### fromBuffer

▸ **fromBuffer**(`bytes`: Buffer, `offset`: number): _number_

_Defined in [src/apis/evm/basetx.ts:49](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/basetx.ts#L49)_

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

### getNetworkID

▸ **getNetworkID**(): _number_

_Inherited from [EVMStandardBaseTx](common_transactions.evmstandardbasetx).[getNetworkID](common_transactions.evmstandardbasetx#getnetworkid)_

_Defined in [src/common/evmtx.ts:84](https://github.com/chain4travel/caminojs/blob/3883166/src/common/evmtx.ts#L84)_

Returns the NetworkID as a number

**Returns:** _number_

---

### getTxType

▸ **getTxType**(): _number_

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

_Inherited from [EVMStandardBaseTx](common_transactions.evmstandardbasetx).[serialize](common_transactions.evmstandardbasetx#serialize)_

_Overrides [Serializable](utils_serialization.serializable).[serialize](utils_serialization.serializable#serialize)_

_Defined in [src/common/evmtx.ts:36](https://github.com/chain4travel/caminojs/blob/3883166/src/common/evmtx.ts#L36)_

**Parameters:**

| Name       | Type                                                                    | Default |
| ---------- | ----------------------------------------------------------------------- | ------- |
| `encoding` | [SerializedEncoding](../modules/utils_serialization#serializedencoding) | "hex"   |

**Returns:** _object_

---

### sign

▸ **sign**(`msg`: Buffer, `kc`: [KeyChain](api_evm_keychain.keychain)): _[Credential](common_signature.credential)[]_

_Defined in [src/apis/evm/basetx.ts:65](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/basetx.ts#L65)_

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

_Inherited from [EVMStandardBaseTx](common_transactions.evmstandardbasetx).[toBuffer](common_transactions.evmstandardbasetx#tobuffer)_

_Defined in [src/common/evmtx.ts:98](https://github.com/chain4travel/caminojs/blob/3883166/src/common/evmtx.ts#L98)_

Returns a [Buffer](https://github.com/feross/buffer) representation of the [StandardBaseTx](common_transactions.standardbasetx).

**Returns:** _Buffer_

---

### toString

▸ **toString**(): _string_

_Inherited from [EVMStandardBaseTx](common_transactions.evmstandardbasetx).[toString](common_transactions.evmstandardbasetx#tostring)_

_Defined in [src/common/evmtx.ts:108](https://github.com/chain4travel/caminojs/blob/3883166/src/common/evmtx.ts#L108)_

Returns a base-58 representation of the [StandardBaseTx](common_transactions.standardbasetx).

**Returns:** _string_
