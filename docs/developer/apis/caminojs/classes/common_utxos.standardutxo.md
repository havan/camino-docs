# Class: StandardUTXO

Class for representing a single StandardUTXO.

## Hierarchy

- [Serializable](utils_serialization.serializable)

  ↳ **StandardUTXO**

  ↳ [UTXO](api_evm_utxos.utxo)

  ↳ [UTXO](api_avm_utxos.utxo)

  ↳ [UTXO](api_platformvm_utxos.utxo)

## Index

### Constructors

- [constructor](common_utxos.standardutxo#constructor)

### Properties

- [\_codecID](common_utxos.standardutxo#protected-_codecid)
- [\_typeID](common_utxos.standardutxo#protected-_typeid)
- [\_typeName](common_utxos.standardutxo#protected-_typename)
- [assetID](common_utxos.standardutxo#protected-assetid)
- [codecID](common_utxos.standardutxo#protected-codecid)
- [output](common_utxos.standardutxo#protected-output)
- [outputidx](common_utxos.standardutxo#protected-outputidx)
- [txid](common_utxos.standardutxo#protected-txid)

### Methods

- [clone](common_utxos.standardutxo#abstract-clone)
- [create](common_utxos.standardutxo#abstract-create)
- [deserialize](common_utxos.standardutxo#deserialize)
- [fromBuffer](common_utxos.standardutxo#abstract-frombuffer)
- [fromString](common_utxos.standardutxo#abstract-fromstring)
- [getAssetID](common_utxos.standardutxo#getassetid)
- [getCodecID](common_utxos.standardutxo#getcodecid)
- [getCodecIDBuffer](common_utxos.standardutxo#getcodecidbuffer)
- [getOutput](common_utxos.standardutxo#getoutput)
- [getOutputIdx](common_utxos.standardutxo#getoutputidx)
- [getTxID](common_utxos.standardutxo#gettxid)
- [getTypeID](common_utxos.standardutxo#gettypeid)
- [getTypeName](common_utxos.standardutxo#gettypename)
- [getUTXOID](common_utxos.standardutxo#getutxoid)
- [sanitizeObject](common_utxos.standardutxo#sanitizeobject)
- [serialize](common_utxos.standardutxo#serialize)
- [toBuffer](common_utxos.standardutxo#tobuffer)
- [toString](common_utxos.standardutxo#abstract-tostring)

## Constructors

### constructor

\+ **new StandardUTXO**(`codecID`: number, `txID`: Buffer, `outputidx`: Buffer | number, `assetID`: Buffer, `output`: [Output](common_output.output)): _[StandardUTXO](common_utxos.standardutxo)_

_Defined in [src/common/utxos.ts:172](https://github.com/chain4travel/caminojs/blob/3883166/src/common/utxos.ts#L172)_

Class for representing a single StandardUTXO.

**Parameters:**

| Name        | Type                           | Default   | Description                                                                                |
| ----------- | ------------------------------ | --------- | ------------------------------------------------------------------------------------------ |
| `codecID`   | number                         | 0         | Optional number which specifies the codeID of the UTXO. Default 0                          |
| `txID`      | Buffer                         | undefined | Optional [Buffer](https://github.com/feross/buffer) of transaction ID for the StandardUTXO |
| `outputidx` | Buffer &#124; number           | undefined | -                                                                                          |
| `assetID`   | Buffer                         | undefined | Optional [Buffer](https://github.com/feross/buffer) of the asset ID for the StandardUTXO   |
| `output`    | [Output](common_output.output) | undefined | -                                                                                          |

**Returns:** _[StandardUTXO](common_utxos.standardutxo)_

## Properties

### `Protected` \_codecID

• **\_codecID**: _number_ = undefined

_Inherited from [SigIdx](common_signature.sigidx).[\_codecID](common_signature.sigidx#protected-_codecid)_

_Defined in [src/utils/serialization.ts:51](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/serialization.ts#L51)_

---

### `Protected` \_typeID

• **\_typeID**: _any_ = undefined

_Overrides [Serializable](utils_serialization.serializable).[\_typeID](utils_serialization.serializable#protected-_typeid)_

_Defined in [src/common/utxos.ts:29](https://github.com/chain4travel/caminojs/blob/3883166/src/common/utxos.ts#L29)_

---

### `Protected` \_typeName

• **\_typeName**: _string_ = "StandardUTXO"

_Overrides [Serializable](utils_serialization.serializable).[\_typeName](utils_serialization.serializable#protected-_typename)_

_Defined in [src/common/utxos.ts:28](https://github.com/chain4travel/caminojs/blob/3883166/src/common/utxos.ts#L28)_

---

### `Protected` assetID

• **assetID**: _Buffer_ = Buffer.alloc(32)

_Defined in [src/common/utxos.ts:87](https://github.com/chain4travel/caminojs/blob/3883166/src/common/utxos.ts#L87)_

---

### `Protected` codecID

• **codecID**: _Buffer_ = Buffer.alloc(2)

_Defined in [src/common/utxos.ts:84](https://github.com/chain4travel/caminojs/blob/3883166/src/common/utxos.ts#L84)_

---

### `Protected` output

• **output**: _[Output](common_output.output)_ = undefined

_Defined in [src/common/utxos.ts:88](https://github.com/chain4travel/caminojs/blob/3883166/src/common/utxos.ts#L88)_

---

### `Protected` outputidx

• **outputidx**: _Buffer_ = Buffer.alloc(4)

_Defined in [src/common/utxos.ts:86](https://github.com/chain4travel/caminojs/blob/3883166/src/common/utxos.ts#L86)_

---

### `Protected` txid

• **txid**: _Buffer_ = Buffer.alloc(32)

_Defined in [src/common/utxos.ts:85](https://github.com/chain4travel/caminojs/blob/3883166/src/common/utxos.ts#L85)_

## Methods

### `Abstract` clone

▸ **clone**(): _this_

_Defined in [src/common/utxos.ts:164](https://github.com/chain4travel/caminojs/blob/3883166/src/common/utxos.ts#L164)_

**Returns:** _this_

---

### `Abstract` create

▸ **create**(`codecID?`: number, `txid?`: Buffer, `outputidx?`: Buffer | number, `assetID?`: Buffer, `output?`: [Output](common_output.output)): _this_

_Defined in [src/common/utxos.ts:166](https://github.com/chain4travel/caminojs/blob/3883166/src/common/utxos.ts#L166)_

**Parameters:**

| Name         | Type                           |
| ------------ | ------------------------------ |
| `codecID?`   | number                         |
| `txid?`      | Buffer                         |
| `outputidx?` | Buffer &#124; number           |
| `assetID?`   | Buffer                         |
| `output?`    | [Output](common_output.output) |

**Returns:** _this_

---

### deserialize

▸ **deserialize**(`fields`: object, `encoding`: [SerializedEncoding](../modules/utils_serialization#serializedencoding)): _void_

_Overrides [StandardParseableInput](common_inputs.standardparseableinput).[deserialize](common_inputs.standardparseableinput#deserialize)_

_Defined in [src/common/utxos.ts:52](https://github.com/chain4travel/caminojs/blob/3883166/src/common/utxos.ts#L52)_

**Parameters:**

| Name       | Type                                                                    | Default |
| ---------- | ----------------------------------------------------------------------- | ------- |
| `fields`   | object                                                                  | -       |
| `encoding` | [SerializedEncoding](../modules/utils_serialization#serializedencoding) | "hex"   |

**Returns:** _void_

---

### `Abstract` fromBuffer

▸ **fromBuffer**(`bytes`: Buffer, `offset?`: number): _number_

_Defined in [src/common/utxos.ts:132](https://github.com/chain4travel/caminojs/blob/3883166/src/common/utxos.ts#L132)_

Takes a [Buffer](https://github.com/feross/buffer) containing an [StandardUTXO](common_utxos.standardutxo), parses it, populates the class, and returns the length of the StandardUTXO in bytes.

**Parameters:**

| Name      | Type   | Description                                                                                             |
| --------- | ------ | ------------------------------------------------------------------------------------------------------- |
| `bytes`   | Buffer | A [Buffer](https://github.com/feross/buffer) containing a raw [StandardUTXO](common_utxos.standardutxo) |
| `offset?` | number | -                                                                                                       |

**Returns:** _number_

---

### `Abstract` fromString

▸ **fromString**(`serialized`: string): _number_

_Defined in [src/common/utxos.ts:160](https://github.com/chain4travel/caminojs/blob/3883166/src/common/utxos.ts#L160)_

**Parameters:**

| Name         | Type   |
| ------------ | ------ |
| `serialized` | string |

**Returns:** _number_

---

### getAssetID

▸ **getAssetID**(): _Buffer_

_Defined in [src/common/utxos.ts:114](https://github.com/chain4travel/caminojs/blob/3883166/src/common/utxos.ts#L114)_

Returns the assetID as a [Buffer](https://github.com/feross/buffer).

**Returns:** _Buffer_

---

### getCodecID

▸ **getCodecID**(): _number_

_Overrides [SigIdx](common_signature.sigidx).[getCodecID](common_signature.sigidx#getcodecid)_

_Defined in [src/common/utxos.ts:93](https://github.com/chain4travel/caminojs/blob/3883166/src/common/utxos.ts#L93)_

Returns the numeric representation of the CodecID.

**Returns:** _number_

---

### getCodecIDBuffer

▸ **getCodecIDBuffer**(): _Buffer_

_Defined in [src/common/utxos.ts:99](https://github.com/chain4travel/caminojs/blob/3883166/src/common/utxos.ts#L99)_

Returns the [Buffer](https://github.com/feross/buffer) representation of the CodecID

**Returns:** _Buffer_

---

### getOutput

▸ **getOutput**(): _[Output](common_output.output)_

_Defined in [src/common/utxos.ts:125](https://github.com/chain4travel/caminojs/blob/3883166/src/common/utxos.ts#L125)_

Returns a reference to the output

**Returns:** _[Output](common_output.output)_

---

### getOutputIdx

▸ **getOutputIdx**(): _Buffer_

_Defined in [src/common/utxos.ts:109](https://github.com/chain4travel/caminojs/blob/3883166/src/common/utxos.ts#L109)_

Returns a [Buffer](https://github.com/feross/buffer) of the OutputIdx.

**Returns:** _Buffer_

---

### getTxID

▸ **getTxID**(): _Buffer_

_Defined in [src/common/utxos.ts:104](https://github.com/chain4travel/caminojs/blob/3883166/src/common/utxos.ts#L104)_

Returns a [Buffer](https://github.com/feross/buffer) of the TxID.

**Returns:** _Buffer_

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

### getUTXOID

▸ **getUTXOID**(): _string_

_Defined in [src/common/utxos.ts:119](https://github.com/chain4travel/caminojs/blob/3883166/src/common/utxos.ts#L119)_

Returns the UTXOID as a base-58 string (UTXOID is a string )

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

_Defined in [src/common/utxos.ts:31](https://github.com/chain4travel/caminojs/blob/3883166/src/common/utxos.ts#L31)_

**Parameters:**

| Name       | Type                                                                    | Default |
| ---------- | ----------------------------------------------------------------------- | ------- |
| `encoding` | [SerializedEncoding](../modules/utils_serialization#serializedencoding) | "hex"   |

**Returns:** _object_

---

### toBuffer

▸ **toBuffer**(): _Buffer_

_Defined in [src/common/utxos.ts:137](https://github.com/chain4travel/caminojs/blob/3883166/src/common/utxos.ts#L137)_

Returns a [Buffer](https://github.com/feross/buffer) representation of the [StandardUTXO](common_utxos.standardutxo).

**Returns:** _Buffer_

---

### `Abstract` toString

▸ **toString**(): _string_

_Defined in [src/common/utxos.ts:162](https://github.com/chain4travel/caminojs/blob/3883166/src/common/utxos.ts#L162)_

**Returns:** _string_
