# Class: AmountInput

## Hierarchy

↳ [StandardAmountInput](common_inputs.standardamountinput)

↳ **AmountInput**

↳ [SECPTransferInput](api_evm_inputs.secptransferinput)

## Index

### Constructors

- [constructor](api_evm_inputs.amountinput#constructor)

### Properties

- [\_codecID](api_evm_inputs.amountinput#protected-_codecid)
- [\_typeID](api_evm_inputs.amountinput#protected-_typeid)
- [\_typeName](api_evm_inputs.amountinput#protected-_typename)
- [amount](api_evm_inputs.amountinput#protected-amount)
- [amountValue](api_evm_inputs.amountinput#protected-amountvalue)
- [sigCount](api_evm_inputs.amountinput#protected-sigcount)
- [sigIdxs](api_evm_inputs.amountinput#protected-sigidxs)

### Methods

- [addSignatureIdx](api_evm_inputs.amountinput#addsignatureidx)
- [clone](api_evm_inputs.amountinput#abstract-clone)
- [create](api_evm_inputs.amountinput#abstract-create)
- [deserialize](api_evm_inputs.amountinput#deserialize)
- [fromBuffer](api_evm_inputs.amountinput#frombuffer)
- [getAmount](api_evm_inputs.amountinput#getamount)
- [getCodecID](api_evm_inputs.amountinput#getcodecid)
- [getCredentialID](api_evm_inputs.amountinput#abstract-getcredentialid)
- [getInputID](api_evm_inputs.amountinput#abstract-getinputid)
- [getSigIdxs](api_evm_inputs.amountinput#getsigidxs)
- [getTypeID](api_evm_inputs.amountinput#gettypeid)
- [getTypeName](api_evm_inputs.amountinput#gettypename)
- [sanitizeObject](api_evm_inputs.amountinput#sanitizeobject)
- [select](api_evm_inputs.amountinput#select)
- [serialize](api_evm_inputs.amountinput#serialize)
- [toBuffer](api_evm_inputs.amountinput#tobuffer)
- [toString](api_evm_inputs.amountinput#tostring)
- [comparator](api_evm_inputs.amountinput#static-comparator)

## Constructors

### constructor

\+ **new AmountInput**(`amount`: BN): _[AmountInput](api_evm_inputs.amountinput)_

_Inherited from [StandardAmountInput](common_inputs.standardamountinput).[constructor](common_inputs.standardamountinput#constructor)_

_Defined in [src/common/input.ts:378](https://github.com/chain4travel/caminojs/blob/3883166/src/common/input.ts#L378)_

An [AmountInput](api_evm_inputs.amountinput) class which issues a payment on an assetID.

**Parameters:**

| Name     | Type | Default   | Description                                                                    |
| -------- | ---- | --------- | ------------------------------------------------------------------------------ |
| `amount` | BN   | undefined | A [BN](https://github.com/indutny/bn.js/) representing the amount in the input |

**Returns:** _[AmountInput](api_evm_inputs.amountinput)_

## Properties

### `Protected` \_codecID

• **\_codecID**: _number_ = undefined

_Inherited from [SigIdx](common_signature.sigidx).[\_codecID](common_signature.sigidx#protected-_codecid)_

_Defined in [src/utils/serialization.ts:51](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/serialization.ts#L51)_

---

### `Protected` \_typeID

• **\_typeID**: _any_ = undefined

_Overrides [StandardAmountInput](common_inputs.standardamountinput).[\_typeID](common_inputs.standardamountinput#protected-_typeid)_

_Defined in [src/apis/evm/inputs.ts:91](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/inputs.ts#L91)_

---

### `Protected` \_typeName

• **\_typeName**: _string_ = "AmountInput"

_Overrides [StandardAmountInput](common_inputs.standardamountinput).[\_typeName](common_inputs.standardamountinput#protected-_typename)_

_Defined in [src/apis/evm/inputs.ts:90](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/inputs.ts#L90)_

---

### `Protected` amount

• **amount**: _Buffer_ = Buffer.alloc(8)

_Inherited from [StandardAmountInput](common_inputs.standardamountinput).[amount](common_inputs.standardamountinput#protected-amount)_

_Defined in [src/common/input.ts:352](https://github.com/chain4travel/caminojs/blob/3883166/src/common/input.ts#L352)_

---

### `Protected` amountValue

• **amountValue**: _BN_ = new BN(0)

_Inherited from [StandardAmountInput](common_inputs.standardamountinput).[amountValue](common_inputs.standardamountinput#protected-amountvalue)_

_Defined in [src/common/input.ts:353](https://github.com/chain4travel/caminojs/blob/3883166/src/common/input.ts#L353)_

---

### `Protected` sigCount

• **sigCount**: _Buffer_ = Buffer.alloc(4)

_Inherited from [Input](common_inputs.input).[sigCount](common_inputs.input#protected-sigcount)_

_Defined in [src/common/input.ts:42](https://github.com/chain4travel/caminojs/blob/3883166/src/common/input.ts#L42)_

---

### `Protected` sigIdxs

• **sigIdxs**: _[SigIdx](common_signature.sigidx)[]_ = []

_Inherited from [Input](common_inputs.input).[sigIdxs](common_inputs.input#protected-sigidxs)_

_Defined in [src/common/input.ts:43](https://github.com/chain4travel/caminojs/blob/3883166/src/common/input.ts#L43)_

## Methods

### addSignatureIdx

▸ **addSignatureIdx**(`addressIdx`: number, `address`: Buffer): _void_

_Inherited from [Input](common_inputs.input).[addSignatureIdx](common_inputs.input#addsignatureidx)_

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

_Inherited from [Input](common_inputs.input).[clone](common_inputs.input#abstract-clone)_

_Defined in [src/common/input.ts:126](https://github.com/chain4travel/caminojs/blob/3883166/src/common/input.ts#L126)_

**Returns:** _this_

---

### `Abstract` create

▸ **create**(...`args`: any[]): _this_

_Inherited from [Input](common_inputs.input).[create](common_inputs.input#abstract-create)_

_Defined in [src/common/input.ts:128](https://github.com/chain4travel/caminojs/blob/3883166/src/common/input.ts#L128)_

**Parameters:**

| Name      | Type  |
| --------- | ----- |
| `...args` | any[] |

**Returns:** _this_

---

### deserialize

▸ **deserialize**(`fields`: object, `encoding`: [SerializedEncoding](../modules/utils_serialization#serializedencoding)): _void_

_Inherited from [StandardAmountInput](common_inputs.standardamountinput).[deserialize](common_inputs.standardamountinput#deserialize)_

_Overrides [Input](common_inputs.input).[deserialize](common_inputs.input#deserialize)_

_Defined in [src/common/input.ts:340](https://github.com/chain4travel/caminojs/blob/3883166/src/common/input.ts#L340)_

**Parameters:**

| Name       | Type                                                                    | Default |
| ---------- | ----------------------------------------------------------------------- | ------- |
| `fields`   | object                                                                  | -       |
| `encoding` | [SerializedEncoding](../modules/utils_serialization#serializedencoding) | "hex"   |

**Returns:** _void_

---

### fromBuffer

▸ **fromBuffer**(`bytes`: Buffer, `offset`: number): _number_

_Inherited from [StandardAmountInput](common_inputs.standardamountinput).[fromBuffer](common_inputs.standardamountinput#frombuffer)_

_Overrides [Input](common_inputs.input).[fromBuffer](common_inputs.input#frombuffer)_

_Defined in [src/common/input.ts:363](https://github.com/chain4travel/caminojs/blob/3883166/src/common/input.ts#L363)_

Popuates the instance from a [Buffer](https://github.com/feross/buffer) representing the [AmountInput](api_evm_inputs.amountinput) and returns the size of the input.

**Parameters:**

| Name     | Type   | Default |
| -------- | ------ | ------- |
| `bytes`  | Buffer | -       |
| `offset` | number | 0       |

**Returns:** _number_

---

### getAmount

▸ **getAmount**(): _BN_

_Inherited from [StandardAmountInput](common_inputs.standardamountinput).[getAmount](common_inputs.standardamountinput#getamount)_

_Defined in [src/common/input.ts:358](https://github.com/chain4travel/caminojs/blob/3883166/src/common/input.ts#L358)_

Returns the amount as a [BN](https://github.com/indutny/bn.js/).

**Returns:** _BN_

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

_Inherited from [Input](common_inputs.input).[getCredentialID](common_inputs.input#abstract-getcredentialid)_

_Defined in [src/common/input.ts:74](https://github.com/chain4travel/caminojs/blob/3883166/src/common/input.ts#L74)_

**Returns:** _number_

---

### `Abstract` getInputID

▸ **getInputID**(): _number_

_Inherited from [Input](common_inputs.input).[getInputID](common_inputs.input#abstract-getinputid)_

_Defined in [src/common/input.ts:67](https://github.com/chain4travel/caminojs/blob/3883166/src/common/input.ts#L67)_

**Returns:** _number_

---

### getSigIdxs

▸ **getSigIdxs**(): _[SigIdx](common_signature.sigidx)[]_

_Inherited from [Input](common_inputs.input).[getSigIdxs](common_inputs.input#getsigidxs)_

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

### select

▸ **select**(`id`: number, ...`args`: any[]): _[Input](common_inputs.input)_

_Overrides [Input](common_inputs.input).[select](common_inputs.input#abstract-select)_

_Defined in [src/apis/evm/inputs.ts:95](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/inputs.ts#L95)_

**Parameters:**

| Name      | Type   |
| --------- | ------ |
| `id`      | number |
| `...args` | any[]  |

**Returns:** _[Input](common_inputs.input)_

---

### serialize

▸ **serialize**(`encoding`: [SerializedEncoding](../modules/utils_serialization#serializedencoding)): _object_

_Inherited from [StandardAmountInput](common_inputs.standardamountinput).[serialize](common_inputs.standardamountinput#serialize)_

_Overrides [Input](common_inputs.input).[serialize](common_inputs.input#serialize)_

_Defined in [src/common/input.ts:327](https://github.com/chain4travel/caminojs/blob/3883166/src/common/input.ts#L327)_

**Parameters:**

| Name       | Type                                                                    | Default |
| ---------- | ----------------------------------------------------------------------- | ------- |
| `encoding` | [SerializedEncoding](../modules/utils_serialization#serializedencoding) | "hex"   |

**Returns:** _object_

---

### toBuffer

▸ **toBuffer**(): _Buffer_

_Inherited from [StandardAmountInput](common_inputs.standardamountinput).[toBuffer](common_inputs.standardamountinput#tobuffer)_

_Overrides [Input](common_inputs.input).[toBuffer](common_inputs.input#tobuffer)_

_Defined in [src/common/input.ts:373](https://github.com/chain4travel/caminojs/blob/3883166/src/common/input.ts#L373)_

Returns the buffer representing the [AmountInput](api_evm_inputs.amountinput) instance.

**Returns:** _Buffer_

---

### toString

▸ **toString**(): _string_

_Inherited from [Input](common_inputs.input).[toString](common_inputs.input#tostring)_

_Defined in [src/common/input.ts:122](https://github.com/chain4travel/caminojs/blob/3883166/src/common/input.ts#L122)_

Returns a base-58 representation of the [Input](common_inputs.input).

**Returns:** _string_

---

### `Static` comparator

▸ **comparator**(): _function_

_Inherited from [Input](common_inputs.input).[comparator](common_inputs.input#static-comparator)_

_Defined in [src/common/input.ts:45](https://github.com/chain4travel/caminojs/blob/3883166/src/common/input.ts#L45)_

**Returns:** _function_

▸ (`a`: [Input](common_inputs.input), `b`: [Input](common_inputs.input)): _1 | -1 | 0_

**Parameters:**

| Name | Type                         |
| ---- | ---------------------------- |
| `a`  | [Input](common_inputs.input) |
| `b`  | [Input](common_inputs.input) |