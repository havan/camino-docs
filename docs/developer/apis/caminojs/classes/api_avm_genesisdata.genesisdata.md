# Class: GenesisData

## Hierarchy

- [Serializable](utils_serialization.serializable)

  ↳ **GenesisData**

## Index

### Constructors

- [constructor](api_avm_genesisdata.genesisdata#constructor)

### Properties

- [\_codecID](api_avm_genesisdata.genesisdata#protected-_codecid)
- [\_typeID](api_avm_genesisdata.genesisdata#protected-_typeid)
- [\_typeName](api_avm_genesisdata.genesisdata#protected-_typename)
- [genesisAssets](api_avm_genesisdata.genesisdata#protected-genesisassets)
- [networkID](api_avm_genesisdata.genesisdata#protected-networkid)

### Methods

- [deserialize](api_avm_genesisdata.genesisdata#deserialize)
- [fromBuffer](api_avm_genesisdata.genesisdata#frombuffer)
- [getCodecID](api_avm_genesisdata.genesisdata#getcodecid)
- [getGenesisAssets](api_avm_genesisdata.genesisdata#getgenesisassets)
- [getNetworkID](api_avm_genesisdata.genesisdata#getnetworkid)
- [getTypeID](api_avm_genesisdata.genesisdata#gettypeid)
- [getTypeName](api_avm_genesisdata.genesisdata#gettypename)
- [sanitizeObject](api_avm_genesisdata.genesisdata#sanitizeobject)
- [serialize](api_avm_genesisdata.genesisdata#serialize)
- [toBuffer](api_avm_genesisdata.genesisdata#tobuffer)

## Constructors

### constructor

\+ **new GenesisData**(`genesisAssets`: [GenesisAsset](api_avm_genesisasset.genesisasset)[], `networkID`: number): _[GenesisData](api_avm_genesisdata.genesisdata)_

_Defined in [src/apis/avm/genesisdata.ts:124](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/genesisdata.ts#L124)_

Class representing AVM GenesisData

**Parameters:**

| Name            | Type                                                | Default          | Description               |
| --------------- | --------------------------------------------------- | ---------------- | ------------------------- |
| `genesisAssets` | [GenesisAsset](api_avm_genesisasset.genesisasset)[] | []               | Optional GenesisAsset[]   |
| `networkID`     | number                                              | DefaultNetworkID | Optional DefaultNetworkID |

**Returns:** _[GenesisData](api_avm_genesisdata.genesisdata)_

## Properties

### `Protected` \_codecID

• **\_codecID**: _number_ = AVMConstants.LATESTCODEC

_Overrides [SigIdx](common_signature.sigidx).[\_codecID](common_signature.sigidx#protected-_codecid)_

_Defined in [src/apis/avm/genesisdata.ts:26](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/genesisdata.ts#L26)_

---

### `Protected` \_typeID

• **\_typeID**: _number_ = undefined

_Inherited from [Serializable](utils_serialization.serializable).[\_typeID](utils_serialization.serializable#protected-_typeid)_

_Defined in [src/utils/serialization.ts:50](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/serialization.ts#L50)_

---

### `Protected` \_typeName

• **\_typeName**: _string_ = "GenesisData"

_Overrides [Serializable](utils_serialization.serializable).[\_typeName](utils_serialization.serializable#protected-_typename)_

_Defined in [src/apis/avm/genesisdata.ts:25](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/genesisdata.ts#L25)_

---

### `Protected` genesisAssets

• **genesisAssets**: _[GenesisAsset](api_avm_genesisasset.genesisasset)[]_

_Defined in [src/apis/avm/genesisdata.ts:63](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/genesisdata.ts#L63)_

---

### `Protected` networkID

• **networkID**: _Buffer_ = Buffer.alloc(4)

_Defined in [src/apis/avm/genesisdata.ts:64](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/genesisdata.ts#L64)_

## Methods

### deserialize

▸ **deserialize**(`fields`: object, `encoding`: [SerializedEncoding](../modules/utils_serialization#serializedencoding)): _void_

_Overrides [StandardParseableInput](common_inputs.standardparseableinput).[deserialize](common_inputs.standardparseableinput#deserialize)_

_Defined in [src/apis/avm/genesisdata.ts:45](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/genesisdata.ts#L45)_

**Parameters:**

| Name       | Type                                                                    | Default |
| ---------- | ----------------------------------------------------------------------- | ------- |
| `fields`   | object                                                                  | -       |
| `encoding` | [SerializedEncoding](../modules/utils_serialization#serializedencoding) | "hex"   |

**Returns:** _void_

---

### fromBuffer

▸ **fromBuffer**(`bytes`: Buffer, `offset`: number): _number_

_Defined in [src/apis/avm/genesisdata.ts:85](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/genesisdata.ts#L85)_

Takes a [Buffer](https://github.com/feross/buffer) containing an [GenesisAsset](api_avm_genesisasset.genesisasset), parses it, populates the class, and returns the length of the [GenesisAsset](api_avm_genesisasset.genesisasset) in bytes.

**`remarks`** assume not-checksummed

**Parameters:**

| Name     | Type   | Default | Description                                                                                                     |
| -------- | ------ | ------- | --------------------------------------------------------------------------------------------------------------- |
| `bytes`  | Buffer | -       | A [Buffer](https://github.com/feross/buffer) containing a raw [GenesisAsset](api_avm_genesisasset.genesisasset) |
| `offset` | number | 0       | -                                                                                                               |

**Returns:** _number_

The length of the raw [GenesisAsset](api_avm_genesisasset.genesisasset)

---

### getCodecID

▸ **getCodecID**(): _number_

_Inherited from [SigIdx](common_signature.sigidx).[getCodecID](common_signature.sigidx#getcodecid)_

_Defined in [src/utils/serialization.ts:70](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/serialization.ts#L70)_

Used in serialization. Optional. TypeID is a number for the typeID of object being output.

**Returns:** _number_

---

### getGenesisAssets

▸ **getGenesisAssets**(): _[GenesisAsset](api_avm_genesisasset.genesisasset)[]_

_Defined in [src/apis/avm/genesisdata.ts:69](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/genesisdata.ts#L69)_

Returns the GenesisAssets[]

**Returns:** _[GenesisAsset](api_avm_genesisasset.genesisasset)[]_

---

### getNetworkID

▸ **getNetworkID**(): _number_

_Defined in [src/apis/avm/genesisdata.ts:74](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/genesisdata.ts#L74)_

Returns the NetworkID as a number

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

_Defined in [src/apis/avm/genesisdata.ts:29](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/genesisdata.ts#L29)_

**Parameters:**

| Name       | Type                                                                    | Default |
| ---------- | ----------------------------------------------------------------------- | ------- |
| `encoding` | [SerializedEncoding](../modules/utils_serialization#serializedencoding) | "hex"   |

**Returns:** _object_

---

### toBuffer

▸ **toBuffer**(): _Buffer_

_Defined in [src/apis/avm/genesisdata.ts:106](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/genesisdata.ts#L106)_

Returns a [Buffer](https://github.com/feross/buffer) representation of the [GenesisData](api_avm_genesisdata.genesisdata).

**Returns:** _Buffer_
