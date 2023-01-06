# Class: UTXO

Class for representing a single UTXO.

## Hierarchy

↳ [StandardUTXO](common_utxos.standardutxo)

↳ **UTXO**

## Index

### Constructors

- [constructor](api_avm_utxos.utxo#constructor)

### Properties

- [\_codecID](api_avm_utxos.utxo#protected-_codecid)
- [\_typeID](api_avm_utxos.utxo#protected-_typeid)
- [\_typeName](api_avm_utxos.utxo#protected-_typename)
- [assetID](api_avm_utxos.utxo#protected-assetid)
- [codecID](api_avm_utxos.utxo#protected-codecid)
- [output](api_avm_utxos.utxo#protected-output)
- [outputidx](api_avm_utxos.utxo#protected-outputidx)
- [txid](api_avm_utxos.utxo#protected-txid)

### Methods

- [clone](api_avm_utxos.utxo#clone)
- [create](api_avm_utxos.utxo#create)
- [deserialize](api_avm_utxos.utxo#deserialize)
- [fromBuffer](api_avm_utxos.utxo#frombuffer)
- [fromString](api_avm_utxos.utxo#fromstring)
- [getAssetID](api_avm_utxos.utxo#getassetid)
- [getCodecID](api_avm_utxos.utxo#getcodecid)
- [getCodecIDBuffer](api_avm_utxos.utxo#getcodecidbuffer)
- [getOutput](api_avm_utxos.utxo#getoutput)
- [getOutputIdx](api_avm_utxos.utxo#getoutputidx)
- [getTxID](api_avm_utxos.utxo#gettxid)
- [getTypeID](api_avm_utxos.utxo#gettypeid)
- [getTypeName](api_avm_utxos.utxo#gettypename)
- [getUTXOID](api_avm_utxos.utxo#getutxoid)
- [sanitizeObject](api_avm_utxos.utxo#sanitizeobject)
- [serialize](api_avm_utxos.utxo#serialize)
- [toBuffer](api_avm_utxos.utxo#tobuffer)
- [toString](api_avm_utxos.utxo#tostring)

## Constructors

### constructor

\+ **new UTXO**(`codecID`: number, `txID`: Buffer, `outputidx`: Buffer | number, `assetID`: Buffer, `output`: [Output](common_output.output)): _[UTXO](api_avm_utxos.utxo)_

_Inherited from [StandardUTXO](common_utxos.standardutxo).[constructor](common_utxos.standardutxo#constructor)_

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

**Returns:** _[UTXO](api_avm_utxos.utxo)_

## Properties

### `Protected` \_codecID

• **\_codecID**: _number_ = undefined

_Inherited from [SigIdx](common_signature.sigidx).[\_codecID](common_signature.sigidx#protected-_codecid)_

_Defined in [src/utils/serialization.ts:51](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/serialization.ts#L51)_

---

### `Protected` \_typeID

• **\_typeID**: _any_ = undefined

_Overrides [StandardUTXO](common_utxos.standardutxo).[\_typeID](common_utxos.standardutxo#protected-_typeid)_

_Defined in [src/apis/avm/utxos.ts:61](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/utxos.ts#L61)_

---

### `Protected` \_typeName

• **\_typeName**: _string_ = "UTXO"

_Overrides [StandardUTXO](common_utxos.standardutxo).[\_typeName](common_utxos.standardutxo#protected-_typename)_

_Defined in [src/apis/avm/utxos.ts:60](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/utxos.ts#L60)_

---

### `Protected` assetID

• **assetID**: _Buffer_ = Buffer.alloc(32)

_Inherited from [StandardUTXO](common_utxos.standardutxo).[assetID](common_utxos.standardutxo#protected-assetid)_

_Defined in [src/common/utxos.ts:87](https://github.com/chain4travel/caminojs/blob/3883166/src/common/utxos.ts#L87)_

---

### `Protected` codecID

• **codecID**: _Buffer_ = Buffer.alloc(2)

_Inherited from [StandardUTXO](common_utxos.standardutxo).[codecID](common_utxos.standardutxo#protected-codecid)_

_Defined in [src/common/utxos.ts:84](https://github.com/chain4travel/caminojs/blob/3883166/src/common/utxos.ts#L84)_

---

### `Protected` output

• **output**: _[Output](common_output.output)_ = undefined

_Inherited from [StandardUTXO](common_utxos.standardutxo).[output](common_utxos.standardutxo#protected-output)_

_Defined in [src/common/utxos.ts:88](https://github.com/chain4travel/caminojs/blob/3883166/src/common/utxos.ts#L88)_

---

### `Protected` outputidx

• **outputidx**: _Buffer_ = Buffer.alloc(4)

_Inherited from [StandardUTXO](common_utxos.standardutxo).[outputidx](common_utxos.standardutxo#protected-outputidx)_

_Defined in [src/common/utxos.ts:86](https://github.com/chain4travel/caminojs/blob/3883166/src/common/utxos.ts#L86)_

---

### `Protected` txid

• **txid**: _Buffer_ = Buffer.alloc(32)

_Inherited from [StandardUTXO](common_utxos.standardutxo).[txid](common_utxos.standardutxo#protected-txid)_

_Defined in [src/common/utxos.ts:85](https://github.com/chain4travel/caminojs/blob/3883166/src/common/utxos.ts#L85)_

## Methods

### clone

▸ **clone**(): _this_

_Overrides [StandardUTXO](common_utxos.standardutxo).[clone](common_utxos.standardutxo#abstract-clone)_

_Defined in [src/apis/avm/utxos.ts:114](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/utxos.ts#L114)_

**Returns:** _this_

---

### create

▸ **create**(`codecID`: number, `txid`: Buffer, `outputidx`: Buffer | number, `assetID`: Buffer, `output`: [Output](common_output.output)): _this_

_Overrides [StandardUTXO](common_utxos.standardutxo).[create](common_utxos.standardutxo#abstract-create)_

_Defined in [src/apis/avm/utxos.ts:120](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/utxos.ts#L120)_

**Parameters:**

| Name        | Type                           | Default                  |
| ----------- | ------------------------------ | ------------------------ |
| `codecID`   | number                         | AVMConstants.LATESTCODEC |
| `txid`      | Buffer                         | undefined                |
| `outputidx` | Buffer &#124; number           | undefined                |
| `assetID`   | Buffer                         | undefined                |
| `output`    | [Output](common_output.output) | undefined                |

**Returns:** _this_

---

### deserialize

▸ **deserialize**(`fields`: object, `encoding`: [SerializedEncoding](../modules/utils_serialization#serializedencoding)): _void_

_Overrides [StandardUTXO](common_utxos.standardutxo).[deserialize](common_utxos.standardutxo#deserialize)_

_Defined in [src/apis/avm/utxos.ts:65](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/utxos.ts#L65)_

**Parameters:**

| Name       | Type                                                                    | Default |
| ---------- | ----------------------------------------------------------------------- | ------- |
| `fields`   | object                                                                  | -       |
| `encoding` | [SerializedEncoding](../modules/utils_serialization#serializedencoding) | "hex"   |

**Returns:** _void_

---

### fromBuffer

▸ **fromBuffer**(`bytes`: Buffer, `offset`: number): _number_

_Overrides [StandardUTXO](common_utxos.standardutxo).[fromBuffer](common_utxos.standardutxo#abstract-frombuffer)_

_Defined in [src/apis/avm/utxos.ts:71](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/utxos.ts#L71)_

**Parameters:**

| Name     | Type   | Default |
| -------- | ------ | ------- |
| `bytes`  | Buffer | -       |
| `offset` | number | 0       |

**Returns:** _number_

---

### fromString

▸ **fromString**(`serialized`: string): _number_

_Overrides [StandardUTXO](common_utxos.standardutxo).[fromString](common_utxos.standardutxo#abstract-fromstring)_

_Defined in [src/apis/avm/utxos.ts:98](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/utxos.ts#L98)_

Takes a base-58 string containing a [UTXO](api_avm_utxos.utxo), parses it, populates the class, and returns the length of the StandardUTXO in bytes.

**`remarks`**
unlike most fromStrings, it expects the string to be serialized in cb58 format

**Parameters:**

| Name         | Type   | Description                                                  |
| ------------ | ------ | ------------------------------------------------------------ |
| `serialized` | string | A base-58 string containing a raw [UTXO](api_avm_utxos.utxo) |

**Returns:** _number_

The length of the raw [UTXO](api_avm_utxos.utxo)

---

### getAssetID

▸ **getAssetID**(): _Buffer_

_Inherited from [StandardUTXO](common_utxos.standardutxo).[getAssetID](common_utxos.standardutxo#getassetid)_

_Defined in [src/common/utxos.ts:114](https://github.com/chain4travel/caminojs/blob/3883166/src/common/utxos.ts#L114)_

Returns the assetID as a [Buffer](https://github.com/feross/buffer).

**Returns:** _Buffer_

---

### getCodecID

▸ **getCodecID**(): _number_

_Inherited from [StandardUTXO](common_utxos.standardutxo).[getCodecID](common_utxos.standardutxo#getcodecid)_

_Overrides [SigIdx](common_signature.sigidx).[getCodecID](common_signature.sigidx#getcodecid)_

_Defined in [src/common/utxos.ts:93](https://github.com/chain4travel/caminojs/blob/3883166/src/common/utxos.ts#L93)_

Returns the numeric representation of the CodecID.

**Returns:** _number_

---

### getCodecIDBuffer

▸ **getCodecIDBuffer**(): _Buffer_

_Inherited from [StandardUTXO](common_utxos.standardutxo).[getCodecIDBuffer](common_utxos.standardutxo#getcodecidbuffer)_

_Defined in [src/common/utxos.ts:99](https://github.com/chain4travel/caminojs/blob/3883166/src/common/utxos.ts#L99)_

Returns the [Buffer](https://github.com/feross/buffer) representation of the CodecID

**Returns:** _Buffer_

---

### getOutput

▸ **getOutput**(): _[Output](common_output.output)_

_Inherited from [StandardUTXO](common_utxos.standardutxo).[getOutput](common_utxos.standardutxo#getoutput)_

_Defined in [src/common/utxos.ts:125](https://github.com/chain4travel/caminojs/blob/3883166/src/common/utxos.ts#L125)_

Returns a reference to the output

**Returns:** _[Output](common_output.output)_

---

### getOutputIdx

▸ **getOutputIdx**(): _Buffer_

_Inherited from [StandardUTXO](common_utxos.standardutxo).[getOutputIdx](common_utxos.standardutxo#getoutputidx)_

_Defined in [src/common/utxos.ts:109](https://github.com/chain4travel/caminojs/blob/3883166/src/common/utxos.ts#L109)_

Returns a [Buffer](https://github.com/feross/buffer) of the OutputIdx.

**Returns:** _Buffer_

---

### getTxID

▸ **getTxID**(): _Buffer_

_Inherited from [StandardUTXO](common_utxos.standardutxo).[getTxID](common_utxos.standardutxo#gettxid)_

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

_Inherited from [StandardUTXO](common_utxos.standardutxo).[getUTXOID](common_utxos.standardutxo#getutxoid)_

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

_Inherited from [StandardUTXO](common_utxos.standardutxo).[serialize](common_utxos.standardutxo#serialize)_

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

_Inherited from [StandardUTXO](common_utxos.standardutxo).[toBuffer](common_utxos.standardutxo#tobuffer)_

_Defined in [src/common/utxos.ts:137](https://github.com/chain4travel/caminojs/blob/3883166/src/common/utxos.ts#L137)_

Returns a [Buffer](https://github.com/feross/buffer) representation of the [StandardUTXO](common_utxos.standardutxo).

**Returns:** _Buffer_

---

### toString

▸ **toString**(): _string_

_Overrides [StandardUTXO](common_utxos.standardutxo).[toString](common_utxos.standardutxo#abstract-tostring)_

_Defined in [src/apis/avm/utxos.ts:109](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/utxos.ts#L109)_

Returns a base-58 representation of the [UTXO](api_avm_utxos.utxo).

**`remarks`**
unlike most toStrings, this returns in cb58 serialization format

**Returns:** _string_
