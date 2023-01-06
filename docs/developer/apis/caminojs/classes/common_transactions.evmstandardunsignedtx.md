# Class: EVMStandardUnsignedTx ‹**KPClass, KCClass, SBTx**›

Class representing an unsigned transaction.

## Type parameters

▪ **KPClass**: _[StandardKeyPair](common_keychain.standardkeypair)_

▪ **KCClass**: _[StandardKeyChain](common_keychain.standardkeychain)‹KPClass›_

▪ **SBTx**: _[EVMStandardBaseTx](common_transactions.evmstandardbasetx)‹KPClass, KCClass›_

## Hierarchy

- [Serializable](utils_serialization.serializable)

  ↳ **EVMStandardUnsignedTx**

  ↳ [UnsignedTx](api_evm_transactions.unsignedtx)

## Index

### Constructors

- [constructor](common_transactions.evmstandardunsignedtx#constructor)

### Properties

- [\_codecID](common_transactions.evmstandardunsignedtx#protected-_codecid)
- [\_typeID](common_transactions.evmstandardunsignedtx#protected-_typeid)
- [\_typeName](common_transactions.evmstandardunsignedtx#protected-_typename)
- [codecID](common_transactions.evmstandardunsignedtx#protected-codecid)
- [transaction](common_transactions.evmstandardunsignedtx#protected-transaction)

### Methods

- [deserialize](common_transactions.evmstandardunsignedtx#deserialize)
- [fromBuffer](common_transactions.evmstandardunsignedtx#abstract-frombuffer)
- [getBurn](common_transactions.evmstandardunsignedtx#getburn)
- [getCodecID](common_transactions.evmstandardunsignedtx#getcodecid)
- [getCodecIDBuffer](common_transactions.evmstandardunsignedtx#getcodecidbuffer)
- [getInputTotal](common_transactions.evmstandardunsignedtx#getinputtotal)
- [getOutputTotal](common_transactions.evmstandardunsignedtx#getoutputtotal)
- [getTransaction](common_transactions.evmstandardunsignedtx#abstract-gettransaction)
- [getTypeID](common_transactions.evmstandardunsignedtx#gettypeid)
- [getTypeName](common_transactions.evmstandardunsignedtx#gettypename)
- [sanitizeObject](common_transactions.evmstandardunsignedtx#sanitizeobject)
- [serialize](common_transactions.evmstandardunsignedtx#serialize)
- [sign](common_transactions.evmstandardunsignedtx#abstract-sign)
- [toBuffer](common_transactions.evmstandardunsignedtx#tobuffer)

## Constructors

### constructor

\+ **new EVMStandardUnsignedTx**(`transaction`: SBTx, `codecID`: number): _[EVMStandardUnsignedTx](common_transactions.evmstandardunsignedtx)_

_Defined in [src/common/evmtx.ts:271](https://github.com/chain4travel/caminojs/blob/3883166/src/common/evmtx.ts#L271)_

**Parameters:**

| Name          | Type   | Default   |
| ------------- | ------ | --------- |
| `transaction` | SBTx   | undefined |
| `codecID`     | number | 0         |

**Returns:** _[EVMStandardUnsignedTx](common_transactions.evmstandardunsignedtx)_

## Properties

### `Protected` \_codecID

• **\_codecID**: _number_ = undefined

_Inherited from [SigIdx](common_signature.sigidx).[\_codecID](common_signature.sigidx#protected-_codecid)_

_Defined in [src/utils/serialization.ts:51](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/serialization.ts#L51)_

---

### `Protected` \_typeID

• **\_typeID**: _any_ = undefined

_Overrides [Serializable](utils_serialization.serializable).[\_typeID](utils_serialization.serializable#protected-_typeid)_

_Defined in [src/common/evmtx.ts:145](https://github.com/chain4travel/caminojs/blob/3883166/src/common/evmtx.ts#L145)_

---

### `Protected` \_typeName

• **\_typeName**: _string_ = "StandardUnsignedTx"

_Overrides [Serializable](utils_serialization.serializable).[\_typeName](utils_serialization.serializable#protected-_typename)_

_Defined in [src/common/evmtx.ts:144](https://github.com/chain4travel/caminojs/blob/3883166/src/common/evmtx.ts#L144)_

---

### `Protected` codecID

• **codecID**: _number_ = 0

_Defined in [src/common/evmtx.ts:172](https://github.com/chain4travel/caminojs/blob/3883166/src/common/evmtx.ts#L172)_

---

### `Protected` transaction

• **transaction**: _SBTx_

_Defined in [src/common/evmtx.ts:173](https://github.com/chain4travel/caminojs/blob/3883166/src/common/evmtx.ts#L173)_

## Methods

### deserialize

▸ **deserialize**(`fields`: object, `encoding`: [SerializedEncoding](../modules/utils_serialization#serializedencoding)): _void_

_Overrides [StandardParseableInput](common_inputs.standardparseableinput).[deserialize](common_inputs.standardparseableinput#deserialize)_

_Defined in [src/common/evmtx.ts:162](https://github.com/chain4travel/caminojs/blob/3883166/src/common/evmtx.ts#L162)_

**Parameters:**

| Name       | Type                                                                    | Default |
| ---------- | ----------------------------------------------------------------------- | ------- |
| `fields`   | object                                                                  | -       |
| `encoding` | [SerializedEncoding](../modules/utils_serialization#serializedencoding) | "hex"   |

**Returns:** _void_

---

### `Abstract` fromBuffer

▸ **fromBuffer**(`bytes`: Buffer, `offset?`: number): _number_

_Defined in [src/common/evmtx.ts:245](https://github.com/chain4travel/caminojs/blob/3883166/src/common/evmtx.ts#L245)_

**Parameters:**

| Name      | Type   |
| --------- | ------ |
| `bytes`   | Buffer |
| `offset?` | number |

**Returns:** _number_

---

### getBurn

▸ **getBurn**(`assetID`: Buffer): _BN_

_Defined in [src/common/evmtx.ts:236](https://github.com/chain4travel/caminojs/blob/3883166/src/common/evmtx.ts#L236)_

Returns the number of burned tokens as a BN

**Parameters:**

| Name      | Type   |
| --------- | ------ |
| `assetID` | Buffer |

**Returns:** _BN_

---

### getCodecID

▸ **getCodecID**(): _number_

_Overrides [SigIdx](common_signature.sigidx).[getCodecID](common_signature.sigidx#getcodecid)_

_Defined in [src/common/evmtx.ts:178](https://github.com/chain4travel/caminojs/blob/3883166/src/common/evmtx.ts#L178)_

Returns the CodecID as a number

**Returns:** _number_

---

### getCodecIDBuffer

▸ **getCodecIDBuffer**(): _Buffer_

_Defined in [src/common/evmtx.ts:185](https://github.com/chain4travel/caminojs/blob/3883166/src/common/evmtx.ts#L185)_

Returns the [Buffer](https://github.com/feross/buffer) representation of the CodecID

**Returns:** _Buffer_

---

### getInputTotal

▸ **getInputTotal**(`assetID`: Buffer): _BN_

_Defined in [src/common/evmtx.ts:194](https://github.com/chain4travel/caminojs/blob/3883166/src/common/evmtx.ts#L194)_

Returns the inputTotal as a BN

**Parameters:**

| Name      | Type   |
| --------- | ------ |
| `assetID` | Buffer |

**Returns:** _BN_

---

### getOutputTotal

▸ **getOutputTotal**(`assetID`: Buffer): _BN_

_Defined in [src/common/evmtx.ts:214](https://github.com/chain4travel/caminojs/blob/3883166/src/common/evmtx.ts#L214)_

Returns the outputTotal as a BN

**Parameters:**

| Name      | Type   |
| --------- | ------ |
| `assetID` | Buffer |

**Returns:** _BN_

---

### `Abstract` getTransaction

▸ **getTransaction**(): _SBTx_

_Defined in [src/common/evmtx.ts:243](https://github.com/chain4travel/caminojs/blob/3883166/src/common/evmtx.ts#L243)_

Returns the Transaction

**Returns:** _SBTx_

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

### serialize

▸ **serialize**(`encoding`: [SerializedEncoding](../modules/utils_serialization#serializedencoding)): _object_

_Overrides [Serializable](utils_serialization.serializable).[serialize](utils_serialization.serializable#serialize)_

_Defined in [src/common/evmtx.ts:147](https://github.com/chain4travel/caminojs/blob/3883166/src/common/evmtx.ts#L147)_

**Parameters:**

| Name       | Type                                                                    | Default |
| ---------- | ----------------------------------------------------------------------- | ------- |
| `encoding` | [SerializedEncoding](../modules/utils_serialization#serializedencoding) | "hex"   |

**Returns:** _object_

---

### `Abstract` sign

▸ **sign**(`kc`: KCClass): _[EVMStandardTx](common_transactions.evmstandardtx)‹KPClass, KCClass, [EVMStandardUnsignedTx](common_transactions.evmstandardunsignedtx)‹KPClass, KCClass, SBTx››_

_Defined in [src/common/evmtx.ts:265](https://github.com/chain4travel/caminojs/blob/3883166/src/common/evmtx.ts#L265)_

Signs this [UnsignedTx](api_evm_transactions.unsignedtx) and returns signed [StandardTx](common_transactions.standardtx)

**Parameters:**

| Name | Type    | Description                                              |
| ---- | ------- | -------------------------------------------------------- |
| `kc` | KCClass | An [KeyChain](api_evm_keychain.keychain) used in signing |

**Returns:** _[EVMStandardTx](common_transactions.evmstandardtx)‹KPClass, KCClass, [EVMStandardUnsignedTx](common_transactions.evmstandardunsignedtx)‹KPClass, KCClass, SBTx››_

A signed [StandardTx](common_transactions.standardtx)

---

### toBuffer

▸ **toBuffer**(): _Buffer_

_Defined in [src/common/evmtx.ts:247](https://github.com/chain4travel/caminojs/blob/3883166/src/common/evmtx.ts#L247)_

**Returns:** _Buffer_
