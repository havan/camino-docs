# Class: Tx

## Hierarchy

↳ [EVMStandardTx](common_transactions.evmstandardtx)‹[KeyPair](api_evm_keychain.keypair), [KeyChain](api_evm_keychain.keychain), [UnsignedTx](api_evm_transactions.unsignedtx)›

↳ **Tx**

## Index

### Constructors

- [constructor](api_evm_transactions.tx#constructor)

### Properties

- [\_codecID](api_evm_transactions.tx#protected-_codecid)
- [\_typeID](api_evm_transactions.tx#protected-_typeid)
- [\_typeName](api_evm_transactions.tx#protected-_typename)
- [credentials](api_evm_transactions.tx#protected-credentials)
- [unsignedTx](api_evm_transactions.tx#protected-unsignedtx)

### Methods

- [deserialize](api_evm_transactions.tx#deserialize)
- [fromBuffer](api_evm_transactions.tx#frombuffer)
- [fromString](api_evm_transactions.tx#fromstring)
- [getCodecID](api_evm_transactions.tx#getcodecid)
- [getTypeID](api_evm_transactions.tx#gettypeid)
- [getTypeName](api_evm_transactions.tx#gettypename)
- [getUnsignedTx](api_evm_transactions.tx#getunsignedtx)
- [sanitizeObject](api_evm_transactions.tx#sanitizeobject)
- [serialize](api_evm_transactions.tx#serialize)
- [toBuffer](api_evm_transactions.tx#tobuffer)
- [toString](api_evm_transactions.tx#tostring)
- [toStringHex](api_evm_transactions.tx#tostringhex)

## Constructors

### constructor

\+ **new Tx**(`unsignedTx`: [UnsignedTx](api_evm_transactions.unsignedtx), `credentials`: [Credential](common_signature.credential)[]): _[Tx](api_evm_transactions.tx)_

_Inherited from [EVMStandardTx](common_transactions.evmstandardtx).[constructor](common_transactions.evmstandardtx#constructor)_

_Defined in [src/common/evmtx.ts:365](https://github.com/chain4travel/caminojs/blob/3883166/src/common/evmtx.ts#L365)_

Class representing a signed transaction.

**Parameters:**

| Name          | Type                                          | Default   | Description                                                           |
| ------------- | --------------------------------------------- | --------- | --------------------------------------------------------------------- |
| `unsignedTx`  | [UnsignedTx](api_evm_transactions.unsignedtx) | undefined | Optional [StandardUnsignedTx](common_transactions.standardunsignedtx) |
| `credentials` | [Credential](common_signature.credential)[]   | undefined | -                                                                     |

**Returns:** _[Tx](api_evm_transactions.tx)_

## Properties

### `Protected` \_codecID

• **\_codecID**: _number_ = undefined

_Inherited from [SigIdx](common_signature.sigidx).[\_codecID](common_signature.sigidx#protected-_codecid)_

_Defined in [src/utils/serialization.ts:51](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/serialization.ts#L51)_

---

### `Protected` \_typeID

• **\_typeID**: _any_ = undefined

_Overrides [EVMStandardTx](common_transactions.evmstandardtx).[\_typeID](common_transactions.evmstandardtx#protected-_typeid)_

_Defined in [src/apis/evm/tx.ts:92](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/tx.ts#L92)_

---

### `Protected` \_typeName

• **\_typeName**: _string_ = "Tx"

_Overrides [EVMStandardTx](common_transactions.evmstandardtx).[\_typeName](common_transactions.evmstandardtx#protected-_typename)_

_Defined in [src/apis/evm/tx.ts:91](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/tx.ts#L91)_

---

### `Protected` credentials

• **credentials**: _[Credential](common_signature.credential)[]_ = []

_Inherited from [EVMStandardTx](common_transactions.evmstandardtx).[credentials](common_transactions.evmstandardtx#protected-credentials)_

_Defined in [src/common/evmtx.ts:305](https://github.com/chain4travel/caminojs/blob/3883166/src/common/evmtx.ts#L305)_

---

### `Protected` unsignedTx

• **unsignedTx**: _[UnsignedTx](api_evm_transactions.unsignedtx)_ = undefined

_Inherited from [EVMStandardTx](common_transactions.evmstandardtx).[unsignedTx](common_transactions.evmstandardtx#protected-unsignedtx)_

_Defined in [src/common/evmtx.ts:304](https://github.com/chain4travel/caminojs/blob/3883166/src/common/evmtx.ts#L304)_

## Methods

### deserialize

▸ **deserialize**(`fields`: object, `encoding`: [SerializedEncoding](../modules/utils_serialization#serializedencoding)): _void_

_Overrides [StandardParseableInput](common_inputs.standardparseableinput).[deserialize](common_inputs.standardparseableinput#deserialize)_

_Defined in [src/apis/evm/tx.ts:96](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/tx.ts#L96)_

**Parameters:**

| Name       | Type                                                                    | Default |
| ---------- | ----------------------------------------------------------------------- | ------- |
| `fields`   | object                                                                  | -       |
| `encoding` | [SerializedEncoding](../modules/utils_serialization#serializedencoding) | "hex"   |

**Returns:** _void_

---

### fromBuffer

▸ **fromBuffer**(`bytes`: Buffer, `offset`: number): _number_

_Overrides [EVMStandardTx](common_transactions.evmstandardtx).[fromBuffer](common_transactions.evmstandardtx#abstract-frombuffer)_

_Defined in [src/apis/evm/tx.ts:119](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/tx.ts#L119)_

Takes a [Buffer](https://github.com/feross/buffer) containing an [Tx](api_evm_transactions.tx), parses it,
populates the class, and returns the length of the Tx in bytes.

**Parameters:**

| Name     | Type   | Default | Description                                                                                 |
| -------- | ------ | ------- | ------------------------------------------------------------------------------------------- |
| `bytes`  | Buffer | -       | A [Buffer](https://github.com/feross/buffer) containing a raw [Tx](api_evm_transactions.tx) |
| `offset` | number | 0       | A number representing the starting point of the bytes to begin parsing                      |

**Returns:** _number_

The length of the raw [Tx](api_evm_transactions.tx)

---

### fromString

▸ **fromString**(`serialized`: string): _number_

_Inherited from [EVMStandardTx](common_transactions.evmstandardtx).[fromString](common_transactions.evmstandardtx#fromstring)_

_Defined in [src/common/evmtx.ts:349](https://github.com/chain4travel/caminojs/blob/3883166/src/common/evmtx.ts#L349)_

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

▸ **getUnsignedTx**(): _[UnsignedTx](api_evm_transactions.unsignedtx)_

_Inherited from [EVMStandardTx](common_transactions.evmstandardtx).[getUnsignedTx](common_transactions.evmstandardtx#getunsignedtx)_

_Defined in [src/common/evmtx.ts:310](https://github.com/chain4travel/caminojs/blob/3883166/src/common/evmtx.ts#L310)_

Returns the [StandardUnsignedTx](common_transactions.standardunsignedtx)

**Returns:** _[UnsignedTx](api_evm_transactions.unsignedtx)_

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

_Inherited from [EVMStandardTx](common_transactions.evmstandardtx).[serialize](common_transactions.evmstandardtx#serialize)_

_Overrides [Serializable](utils_serialization.serializable).[serialize](utils_serialization.serializable#serialize)_

_Defined in [src/common/evmtx.ts:295](https://github.com/chain4travel/caminojs/blob/3883166/src/common/evmtx.ts#L295)_

**Parameters:**

| Name       | Type                                                                    | Default |
| ---------- | ----------------------------------------------------------------------- | ------- |
| `encoding` | [SerializedEncoding](../modules/utils_serialization#serializedencoding) | "hex"   |

**Returns:** _object_

---

### toBuffer

▸ **toBuffer**(): _Buffer_

_Inherited from [EVMStandardTx](common_transactions.evmstandardtx).[toBuffer](common_transactions.evmstandardtx#tobuffer)_

_Defined in [src/common/evmtx.ts:319](https://github.com/chain4travel/caminojs/blob/3883166/src/common/evmtx.ts#L319)_

Returns a [Buffer](https://github.com/feross/buffer) representation of the [StandardTx](common_transactions.standardtx).

**Returns:** _Buffer_

---

### toString

▸ **toString**(): _string_

_Inherited from [EVMStandardTx](common_transactions.evmstandardtx).[toString](common_transactions.evmstandardtx#tostring)_

_Defined in [src/common/evmtx.ts:359](https://github.com/chain4travel/caminojs/blob/3883166/src/common/evmtx.ts#L359)_

Returns a cb58 representation of the [StandardTx](common_transactions.standardtx).

**`remarks`**
unlike most toStrings, this returns in cb58 serialization format

**Returns:** _string_

---

### toStringHex

▸ **toStringHex**(): _string_

_Inherited from [EVMStandardTx](common_transactions.evmstandardtx).[toStringHex](common_transactions.evmstandardtx#tostringhex)_

_Defined in [src/common/evmtx.ts:363](https://github.com/chain4travel/caminojs/blob/3883166/src/common/evmtx.ts#L363)_

**Returns:** _string_
