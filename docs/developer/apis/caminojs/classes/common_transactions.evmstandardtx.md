# Class: EVMStandardTx ‹**KPClass, KCClass, SUBTx**›

Class representing a signed transaction.

## Type parameters

▪ **KPClass**: _[StandardKeyPair](common_keychain.standardkeypair)_

▪ **KCClass**: _[StandardKeyChain](common_keychain.standardkeychain)‹KPClass›_

▪ **SUBTx**: _[EVMStandardUnsignedTx](common_transactions.evmstandardunsignedtx)‹KPClass, KCClass, [EVMStandardBaseTx](common_transactions.evmstandardbasetx)‹KPClass, KCClass››_

## Hierarchy

- [Serializable](utils_serialization.serializable)

  ↳ **EVMStandardTx**

  ↳ [Tx](api_evm_transactions.tx)

## Index

### Constructors

- [constructor](common_transactions.evmstandardtx#constructor)

### Properties

- [\_codecID](common_transactions.evmstandardtx#protected-_codecid)
- [\_typeID](common_transactions.evmstandardtx#protected-_typeid)
- [\_typeName](common_transactions.evmstandardtx#protected-_typename)
- [credentials](common_transactions.evmstandardtx#protected-credentials)
- [unsignedTx](common_transactions.evmstandardtx#protected-unsignedtx)

### Methods

- [deserialize](common_transactions.evmstandardtx#deserialize)
- [fromBuffer](common_transactions.evmstandardtx#abstract-frombuffer)
- [fromString](common_transactions.evmstandardtx#fromstring)
- [getCodecID](common_transactions.evmstandardtx#getcodecid)
- [getTypeID](common_transactions.evmstandardtx#gettypeid)
- [getTypeName](common_transactions.evmstandardtx#gettypename)
- [getUnsignedTx](common_transactions.evmstandardtx#getunsignedtx)
- [sanitizeObject](common_transactions.evmstandardtx#sanitizeobject)
- [serialize](common_transactions.evmstandardtx#serialize)
- [toBuffer](common_transactions.evmstandardtx#tobuffer)
- [toString](common_transactions.evmstandardtx#tostring)
- [toStringHex](common_transactions.evmstandardtx#tostringhex)

## Constructors

### constructor

\+ **new EVMStandardTx**(`unsignedTx`: SUBTx, `credentials`: [Credential](common_signature.credential)[]): _[EVMStandardTx](common_transactions.evmstandardtx)_

_Defined in [src/common/evmtx.ts:365](https://github.com/chain4travel/caminojs/blob/3883166/src/common/evmtx.ts#L365)_

Class representing a signed transaction.

**Parameters:**

| Name          | Type                                        | Default   | Description                                                           |
| ------------- | ------------------------------------------- | --------- | --------------------------------------------------------------------- |
| `unsignedTx`  | SUBTx                                       | undefined | Optional [StandardUnsignedTx](common_transactions.standardunsignedtx) |
| `credentials` | [Credential](common_signature.credential)[] | undefined | -                                                                     |

**Returns:** _[EVMStandardTx](common_transactions.evmstandardtx)_

## Properties

### `Protected` \_codecID

• **\_codecID**: _number_ = undefined

_Inherited from [SigIdx](common_signature.sigidx).[\_codecID](common_signature.sigidx#protected-_codecid)_

_Defined in [src/utils/serialization.ts:51](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/serialization.ts#L51)_

---

### `Protected` \_typeID

• **\_typeID**: _any_ = undefined

_Overrides [Serializable](utils_serialization.serializable).[\_typeID](utils_serialization.serializable#protected-_typeid)_

_Defined in [src/common/evmtx.ts:293](https://github.com/chain4travel/caminojs/blob/3883166/src/common/evmtx.ts#L293)_

---

### `Protected` \_typeName

• **\_typeName**: _string_ = "StandardTx"

_Overrides [Serializable](utils_serialization.serializable).[\_typeName](utils_serialization.serializable#protected-_typename)_

_Defined in [src/common/evmtx.ts:292](https://github.com/chain4travel/caminojs/blob/3883166/src/common/evmtx.ts#L292)_

---

### `Protected` credentials

• **credentials**: _[Credential](common_signature.credential)[]_ = []

_Defined in [src/common/evmtx.ts:305](https://github.com/chain4travel/caminojs/blob/3883166/src/common/evmtx.ts#L305)_

---

### `Protected` unsignedTx

• **unsignedTx**: _SUBTx_ = undefined

_Defined in [src/common/evmtx.ts:304](https://github.com/chain4travel/caminojs/blob/3883166/src/common/evmtx.ts#L304)_

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

_Defined in [src/common/evmtx.ts:314](https://github.com/chain4travel/caminojs/blob/3883166/src/common/evmtx.ts#L314)_

**Parameters:**

| Name      | Type   |
| --------- | ------ |
| `bytes`   | Buffer |
| `offset?` | number |

**Returns:** _number_

---

### fromString

▸ **fromString**(`serialized`: string): _number_

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

▸ **getUnsignedTx**(): _SUBTx_

_Defined in [src/common/evmtx.ts:310](https://github.com/chain4travel/caminojs/blob/3883166/src/common/evmtx.ts#L310)_

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

_Defined in [src/common/evmtx.ts:295](https://github.com/chain4travel/caminojs/blob/3883166/src/common/evmtx.ts#L295)_

**Parameters:**

| Name       | Type                                                                    | Default |
| ---------- | ----------------------------------------------------------------------- | ------- |
| `encoding` | [SerializedEncoding](../modules/utils_serialization#serializedencoding) | "hex"   |

**Returns:** _object_

---

### toBuffer

▸ **toBuffer**(): _Buffer_

_Defined in [src/common/evmtx.ts:319](https://github.com/chain4travel/caminojs/blob/3883166/src/common/evmtx.ts#L319)_

Returns a [Buffer](https://github.com/feross/buffer) representation of the [StandardTx](common_transactions.standardtx).

**Returns:** _Buffer_

---

### toString

▸ **toString**(): _string_

_Defined in [src/common/evmtx.ts:359](https://github.com/chain4travel/caminojs/blob/3883166/src/common/evmtx.ts#L359)_

Returns a cb58 representation of the [StandardTx](common_transactions.standardtx).

**`remarks`**
unlike most toStrings, this returns in cb58 serialization format

**Returns:** _string_

---

### toStringHex

▸ **toStringHex**(): _string_

_Defined in [src/common/evmtx.ts:363](https://github.com/chain4travel/caminojs/blob/3883166/src/common/evmtx.ts#L363)_

**Returns:** _string_
