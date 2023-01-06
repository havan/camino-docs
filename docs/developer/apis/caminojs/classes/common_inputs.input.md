# Class: Input

## Hierarchy

- [Serializable](utils_serialization.serializable)

  ↳ **Input**

  ↳ [StandardAmountInput](common_inputs.standardamountinput)

## Index

### Properties

- [\_codecID](common_inputs.input#protected-_codecid)
- [\_typeID](common_inputs.input#protected-_typeid)
- [\_typeName](common_inputs.input#protected-_typename)
- [sigCount](common_inputs.input#protected-sigcount)
- [sigIdxs](common_inputs.input#protected-sigidxs)

### Methods

- [addSignatureIdx](common_inputs.input#addsignatureidx)
- [clone](common_inputs.input#abstract-clone)
- [create](common_inputs.input#abstract-create)
- [deserialize](common_inputs.input#deserialize)
- [fromBuffer](common_inputs.input#frombuffer)
- [getCodecID](common_inputs.input#getcodecid)
- [getCredentialID](common_inputs.input#abstract-getcredentialid)
- [getInputID](common_inputs.input#abstract-getinputid)
- [getSigIdxs](common_inputs.input#getsigidxs)
- [getTypeID](common_inputs.input#gettypeid)
- [getTypeName](common_inputs.input#gettypename)
- [sanitizeObject](common_inputs.input#sanitizeobject)
- [select](common_inputs.input#abstract-select)
- [serialize](common_inputs.input#serialize)
- [toBuffer](common_inputs.input#tobuffer)
- [toString](common_inputs.input#tostring)
- [comparator](common_inputs.input#static-comparator)

## Properties

### `Protected` \_codecID

• **\_codecID**: _number_ = undefined

_Inherited from [SigIdx](common_signature.sigidx).[\_codecID](common_signature.sigidx#protected-_codecid)_

_Defined in [src/utils/serialization.ts:51](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/serialization.ts#L51)_

---

### `Protected` \_typeID

• **\_typeID**: _any_ = undefined

_Overrides [Serializable](utils_serialization.serializable).[\_typeID](utils_serialization.serializable#protected-_typeid)_

_Defined in [src/common/input.ts:23](https://github.com/chain4travel/caminojs/blob/3883166/src/common/input.ts#L23)_

---

### `Protected` \_typeName

• **\_typeName**: _string_ = "Input"

_Overrides [Serializable](utils_serialization.serializable).[\_typeName](utils_serialization.serializable#protected-_typename)_

_Defined in [src/common/input.ts:22](https://github.com/chain4travel/caminojs/blob/3883166/src/common/input.ts#L22)_

---

### `Protected` sigCount

• **sigCount**: _Buffer_ = Buffer.alloc(4)

_Defined in [src/common/input.ts:42](https://github.com/chain4travel/caminojs/blob/3883166/src/common/input.ts#L42)_

---

### `Protected` sigIdxs

• **sigIdxs**: _[SigIdx](common_signature.sigidx)[]_ = []

_Defined in [src/common/input.ts:43](https://github.com/chain4travel/caminojs/blob/3883166/src/common/input.ts#L43)_

## Methods

### addSignatureIdx

▸ **addSignatureIdx**(`addressIdx`: number, `address`: Buffer): _void_

_Defined in [src/common/input.ts:82](https://github.com/chain4travel/caminojs/blob/3883166/src/common/input.ts#L82)_

Creates and adds a [SigIdx](common_signature.sigidx) to the [Input](common_inputs.input).

**Parameters:**

| Name         | Type   | Description                                             |
| ------------ | ------ | ------------------------------------------------------- |
| `addressIdx` | number | The index of the address to reference in the signatures |
| `address`    | Buffer | The address of the source of the signature              |

**Returns:** _void_

---

### `Abstract` clone

▸ **clone**(): _this_

_Defined in [src/common/input.ts:126](https://github.com/chain4travel/caminojs/blob/3883166/src/common/input.ts#L126)_

**Returns:** _this_

---

### `Abstract` create

▸ **create**(...`args`: any[]): _this_

_Defined in [src/common/input.ts:128](https://github.com/chain4travel/caminojs/blob/3883166/src/common/input.ts#L128)_

**Parameters:**

| Name      | Type  |
| --------- | ----- |
| `...args` | any[] |

**Returns:** _this_

---

### deserialize

▸ **deserialize**(`fields`: object, `encoding`: [SerializedEncoding](../modules/utils_serialization#serializedencoding)): _void_

_Overrides [StandardParseableInput](common_inputs.standardparseableinput).[deserialize](common_inputs.standardparseableinput#deserialize)_

_Defined in [src/common/input.ts:32](https://github.com/chain4travel/caminojs/blob/3883166/src/common/input.ts#L32)_

**Parameters:**

| Name       | Type                                                                    | Default |
| ---------- | ----------------------------------------------------------------------- | ------- |
| `fields`   | object                                                                  | -       |
| `encoding` | [SerializedEncoding](../modules/utils_serialization#serializedencoding) | "hex"   |

**Returns:** _void_

---

### fromBuffer

▸ **fromBuffer**(`bytes`: Buffer, `offset`: number): _number_

_Defined in [src/common/input.ts:92](https://github.com/chain4travel/caminojs/blob/3883166/src/common/input.ts#L92)_

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

_Defined in [src/common/input.ts:74](https://github.com/chain4travel/caminojs/blob/3883166/src/common/input.ts#L74)_

**Returns:** _number_

---

### `Abstract` getInputID

▸ **getInputID**(): _number_

_Defined in [src/common/input.ts:67](https://github.com/chain4travel/caminojs/blob/3883166/src/common/input.ts#L67)_

**Returns:** _number_

---

### getSigIdxs

▸ **getSigIdxs**(): _[SigIdx](common_signature.sigidx)[]_

_Defined in [src/common/input.ts:72](https://github.com/chain4travel/caminojs/blob/3883166/src/common/input.ts#L72)_

Returns the array of [SigIdx](common_signature.sigidx) for this [Input](common_inputs.input)

**Returns:** _[SigIdx](common_signature.sigidx)[]_

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

▸ **select**(`id`: number, ...`args`: any[]): _[Input](common_inputs.input)_

_Defined in [src/common/input.ts:130](https://github.com/chain4travel/caminojs/blob/3883166/src/common/input.ts#L130)_

**Parameters:**

| Name      | Type   |
| --------- | ------ |
| `id`      | number |
| `...args` | any[]  |

**Returns:** _[Input](common_inputs.input)_

---

### serialize

▸ **serialize**(`encoding`: [SerializedEncoding](../modules/utils_serialization#serializedencoding)): _object_

_Overrides [Serializable](utils_serialization.serializable).[serialize](utils_serialization.serializable#serialize)_

_Defined in [src/common/input.ts:25](https://github.com/chain4travel/caminojs/blob/3883166/src/common/input.ts#L25)_

**Parameters:**

| Name       | Type                                                                    | Default |
| ---------- | ----------------------------------------------------------------------- | ------- |
| `encoding` | [SerializedEncoding](../modules/utils_serialization#serializedencoding) | "hex"   |

**Returns:** _object_

---

### toBuffer

▸ **toBuffer**(): _Buffer_

_Defined in [src/common/input.ts:107](https://github.com/chain4travel/caminojs/blob/3883166/src/common/input.ts#L107)_

**Returns:** _Buffer_

---

### toString

▸ **toString**(): _string_

_Defined in [src/common/input.ts:122](https://github.com/chain4travel/caminojs/blob/3883166/src/common/input.ts#L122)_

Returns a base-58 representation of the [Input](common_inputs.input).

**Returns:** _string_

---

### `Static` comparator

▸ **comparator**(): _function_

_Defined in [src/common/input.ts:45](https://github.com/chain4travel/caminojs/blob/3883166/src/common/input.ts#L45)_

**Returns:** _function_

▸ (`a`: [Input](common_inputs.input), `b`: [Input](common_inputs.input)): _1 | -1 | 0_

**Parameters:**

| Name | Type                         |
| ---- | ---------------------------- |
| `a`  | [Input](common_inputs.input) |
| `b`  | [Input](common_inputs.input) |
