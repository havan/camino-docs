# Class: NFTCredential

## Hierarchy

↳ [Credential](common_signature.credential)

↳ **NFTCredential**

## Index

### Constructors

- [constructor](api_avm_credentials.nftcredential#constructor)

### Properties

- [\_codecID](api_avm_credentials.nftcredential#protected-_codecid)
- [\_typeID](api_avm_credentials.nftcredential#protected-_typeid)
- [\_typeName](api_avm_credentials.nftcredential#protected-_typename)
- [sigArray](api_avm_credentials.nftcredential#protected-sigarray)

### Methods

- [addSignature](api_avm_credentials.nftcredential#addsignature)
- [clone](api_avm_credentials.nftcredential#clone)
- [create](api_avm_credentials.nftcredential#create)
- [deserialize](api_avm_credentials.nftcredential#deserialize)
- [fromBuffer](api_avm_credentials.nftcredential#frombuffer)
- [getCodecID](api_avm_credentials.nftcredential#getcodecid)
- [getCredentialID](api_avm_credentials.nftcredential#getcredentialid)
- [getTypeID](api_avm_credentials.nftcredential#gettypeid)
- [getTypeName](api_avm_credentials.nftcredential#gettypename)
- [sanitizeObject](api_avm_credentials.nftcredential#sanitizeobject)
- [select](api_avm_credentials.nftcredential#select)
- [serialize](api_avm_credentials.nftcredential#serialize)
- [setCodecID](api_avm_credentials.nftcredential#setcodecid)
- [toBuffer](api_avm_credentials.nftcredential#tobuffer)

## Constructors

### constructor

\+ **new NFTCredential**(`sigarray`: [Signature](common_signature.signature)[]): _[NFTCredential](api_avm_credentials.nftcredential)_

_Inherited from [Credential](common_signature.credential).[constructor](common_signature.credential#constructor)_

_Defined in [src/common/credentials.ts:176](https://github.com/chain4travel/caminojs/blob/3883166/src/common/credentials.ts#L176)_

**Parameters:**

| Name       | Type                                      | Default   |
| ---------- | ----------------------------------------- | --------- |
| `sigarray` | [Signature](common_signature.signature)[] | undefined |

**Returns:** _[NFTCredential](api_avm_credentials.nftcredential)_

## Properties

### `Protected` \_codecID

• **\_codecID**: _number_ = AVMConstants.LATESTCODEC

_Overrides [SigIdx](common_signature.sigidx).[\_codecID](common_signature.sigidx#protected-_codecid)_

_Defined in [src/apis/avm/credentials.ts:88](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/credentials.ts#L88)_

---

### `Protected` \_typeID

• **\_typeID**: _number_ = this.\_codecID === 0
? AVMConstants.NFTCREDENTIAL
: AVMConstants.NFTCREDENTIAL_CODECONE

_Overrides [Credential](common_signature.credential).[\_typeID](common_signature.credential#protected-_typeid)_

_Defined in [src/apis/avm/credentials.ts:89](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/credentials.ts#L89)_

---

### `Protected` \_typeName

• **\_typeName**: _string_ = "NFTCredential"

_Overrides [Credential](common_signature.credential).[\_typeName](common_signature.credential#protected-_typename)_

_Defined in [src/apis/avm/credentials.ts:87](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/credentials.ts#L87)_

---

### `Protected` sigArray

• **sigArray**: _[Signature](common_signature.signature)[]_ = []

_Inherited from [Credential](common_signature.credential).[sigArray](common_signature.credential#protected-sigarray)_

_Defined in [src/common/credentials.ts:128](https://github.com/chain4travel/caminojs/blob/3883166/src/common/credentials.ts#L128)_

## Methods

### addSignature

▸ **addSignature**(`sig`: [Signature](common_signature.signature)): _number_

_Inherited from [Credential](common_signature.credential).[addSignature](common_signature.credential#addsignature)_

_Defined in [src/common/credentials.ts:142](https://github.com/chain4travel/caminojs/blob/3883166/src/common/credentials.ts#L142)_

Adds a signature to the credentials and returns the index off the added signature.

**Parameters:**

| Name  | Type                                    |
| ----- | --------------------------------------- |
| `sig` | [Signature](common_signature.signature) |

**Returns:** _number_

---

### clone

▸ **clone**(): _this_

_Overrides [Credential](common_signature.credential).[clone](common_signature.credential#abstract-clone)_

_Defined in [src/apis/avm/credentials.ts:119](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/credentials.ts#L119)_

**Returns:** _this_

---

### create

▸ **create**(...`args`: any[]): _this_

_Overrides [Credential](common_signature.credential).[create](common_signature.credential#abstract-create)_

_Defined in [src/apis/avm/credentials.ts:125](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/credentials.ts#L125)_

**Parameters:**

| Name      | Type  |
| --------- | ----- |
| `...args` | any[] |

**Returns:** _this_

---

### deserialize

▸ **deserialize**(`fields`: object, `encoding`: [SerializedEncoding](../modules/utils_serialization#serializedencoding)): _void_

_Inherited from [Credential](common_signature.credential).[deserialize](common_signature.credential#deserialize)_

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

_Inherited from [Credential](common_signature.credential).[fromBuffer](common_signature.credential#frombuffer)_

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

### getCredentialID

▸ **getCredentialID**(): _number_

_Overrides [Credential](common_signature.credential).[getCredentialID](common_signature.credential#abstract-getcredentialid)_

_Defined in [src/apis/avm/credentials.ts:115](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/credentials.ts#L115)_

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

### select

▸ **select**(`id`: number, ...`args`: any[]): _[Credential](common_signature.credential)_

_Overrides [Credential](common_signature.credential).[select](common_signature.credential#abstract-select)_

_Defined in [src/apis/avm/credentials.ts:129](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/credentials.ts#L129)_

**Parameters:**

| Name      | Type   |
| --------- | ------ |
| `id`      | number |
| `...args` | any[]  |

**Returns:** _[Credential](common_signature.credential)_

---

### serialize

▸ **serialize**(`encoding`: [SerializedEncoding](../modules/utils_serialization#serializedencoding)): _object_

_Inherited from [Credential](common_signature.credential).[serialize](common_signature.credential#serialize)_

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

_Overrides [Credential](common_signature.credential).[setCodecID](common_signature.credential#setcodecid)_

_Defined in [src/apis/avm/credentials.ts:101](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/credentials.ts#L101)_

Set the codecID

**Parameters:**

| Name      | Type   | Description        |
| --------- | ------ | ------------------ |
| `codecID` | number | The codecID to set |

**Returns:** _void_

---

### toBuffer

▸ **toBuffer**(): _Buffer_

_Inherited from [Credential](common_signature.credential).[toBuffer](common_signature.credential#tobuffer)_

_Defined in [src/common/credentials.ts:161](https://github.com/chain4travel/caminojs/blob/3883166/src/common/credentials.ts#L161)_

**Returns:** _Buffer_
