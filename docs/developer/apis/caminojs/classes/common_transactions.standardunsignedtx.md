# Class: StandardUnsignedTx ‹**KPClass, KCClass, SBTx**›

Class representing an unsigned transaction.

## Type parameters

▪ **KPClass**: _[StandardKeyPair](common_keychain.standardkeypair)_

▪ **KCClass**: _[StandardKeyChain](common_keychain.standardkeychain)‹KPClass›_

▪ **SBTx**: _[StandardBaseTx](common_transactions.standardbasetx)‹KPClass, KCClass›_

## Hierarchy

- [Serializable](utils_serialization.serializable)

  ↳ **StandardUnsignedTx**

  ↳ [UnsignedTx](api_avm_transactions.unsignedtx)

  ↳ [UnsignedTx](api_platformvm_transactions.unsignedtx)

## Index

### Constructors

- [constructor](common_transactions.standardunsignedtx#constructor)

### Properties

- [\_codecID](common_transactions.standardunsignedtx#protected-_codecid)
- [\_typeID](common_transactions.standardunsignedtx#protected-_typeid)
- [\_typeName](common_transactions.standardunsignedtx#protected-_typename)
- [codecID](common_transactions.standardunsignedtx#protected-codecid)
- [transaction](common_transactions.standardunsignedtx#protected-transaction)

### Methods

- [deserialize](common_transactions.standardunsignedtx#deserialize)
- [fromBuffer](common_transactions.standardunsignedtx#abstract-frombuffer)
- [getBurn](common_transactions.standardunsignedtx#getburn)
- [getCodecID](common_transactions.standardunsignedtx#getcodecid)
- [getCodecIDBuffer](common_transactions.standardunsignedtx#getcodecidbuffer)
- [getInputTotal](common_transactions.standardunsignedtx#getinputtotal)
- [getOutputTotal](common_transactions.standardunsignedtx#getoutputtotal)
- [getTransaction](common_transactions.standardunsignedtx#abstract-gettransaction)
- [getTypeID](common_transactions.standardunsignedtx#gettypeid)
- [getTypeName](common_transactions.standardunsignedtx#gettypename)
- [sanitizeObject](common_transactions.standardunsignedtx#sanitizeobject)
- [serialize](common_transactions.standardunsignedtx#serialize)
- [sign](common_transactions.standardunsignedtx#abstract-sign)
- [toBuffer](common_transactions.standardunsignedtx#tobuffer)

## Constructors

### constructor

\+ **new StandardUnsignedTx**(`transaction`: SBTx, `codecID`: number): _[StandardUnsignedTx](common_transactions.standardunsignedtx)_

_Defined in [src/common/tx.ts:359](https://github.com/chain4travel/caminojs/blob/3883166/src/common/tx.ts#L359)_

**Parameters:**

| Name          | Type   | Default   |
| ------------- | ------ | --------- |
| `transaction` | SBTx   | undefined |
| `codecID`     | number | 0         |

**Returns:** _[StandardUnsignedTx](common_transactions.standardunsignedtx)_

## Properties

### `Protected` \_codecID

• **\_codecID**: _number_ = undefined

_Inherited from [SigIdx](common_signature.sigidx).[\_codecID](common_signature.sigidx#protected-_codecid)_

_Defined in [src/utils/serialization.ts:51](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/serialization.ts#L51)_

---

### `Protected` \_typeID

• **\_typeID**: _any_ = undefined

_Overrides [Serializable](utils_serialization.serializable).[\_typeID](utils_serialization.serializable#protected-_typeid)_

_Defined in [src/common/tx.ts:231](https://github.com/chain4travel/caminojs/blob/3883166/src/common/tx.ts#L231)_

---

### `Protected` \_typeName

• **\_typeName**: _string_ = "StandardUnsignedTx"

_Overrides [Serializable](utils_serialization.serializable).[\_typeName](utils_serialization.serializable#protected-_typename)_

_Defined in [src/common/tx.ts:230](https://github.com/chain4travel/caminojs/blob/3883166/src/common/tx.ts#L230)_

---

### `Protected` codecID

• **codecID**: _number_ = 0

_Defined in [src/common/tx.ts:258](https://github.com/chain4travel/caminojs/blob/3883166/src/common/tx.ts#L258)_

---

### `Protected` transaction

• **transaction**: _SBTx_

_Defined in [src/common/tx.ts:259](https://github.com/chain4travel/caminojs/blob/3883166/src/common/tx.ts#L259)_

## Methods

### deserialize

▸ **deserialize**(`fields`: object, `encoding`: [SerializedEncoding](../modules/utils_serialization#serializedencoding)): _void_

_Overrides [StandardParseableInput](common_inputs.standardparseableinput).[deserialize](common_inputs.standardparseableinput#deserialize)_

_Defined in [src/common/tx.ts:248](https://github.com/chain4travel/caminojs/blob/3883166/src/common/tx.ts#L248)_

**Parameters:**

| Name       | Type                                                                    | Default |
| ---------- | ----------------------------------------------------------------------- | ------- |
| `fields`   | object                                                                  | -       |
| `encoding` | [SerializedEncoding](../modules/utils_serialization#serializedencoding) | "hex"   |

**Returns:** _void_

---

### `Abstract` fromBuffer

▸ **fromBuffer**(`bytes`: Buffer, `offset?`: number): _number_

_Defined in [src/common/tx.ts:336](https://github.com/chain4travel/caminojs/blob/3883166/src/common/tx.ts#L336)_

**Parameters:**

| Name      | Type   |
| --------- | ------ |
| `bytes`   | Buffer |
| `offset?` | number |

**Returns:** _number_

---

### getBurn

▸ **getBurn**(`assetID`: Buffer): _BN_

_Defined in [src/common/tx.ts:327](https://github.com/chain4travel/caminojs/blob/3883166/src/common/tx.ts#L327)_

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

_Defined in [src/common/tx.ts:264](https://github.com/chain4travel/caminojs/blob/3883166/src/common/tx.ts#L264)_

Returns the CodecID as a number

**Returns:** _number_

---

### getCodecIDBuffer

▸ **getCodecIDBuffer**(): _Buffer_

_Defined in [src/common/tx.ts:271](https://github.com/chain4travel/caminojs/blob/3883166/src/common/tx.ts#L271)_

Returns the [Buffer](https://github.com/feross/buffer) representation of the CodecID

**Returns:** _Buffer_

---

### getInputTotal

▸ **getInputTotal**(`assetID`: Buffer): _BN_

_Defined in [src/common/tx.ts:280](https://github.com/chain4travel/caminojs/blob/3883166/src/common/tx.ts#L280)_

Returns the inputTotal as a BN

**Parameters:**

| Name      | Type   |
| --------- | ------ |
| `assetID` | Buffer |

**Returns:** _BN_

---

### getOutputTotal

▸ **getOutputTotal**(`assetID`: Buffer): _BN_

_Defined in [src/common/tx.ts:303](https://github.com/chain4travel/caminojs/blob/3883166/src/common/tx.ts#L303)_

Returns the outputTotal as a BN

**Parameters:**

| Name      | Type   |
| --------- | ------ |
| `assetID` | Buffer |

**Returns:** _BN_

---

### `Abstract` getTransaction

▸ **getTransaction**(): _SBTx_

_Defined in [src/common/tx.ts:334](https://github.com/chain4travel/caminojs/blob/3883166/src/common/tx.ts#L334)_

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

_Defined in [src/common/tx.ts:233](https://github.com/chain4travel/caminojs/blob/3883166/src/common/tx.ts#L233)_

**Parameters:**

| Name       | Type                                                                    | Default |
| ---------- | ----------------------------------------------------------------------- | ------- |
| `encoding` | [SerializedEncoding](../modules/utils_serialization#serializedencoding) | "hex"   |

**Returns:** _object_

---

### `Abstract` sign

▸ **sign**(`kc`: KCClass): _[StandardTx](common_transactions.standardtx)‹KPClass, KCClass, [StandardUnsignedTx](common_transactions.standardunsignedtx)‹KPClass, KCClass, SBTx››_

_Defined in [src/common/tx.ts:357](https://github.com/chain4travel/caminojs/blob/3883166/src/common/tx.ts#L357)_

Signs this [UnsignedTx](api_evm_transactions.unsignedtx) and returns signed [StandardTx](common_transactions.standardtx)

**Parameters:**

| Name | Type    | Description                                              |
| ---- | ------- | -------------------------------------------------------- |
| `kc` | KCClass | An [KeyChain](api_evm_keychain.keychain) used in signing |

**Returns:** _[StandardTx](common_transactions.standardtx)‹KPClass, KCClass, [StandardUnsignedTx](common_transactions.standardunsignedtx)‹KPClass, KCClass, SBTx››_

A signed [StandardTx](common_transactions.standardtx)

---

### toBuffer

▸ **toBuffer**(): _Buffer_

_Defined in [src/common/tx.ts:338](https://github.com/chain4travel/caminojs/blob/3883166/src/common/tx.ts#L338)_

**Returns:** _Buffer_
