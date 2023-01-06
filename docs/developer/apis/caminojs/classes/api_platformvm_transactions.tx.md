# Class: Tx

## Hierarchy

↳ [StandardTx](common_transactions.standardtx)‹[KeyPair](api_platformvm_keychain.keypair), [KeyChain](api_platformvm_keychain.keychain), [UnsignedTx](api_platformvm_transactions.unsignedtx)›

↳ **Tx**

## Index

### Constructors

- [constructor](api_platformvm_transactions.tx#constructor)

### Properties

- [\_codecID](api_platformvm_transactions.tx#protected-_codecid)
- [\_typeID](api_platformvm_transactions.tx#protected-_typeid)
- [\_typeName](api_platformvm_transactions.tx#protected-_typename)
- [credentials](api_platformvm_transactions.tx#protected-credentials)
- [unsignedTx](api_platformvm_transactions.tx#protected-unsignedtx)

### Methods

- [deserialize](api_platformvm_transactions.tx#deserialize)
- [fromBuffer](api_platformvm_transactions.tx#frombuffer)
- [fromString](api_platformvm_transactions.tx#fromstring)
- [getCodecID](api_platformvm_transactions.tx#getcodecid)
- [getCredentials](api_platformvm_transactions.tx#getcredentials)
- [getTypeID](api_platformvm_transactions.tx#gettypeid)
- [getTypeName](api_platformvm_transactions.tx#gettypename)
- [getUnsignedTx](api_platformvm_transactions.tx#getunsignedtx)
- [sanitizeObject](api_platformvm_transactions.tx#sanitizeobject)
- [serialize](api_platformvm_transactions.tx#serialize)
- [toBuffer](api_platformvm_transactions.tx#tobuffer)
- [toString](api_platformvm_transactions.tx#tostring)
- [toStringHex](api_platformvm_transactions.tx#tostringhex)

## Constructors

### constructor

\+ **new Tx**(`unsignedTx`: [UnsignedTx](api_platformvm_transactions.unsignedtx), `credentials`: [Credential](common_signature.credential)[]): _[Tx](api_platformvm_transactions.tx)_

_Inherited from [StandardTx](common_transactions.standardtx).[constructor](common_transactions.standardtx#constructor)_

_Defined in [src/common/tx.ts:464](https://github.com/chain4travel/caminojs/blob/3883166/src/common/tx.ts#L464)_

Class representing a signed transaction.

**Parameters:**

| Name          | Type                                                 | Default   | Description                                                           |
| ------------- | ---------------------------------------------------- | --------- | --------------------------------------------------------------------- |
| `unsignedTx`  | [UnsignedTx](api_platformvm_transactions.unsignedtx) | undefined | Optional [StandardUnsignedTx](common_transactions.standardunsignedtx) |
| `credentials` | [Credential](common_signature.credential)[]          | undefined | -                                                                     |

**Returns:** _[Tx](api_platformvm_transactions.tx)_

## Properties

### `Protected` \_codecID

• **\_codecID**: _number_ = undefined

_Inherited from [SigIdx](common_signature.sigidx).[\_codecID](common_signature.sigidx#protected-_codecid)_

_Defined in [src/utils/serialization.ts:51](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/serialization.ts#L51)_

---

### `Protected` \_typeID

• **\_typeID**: _any_ = undefined

_Overrides [StandardTx](common_transactions.standardtx).[\_typeID](common_transactions.standardtx#protected-_typeid)_

_Defined in [src/apis/platformvm/tx.ts:97](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/tx.ts#L97)_

---

### `Protected` \_typeName

• **\_typeName**: _string_ = "Tx"

_Overrides [StandardTx](common_transactions.standardtx).[\_typeName](common_transactions.standardtx#protected-_typename)_

_Defined in [src/apis/platformvm/tx.ts:96](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/tx.ts#L96)_

---

### `Protected` credentials

• **credentials**: _[Credential](common_signature.credential)[]_ = []

_Inherited from [StandardTx](common_transactions.standardtx).[credentials](common_transactions.standardtx#protected-credentials)_

_Defined in [src/common/tx.ts:393](https://github.com/chain4travel/caminojs/blob/3883166/src/common/tx.ts#L393)_

---

### `Protected` unsignedTx

• **unsignedTx**: _[UnsignedTx](api_platformvm_transactions.unsignedtx)_ = undefined

_Inherited from [StandardTx](common_transactions.standardtx).[unsignedTx](common_transactions.standardtx#protected-unsignedtx)_

_Defined in [src/common/tx.ts:392](https://github.com/chain4travel/caminojs/blob/3883166/src/common/tx.ts#L392)_

## Methods

### deserialize

▸ **deserialize**(`fields`: object, `encoding`: [SerializedEncoding](../modules/utils_serialization#serializedencoding)): _void_

_Overrides [StandardParseableInput](common_inputs.standardparseableinput).[deserialize](common_inputs.standardparseableinput#deserialize)_

_Defined in [src/apis/platformvm/tx.ts:101](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/tx.ts#L101)_

**Parameters:**

| Name       | Type                                                                    | Default |
| ---------- | ----------------------------------------------------------------------- | ------- |
| `fields`   | object                                                                  | -       |
| `encoding` | [SerializedEncoding](../modules/utils_serialization#serializedencoding) | "hex"   |

**Returns:** _void_

---

### fromBuffer

▸ **fromBuffer**(`bytes`: Buffer, `offset`: number): _number_

_Overrides [StandardTx](common_transactions.standardtx).[fromBuffer](common_transactions.standardtx#abstract-frombuffer)_

_Defined in [src/apis/platformvm/tx.ts:123](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/tx.ts#L123)_

Takes a [Buffer](https://github.com/feross/buffer) containing an [Tx](api_platformvm_transactions.tx), parses it, populates the class, and returns the length of the Tx in bytes.

**Parameters:**

| Name     | Type   | Default | Description                                                                                        |
| -------- | ------ | ------- | -------------------------------------------------------------------------------------------------- |
| `bytes`  | Buffer | -       | A [Buffer](https://github.com/feross/buffer) containing a raw [Tx](api_platformvm_transactions.tx) |
| `offset` | number | 0       | A number representing the starting point of the bytes to begin parsing                             |

**Returns:** _number_

The length of the raw [Tx](api_platformvm_transactions.tx)

---

### fromString

▸ **fromString**(`serialized`: string): _number_

_Inherited from [StandardTx](common_transactions.standardtx).[fromString](common_transactions.standardtx#fromstring)_

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

_Inherited from [StandardTx](common_transactions.standardtx).[getCredentials](common_transactions.standardtx#getcredentials)_

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

▸ **getUnsignedTx**(): _[UnsignedTx](api_platformvm_transactions.unsignedtx)_

_Inherited from [StandardTx](common_transactions.standardtx).[getUnsignedTx](common_transactions.standardtx#getunsignedtx)_

_Defined in [src/common/tx.ts:405](https://github.com/chain4travel/caminojs/blob/3883166/src/common/tx.ts#L405)_

Returns the [StandardUnsignedTx](common_transactions.standardunsignedtx)

**Returns:** _[UnsignedTx](api_platformvm_transactions.unsignedtx)_

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

_Inherited from [StandardTx](common_transactions.standardtx).[serialize](common_transactions.standardtx#serialize)_

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

_Inherited from [StandardTx](common_transactions.standardtx).[toBuffer](common_transactions.standardtx#tobuffer)_

_Defined in [src/common/tx.ts:414](https://github.com/chain4travel/caminojs/blob/3883166/src/common/tx.ts#L414)_

Returns a [Buffer](https://github.com/feross/buffer) representation of the [StandardTx](common_transactions.standardtx).

**Returns:** _Buffer_

---

### toString

▸ **toString**(): _string_

_Inherited from [StandardTx](common_transactions.standardtx).[toString](common_transactions.standardtx#tostring)_

_Defined in [src/common/tx.ts:458](https://github.com/chain4travel/caminojs/blob/3883166/src/common/tx.ts#L458)_

Returns a cb58 representation of the [StandardTx](common_transactions.standardtx).

**`remarks`**
unlike most toStrings, this returns in cb58 serialization format

**Returns:** _string_

---

### toStringHex

▸ **toStringHex**(): _string_

_Inherited from [StandardTx](common_transactions.standardtx).[toStringHex](common_transactions.standardtx#tostringhex)_

_Defined in [src/common/tx.ts:462](https://github.com/chain4travel/caminojs/blob/3883166/src/common/tx.ts#L462)_

**Returns:** _string_
