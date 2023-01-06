# Class: SubnetAuth

## Hierarchy

- [Serializable](utils_serialization.serializable)

  ↳ **SubnetAuth**

## Index

### Properties

- [\_codecID](api_platformvm_subnetauth.subnetauth#protected-_codecid)
- [\_typeID](api_platformvm_subnetauth.subnetauth#protected-_typeid)
- [\_typeName](api_platformvm_subnetauth.subnetauth#protected-_typename)
- [addressIndices](api_platformvm_subnetauth.subnetauth#protected-addressindices)
- [numAddressIndices](api_platformvm_subnetauth.subnetauth#protected-numaddressindices)

### Methods

- [addAddressIndex](api_platformvm_subnetauth.subnetauth#addaddressindex)
- [deserialize](api_platformvm_subnetauth.subnetauth#deserialize)
- [fromBuffer](api_platformvm_subnetauth.subnetauth#frombuffer)
- [getAddressIndices](api_platformvm_subnetauth.subnetauth#getaddressindices)
- [getCodecID](api_platformvm_subnetauth.subnetauth#getcodecid)
- [getNumAddressIndices](api_platformvm_subnetauth.subnetauth#getnumaddressindices)
- [getTypeID](api_platformvm_subnetauth.subnetauth#gettypeid)
- [getTypeName](api_platformvm_subnetauth.subnetauth#gettypename)
- [sanitizeObject](api_platformvm_subnetauth.subnetauth#sanitizeobject)
- [serialize](api_platformvm_subnetauth.subnetauth#serialize)
- [toBuffer](api_platformvm_subnetauth.subnetauth#tobuffer)

## Properties

### `Protected` \_codecID

• **\_codecID**: _number_ = undefined

_Inherited from [SigIdx](common_signature.sigidx).[\_codecID](common_signature.sigidx#protected-_codecid)_

_Defined in [src/utils/serialization.ts:51](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/serialization.ts#L51)_

---

### `Protected` \_typeID

• **\_typeID**: _number_ = PlatformVMConstants.SUBNETAUTH

_Overrides [Serializable](utils_serialization.serializable).[\_typeID](utils_serialization.serializable#protected-_typeid)_

_Defined in [src/apis/platformvm/subnetauth.ts:17](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/subnetauth.ts#L17)_

---

### `Protected` \_typeName

• **\_typeName**: _string_ = "SubnetAuth"

_Overrides [Serializable](utils_serialization.serializable).[\_typeName](utils_serialization.serializable#protected-_typename)_

_Defined in [src/apis/platformvm/subnetauth.ts:16](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/subnetauth.ts#L16)_

---

### `Protected` addressIndices

• **addressIndices**: _Buffer[]_ = []

_Defined in [src/apis/platformvm/subnetauth.ts:54](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/subnetauth.ts#L54)_

---

### `Protected` numAddressIndices

• **numAddressIndices**: _Buffer_ = Buffer.alloc(4)

_Defined in [src/apis/platformvm/subnetauth.ts:55](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/subnetauth.ts#L55)_

## Methods

### addAddressIndex

▸ **addAddressIndex**(`index`: Buffer): _void_

_Defined in [src/apis/platformvm/subnetauth.ts:34](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/subnetauth.ts#L34)_

Add an address index for Subnet Auth signing

**Parameters:**

| Name    | Type   | Description                            |
| ------- | ------ | -------------------------------------- |
| `index` | Buffer | the Buffer of the address index to add |

**Returns:** _void_

---

### deserialize

▸ **deserialize**(`fields`: object, `encoding`: [SerializedEncoding](../modules/utils_serialization#serializedencoding)): _void_

_Overrides [StandardParseableInput](common_inputs.standardparseableinput).[deserialize](common_inputs.standardparseableinput#deserialize)_

_Defined in [src/apis/platformvm/subnetauth.ts:25](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/subnetauth.ts#L25)_

**Parameters:**

| Name       | Type                                                                    | Default |
| ---------- | ----------------------------------------------------------------------- | ------- |
| `fields`   | object                                                                  | -       |
| `encoding` | [SerializedEncoding](../modules/utils_serialization#serializedencoding) | "hex"   |

**Returns:** _void_

---

### fromBuffer

▸ **fromBuffer**(`bytes`: Buffer, `offset`: number): _number_

_Defined in [src/apis/platformvm/subnetauth.ts:57](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/subnetauth.ts#L57)_

**Parameters:**

| Name     | Type   | Default |
| -------- | ------ | ------- |
| `bytes`  | Buffer | -       |
| `offset` | number | 0       |

**Returns:** _number_

---

### getAddressIndices

▸ **getAddressIndices**(): _Buffer[]_

_Defined in [src/apis/platformvm/subnetauth.ts:50](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/subnetauth.ts#L50)_

Returns an array of AddressIndices as Buffers

**Returns:** _Buffer[]_

---

### getCodecID

▸ **getCodecID**(): _number_

_Inherited from [SigIdx](common_signature.sigidx).[getCodecID](common_signature.sigidx#getcodecid)_

_Defined in [src/utils/serialization.ts:70](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/serialization.ts#L70)_

Used in serialization. Optional. TypeID is a number for the typeID of object being output.

**Returns:** _number_

---

### getNumAddressIndices

▸ **getNumAddressIndices**(): _number_

_Defined in [src/apis/platformvm/subnetauth.ts:43](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/subnetauth.ts#L43)_

Returns the number of address indices as a number

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

_Defined in [src/apis/platformvm/subnetauth.ts:19](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/subnetauth.ts#L19)_

**Parameters:**

| Name       | Type                                                                    | Default |
| ---------- | ----------------------------------------------------------------------- | ------- |
| `encoding` | [SerializedEncoding](../modules/utils_serialization#serializedencoding) | "hex"   |

**Returns:** _object_

---

### toBuffer

▸ **toBuffer**(): _Buffer_

_Defined in [src/apis/platformvm/subnetauth.ts:72](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/subnetauth.ts#L72)_

Returns a [Buffer](https://github.com/feross/buffer) representation of the [SubnetAuth](api_platformvm_subnetauth.subnetauth).

**Returns:** _Buffer_
