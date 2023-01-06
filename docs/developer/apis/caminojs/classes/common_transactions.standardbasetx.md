# Class: StandardBaseTx ‹**KPClass, KCClass**›

Class representing a base for all transactions.

## Type parameters

▪ **KPClass**: _[StandardKeyPair](common_keychain.standardkeypair)_

▪ **KCClass**: _[StandardKeyChain](common_keychain.standardkeychain)‹KPClass›_

## Hierarchy

- [Serializable](utils_serialization.serializable)

  ↳ **StandardBaseTx**

  ↳ [BaseTx](api_avm_basetx.basetx)

  ↳ [BaseTx](api_platformvm_basetx.basetx)

## Index

### Constructors

- [constructor](common_transactions.standardbasetx#constructor)

### Properties

- [\_codecID](common_transactions.standardbasetx#protected-_codecid)
- [\_typeID](common_transactions.standardbasetx#protected-_typeid)
- [\_typeName](common_transactions.standardbasetx#protected-_typename)
- [blockchainID](common_transactions.standardbasetx#protected-blockchainid)
- [ins](common_transactions.standardbasetx#protected-ins)
- [memo](common_transactions.standardbasetx#protected-memo)
- [networkID](common_transactions.standardbasetx#protected-networkid)
- [numins](common_transactions.standardbasetx#protected-numins)
- [numouts](common_transactions.standardbasetx#protected-numouts)
- [outs](common_transactions.standardbasetx#protected-outs)

### Methods

- [clone](common_transactions.standardbasetx#abstract-clone)
- [create](common_transactions.standardbasetx#abstract-create)
- [deserialize](common_transactions.standardbasetx#deserialize)
- [getBlockchainID](common_transactions.standardbasetx#getblockchainid)
- [getCodecID](common_transactions.standardbasetx#getcodecid)
- [getIns](common_transactions.standardbasetx#abstract-getins)
- [getMemo](common_transactions.standardbasetx#getmemo)
- [getNetworkID](common_transactions.standardbasetx#getnetworkid)
- [getOuts](common_transactions.standardbasetx#abstract-getouts)
- [getTotalOuts](common_transactions.standardbasetx#abstract-gettotalouts)
- [getTxType](common_transactions.standardbasetx#abstract-gettxtype)
- [getTypeID](common_transactions.standardbasetx#gettypeid)
- [getTypeName](common_transactions.standardbasetx#gettypename)
- [sanitizeObject](common_transactions.standardbasetx#sanitizeobject)
- [select](common_transactions.standardbasetx#abstract-select)
- [serialize](common_transactions.standardbasetx#serialize)
- [sign](common_transactions.standardbasetx#abstract-sign)
- [toBuffer](common_transactions.standardbasetx#tobuffer)
- [toString](common_transactions.standardbasetx#tostring)
- [toStringHex](common_transactions.standardbasetx#tostringhex)

## Constructors

### constructor

\+ **new StandardBaseTx**(`networkID`: number, `blockchainID`: Buffer, `outs`: [StandardTransferableOutput](common_output.standardtransferableoutput)[], `ins`: [StandardTransferableInput](common_inputs.standardtransferableinput)[], `memo`: Buffer): _[StandardBaseTx](common_transactions.standardbasetx)_

_Defined in [src/common/tx.ts:188](https://github.com/chain4travel/caminojs/blob/3883166/src/common/tx.ts#L188)_

Class representing a StandardBaseTx which is the foundation for all transactions.

**Parameters:**

| Name           | Type                                                                     | Default              | Description                                                                               |
| -------------- | ------------------------------------------------------------------------ | -------------------- | ----------------------------------------------------------------------------------------- |
| `networkID`    | number                                                                   | DefaultNetworkID     | Optional networkID, [DefaultNetworkID](../modules/utils_constants#const-defaultnetworkid) |
| `blockchainID` | Buffer                                                                   | Buffer.alloc(32, 16) | Optional blockchainID, default Buffer.alloc(32, 16)                                       |
| `outs`         | [StandardTransferableOutput](common_output.standardtransferableoutput)[] | undefined            | Optional array of the [TransferableOutput](api_evm_outputs.transferableoutput)s           |
| `ins`          | [StandardTransferableInput](common_inputs.standardtransferableinput)[]   | undefined            | Optional array of the [TransferableInput](api_evm_inputs.transferableinput)s              |
| `memo`         | Buffer                                                                   | undefined            | Optional [Buffer](https://github.com/feross/buffer) for the memo field                    |

**Returns:** _[StandardBaseTx](common_transactions.standardbasetx)_

## Properties

### `Protected` \_codecID

• **\_codecID**: _number_ = undefined

_Inherited from [SigIdx](common_signature.sigidx).[\_codecID](common_signature.sigidx#protected-_codecid)_

_Defined in [src/utils/serialization.ts:51](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/serialization.ts#L51)_

---

### `Protected` \_typeID

• **\_typeID**: _any_ = undefined

_Overrides [Serializable](utils_serialization.serializable).[\_typeID](utils_serialization.serializable#protected-_typeid)_

_Defined in [src/common/tx.ts:38](https://github.com/chain4travel/caminojs/blob/3883166/src/common/tx.ts#L38)_

---

### `Protected` \_typeName

• **\_typeName**: _string_ = "StandardBaseTx"

_Overrides [Serializable](utils_serialization.serializable).[\_typeName](utils_serialization.serializable#protected-_typename)_

_Defined in [src/common/tx.ts:37](https://github.com/chain4travel/caminojs/blob/3883166/src/common/tx.ts#L37)_

---

### `Protected` blockchainID

• **blockchainID**: _Buffer_ = Buffer.alloc(32)

_Defined in [src/common/tx.ts:82](https://github.com/chain4travel/caminojs/blob/3883166/src/common/tx.ts#L82)_

---

### `Protected` ins

• **ins**: _[StandardTransferableInput](common_inputs.standardtransferableinput)[]_

_Defined in [src/common/tx.ts:86](https://github.com/chain4travel/caminojs/blob/3883166/src/common/tx.ts#L86)_

---

### `Protected` memo

• **memo**: _Buffer_ = Buffer.alloc(0)

_Defined in [src/common/tx.ts:87](https://github.com/chain4travel/caminojs/blob/3883166/src/common/tx.ts#L87)_

---

### `Protected` networkID

• **networkID**: _Buffer_ = Buffer.alloc(4)

_Defined in [src/common/tx.ts:81](https://github.com/chain4travel/caminojs/blob/3883166/src/common/tx.ts#L81)_

---

### `Protected` numins

• **numins**: _Buffer_ = Buffer.alloc(4)

_Defined in [src/common/tx.ts:85](https://github.com/chain4travel/caminojs/blob/3883166/src/common/tx.ts#L85)_

---

### `Protected` numouts

• **numouts**: _Buffer_ = Buffer.alloc(4)

_Defined in [src/common/tx.ts:83](https://github.com/chain4travel/caminojs/blob/3883166/src/common/tx.ts#L83)_

---

### `Protected` outs

• **outs**: _[StandardTransferableOutput](common_output.standardtransferableoutput)[]_

_Defined in [src/common/tx.ts:84](https://github.com/chain4travel/caminojs/blob/3883166/src/common/tx.ts#L84)_

## Methods

### `Abstract` clone

▸ **clone**(): _this_

_Defined in [src/common/tx.ts:184](https://github.com/chain4travel/caminojs/blob/3883166/src/common/tx.ts#L184)_

**Returns:** _this_

---

### `Abstract` create

▸ **create**(...`args`: any[]): _this_

_Defined in [src/common/tx.ts:186](https://github.com/chain4travel/caminojs/blob/3883166/src/common/tx.ts#L186)_

**Parameters:**

| Name      | Type  |
| --------- | ----- |
| `...args` | any[] |

**Returns:** _this_

---

### deserialize

▸ **deserialize**(`fields`: object, `encoding`: [SerializedEncoding](../modules/utils_serialization#serializedencoding)): _void_

_Overrides [StandardParseableInput](common_inputs.standardparseableinput).[deserialize](common_inputs.standardparseableinput#deserialize)_

_Defined in [src/common/tx.ts:62](https://github.com/chain4travel/caminojs/blob/3883166/src/common/tx.ts#L62)_

**Parameters:**

| Name       | Type                                                                    | Default |
| ---------- | ----------------------------------------------------------------------- | ------- |
| `fields`   | object                                                                  | -       |
| `encoding` | [SerializedEncoding](../modules/utils_serialization#serializedencoding) | "hex"   |

**Returns:** _void_

---

### getBlockchainID

▸ **getBlockchainID**(): _Buffer_

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

### `Abstract` getIns

▸ **getIns**(): _[StandardTransferableInput](common_inputs.standardtransferableinput)[]_

_Defined in [src/common/tx.ts:111](https://github.com/chain4travel/caminojs/blob/3883166/src/common/tx.ts#L111)_

Returns the array of [StandardTransferableInput](common_inputs.standardtransferableinput)s

**Returns:** _[StandardTransferableInput](common_inputs.standardtransferableinput)[]_

---

### getMemo

▸ **getMemo**(): _Buffer_

_Defined in [src/common/tx.ts:126](https://github.com/chain4travel/caminojs/blob/3883166/src/common/tx.ts#L126)_

Returns the [Buffer](https://github.com/feross/buffer) representation of the memo

**Returns:** _Buffer_

---

### getNetworkID

▸ **getNetworkID**(): _number_

_Defined in [src/common/tx.ts:97](https://github.com/chain4travel/caminojs/blob/3883166/src/common/tx.ts#L97)_

Returns the NetworkID as a number

**Returns:** _number_

---

### `Abstract` getOuts

▸ **getOuts**(): _[StandardTransferableOutput](common_output.standardtransferableoutput)[]_

_Defined in [src/common/tx.ts:116](https://github.com/chain4travel/caminojs/blob/3883166/src/common/tx.ts#L116)_

Returns the array of [StandardTransferableOutput](../modules/src_common#standardtransferableoutput)s

**Returns:** _[StandardTransferableOutput](common_output.standardtransferableoutput)[]_

---

### `Abstract` getTotalOuts

▸ **getTotalOuts**(): _[StandardTransferableOutput](common_output.standardtransferableoutput)[]_

_Defined in [src/common/tx.ts:121](https://github.com/chain4travel/caminojs/blob/3883166/src/common/tx.ts#L121)_

Returns the array of combined total [StandardTransferableOutput](../modules/src_common#standardtransferableoutput)s

**Returns:** _[StandardTransferableOutput](common_output.standardtransferableoutput)[]_

---

### `Abstract` getTxType

▸ **getTxType**(): _number_

_Defined in [src/common/tx.ts:92](https://github.com/chain4travel/caminojs/blob/3883166/src/common/tx.ts#L92)_

Returns the id of the [StandardBaseTx](common_transactions.standardbasetx)

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

### `Abstract` select

▸ **select**(`id`: number, ...`args`: any[]): _this_

_Defined in [src/common/tx.ts:188](https://github.com/chain4travel/caminojs/blob/3883166/src/common/tx.ts#L188)_

**Parameters:**

| Name      | Type   |
| --------- | ------ |
| `id`      | number |
| `...args` | any[]  |

**Returns:** _this_

---

### serialize

▸ **serialize**(`encoding`: [SerializedEncoding](../modules/utils_serialization#serializedencoding)): _object_

_Overrides [Serializable](utils_serialization.serializable).[serialize](utils_serialization.serializable#serialize)_

_Defined in [src/common/tx.ts:40](https://github.com/chain4travel/caminojs/blob/3883166/src/common/tx.ts#L40)_

**Parameters:**

| Name       | Type                                                                    | Default |
| ---------- | ----------------------------------------------------------------------- | ------- |
| `encoding` | [SerializedEncoding](../modules/utils_serialization#serializedencoding) | "hex"   |

**Returns:** _object_

---

### `Abstract` sign

▸ **sign**(`msg`: Buffer, `kc`: [StandardKeyChain](common_keychain.standardkeychain)‹KPClass›): _[Credential](common_signature.credential)[]_

_Defined in [src/common/tx.ts:182](https://github.com/chain4travel/caminojs/blob/3883166/src/common/tx.ts#L182)_

Takes the bytes of an [UnsignedTx](api_evm_transactions.unsignedtx) and returns an array of [Credential](common_signature.credential)s

**Parameters:**

| Name  | Type                                                          | Description                                                    |
| ----- | ------------------------------------------------------------- | -------------------------------------------------------------- |
| `msg` | Buffer                                                        | A Buffer for the [UnsignedTx](api_evm_transactions.unsignedtx) |
| `kc`  | [StandardKeyChain](common_keychain.standardkeychain)‹KPClass› | An [KeyChain](api_evm_keychain.keychain) used in signing       |

**Returns:** _[Credential](common_signature.credential)[]_

An array of [Credential](common_signature.credential)s

---

### toBuffer

▸ **toBuffer**(): _Buffer_

_Defined in [src/common/tx.ts:133](https://github.com/chain4travel/caminojs/blob/3883166/src/common/tx.ts#L133)_

Returns a [Buffer](https://github.com/feross/buffer) representation of the [StandardBaseTx](common_transactions.standardbasetx).

**Returns:** _Buffer_

---

### toString

▸ **toString**(): _string_

_Defined in [src/common/tx.ts:166](https://github.com/chain4travel/caminojs/blob/3883166/src/common/tx.ts#L166)_

Returns a base-58 representation of the [StandardBaseTx](common_transactions.standardbasetx).

**Returns:** _string_

---

### toStringHex

▸ **toStringHex**(): _string_

_Defined in [src/common/tx.ts:170](https://github.com/chain4travel/caminojs/blob/3883166/src/common/tx.ts#L170)_

**Returns:** _string_
