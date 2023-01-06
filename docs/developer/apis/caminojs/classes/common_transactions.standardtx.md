# Class: StandardTx ‹**KPClass, KCClass, SUBTx**›

Class representing a signed transaction.

## Type parameters

▪ **KPClass**: _[StandardKeyPair](common_keychain.standardkeypair)_

▪ **KCClass**: _[StandardKeyChain](common_keychain.standardkeychain)‹KPClass›_

▪ **SUBTx**: _[StandardUnsignedTx](common_transactions.standardunsignedtx)‹KPClass, KCClass, [StandardBaseTx](common_transactions.standardbasetx)‹KPClass, KCClass››_

## Hierarchy

- [Serializable](utils_serialization.serializable)

  ↳ **StandardTx**

  ↳ [Tx](api_avm_transactions.tx)

  ↳ [Tx](api_platformvm_transactions.tx)

## Index

### Constructors

- [constructor](common_transactions.standardtx#constructor)

### Properties

- [\_codecID](common_transactions.standardtx#protected-_codecid)
- [\_typeID](common_transactions.standardtx#protected-_typeid)
- [\_typeName](common_transactions.standardtx#protected-_typename)
- [credentials](common_transactions.standardtx#protected-credentials)
- [unsignedTx](common_transactions.standardtx#protected-unsignedtx)

### Methods

- [deserialize](common_transactions.standardtx#deserialize)
- [fromBuffer](common_transactions.standardtx#abstract-frombuffer)
- [fromString](common_transactions.standardtx#fromstring)
- [getCodecID](common_transactions.standardtx#getcodecid)
- [getCredentials](common_transactions.standardtx#getcredentials)
- [getTypeID](common_transactions.standardtx#gettypeid)
- [getTypeName](common_transactions.standardtx#gettypename)
- [getUnsignedTx](common_transactions.standardtx#getunsignedtx)
- [sanitizeObject](common_transactions.standardtx#sanitizeobject)
- [serialize](common_transactions.standardtx#serialize)
- [toBuffer](common_transactions.standardtx#tobuffer)
- [toString](common_transactions.standardtx#tostring)
- [toStringHex](common_transactions.standardtx#tostringhex)

## Constructors

### constructor

\+ **new StandardTx**(`unsignedTx`: SUBTx, `credentials`: [Credential](common_signature.credential)[]): _[StandardTx](common_transactions.standardtx)_

_Defined in [src/common/tx.ts:464](https://github.com/chain4travel/caminojs/blob/3883166/src/common/tx.ts#L464)_

Class representing a signed transaction.

**Parameters:**

| Name          | Type                                        | Default   | Description                                                           |
| ------------- | ------------------------------------------- | --------- | --------------------------------------------------------------------- |
| `unsignedTx`  | SUBTx                                       | undefined | Optional [StandardUnsignedTx](common_transactions.standardunsignedtx) |
| `credentials` | [Credential](common_signature.credential)[] | undefined | -                                                                     |

**Returns:** _[StandardTx](common_transactions.standardtx)_

## Properties

### `Protected` \_codecID

• **\_codecID**: _number_ = undefined

_Inherited from [SigIdx](common_signature.sigidx).[\_codecID](common_signature.sigidx#protected-_codecid)_

_Defined in [src/utils/serialization.ts:51](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/serialization.ts#L51)_

---

### `Protected` \_typeID

• **\_typeID**: _any_ = undefined

_Overrides [Serializable](utils_serialization.serializable).[\_typeID](utils_serialization.serializable#protected-_typeid)_

_Defined in [src/common/tx.ts:381](https://github.com/chain4travel/caminojs/blob/3883166/src/common/tx.ts#L381)_

---

### `Protected` \_typeName

• **\_typeName**: _string_ = "StandardTx"

_Overrides [Serializable](utils_serialization.serializable).[\_typeName](utils_serialization.serializable#protected-_typename)_

_Defined in [src/common/tx.ts:380](https://github.com/chain4travel/caminojs/blob/3883166/src/common/tx.ts#L380)_

---

### `Protected` credentials

• **credentials**: _[Credential](common_signature.credential)[]_ = []

_Defined in [src/common/tx.ts:393](https://github.com/chain4travel/caminojs/blob/3883166/src/common/tx.ts#L393)_

---

### `Protected` unsignedTx

• **unsignedTx**: _SUBTx_ = undefined

_Defined in [src/common/tx.ts:392](https://github.com/chain4travel/caminojs/blob/3883166/src/common/tx.ts#L392)_

## Methods

### deserialize

▸ **deserialize**(`fields`: object, `encoding?`: [SerializedEncoding](../modules/utils_serialization#serializedencoding)): _void_

_Inherited from [StandardParseableInput](common_inputs.standardparseableinput).[deserialize](common_inputs.standardparseableinput#deserialize)_

_Defined in [src/utils/serialization.ts:97](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/serialization.ts#L97)_

**Parameters:**

| Name        | Type                                                                    |
| ----------- | ----------------------------------------------------------------------- |
| `fields`    | object                                                                  |
| `encoding?` | [SerializedEncoding](../modules/utils_serialization#serializedencoding) |

**Returns:** _void_

---

### `Abstract` fromBuffer

▸ **fromBuffer**(`bytes`: Buffer, `offset?`: number): _number_

_Defined in [src/common/tx.ts:409](https://github.com/chain4travel/caminojs/blob/3883166/src/common/tx.ts#L409)_

**Parameters:**

| Name      | Type   |
| --------- | ------ |
| `bytes`   | Buffer |
| `offset?` | number |

**Returns:** _number_

---

### fromString

▸ **fromString**(`serialized`: string): _number_

_Defined in [src/common/tx.ts:448](https://github.com/chain4travel/caminojs/blob/3883166/src/common/tx.ts#L448)_

Takes a base-58 string containing an [StandardTx](common_transactions.standardtx), parses it, populates the class, and returns the length of the Tx in bytes.

**`remarks`**
unlike most fromStrings, it expects the string to be serialized in cb58 format

**Parameters:**

| Name         | Type   | Description                                                                    |
| ------------ | ------ | ------------------------------------------------------------------------------ |
| `serialized` | string | A base-58 string containing a raw [StandardTx](common_transactions.standardtx) |

**Returns:** _number_

The length of the raw [StandardTx](common_transactions.standardtx)

---

### getCodecID

▸ **getCodecID**(): _number_

_Inherited from [SigIdx](common_signature.sigidx).[getCodecID](common_signature.sigidx#getcodecid)_

_Defined in [src/utils/serialization.ts:70](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/serialization.ts#L70)_

Used in serialization. Optional. TypeID is a number for the typeID of object being output.

**Returns:** _number_

---

### getCredentials

▸ **getCredentials**(): _[Credential](common_signature.credential)[]_

_Defined in [src/common/tx.ts:398](https://github.com/chain4travel/caminojs/blob/3883166/src/common/tx.ts#L398)_

Returns the [[Credential[]]]

**Returns:** _[Credential](common_signature.credential)[]_

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

### getUnsignedTx

▸ **getUnsignedTx**(): _SUBTx_

_Defined in [src/common/tx.ts:405](https://github.com/chain4travel/caminojs/blob/3883166/src/common/tx.ts#L405)_

Returns the [StandardUnsignedTx](common_transactions.standardunsignedtx)

**Returns:** _SUBTx_

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

_Defined in [src/common/tx.ts:383](https://github.com/chain4travel/caminojs/blob/3883166/src/common/tx.ts#L383)_

**Parameters:**

| Name       | Type                                                                    | Default |
| ---------- | ----------------------------------------------------------------------- | ------- |
| `encoding` | [SerializedEncoding](../modules/utils_serialization#serializedencoding) | "hex"   |

**Returns:** _object_

---

### toBuffer

▸ **toBuffer**(): _Buffer_

_Defined in [src/common/tx.ts:414](https://github.com/chain4travel/caminojs/blob/3883166/src/common/tx.ts#L414)_

Returns a [Buffer](https://github.com/feross/buffer) representation of the [StandardTx](common_transactions.standardtx).

**Returns:** _Buffer_

---

### toString

▸ **toString**(): _string_

_Defined in [src/common/tx.ts:458](https://github.com/chain4travel/caminojs/blob/3883166/src/common/tx.ts#L458)_

Returns a cb58 representation of the [StandardTx](common_transactions.standardtx).

**`remarks`**
unlike most toStrings, this returns in cb58 serialization format

**Returns:** _string_

---

### toStringHex

▸ **toStringHex**(): _string_

_Defined in [src/common/tx.ts:462](https://github.com/chain4travel/caminojs/blob/3883166/src/common/tx.ts#L462)_

**Returns:** _string_
