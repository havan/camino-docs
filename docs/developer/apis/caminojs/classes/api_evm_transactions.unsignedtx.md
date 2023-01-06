# Class: UnsignedTx

## Hierarchy

↳ [EVMStandardUnsignedTx](common_transactions.evmstandardunsignedtx)‹[KeyPair](api_evm_keychain.keypair), [KeyChain](api_evm_keychain.keychain), [EVMBaseTx](api_evm_basetx.evmbasetx)›

↳ **UnsignedTx**

## Index

### Constructors

- [constructor](api_evm_transactions.unsignedtx#constructor)

### Properties

- [\_codecID](api_evm_transactions.unsignedtx#protected-_codecid)
- [\_typeID](api_evm_transactions.unsignedtx#protected-_typeid)
- [\_typeName](api_evm_transactions.unsignedtx#protected-_typename)
- [codecID](api_evm_transactions.unsignedtx#protected-codecid)
- [transaction](api_evm_transactions.unsignedtx#protected-transaction)

### Methods

- [deserialize](api_evm_transactions.unsignedtx#deserialize)
- [fromBuffer](api_evm_transactions.unsignedtx#frombuffer)
- [getBurn](api_evm_transactions.unsignedtx#getburn)
- [getCodecID](api_evm_transactions.unsignedtx#getcodecid)
- [getCodecIDBuffer](api_evm_transactions.unsignedtx#getcodecidbuffer)
- [getInputTotal](api_evm_transactions.unsignedtx#getinputtotal)
- [getOutputTotal](api_evm_transactions.unsignedtx#getoutputtotal)
- [getTransaction](api_evm_transactions.unsignedtx#gettransaction)
- [getTypeID](api_evm_transactions.unsignedtx#gettypeid)
- [getTypeName](api_evm_transactions.unsignedtx#gettypename)
- [sanitizeObject](api_evm_transactions.unsignedtx#sanitizeobject)
- [serialize](api_evm_transactions.unsignedtx#serialize)
- [sign](api_evm_transactions.unsignedtx#sign)
- [toBuffer](api_evm_transactions.unsignedtx#tobuffer)

## Constructors

### constructor

\+ **new UnsignedTx**(`transaction`: [EVMBaseTx](api_evm_basetx.evmbasetx), `codecID`: number): _[UnsignedTx](api_evm_transactions.unsignedtx)_

_Inherited from [EVMStandardUnsignedTx](common_transactions.evmstandardunsignedtx).[constructor](common_transactions.evmstandardunsignedtx#constructor)_

_Defined in [src/common/evmtx.ts:271](https://github.com/chain4travel/caminojs/blob/3883166/src/common/evmtx.ts#L271)_

**Parameters:**

| Name          | Type                                  | Default   |
| ------------- | ------------------------------------- | --------- |
| `transaction` | [EVMBaseTx](api_evm_basetx.evmbasetx) | undefined |
| `codecID`     | number                                | 0         |

**Returns:** _[UnsignedTx](api_evm_transactions.unsignedtx)_

## Properties

### `Protected` \_codecID

• **\_codecID**: _number_ = undefined

_Inherited from [SigIdx](common_signature.sigidx).[\_codecID](common_signature.sigidx#protected-_codecid)_

_Defined in [src/utils/serialization.ts:51](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/serialization.ts#L51)_

---

### `Protected` \_typeID

• **\_typeID**: _any_ = undefined

_Overrides [EVMStandardUnsignedTx](common_transactions.evmstandardunsignedtx).[\_typeID](common_transactions.evmstandardunsignedtx#protected-_typeid)_

_Defined in [src/apis/evm/tx.ts:48](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/tx.ts#L48)_

---

### `Protected` \_typeName

• **\_typeName**: _string_ = "UnsignedTx"

_Overrides [EVMStandardUnsignedTx](common_transactions.evmstandardunsignedtx).[\_typeName](common_transactions.evmstandardunsignedtx#protected-_typename)_

_Defined in [src/apis/evm/tx.ts:47](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/tx.ts#L47)_

---

### `Protected` codecID

• **codecID**: _number_ = 0

_Inherited from [EVMStandardUnsignedTx](common_transactions.evmstandardunsignedtx).[codecID](common_transactions.evmstandardunsignedtx#protected-codecid)_

_Defined in [src/common/evmtx.ts:172](https://github.com/chain4travel/caminojs/blob/3883166/src/common/evmtx.ts#L172)_

---

### `Protected` transaction

• **transaction**: _[EVMBaseTx](api_evm_basetx.evmbasetx)_

_Inherited from [EVMStandardUnsignedTx](common_transactions.evmstandardunsignedtx).[transaction](common_transactions.evmstandardunsignedtx#protected-transaction)_

_Defined in [src/common/evmtx.ts:173](https://github.com/chain4travel/caminojs/blob/3883166/src/common/evmtx.ts#L173)_

## Methods

### deserialize

▸ **deserialize**(`fields`: object, `encoding`: [SerializedEncoding](../modules/utils_serialization#serializedencoding)): _void_

_Overrides [EVMStandardUnsignedTx](common_transactions.evmstandardunsignedtx).[deserialize](common_transactions.evmstandardunsignedtx#deserialize)_

_Defined in [src/apis/evm/tx.ts:52](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/tx.ts#L52)_

**Parameters:**

| Name       | Type                                                                    | Default |
| ---------- | ----------------------------------------------------------------------- | ------- |
| `fields`   | object                                                                  | -       |
| `encoding` | [SerializedEncoding](../modules/utils_serialization#serializedencoding) | "hex"   |

**Returns:** _void_

---

### fromBuffer

▸ **fromBuffer**(`bytes`: Buffer, `offset`: number): _number_

_Overrides [EVMStandardUnsignedTx](common_transactions.evmstandardunsignedtx).[fromBuffer](common_transactions.evmstandardunsignedtx#abstract-frombuffer)_

_Defined in [src/apis/evm/tx.ts:62](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/tx.ts#L62)_

**Parameters:**

| Name     | Type   | Default |
| -------- | ------ | ------- |
| `bytes`  | Buffer | -       |
| `offset` | number | 0       |

**Returns:** _number_

---

### getBurn

▸ **getBurn**(`assetID`: Buffer): _BN_

_Inherited from [EVMStandardUnsignedTx](common_transactions.evmstandardunsignedtx).[getBurn](common_transactions.evmstandardunsignedtx#getburn)_

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

_Inherited from [EVMStandardUnsignedTx](common_transactions.evmstandardunsignedtx).[getCodecID](common_transactions.evmstandardunsignedtx#getcodecid)_

_Overrides [SigIdx](common_signature.sigidx).[getCodecID](common_signature.sigidx#getcodecid)_

_Defined in [src/common/evmtx.ts:178](https://github.com/chain4travel/caminojs/blob/3883166/src/common/evmtx.ts#L178)_

Returns the CodecID as a number

**Returns:** _number_

---

### getCodecIDBuffer

▸ **getCodecIDBuffer**(): _Buffer_

_Inherited from [EVMStandardUnsignedTx](common_transactions.evmstandardunsignedtx).[getCodecIDBuffer](common_transactions.evmstandardunsignedtx#getcodecidbuffer)_

_Defined in [src/common/evmtx.ts:185](https://github.com/chain4travel/caminojs/blob/3883166/src/common/evmtx.ts#L185)_

Returns the [Buffer](https://github.com/feross/buffer) representation of the CodecID

**Returns:** _Buffer_

---

### getInputTotal

▸ **getInputTotal**(`assetID`: Buffer): _BN_

_Inherited from [EVMStandardUnsignedTx](common_transactions.evmstandardunsignedtx).[getInputTotal](common_transactions.evmstandardunsignedtx#getinputtotal)_

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

_Inherited from [EVMStandardUnsignedTx](common_transactions.evmstandardunsignedtx).[getOutputTotal](common_transactions.evmstandardunsignedtx#getoutputtotal)_

_Defined in [src/common/evmtx.ts:214](https://github.com/chain4travel/caminojs/blob/3883166/src/common/evmtx.ts#L214)_

Returns the outputTotal as a BN

**Parameters:**

| Name      | Type   |
| --------- | ------ |
| `assetID` | Buffer |

**Returns:** _BN_

---

### getTransaction

▸ **getTransaction**(): _[EVMBaseTx](api_evm_basetx.evmbasetx)_

_Overrides [EVMStandardUnsignedTx](common_transactions.evmstandardunsignedtx).[getTransaction](common_transactions.evmstandardunsignedtx#abstract-gettransaction)_

_Defined in [src/apis/evm/tx.ts:58](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/tx.ts#L58)_

**Returns:** _[EVMBaseTx](api_evm_basetx.evmbasetx)_

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

_Inherited from [EVMStandardUnsignedTx](common_transactions.evmstandardunsignedtx).[serialize](common_transactions.evmstandardunsignedtx#serialize)_

_Overrides [Serializable](utils_serialization.serializable).[serialize](utils_serialization.serializable#serialize)_

_Defined in [src/common/evmtx.ts:147](https://github.com/chain4travel/caminojs/blob/3883166/src/common/evmtx.ts#L147)_

**Parameters:**

| Name       | Type                                                                    | Default |
| ---------- | ----------------------------------------------------------------------- | ------- |
| `encoding` | [SerializedEncoding](../modules/utils_serialization#serializedencoding) | "hex"   |

**Returns:** _object_

---

### sign

▸ **sign**(`kc`: [KeyChain](api_evm_keychain.keychain)): _[Tx](api_evm_transactions.tx)_

_Overrides [EVMStandardUnsignedTx](common_transactions.evmstandardunsignedtx).[sign](common_transactions.evmstandardunsignedtx#abstract-sign)_

_Defined in [src/apis/evm/tx.ts:80](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/tx.ts#L80)_

Signs this [UnsignedTx](api_evm_transactions.unsignedtx) and returns signed [StandardTx](common_transactions.standardtx)

**Parameters:**

| Name | Type                                  | Description                                              |
| ---- | ------------------------------------- | -------------------------------------------------------- |
| `kc` | [KeyChain](api_evm_keychain.keychain) | An [KeyChain](api_evm_keychain.keychain) used in signing |

**Returns:** _[Tx](api_evm_transactions.tx)_

A signed [StandardTx](common_transactions.standardtx)

---

### toBuffer

▸ **toBuffer**(): _Buffer_

_Inherited from [EVMStandardUnsignedTx](common_transactions.evmstandardunsignedtx).[toBuffer](common_transactions.evmstandardunsignedtx#tobuffer)_

_Defined in [src/common/evmtx.ts:247](https://github.com/chain4travel/caminojs/blob/3883166/src/common/evmtx.ts#L247)_

**Returns:** _Buffer_
