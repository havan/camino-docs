# Class: EVMInput

## Hierarchy

- [EVMOutput](api_evm_outputs.evmoutput)

  ↳ **EVMInput**

## Index

### Constructors

- [constructor](api_evm_inputs.evminput#constructor)

### Properties

- [address](api_evm_inputs.evminput#protected-address)
- [amount](api_evm_inputs.evminput#protected-amount)
- [amountValue](api_evm_inputs.evminput#protected-amountvalue)
- [assetID](api_evm_inputs.evminput#protected-assetid)
- [nonce](api_evm_inputs.evminput#protected-nonce)
- [nonceValue](api_evm_inputs.evminput#protected-noncevalue)
- [sigCount](api_evm_inputs.evminput#protected-sigcount)
- [sigIdxs](api_evm_inputs.evminput#protected-sigidxs)

### Methods

- [addSignatureIdx](api_evm_inputs.evminput#addsignatureidx)
- [clone](api_evm_inputs.evminput#clone)
- [create](api_evm_inputs.evminput#create)
- [fromBuffer](api_evm_inputs.evminput#frombuffer)
- [getAddress](api_evm_inputs.evminput#getaddress)
- [getAddressString](api_evm_inputs.evminput#getaddressstring)
- [getAmount](api_evm_inputs.evminput#getamount)
- [getAssetID](api_evm_inputs.evminput#getassetid)
- [getCredentialID](api_evm_inputs.evminput#getcredentialid)
- [getNonce](api_evm_inputs.evminput#getnonce)
- [getSigIdxs](api_evm_inputs.evminput#getsigidxs)
- [toBuffer](api_evm_inputs.evminput#tobuffer)
- [toString](api_evm_inputs.evminput#tostring)
- [comparator](api_evm_inputs.evminput#static-comparator)

## Constructors

### constructor

\+ **new EVMInput**(`address`: Buffer | string, `amount`: BN | number, `assetID`: Buffer | string, `nonce`: BN | number): _[EVMInput](api_evm_inputs.evminput)_

_Overrides [EVMOutput](api_evm_outputs.evmoutput).[constructor](api_evm_outputs.evmoutput#constructor)_

_Defined in [src/apis/evm/inputs.ts:198](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/inputs.ts#L198)_

An [EVMInput](api_evm_inputs.evminput) class which contains address, amount, assetID, nonce.

**Parameters:**

| Name      | Type                 | Default   | Description                                                                                                                    |
| --------- | -------------------- | --------- | ------------------------------------------------------------------------------------------------------------------------------ |
| `address` | Buffer &#124; string | undefined | is the EVM address from which to transfer funds.                                                                               |
| `amount`  | BN &#124; number     | undefined | is the amount of the asset to be transferred (specified in nAVAX for AVAX and the smallest denomination for all other assets). |
| `assetID` | Buffer &#124; string | undefined | The assetID which is being sent as a [Buffer](https://github.com/feross/buffer) or as a string.                                |
| `nonce`   | BN &#124; number     | undefined | A [BN](https://github.com/indutny/bn.js/) or a number representing the nonce.                                                  |

**Returns:** _[EVMInput](api_evm_inputs.evminput)_

## Properties

### `Protected` address

• **address**: _Buffer_ = Buffer.alloc(20)

_Inherited from [EVMInput](api_evm_inputs.evminput).[address](api_evm_inputs.evminput#protected-address)_

_Defined in [src/apis/evm/outputs.ts:109](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/outputs.ts#L109)_

---

### `Protected` amount

• **amount**: _Buffer_ = Buffer.alloc(8)

_Inherited from [EVMInput](api_evm_inputs.evminput).[amount](api_evm_inputs.evminput#protected-amount)_

_Defined in [src/apis/evm/outputs.ts:110](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/outputs.ts#L110)_

---

### `Protected` amountValue

• **amountValue**: _BN_ = new BN(0)

_Inherited from [EVMInput](api_evm_inputs.evminput).[amountValue](api_evm_inputs.evminput#protected-amountvalue)_

_Defined in [src/apis/evm/outputs.ts:111](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/outputs.ts#L111)_

---

### `Protected` assetID

• **assetID**: _Buffer_ = Buffer.alloc(32)

_Inherited from [EVMInput](api_evm_inputs.evminput).[assetID](api_evm_inputs.evminput#protected-assetid)_

_Defined in [src/apis/evm/outputs.ts:112](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/outputs.ts#L112)_

---

### `Protected` nonce

• **nonce**: _Buffer_ = Buffer.alloc(8)

_Defined in [src/apis/evm/inputs.ts:127](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/inputs.ts#L127)_

---

### `Protected` nonceValue

• **nonceValue**: _BN_ = new BN(0)

_Defined in [src/apis/evm/inputs.ts:128](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/inputs.ts#L128)_

---

### `Protected` sigCount

• **sigCount**: _Buffer_ = Buffer.alloc(4)

_Defined in [src/apis/evm/inputs.ts:129](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/inputs.ts#L129)_

---

### `Protected` sigIdxs

• **sigIdxs**: _[SigIdx](common_signature.sigidx)[]_ = []

_Defined in [src/apis/evm/inputs.ts:130](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/inputs.ts#L130)_

## Methods

### addSignatureIdx

▸ **addSignatureIdx**(`addressIdx`: number, `address`: Buffer): _void_

_Defined in [src/apis/evm/inputs.ts:143](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/inputs.ts#L143)_

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

_Overrides [EVMOutput](api_evm_outputs.evmoutput).[clone](api_evm_outputs.evmoutput#clone)_

_Defined in [src/apis/evm/inputs.ts:194](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/inputs.ts#L194)_

**Returns:** _this_

---

### create

▸ **create**(...`args`: any[]): _this_

_Overrides [EVMOutput](api_evm_outputs.evmoutput).[create](api_evm_outputs.evmoutput#create)_

_Defined in [src/apis/evm/inputs.ts:190](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/inputs.ts#L190)_

**Parameters:**

| Name      | Type  |
| --------- | ----- |
| `...args` | any[] |

**Returns:** _this_

---

### fromBuffer

▸ **fromBuffer**(`bytes`: Buffer, `offset`: number): _number_

_Overrides [EVMOutput](api_evm_outputs.evmoutput).[fromBuffer](api_evm_outputs.evmoutput#frombuffer)_

_Defined in [src/apis/evm/inputs.ts:176](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/inputs.ts#L176)_

Decodes the [EVMInput](api_evm_inputs.evminput) as a [Buffer](https://github.com/feross/buffer) and returns the size.

**Parameters:**

| Name     | Type   | Default | Description                                                |
| -------- | ------ | ------- | ---------------------------------------------------------- |
| `bytes`  | Buffer | -       | The bytes as a [Buffer](https://github.com/feross/buffer). |
| `offset` | number | 0       | An offset as a number.                                     |

**Returns:** _number_

---

### getAddress

▸ **getAddress**(): _Buffer_

_Inherited from [EVMInput](api_evm_inputs.evminput).[getAddress](api_evm_inputs.evminput#getaddress)_

_Defined in [src/apis/evm/outputs.ts:134](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/outputs.ts#L134)_

Returns the address of the input as [Buffer](https://github.com/feross/buffer)

**Returns:** _Buffer_

---

### getAddressString

▸ **getAddressString**(): _string_

_Inherited from [EVMInput](api_evm_inputs.evminput).[getAddressString](api_evm_inputs.evminput#getaddressstring)_

_Defined in [src/apis/evm/outputs.ts:139](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/outputs.ts#L139)_

Returns the address as a bech32 encoded string.

**Returns:** _string_

---

### getAmount

▸ **getAmount**(): _BN_

_Inherited from [EVMInput](api_evm_inputs.evminput).[getAmount](api_evm_inputs.evminput#getamount)_

_Defined in [src/apis/evm/outputs.ts:144](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/outputs.ts#L144)_

Returns the amount as a [BN](https://github.com/indutny/bn.js/).

**Returns:** _BN_

---

### getAssetID

▸ **getAssetID**(): _Buffer_

_Inherited from [EVMInput](api_evm_inputs.evminput).[getAssetID](api_evm_inputs.evminput#getassetid)_

_Defined in [src/apis/evm/outputs.ts:149](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/outputs.ts#L149)_

Returns the assetID of the input as [Buffer](https://github.com/feross/buffer)

**Returns:** _Buffer_

---

### getCredentialID

▸ **getCredentialID**(): _number_

_Defined in [src/apis/evm/inputs.ts:168](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/inputs.ts#L168)_

**Returns:** _number_

---

### getNonce

▸ **getNonce**(): _BN_

_Defined in [src/apis/evm/inputs.ts:156](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/inputs.ts#L156)_

Returns the nonce as a [BN](https://github.com/indutny/bn.js/).

**Returns:** _BN_

---

### getSigIdxs

▸ **getSigIdxs**(): _[SigIdx](common_signature.sigidx)[]_

_Defined in [src/apis/evm/inputs.ts:135](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/inputs.ts#L135)_

Returns the array of [SigIdx](common_signature.sigidx) for this [Input](common_inputs.input)

**Returns:** _[SigIdx](common_signature.sigidx)[]_

---

### toBuffer

▸ **toBuffer**(): _Buffer_

_Overrides [EVMOutput](api_evm_outputs.evmoutput).[toBuffer](api_evm_outputs.evmoutput#tobuffer)_

_Defined in [src/apis/evm/inputs.ts:161](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/inputs.ts#L161)_

Returns a [Buffer](https://github.com/feross/buffer) representation of the [EVMOutput](api_evm_outputs.evmoutput).

**Returns:** _Buffer_

---

### toString

▸ **toString**(): _string_

_Overrides [EVMOutput](api_evm_outputs.evmoutput).[toString](api_evm_outputs.evmoutput#tostring)_

_Defined in [src/apis/evm/inputs.ts:186](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/inputs.ts#L186)_

Returns a base-58 representation of the [EVMInput](api_evm_inputs.evminput).

**Returns:** _string_

---

### `Static` comparator

▸ **comparator**(): _function_

_Inherited from [EVMInput](api_evm_inputs.evminput).[comparator](api_evm_inputs.evminput#static-comparator)_

_Defined in [src/apis/evm/outputs.ts:117](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/outputs.ts#L117)_

Returns a function used to sort an array of [EVMOutput](api_evm_outputs.evmoutput)s

**Returns:** _function_

▸ (`a`: [EVMOutput](api_evm_outputs.evmoutput) | [EVMInput](api_evm_inputs.evminput), `b`: [EVMOutput](api_evm_outputs.evmoutput) | [EVMInput](api_evm_inputs.evminput)): _1 | -1 | 0_

**Parameters:**

| Name | Type                                                                              |
| ---- | --------------------------------------------------------------------------------- |
| `a`  | [EVMOutput](api_evm_outputs.evmoutput) &#124; [EVMInput](api_evm_inputs.evminput) |
| `b`  | [EVMOutput](api_evm_outputs.evmoutput) &#124; [EVMInput](api_evm_inputs.evminput) |
