# Class: Vertex

Class representing a Vertex

## Hierarchy

- [Serializable](utils_serialization.serializable)

  ↳ **Vertex**

## Index

### Constructors

- [constructor](api_avm_vertex.vertex#constructor)

### Properties

- [\_codecID](api_avm_vertex.vertex#protected-_codecid)
- [\_typeID](api_avm_vertex.vertex#protected-_typeid)
- [\_typeName](api_avm_vertex.vertex#protected-_typename)
- [blockchainID](api_avm_vertex.vertex#protected-blockchainid)
- [epoch](api_avm_vertex.vertex#protected-epoch)
- [height](api_avm_vertex.vertex#protected-height)
- [networkID](api_avm_vertex.vertex#protected-networkid)
- [numParentIDs](api_avm_vertex.vertex#protected-numparentids)
- [numRestrictions](api_avm_vertex.vertex#protected-numrestrictions)
- [numTxs](api_avm_vertex.vertex#protected-numtxs)
- [parentIDs](api_avm_vertex.vertex#protected-parentids)
- [restrictions](api_avm_vertex.vertex#protected-restrictions)
- [txs](api_avm_vertex.vertex#protected-txs)

### Methods

- [clone](api_avm_vertex.vertex#clone)
- [deserialize](api_avm_vertex.vertex#deserialize)
- [fromBuffer](api_avm_vertex.vertex#frombuffer)
- [getBlockchainID](api_avm_vertex.vertex#getblockchainid)
- [getCodecID](api_avm_vertex.vertex#getcodecid)
- [getEpoch](api_avm_vertex.vertex#getepoch)
- [getHeight](api_avm_vertex.vertex#getheight)
- [getNetworkID](api_avm_vertex.vertex#getnetworkid)
- [getParentIDs](api_avm_vertex.vertex#getparentids)
- [getRestrictions](api_avm_vertex.vertex#getrestrictions)
- [getTxs](api_avm_vertex.vertex#gettxs)
- [getTypeID](api_avm_vertex.vertex#gettypeid)
- [getTypeName](api_avm_vertex.vertex#gettypename)
- [sanitizeObject](api_avm_vertex.vertex#sanitizeobject)
- [serialize](api_avm_vertex.vertex#serialize)
- [setCodecID](api_avm_vertex.vertex#setcodecid)
- [toBuffer](api_avm_vertex.vertex#tobuffer)

## Constructors

### constructor

\+ **new Vertex**(`networkID`: number, `blockchainID`: string, `height`: BN, `epoch`: number, `parentIDs`: Buffer[], `txs`: [Tx](api_avm_transactions.tx)[], `restrictions`: Buffer[]): _[Vertex](api_avm_vertex.vertex)_

_Defined in [src/apis/avm/vertex.ts:209](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/vertex.ts#L209)_

Class representing a Vertex which is a container for AVM Transactions.

**Parameters:**

| Name           | Type                            | Default                                              | Description                                                                     |
| -------------- | ------------------------------- | ---------------------------------------------------- | ------------------------------------------------------------------------------- |
| `networkID`    | number                          | DefaultNetworkID                                     | Optional, [DefaultNetworkID](../modules/utils_constants#const-defaultnetworkid) |
| `blockchainID` | string                          | "2oYMBNV4eNHyqk2fjjV5nVQLDbtmNJzq5s3qs3Lo6ftnC6FByM" | Optional, default "2oYMBNV4eNHyqk2fjjV5nVQLDbtmNJzq5s3qs3Lo6ftnC6FByM"          |
| `height`       | BN                              | new BN(0)                                            | Optional, default new BN(0)                                                     |
| `epoch`        | number                          | 0                                                    | Optional, default new BN(0)                                                     |
| `parentIDs`    | Buffer[]                        | []                                                   | Optional, default []                                                            |
| `txs`          | [Tx](api_avm_transactions.tx)[] | []                                                   | Optional, default []                                                            |
| `restrictions` | Buffer[]                        | []                                                   | Optional, default []                                                            |

**Returns:** _[Vertex](api_avm_vertex.vertex)_

## Properties

### `Protected` \_codecID

• **\_codecID**: _number_ = AVMConstants.LATESTCODEC

_Overrides [SigIdx](common_signature.sigidx).[\_codecID](common_signature.sigidx#protected-_codecid)_

_Defined in [src/apis/avm/vertex.ts:23](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/vertex.ts#L23)_

---

### `Protected` \_typeID

• **\_typeID**: _number_ = undefined

_Inherited from [Serializable](utils_serialization.serializable).[\_typeID](utils_serialization.serializable#protected-_typeid)_

_Defined in [src/utils/serialization.ts:50](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/serialization.ts#L50)_

---

### `Protected` \_typeName

• **\_typeName**: _string_ = "Vertex"

_Overrides [Serializable](utils_serialization.serializable).[\_typeName](utils_serialization.serializable#protected-_typename)_

_Defined in [src/apis/avm/vertex.ts:22](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/vertex.ts#L22)_

---

### `Protected` blockchainID

• **blockchainID**: _Buffer_

_Defined in [src/apis/avm/vertex.ts:27](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/vertex.ts#L27)_

---

### `Protected` epoch

• **epoch**: _number_

_Defined in [src/apis/avm/vertex.ts:29](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/vertex.ts#L29)_

---

### `Protected` height

• **height**: _BN_

_Defined in [src/apis/avm/vertex.ts:28](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/vertex.ts#L28)_

---

### `Protected` networkID

• **networkID**: _number_

_Defined in [src/apis/avm/vertex.ts:26](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/vertex.ts#L26)_

---

### `Protected` numParentIDs

• **numParentIDs**: _number_

_Defined in [src/apis/avm/vertex.ts:31](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/vertex.ts#L31)_

---

### `Protected` numRestrictions

• **numRestrictions**: _number_

_Defined in [src/apis/avm/vertex.ts:35](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/vertex.ts#L35)_

---

### `Protected` numTxs

• **numTxs**: _number_

_Defined in [src/apis/avm/vertex.ts:33](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/vertex.ts#L33)_

---

### `Protected` parentIDs

• **parentIDs**: _Buffer[]_

_Defined in [src/apis/avm/vertex.ts:30](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/vertex.ts#L30)_

---

### `Protected` restrictions

• **restrictions**: _Buffer[]_

_Defined in [src/apis/avm/vertex.ts:34](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/vertex.ts#L34)_

---

### `Protected` txs

• **txs**: _[Tx](api_avm_transactions.tx)[]_

_Defined in [src/apis/avm/vertex.ts:32](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/vertex.ts#L32)_

## Methods

### clone

▸ **clone**(): _this_

_Defined in [src/apis/avm/vertex.ts:205](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/vertex.ts#L205)_

**Returns:** _this_

---

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

### fromBuffer

▸ **fromBuffer**(`bytes`: Buffer, `offset`: number): _number_

_Defined in [src/apis/avm/vertex.ts:111](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/vertex.ts#L111)_

Takes a [Buffer](https://github.com/feross/buffer) containing an [Vertex](api_avm_vertex.vertex), parses it, populates the class, and returns the length of the Vertex in bytes.

**`remarks`** assume not-checksummed

**Parameters:**

| Name     | Type   | Default | Description                                                                                   |
| -------- | ------ | ------- | --------------------------------------------------------------------------------------------- |
| `bytes`  | Buffer | -       | A [Buffer](https://github.com/feross/buffer) containing a raw [Vertex](api_avm_vertex.vertex) |
| `offset` | number | 0       | -                                                                                             |

**Returns:** _number_

The length of the raw [Vertex](api_avm_vertex.vertex)

---

### getBlockchainID

▸ **getBlockchainID**(): _string_

_Defined in [src/apis/avm/vertex.ts:46](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/vertex.ts#L46)_

Returns the BlockchainID as a CB58 string

**Returns:** _string_

---

### getCodecID

▸ **getCodecID**(): _number_

_Inherited from [SigIdx](common_signature.sigidx).[getCodecID](common_signature.sigidx#getcodecid)_

_Defined in [src/utils/serialization.ts:70](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/serialization.ts#L70)_

Used in serialization. Optional. TypeID is a number for the typeID of object being output.

**Returns:** _number_

---

### getEpoch

▸ **getEpoch**(): _number_

_Defined in [src/apis/avm/vertex.ts:60](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/vertex.ts#L60)_

Returns the Epoch as a number.

**Returns:** _number_

---

### getHeight

▸ **getHeight**(): _BN_

_Defined in [src/apis/avm/vertex.ts:53](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/vertex.ts#L53)_

Returns the Height as a [BN](https://github.com/indutny/bn.js/).

**Returns:** _BN_

---

### getNetworkID

▸ **getNetworkID**(): _number_

_Defined in [src/apis/avm/vertex.ts:40](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/vertex.ts#L40)_

Returns the NetworkID as a number

**Returns:** _number_

---

### getParentIDs

▸ **getParentIDs**(): _Buffer[]_

_Defined in [src/apis/avm/vertex.ts:67](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/vertex.ts#L67)_

**Returns:** _Buffer[]_

An array of Buffers

---

### getRestrictions

▸ **getRestrictions**(): _Buffer[]_

_Defined in [src/apis/avm/vertex.ts:81](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/vertex.ts#L81)_

**Returns:** _Buffer[]_

An array of Buffers

---

### getTxs

▸ **getTxs**(): _[Tx](api_avm_transactions.tx)[]_

_Defined in [src/apis/avm/vertex.ts:74](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/vertex.ts#L74)_

Returns array of UnsignedTxs.

**Returns:** _[Tx](api_avm_transactions.tx)[]_

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

▸ **serialize**(`encoding?`: [SerializedEncoding](../modules/utils_serialization#serializedencoding)): _object_

_Inherited from [Serializable](utils_serialization.serializable).[serialize](utils_serialization.serializable#serialize)_

_Defined in [src/utils/serialization.ts:90](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/serialization.ts#L90)_

**Parameters:**

| Name        | Type                                                                    |
| ----------- | ----------------------------------------------------------------------- |
| `encoding?` | [SerializedEncoding](../modules/utils_serialization#serializedencoding) |

**Returns:** _object_

---

### setCodecID

▸ **setCodecID**(`codecID`: number): _void_

_Defined in [src/apis/avm/vertex.ts:90](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/vertex.ts#L90)_

Set the codecID

**Parameters:**

| Name      | Type   | Description        |
| --------- | ------ | ------------------ |
| `codecID` | number | The codecID to set |

**Returns:** _void_

---

### toBuffer

▸ **toBuffer**(): _Buffer_

_Defined in [src/apis/avm/vertex.ts:162](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/vertex.ts#L162)_

Returns a [Buffer](https://github.com/feross/buffer) representation of the [Vertex](api_avm_vertex.vertex).

**Returns:** _Buffer_
