# Class: EVMStandardBaseTx ‹**KPClass, KCClass**›

Class representing a base for all transactions.

## Type parameters

▪ **KPClass**: _[StandardKeyPair](common_keychain.standardkeypair)_

▪ **KCClass**: _[StandardKeyChain](common_keychain.standardkeychain)‹KPClass›_

## Hierarchy

- [Serializable](utils_serialization.serializable)

  ↳ **EVMStandardBaseTx**

  ↳ [EVMBaseTx](api_evm_basetx.evmbasetx)

## Index

### Constructors

- [constructor](common_transactions.evmstandardbasetx#constructor)

### Properties

- [\_codecID](common_transactions.evmstandardbasetx#protected-_codecid)
- [\_typeID](common_transactions.evmstandardbasetx#protected-_typeid)
- [\_typeName](common_transactions.evmstandardbasetx#protected-_typename)
- [blockchainID](common_transactions.evmstandardbasetx#protected-blockchainid)
- [networkID](common_transactions.evmstandardbasetx#protected-networkid)

### Methods

- [clone](common_transactions.evmstandardbasetx#abstract-clone)
- [create](common_transactions.evmstandardbasetx#abstract-create)
- [deserialize](common_transactions.evmstandardbasetx#deserialize)
- [getBlockchainID](common_transactions.evmstandardbasetx#getblockchainid)
- [getCodecID](common_transactions.evmstandardbasetx#getcodecid)
- [getNetworkID](common_transactions.evmstandardbasetx#getnetworkid)
- [getTxType](common_transactions.evmstandardbasetx#abstract-gettxtype)
- [getTypeID](common_transactions.evmstandardbasetx#gettypeid)
- [getTypeName](common_transactions.evmstandardbasetx#gettypename)
- [sanitizeObject](common_transactions.evmstandardbasetx#sanitizeobject)
- [select](common_transactions.evmstandardbasetx#abstract-select)
- [serialize](common_transactions.evmstandardbasetx#serialize)
- [toBuffer](common_transactions.evmstandardbasetx#tobuffer)
- [toString](common_transactions.evmstandardbasetx#tostring)

## Constructors

### constructor

\+ **new EVMStandardBaseTx**(`networkID`: number, `blockchainID`: Buffer): _[EVMStandardBaseTx](common_transactions.evmstandardbasetx)_

_Defined in [src/common/evmtx.ts:116](https://github.com/chain4travel/caminojs/blob/3883166/src/common/evmtx.ts#L116)_

Class representing a StandardBaseTx which is the foundation for all transactions.

**Parameters:**

| Name           | Type   | Default              | Description                                                                               |
| -------------- | ------ | -------------------- | ----------------------------------------------------------------------------------------- |
| `networkID`    | number | DefaultNetworkID     | Optional networkID, [DefaultNetworkID](../modules/utils_constants#const-defaultnetworkid) |
| `blockchainID` | Buffer | Buffer.alloc(32, 16) | Optional blockchainID, default Buffer.alloc(32, 16)                                       |

**Returns:** _[EVMStandardBaseTx](common_transactions.evmstandardbasetx)_

## Properties

### `Protected` \_codecID

• **\_codecID**: _number_ = undefined

_Inherited from [SigIdx](common_signature.sigidx).[\_codecID](common_signature.sigidx#protected-_codecid)_

_Defined in [src/utils/serialization.ts:51](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/serialization.ts#L51)_

---

### `Protected` \_typeID

• **\_typeID**: _any_ = undefined

_Overrides [Serializable](utils_serialization.serializable).[\_typeID](utils_serialization.serializable#protected-_typeid)_

_Defined in [src/common/evmtx.ts:34](https://github.com/chain4travel/caminojs/blob/3883166/src/common/evmtx.ts#L34)_

---

### `Protected` \_typeName

• **\_typeName**: _string_ = "EVMStandardBaseTx"

_Overrides [Serializable](utils_serialization.serializable).[\_typeName](utils_serialization.serializable#protected-_typename)_

_Defined in [src/common/evmtx.ts:33](https://github.com/chain4travel/caminojs/blob/3883166/src/common/evmtx.ts#L33)_

---

### `Protected` blockchainID

• **blockchainID**: _Buffer_ = Buffer.alloc(32)

_Defined in [src/common/evmtx.ts:74](https://github.com/chain4travel/caminojs/blob/3883166/src/common/evmtx.ts#L74)_

---

### `Protected` networkID

• **networkID**: _Buffer_ = Buffer.alloc(4)

_Defined in [src/common/evmtx.ts:73](https://github.com/chain4travel/caminojs/blob/3883166/src/common/evmtx.ts#L73)_

## Methods

### `Abstract` clone

▸ **clone**(): _this_

_Defined in [src/common/evmtx.ts:112](https://github.com/chain4travel/caminojs/blob/3883166/src/common/evmtx.ts#L112)_

**Returns:** _this_

---

### `Abstract` create

▸ **create**(...`args`: any[]): _this_

_Defined in [src/common/evmtx.ts:114](https://github.com/chain4travel/caminojs/blob/3883166/src/common/evmtx.ts#L114)_

**Parameters:**

| Name      | Type  |
| --------- | ----- |
| `...args` | any[] |

**Returns:** _this_

---

### deserialize

▸ **deserialize**(`fields`: object, `encoding`: [SerializedEncoding](../modules/utils_serialization#serializedencoding)): _void_

_Overrides [StandardParseableInput](common_inputs.standardparseableinput).[deserialize](common_inputs.standardparseableinput#deserialize)_

_Defined in [src/common/evmtx.ts:55](https://github.com/chain4travel/caminojs/blob/3883166/src/common/evmtx.ts#L55)_

**Parameters:**

| Name       | Type                                                                    | Default |
| ---------- | ----------------------------------------------------------------------- | ------- |
| `fields`   | object                                                                  | -       |
| `encoding` | [SerializedEncoding](../modules/utils_serialization#serializedencoding) | "hex"   |

**Returns:** _void_

---

### getBlockchainID

▸ **getBlockchainID**(): _Buffer_

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

_Defined in [src/common/evmtx.ts:84](https://github.com/chain4travel/caminojs/blob/3883166/src/common/evmtx.ts#L84)_

Returns the NetworkID as a number

**Returns:** _number_

---

### `Abstract` getTxType

▸ **getTxType**(): _number_

_Defined in [src/common/evmtx.ts:79](https://github.com/chain4travel/caminojs/blob/3883166/src/common/evmtx.ts#L79)_

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

_Defined in [src/common/evmtx.ts:116](https://github.com/chain4travel/caminojs/blob/3883166/src/common/evmtx.ts#L116)_

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

_Defined in [src/common/evmtx.ts:36](https://github.com/chain4travel/caminojs/blob/3883166/src/common/evmtx.ts#L36)_

**Parameters:**

| Name       | Type                                                                    | Default |
| ---------- | ----------------------------------------------------------------------- | ------- |
| `encoding` | [SerializedEncoding](../modules/utils_serialization#serializedencoding) | "hex"   |

**Returns:** _object_

---

### toBuffer

▸ **toBuffer**(): _Buffer_

_Defined in [src/common/evmtx.ts:98](https://github.com/chain4travel/caminojs/blob/3883166/src/common/evmtx.ts#L98)_

Returns a [Buffer](https://github.com/feross/buffer) representation of the [StandardBaseTx](common_transactions.standardbasetx).

**Returns:** _Buffer_

---

### toString

▸ **toString**(): _string_

_Defined in [src/common/evmtx.ts:108](https://github.com/chain4travel/caminojs/blob/3883166/src/common/evmtx.ts#L108)_

Returns a base-58 representation of the [StandardBaseTx](common_transactions.standardbasetx).

**Returns:** _string_
