# Class: UnsignedTx

## Hierarchy

↳ [StandardUnsignedTx](common_transactions.standardunsignedtx)‹[KeyPair](api_platformvm_keychain.keypair), [KeyChain](api_platformvm_keychain.keychain), [BaseTx](api_platformvm_basetx.basetx)›

↳ **UnsignedTx**

## Index

### Constructors

- [constructor](api_platformvm_transactions.unsignedtx#constructor)

### Properties

- [\_codecID](api_platformvm_transactions.unsignedtx#protected-_codecid)
- [\_typeID](api_platformvm_transactions.unsignedtx#protected-_typeid)
- [\_typeName](api_platformvm_transactions.unsignedtx#protected-_typename)
- [codecID](api_platformvm_transactions.unsignedtx#protected-codecid)
- [transaction](api_platformvm_transactions.unsignedtx#protected-transaction)

### Methods

- [deserialize](api_platformvm_transactions.unsignedtx#deserialize)
- [fromBuffer](api_platformvm_transactions.unsignedtx#frombuffer)
- [getBurn](api_platformvm_transactions.unsignedtx#getburn)
- [getCodecID](api_platformvm_transactions.unsignedtx#getcodecid)
- [getCodecIDBuffer](api_platformvm_transactions.unsignedtx#getcodecidbuffer)
- [getInputTotal](api_platformvm_transactions.unsignedtx#getinputtotal)
- [getOutputTotal](api_platformvm_transactions.unsignedtx#getoutputtotal)
- [getTransaction](api_platformvm_transactions.unsignedtx#gettransaction)
- [getTypeID](api_platformvm_transactions.unsignedtx#gettypeid)
- [getTypeName](api_platformvm_transactions.unsignedtx#gettypename)
- [sanitizeObject](api_platformvm_transactions.unsignedtx#sanitizeobject)
- [serialize](api_platformvm_transactions.unsignedtx#serialize)
- [sign](api_platformvm_transactions.unsignedtx#sign)
- [toBuffer](api_platformvm_transactions.unsignedtx#tobuffer)

## Constructors

### constructor

\+ **new UnsignedTx**(`transaction`: [BaseTx](api_platformvm_basetx.basetx), `codecID`: number): _[UnsignedTx](api_platformvm_transactions.unsignedtx)_

_Inherited from [StandardUnsignedTx](common_transactions.standardunsignedtx).[constructor](common_transactions.standardunsignedtx#constructor)_

_Defined in [src/common/tx.ts:359](https://github.com/chain4travel/caminojs/blob/3883166/src/common/tx.ts#L359)_

**Parameters:**

| Name          | Type                                   | Default   |
| ------------- | -------------------------------------- | --------- |
| `transaction` | [BaseTx](api_platformvm_basetx.basetx) | undefined |
| `codecID`     | number                                 | 0         |

**Returns:** _[UnsignedTx](api_platformvm_transactions.unsignedtx)_

## Properties

### `Protected` \_codecID

• **\_codecID**: _number_ = undefined

_Inherited from [SigIdx](common_signature.sigidx).[\_codecID](common_signature.sigidx#protected-_codecid)_

_Defined in [src/utils/serialization.ts:51](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/serialization.ts#L51)_

---

### `Protected` \_typeID

• **\_typeID**: _any_ = undefined

_Overrides [StandardUnsignedTx](common_transactions.standardunsignedtx).[\_typeID](common_transactions.standardunsignedtx#protected-_typeid)_

_Defined in [src/apis/platformvm/tx.ts:53](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/tx.ts#L53)_

---

### `Protected` \_typeName

• **\_typeName**: _string_ = "UnsignedTx"

_Overrides [StandardUnsignedTx](common_transactions.standardunsignedtx).[\_typeName](common_transactions.standardunsignedtx#protected-_typename)_

_Defined in [src/apis/platformvm/tx.ts:52](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/tx.ts#L52)_

---

### `Protected` codecID

• **codecID**: _number_ = 0

_Inherited from [StandardUnsignedTx](common_transactions.standardunsignedtx).[codecID](common_transactions.standardunsignedtx#protected-codecid)_

_Defined in [src/common/tx.ts:258](https://github.com/chain4travel/caminojs/blob/3883166/src/common/tx.ts#L258)_

---

### `Protected` transaction

• **transaction**: _[BaseTx](api_platformvm_basetx.basetx)_

_Inherited from [StandardUnsignedTx](common_transactions.standardunsignedtx).[transaction](common_transactions.standardunsignedtx#protected-transaction)_

_Defined in [src/common/tx.ts:259](https://github.com/chain4travel/caminojs/blob/3883166/src/common/tx.ts#L259)_

## Methods

### deserialize

▸ **deserialize**(`fields`: object, `encoding`: [SerializedEncoding](../modules/utils_serialization#serializedencoding)): _void_

_Overrides [StandardUnsignedTx](common_transactions.standardunsignedtx).[deserialize](common_transactions.standardunsignedtx#deserialize)_

_Defined in [src/apis/platformvm/tx.ts:57](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/tx.ts#L57)_

**Parameters:**

| Name       | Type                                                                    | Default |
| ---------- | ----------------------------------------------------------------------- | ------- |
| `fields`   | object                                                                  | -       |
| `encoding` | [SerializedEncoding](../modules/utils_serialization#serializedencoding) | "hex"   |

**Returns:** _void_

---

### fromBuffer

▸ **fromBuffer**(`bytes`: Buffer, `offset`: number): _number_

_Overrides [StandardUnsignedTx](common_transactions.standardunsignedtx).[fromBuffer](common_transactions.standardunsignedtx#abstract-frombuffer)_

_Defined in [src/apis/platformvm/tx.ts:67](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/tx.ts#L67)_

**Parameters:**

| Name     | Type   | Default |
| -------- | ------ | ------- |
| `bytes`  | Buffer | -       |
| `offset` | number | 0       |

**Returns:** _number_

---

### getBurn

▸ **getBurn**(`assetID`: Buffer): _BN_

_Inherited from [StandardUnsignedTx](common_transactions.standardunsignedtx).[getBurn](common_transactions.standardunsignedtx#getburn)_

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

_Inherited from [StandardUnsignedTx](common_transactions.standardunsignedtx).[getCodecID](common_transactions.standardunsignedtx#getcodecid)_

_Overrides [SigIdx](common_signature.sigidx).[getCodecID](common_signature.sigidx#getcodecid)_

_Defined in [src/common/tx.ts:264](https://github.com/chain4travel/caminojs/blob/3883166/src/common/tx.ts#L264)_

Returns the CodecID as a number

**Returns:** _number_

---

### getCodecIDBuffer

▸ **getCodecIDBuffer**(): _Buffer_

_Inherited from [StandardUnsignedTx](common_transactions.standardunsignedtx).[getCodecIDBuffer](common_transactions.standardunsignedtx#getcodecidbuffer)_

_Defined in [src/common/tx.ts:271](https://github.com/chain4travel/caminojs/blob/3883166/src/common/tx.ts#L271)_

Returns the [Buffer](https://github.com/feross/buffer) representation of the CodecID

**Returns:** _Buffer_

---

### getInputTotal

▸ **getInputTotal**(`assetID`: Buffer): _BN_

_Inherited from [StandardUnsignedTx](common_transactions.standardunsignedtx).[getInputTotal](common_transactions.standardunsignedtx#getinputtotal)_

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

_Inherited from [StandardUnsignedTx](common_transactions.standardunsignedtx).[getOutputTotal](common_transactions.standardunsignedtx#getoutputtotal)_

_Defined in [src/common/tx.ts:303](https://github.com/chain4travel/caminojs/blob/3883166/src/common/tx.ts#L303)_

Returns the outputTotal as a BN

**Parameters:**

| Name      | Type   |
| --------- | ------ |
| `assetID` | Buffer |

**Returns:** _BN_

---

### getTransaction

▸ **getTransaction**(): _[BaseTx](api_platformvm_basetx.basetx)_

_Overrides [StandardUnsignedTx](common_transactions.standardunsignedtx).[getTransaction](common_transactions.standardunsignedtx#abstract-gettransaction)_

_Defined in [src/apis/platformvm/tx.ts:63](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/tx.ts#L63)_

**Returns:** _[BaseTx](api_platformvm_basetx.basetx)_

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

_Inherited from [StandardUnsignedTx](common_transactions.standardunsignedtx).[serialize](common_transactions.standardunsignedtx#serialize)_

_Overrides [Serializable](utils_serialization.serializable).[serialize](utils_serialization.serializable#serialize)_

_Defined in [src/common/tx.ts:233](https://github.com/chain4travel/caminojs/blob/3883166/src/common/tx.ts#L233)_

**Parameters:**

| Name       | Type                                                                    | Default |
| ---------- | ----------------------------------------------------------------------- | ------- |
| `encoding` | [SerializedEncoding](../modules/utils_serialization#serializedencoding) | "hex"   |

**Returns:** _object_

---

### sign

▸ **sign**(`kc`: [KeyChain](api_platformvm_keychain.keychain)): _[Tx](api_platformvm_transactions.tx)_

_Overrides [StandardUnsignedTx](common_transactions.standardunsignedtx).[sign](common_transactions.standardunsignedtx#abstract-sign)_

_Defined in [src/apis/platformvm/tx.ts:85](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/tx.ts#L85)_

Signs this [UnsignedTx](api_platformvm_transactions.unsignedtx) and returns signed [StandardTx](common_transactions.standardtx)

**Parameters:**

| Name | Type                                         | Description                                              |
| ---- | -------------------------------------------- | -------------------------------------------------------- |
| `kc` | [KeyChain](api_platformvm_keychain.keychain) | An [KeyChain](api_evm_keychain.keychain) used in signing |

**Returns:** _[Tx](api_platformvm_transactions.tx)_

A signed [StandardTx](common_transactions.standardtx)

---

### toBuffer

▸ **toBuffer**(): _Buffer_

_Inherited from [StandardUnsignedTx](common_transactions.standardunsignedtx).[toBuffer](common_transactions.standardunsignedtx#tobuffer)_

_Defined in [src/common/tx.ts:338](https://github.com/chain4travel/caminojs/blob/3883166/src/common/tx.ts#L338)_

**Returns:** _Buffer_
