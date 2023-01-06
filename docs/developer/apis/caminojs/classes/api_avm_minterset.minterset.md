# Class: MinterSet

Class for representing a threshold and set of minting addresses in Avalanche.

**`typeparam`** including a threshold and array of addresses

## Hierarchy

- [Serializable](utils_serialization.serializable)

  ↳ **MinterSet**

## Index

### Constructors

- [constructor](api_avm_minterset.minterset#constructor)

### Properties

- [\_codecID](api_avm_minterset.minterset#protected-_codecid)
- [\_typeID](api_avm_minterset.minterset#protected-_typeid)
- [\_typeName](api_avm_minterset.minterset#protected-_typename)
- [minters](api_avm_minterset.minterset#protected-minters)
- [threshold](api_avm_minterset.minterset#protected-threshold)

### Methods

- [\_cleanAddresses](api_avm_minterset.minterset#protected-_cleanaddresses)
- [deserialize](api_avm_minterset.minterset#deserialize)
- [getCodecID](api_avm_minterset.minterset#getcodecid)
- [getMinters](api_avm_minterset.minterset#getminters)
- [getThreshold](api_avm_minterset.minterset#getthreshold)
- [getTypeID](api_avm_minterset.minterset#gettypeid)
- [getTypeName](api_avm_minterset.minterset#gettypename)
- [sanitizeObject](api_avm_minterset.minterset#sanitizeobject)
- [serialize](api_avm_minterset.minterset#serialize)

## Constructors

### constructor

\+ **new MinterSet**(`threshold`: number, `minters`: string[] | Buffer[]): _[MinterSet](api_avm_minterset.minterset)_

_Defined in [src/apis/avm/minterset.ts:91](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/minterset.ts#L91)_

**Parameters:**

| Name        | Type                     | Default | Description                                                                                 |
| ----------- | ------------------------ | ------- | ------------------------------------------------------------------------------------------- |
| `threshold` | number                   | 1       | The number of signatures required to mint more of an asset by signing a minting transaction |
| `minters`   | string[] &#124; Buffer[] | []      | Array of addresss which are authorized to sign a minting transaction                        |

**Returns:** _[MinterSet](api_avm_minterset.minterset)_

## Properties

### `Protected` \_codecID

• **\_codecID**: _number_ = undefined

_Inherited from [SigIdx](common_signature.sigidx).[\_codecID](common_signature.sigidx#protected-_codecid)_

_Defined in [src/utils/serialization.ts:51](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/serialization.ts#L51)_

---

### `Protected` \_typeID

• **\_typeID**: _any_ = undefined

_Overrides [Serializable](utils_serialization.serializable).[\_typeID](utils_serialization.serializable#protected-_typeid)_

_Defined in [src/apis/avm/minterset.ts:32](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/minterset.ts#L32)_

---

### `Protected` \_typeName

• **\_typeName**: _string_ = "MinterSet"

_Overrides [Serializable](utils_serialization.serializable).[\_typeName](utils_serialization.serializable#protected-_typename)_

_Defined in [src/apis/avm/minterset.ts:31](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/minterset.ts#L31)_

---

### `Protected` minters

• **minters**: _Buffer[]_ = []

_Defined in [src/apis/avm/minterset.ts:65](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/minterset.ts#L65)_

---

### `Protected` threshold

• **threshold**: _number_

_Defined in [src/apis/avm/minterset.ts:64](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/minterset.ts#L64)_

## Methods

### `Protected` \_cleanAddresses

▸ **\_cleanAddresses**(`addresses`: string[] | Buffer[]): _Buffer[]_

_Defined in [src/apis/avm/minterset.ts:81](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/minterset.ts#L81)_

**Parameters:**

| Name        | Type                     |
| ----------- | ------------------------ |
| `addresses` | string[] &#124; Buffer[] |

**Returns:** _Buffer[]_

---

### deserialize

▸ **deserialize**(`fields`: object, `encoding`: [SerializedEncoding](../modules/utils_serialization#serializedencoding)): _void_

_Overrides [StandardParseableInput](common_inputs.standardparseableinput).[deserialize](common_inputs.standardparseableinput#deserialize)_

_Defined in [src/apis/avm/minterset.ts:50](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/minterset.ts#L50)_

**Parameters:**

| Name       | Type                                                                    | Default |
| ---------- | ----------------------------------------------------------------------- | ------- |
| `fields`   | object                                                                  | -       |
| `encoding` | [SerializedEncoding](../modules/utils_serialization#serializedencoding) | "hex"   |

**Returns:** _void_

---

### getCodecID

▸ **getCodecID**(): _number_

_Inherited from [SigIdx](common_signature.sigidx).[getCodecID](common_signature.sigidx#getcodecid)_

_Defined in [src/utils/serialization.ts:70](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/serialization.ts#L70)_

Used in serialization. Optional. TypeID is a number for the typeID of object being output.

**Returns:** _number_

---

### getMinters

▸ **getMinters**(): _Buffer[]_

_Defined in [src/apis/avm/minterset.ts:77](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/minterset.ts#L77)_

Returns the minters.

**Returns:** _Buffer[]_

---

### getThreshold

▸ **getThreshold**(): _number_

_Defined in [src/apis/avm/minterset.ts:70](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/minterset.ts#L70)_

Returns the threshold.

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

### serialize

▸ **serialize**(`encoding`: [SerializedEncoding](../modules/utils_serialization#serializedencoding)): _object_

_Overrides [Serializable](utils_serialization.serializable).[serialize](utils_serialization.serializable#serialize)_

_Defined in [src/apis/avm/minterset.ts:34](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/minterset.ts#L34)_

**Parameters:**

| Name       | Type                                                                    | Default |
| ---------- | ----------------------------------------------------------------------- | ------- |
| `encoding` | [SerializedEncoding](../modules/utils_serialization#serializedencoding) | "hex"   |

**Returns:** _object_
