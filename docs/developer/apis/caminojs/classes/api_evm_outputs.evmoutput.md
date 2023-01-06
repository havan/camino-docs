# Class: EVMOutput

## Hierarchy

- **EVMOutput**

  ↳ [EVMInput](api_evm_inputs.evminput)

## Index

### Constructors

- [constructor](api_evm_outputs.evmoutput#constructor)

### Properties

- [address](api_evm_outputs.evmoutput#protected-address)
- [amount](api_evm_outputs.evmoutput#protected-amount)
- [amountValue](api_evm_outputs.evmoutput#protected-amountvalue)
- [assetID](api_evm_outputs.evmoutput#protected-assetid)

### Methods

- [clone](api_evm_outputs.evmoutput#clone)
- [create](api_evm_outputs.evmoutput#create)
- [fromBuffer](api_evm_outputs.evmoutput#frombuffer)
- [getAddress](api_evm_outputs.evmoutput#getaddress)
- [getAddressString](api_evm_outputs.evmoutput#getaddressstring)
- [getAmount](api_evm_outputs.evmoutput#getamount)
- [getAssetID](api_evm_outputs.evmoutput#getassetid)
- [toBuffer](api_evm_outputs.evmoutput#tobuffer)
- [toString](api_evm_outputs.evmoutput#tostring)
- [comparator](api_evm_outputs.evmoutput#static-comparator)

## Constructors

### constructor

\+ **new EVMOutput**(`address`: Buffer | string, `amount`: BN | number, `assetID`: Buffer | string): _[EVMOutput](api_evm_outputs.evmoutput)_

_Defined in [src/apis/evm/outputs.ts:190](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/outputs.ts#L190)_

An [EVMOutput](api_evm_outputs.evmoutput) class which contains address, amount, and assetID.

**Parameters:**

| Name      | Type                 | Default   | Description                                                                                  |
| --------- | -------------------- | --------- | -------------------------------------------------------------------------------------------- |
| `address` | Buffer &#124; string | undefined | The address recieving the asset as a [Buffer](https://github.com/feross/buffer) or a string. |
| `amount`  | BN &#124; number     | undefined | A [BN](https://github.com/indutny/bn.js/) or number representing the amount.                 |
| `assetID` | Buffer &#124; string | undefined | The assetID which is being sent as a [Buffer](https://github.com/feross/buffer) or a string. |

**Returns:** _[EVMOutput](api_evm_outputs.evmoutput)_

## Properties

### `Protected` address

• **address**: _Buffer_ = Buffer.alloc(20)

_Defined in [src/apis/evm/outputs.ts:109](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/outputs.ts#L109)_

---

### `Protected` amount

• **amount**: _Buffer_ = Buffer.alloc(8)

_Defined in [src/apis/evm/outputs.ts:110](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/outputs.ts#L110)_

---

### `Protected` amountValue

• **amountValue**: _BN_ = new BN(0)

_Defined in [src/apis/evm/outputs.ts:111](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/outputs.ts#L111)_

---

### `Protected` assetID

• **assetID**: _Buffer_ = Buffer.alloc(32)

_Defined in [src/apis/evm/outputs.ts:112](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/outputs.ts#L112)_

## Methods

### clone

▸ **clone**(): _this_

_Defined in [src/apis/evm/outputs.ts:186](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/outputs.ts#L186)_

**Returns:** _this_

---

### create

▸ **create**(...`args`: any[]): _this_

_Defined in [src/apis/evm/outputs.ts:182](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/outputs.ts#L182)_

**Parameters:**

| Name      | Type  |
| --------- | ----- |
| `...args` | any[] |

**Returns:** _this_

---

### fromBuffer

▸ **fromBuffer**(`bytes`: Buffer, `offset`: number): _number_

_Defined in [src/apis/evm/outputs.ts:165](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/outputs.ts#L165)_

Decodes the [EVMOutput](api_evm_outputs.evmoutput) as a [Buffer](https://github.com/feross/buffer) and returns the size.

**Parameters:**

| Name     | Type   | Default |
| -------- | ------ | ------- |
| `bytes`  | Buffer | -       |
| `offset` | number | 0       |

**Returns:** _number_

---

### getAddress

▸ **getAddress**(): _Buffer_

_Defined in [src/apis/evm/outputs.ts:134](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/outputs.ts#L134)_

Returns the address of the input as [Buffer](https://github.com/feross/buffer)

**Returns:** _Buffer_

---

### getAddressString

▸ **getAddressString**(): _string_

_Defined in [src/apis/evm/outputs.ts:139](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/outputs.ts#L139)_

Returns the address as a bech32 encoded string.

**Returns:** _string_

---

### getAmount

▸ **getAmount**(): _BN_

_Defined in [src/apis/evm/outputs.ts:144](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/outputs.ts#L144)_

Returns the amount as a [BN](https://github.com/indutny/bn.js/).

**Returns:** _BN_

---

### getAssetID

▸ **getAssetID**(): _Buffer_

_Defined in [src/apis/evm/outputs.ts:149](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/outputs.ts#L149)_

Returns the assetID of the input as [Buffer](https://github.com/feross/buffer)

**Returns:** _Buffer_

---

### toBuffer

▸ **toBuffer**(): _Buffer_

_Defined in [src/apis/evm/outputs.ts:154](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/outputs.ts#L154)_

Returns a [Buffer](https://github.com/feross/buffer) representation of the [EVMOutput](api_evm_outputs.evmoutput).

**Returns:** _Buffer_

---

### toString

▸ **toString**(): _string_

_Defined in [src/apis/evm/outputs.ts:178](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/outputs.ts#L178)_

Returns a base-58 representation of the [EVMOutput](api_evm_outputs.evmoutput).

**Returns:** _string_

---

### `Static` comparator

▸ **comparator**(): _function_

_Defined in [src/apis/evm/outputs.ts:117](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/outputs.ts#L117)_

Returns a function used to sort an array of [EVMOutput](api_evm_outputs.evmoutput)s

**Returns:** _function_

▸ (`a`: [EVMOutput](api_evm_outputs.evmoutput) | [EVMInput](api_evm_inputs.evminput), `b`: [EVMOutput](api_evm_outputs.evmoutput) | [EVMInput](api_evm_inputs.evminput)): _1 | -1 | 0_

**Parameters:**

| Name | Type                                                                              |
| ---- | --------------------------------------------------------------------------------- |
| `a`  | [EVMOutput](api_evm_outputs.evmoutput) &#124; [EVMInput](api_evm_inputs.evminput) |
| `b`  | [EVMOutput](api_evm_outputs.evmoutput) &#124; [EVMInput](api_evm_inputs.evminput) |
