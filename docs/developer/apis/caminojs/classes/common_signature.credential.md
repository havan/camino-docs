# Class: Credential

## Hierarchy

- [Serializable](utils_serialization.serializable)

  ↳ **Credential**

  ↳ [SECPCredential](api_evm_credentials.secpcredential)

  ↳ [SECPCredential](api_avm_credentials.secpcredential)

  ↳ [NFTCredential](api_avm_credentials.nftcredential)

  ↳ [SECPCredential](api_platformvm_credentials.secpcredential)

## Index

### Constructors

- [constructor](common_signature.credential#constructor)

### Properties

- [\_codecID](common_signature.credential#protected-_codecid)
- [\_typeID](common_signature.credential#protected-_typeid)
- [\_typeName](common_signature.credential#protected-_typename)
- [sigArray](common_signature.credential#protected-sigarray)

### Methods

- [addSignature](common_signature.credential#addsignature)
- [clone](common_signature.credential#abstract-clone)
- [create](common_signature.credential#abstract-create)
- [deserialize](common_signature.credential#deserialize)
- [fromBuffer](common_signature.credential#frombuffer)
- [getCodecID](common_signature.credential#getcodecid)
- [getCredentialID](common_signature.credential#abstract-getcredentialid)
- [getTypeID](common_signature.credential#gettypeid)
- [getTypeName](common_signature.credential#gettypename)
- [sanitizeObject](common_signature.credential#sanitizeobject)
- [select](common_signature.credential#abstract-select)
- [serialize](common_signature.credential#serialize)
- [setCodecID](common_signature.credential#setcodecid)
- [toBuffer](common_signature.credential#tobuffer)

## Constructors

### constructor

\+ **new Credential**(`sigarray`: [Signature](common_signature.signature)[]): _[Credential](common_signature.credential)_

_Defined in [src/common/credentials.ts:176](https://github.com/chain4travel/caminojs/blob/3883166/src/common/credentials.ts#L176)_

**Parameters:**

| Name       | Type                                      | Default   |
| ---------- | ----------------------------------------- | --------- |
| `sigarray` | [Signature](common_signature.signature)[] | undefined |

**Returns:** _[Credential](common_signature.credential)_

## Properties

### `Protected` \_codecID

• **\_codecID**: _number_ = undefined

_Inherited from [SigIdx](common_signature.sigidx).[\_codecID](common_signature.sigidx#protected-_codecid)_

_Defined in [src/utils/serialization.ts:51](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/serialization.ts#L51)_

---

### `Protected` \_typeID

• **\_typeID**: _any_ = undefined

_Overrides [Serializable](utils_serialization.serializable).[\_typeID](utils_serialization.serializable#protected-_typeid)_

_Defined in [src/common/credentials.ts:110](https://github.com/chain4travel/caminojs/blob/3883166/src/common/credentials.ts#L110)_

---

### `Protected` \_typeName

• **\_typeName**: _string_ = "Credential"

_Overrides [Serializable](utils_serialization.serializable).[\_typeName](utils_serialization.serializable#protected-_typename)_

_Defined in [src/common/credentials.ts:109](https://github.com/chain4travel/caminojs/blob/3883166/src/common/credentials.ts#L109)_

---

### `Protected` sigArray

• **sigArray**: _[Signature](common_signature.signature)[]_ = []

_Defined in [src/common/credentials.ts:128](https://github.com/chain4travel/caminojs/blob/3883166/src/common/credentials.ts#L128)_

## Methods

### addSignature

▸ **addSignature**(`sig`: [Signature](common_signature.signature)): _number_

_Defined in [src/common/credentials.ts:142](https://github.com/chain4travel/caminojs/blob/3883166/src/common/credentials.ts#L142)_

Adds a signature to the credentials and returns the index off the added signature.

**Parameters:**

| Name  | Type                                    |
| ----- | --------------------------------------- |
| `sig` | [Signature](common_signature.signature) |

**Returns:** _number_

---

### `Abstract` clone

▸ **clone**(): _this_

_Defined in [src/common/credentials.ts:174](https://github.com/chain4travel/caminojs/blob/3883166/src/common/credentials.ts#L174)_

**Returns:** _this_

---

### `Abstract` create

▸ **create**(...`args`: any[]): _this_

_Defined in [src/common/credentials.ts:175](https://github.com/chain4travel/caminojs/blob/3883166/src/common/credentials.ts#L175)_

**Parameters:**

| Name      | Type  |
| --------- | ----- |
| `...args` | any[] |

**Returns:** _this_

---

### deserialize

▸ **deserialize**(`fields`: object, `encoding`: [SerializedEncoding](../modules/utils_serialization#serializedencoding)): _void_

_Overrides [StandardParseableInput](common_inputs.standardparseableinput).[deserialize](common_inputs.standardparseableinput#deserialize)_

_Defined in [src/common/credentials.ts:119](https://github.com/chain4travel/caminojs/blob/3883166/src/common/credentials.ts#L119)_

**Parameters:**

| Name       | Type                                                                    | Default |
| ---------- | ----------------------------------------------------------------------- | ------- |
| `fields`   | object                                                                  | -       |
| `encoding` | [SerializedEncoding](../modules/utils_serialization#serializedencoding) | "hex"   |

**Returns:** _void_

---

### fromBuffer

▸ **fromBuffer**(`bytes`: Buffer, `offset`: number): _number_

_Defined in [src/common/credentials.ts:147](https://github.com/chain4travel/caminojs/blob/3883166/src/common/credentials.ts#L147)_

**Parameters:**

| Name     | Type   | Default |
| -------- | ------ | ------- |
| `bytes`  | Buffer | -       |
| `offset` | number | 0       |

**Returns:** _number_

---

### getCodecID

▸ **getCodecID**(): _number_

_Inherited from [SigIdx](common_signature.sigidx).[getCodecID](common_signature.sigidx#getcodecid)_

_Defined in [src/utils/serialization.ts:70](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/serialization.ts#L70)_

Used in serialization. Optional. TypeID is a number for the typeID of object being output.

**Returns:** _number_

---

### `Abstract` getCredentialID

▸ **getCredentialID**(): _number_

_Defined in [src/common/credentials.ts:130](https://github.com/chain4travel/caminojs/blob/3883166/src/common/credentials.ts#L130)_

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

▸ **select**(`id`: number, ...`args`: any[]): _[Credential](common_signature.credential)_

_Defined in [src/common/credentials.ts:176](https://github.com/chain4travel/caminojs/blob/3883166/src/common/credentials.ts#L176)_

**Parameters:**

| Name      | Type   |
| --------- | ------ |
| `id`      | number |
| `...args` | any[]  |

**Returns:** _[Credential](common_signature.credential)_

---

### serialize

▸ **serialize**(`encoding`: [SerializedEncoding](../modules/utils_serialization#serializedencoding)): _object_

_Overrides [Serializable](utils_serialization.serializable).[serialize](utils_serialization.serializable#serialize)_

_Defined in [src/common/credentials.ts:112](https://github.com/chain4travel/caminojs/blob/3883166/src/common/credentials.ts#L112)_

**Parameters:**

| Name       | Type                                                                    | Default |
| ---------- | ----------------------------------------------------------------------- | ------- |
| `encoding` | [SerializedEncoding](../modules/utils_serialization#serializedencoding) | "hex"   |

**Returns:** _object_

---

### setCodecID

▸ **setCodecID**(`codecID`: number): _void_

_Defined in [src/common/credentials.ts:137](https://github.com/chain4travel/caminojs/blob/3883166/src/common/credentials.ts#L137)_

Set the codecID

**Parameters:**

| Name      | Type   | Description        |
| --------- | ------ | ------------------ |
| `codecID` | number | The codecID to set |

**Returns:** _void_

---

### toBuffer

▸ **toBuffer**(): _Buffer_

_Defined in [src/common/credentials.ts:161](https://github.com/chain4travel/caminojs/blob/3883166/src/common/credentials.ts#L161)_

**Returns:** _Buffer_
