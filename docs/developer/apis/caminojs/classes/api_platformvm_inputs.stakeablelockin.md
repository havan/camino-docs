# Class: StakeableLockIn

An [Input](common_inputs.input) class which specifies an input that has a locktime which can also enable staking of the value held, preventing transfers but not validation.

## Hierarchy

↳ [AmountInput](api_platformvm_inputs.amountinput)

↳ **StakeableLockIn**

## Index

### Constructors

- [constructor](api_platformvm_inputs.stakeablelockin#constructor)

### Properties

- [\_codecID](api_platformvm_inputs.stakeablelockin#protected-_codecid)
- [\_typeID](api_platformvm_inputs.stakeablelockin#protected-_typeid)
- [\_typeName](api_platformvm_inputs.stakeablelockin#protected-_typename)
- [amount](api_platformvm_inputs.stakeablelockin#protected-amount)
- [amountValue](api_platformvm_inputs.stakeablelockin#protected-amountvalue)
- [sigCount](api_platformvm_inputs.stakeablelockin#protected-sigcount)
- [sigIdxs](api_platformvm_inputs.stakeablelockin#protected-sigidxs)
- [stakeableLocktime](api_platformvm_inputs.stakeablelockin#protected-stakeablelocktime)
- [transferableInput](api_platformvm_inputs.stakeablelockin#protected-transferableinput)

### Methods

- [addSignatureIdx](api_platformvm_inputs.stakeablelockin#addsignatureidx)
- [clone](api_platformvm_inputs.stakeablelockin#clone)
- [create](api_platformvm_inputs.stakeablelockin#create)
- [deserialize](api_platformvm_inputs.stakeablelockin#deserialize)
- [fromBuffer](api_platformvm_inputs.stakeablelockin#frombuffer)
- [getAmount](api_platformvm_inputs.stakeablelockin#getamount)
- [getCodecID](api_platformvm_inputs.stakeablelockin#getcodecid)
- [getCredentialID](api_platformvm_inputs.stakeablelockin#getcredentialid)
- [getInputID](api_platformvm_inputs.stakeablelockin#getinputid)
- [getSigIdxs](api_platformvm_inputs.stakeablelockin#getsigidxs)
- [getStakeableLocktime](api_platformvm_inputs.stakeablelockin#getstakeablelocktime)
- [getTransferablInput](api_platformvm_inputs.stakeablelockin#gettransferablinput)
- [getTypeID](api_platformvm_inputs.stakeablelockin#gettypeid)
- [getTypeName](api_platformvm_inputs.stakeablelockin#gettypename)
- [sanitizeObject](api_platformvm_inputs.stakeablelockin#sanitizeobject)
- [select](api_platformvm_inputs.stakeablelockin#select)
- [serialize](api_platformvm_inputs.stakeablelockin#serialize)
- [synchronize](api_platformvm_inputs.stakeablelockin#private-synchronize)
- [toBuffer](api_platformvm_inputs.stakeablelockin#tobuffer)
- [toString](api_platformvm_inputs.stakeablelockin#tostring)
- [comparator](api_platformvm_inputs.stakeablelockin#static-comparator)

## Constructors

### constructor

\+ **new StakeableLockIn**(`amount`: BN, `stakeableLocktime`: BN, `transferableInput`: [ParseableInput](api_platformvm_inputs.parseableinput)): _[StakeableLockIn](api_platformvm_inputs.stakeablelockin)_

_Overrides [StandardAmountInput](common_inputs.standardamountinput).[constructor](common_inputs.standardamountinput#constructor)_

_Defined in [src/apis/platformvm/inputs.ts:245](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/inputs.ts#L245)_

A [Output](../modules/src_common#output) class which specifies an [Input](common_inputs.input) that has a locktime which can also enable staking of the value held, preventing transfers but not validation.

**Parameters:**

| Name                | Type                                                   | Default   | Description                                                                                 |
| ------------------- | ------------------------------------------------------ | --------- | ------------------------------------------------------------------------------------------- |
| `amount`            | BN                                                     | undefined | A [BN](https://github.com/indutny/bn.js/) representing the amount in the input              |
| `stakeableLocktime` | BN                                                     | undefined | A [BN](https://github.com/indutny/bn.js/) representing the stakeable locktime               |
| `transferableInput` | [ParseableInput](api_platformvm_inputs.parseableinput) | undefined | A [ParseableInput](api_platformvm_inputs.parseableinput) which is embedded into this input. |

**Returns:** _[StakeableLockIn](api_platformvm_inputs.stakeablelockin)_

## Properties

### `Protected` \_codecID

• **\_codecID**: _number_ = undefined

_Inherited from [SigIdx](common_signature.sigidx).[\_codecID](common_signature.sigidx#protected-_codecid)_

_Defined in [src/utils/serialization.ts:51](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/serialization.ts#L51)_

---

### `Protected` \_typeID

• **\_typeID**: _number_ = PlatformVMConstants.STAKEABLELOCKINID

_Overrides [AmountInput](api_platformvm_inputs.amountinput).[\_typeID](api_platformvm_inputs.amountinput#protected-_typeid)_

_Defined in [src/apis/platformvm/inputs.ts:144](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/inputs.ts#L144)_

---

### `Protected` \_typeName

• **\_typeName**: _string_ = "StakeableLockIn"

_Overrides [AmountInput](api_platformvm_inputs.amountinput).[\_typeName](api_platformvm_inputs.amountinput#protected-_typename)_

_Defined in [src/apis/platformvm/inputs.ts:143](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/inputs.ts#L143)_

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

---

### `Protected` stakeableLocktime

• **stakeableLocktime**: _Buffer_

_Defined in [src/apis/platformvm/inputs.ts:183](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/inputs.ts#L183)_

---

### `Protected` transferableInput

• **transferableInput**: _[ParseableInput](api_platformvm_inputs.parseableinput)_

_Defined in [src/apis/platformvm/inputs.ts:184](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/inputs.ts#L184)_

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

### clone

▸ **clone**(): _this_

_Overrides [Input](common_inputs.input).[clone](common_inputs.input#abstract-clone)_

_Defined in [src/apis/platformvm/inputs.ts:237](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/inputs.ts#L237)_

**Returns:** _this_

---

### create

▸ **create**(...`args`: any[]): _this_

_Overrides [Input](common_inputs.input).[create](common_inputs.input#abstract-create)_

_Defined in [src/apis/platformvm/inputs.ts:233](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/inputs.ts#L233)_

**Parameters:**

| Name      | Type  |
| --------- | ----- |
| `...args` | any[] |

**Returns:** _this_

---

### deserialize

▸ **deserialize**(`fields`: object, `encoding`: [SerializedEncoding](../modules/utils_serialization#serializedencoding)): _void_

_Overrides [StandardAmountInput](common_inputs.standardamountinput).[deserialize](common_inputs.standardamountinput#deserialize)_

_Defined in [src/apis/platformvm/inputs.ts:166](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/inputs.ts#L166)_

**Parameters:**

| Name       | Type                                                                    | Default |
| ---------- | ----------------------------------------------------------------------- | ------- |
| `fields`   | object                                                                  | -       |
| `encoding` | [SerializedEncoding](../modules/utils_serialization#serializedencoding) | "hex"   |

**Returns:** _void_

---

### fromBuffer

▸ **fromBuffer**(`bytes`: Buffer, `offset`: number): _number_

_Overrides [StandardAmountInput](common_inputs.standardamountinput).[fromBuffer](common_inputs.standardamountinput#frombuffer)_

_Defined in [src/apis/platformvm/inputs.ts:214](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/inputs.ts#L214)_

Popuates the instance from a [Buffer](https://github.com/feross/buffer) representing the [StakeableLockIn](api_platformvm_inputs.stakeablelockin) and returns the size of the output.

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

### getCredentialID

▸ **getCredentialID**(): _number_

_Overrides [Input](common_inputs.input).[getCredentialID](common_inputs.input#abstract-getcredentialid)_

_Defined in [src/apis/platformvm/inputs.ts:209](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/inputs.ts#L209)_

**Returns:** _number_

---

### getInputID

▸ **getInputID**(): _number_

_Overrides [Input](common_inputs.input).[getInputID](common_inputs.input#abstract-getinputid)_

_Defined in [src/apis/platformvm/inputs.ts:205](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/inputs.ts#L205)_

Returns the inputID for this input

**Returns:** _number_

---

### getSigIdxs

▸ **getSigIdxs**(): _[SigIdx](common_signature.sigidx)[]_

_Inherited from [Input](common_inputs.input).[getSigIdxs](common_inputs.input#getsigidxs)_

_Defined in [src/common/input.ts:72](https://github.com/chain4travel/caminojs/blob/3883166/src/common/input.ts#L72)_

Returns the array of [SigIdx](common_signature.sigidx) for this [Input](common_inputs.input)

**Returns:** _[SigIdx](common_signature.sigidx)[]_

---

### getStakeableLocktime

▸ **getStakeableLocktime**(): _BN_

_Defined in [src/apis/platformvm/inputs.ts:195](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/inputs.ts#L195)_

**Returns:** _BN_

---

### getTransferablInput

▸ **getTransferablInput**(): _[ParseableInput](api_platformvm_inputs.parseableinput)_

_Defined in [src/apis/platformvm/inputs.ts:199](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/inputs.ts#L199)_

**Returns:** _[ParseableInput](api_platformvm_inputs.parseableinput)_

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

_Overrides [AmountInput](api_platformvm_inputs.amountinput).[select](api_platformvm_inputs.amountinput#select)_

_Defined in [src/apis/platformvm/inputs.ts:243](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/inputs.ts#L243)_

**Parameters:**

| Name      | Type   |
| --------- | ------ |
| `id`      | number |
| `...args` | any[]  |

**Returns:** _[Input](common_inputs.input)_

---

### serialize

▸ **serialize**(`encoding`: [SerializedEncoding](../modules/utils_serialization#serializedencoding)): _object_

_Overrides [StandardAmountInput](common_inputs.standardamountinput).[serialize](common_inputs.standardamountinput#serialize)_

_Defined in [src/apis/platformvm/inputs.ts:148](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/inputs.ts#L148)_

**Parameters:**

| Name       | Type                                                                    | Default |
| ---------- | ----------------------------------------------------------------------- | ------- |
| `encoding` | [SerializedEncoding](../modules/utils_serialization#serializedencoding) | "hex"   |

**Returns:** _object_

---

### `Private` synchronize

▸ **synchronize**(): _void_

_Defined in [src/apis/platformvm/inputs.ts:186](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/inputs.ts#L186)_

**Returns:** _void_

---

### toBuffer

▸ **toBuffer**(): _Buffer_

_Overrides [StandardAmountInput](common_inputs.standardamountinput).[toBuffer](common_inputs.standardamountinput#tobuffer)_

_Defined in [src/apis/platformvm/inputs.ts:226](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/inputs.ts#L226)_

Returns the buffer representing the [StakeableLockIn](api_platformvm_inputs.stakeablelockin) instance.

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
