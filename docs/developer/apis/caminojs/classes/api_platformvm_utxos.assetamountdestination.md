# Class: AssetAmountDestination

## Hierarchy

- [StandardAssetAmountDestination](common_assetamount.standardassetamountdestination)‹[TransferableOutput](api_platformvm_outputs.transferableoutput), [TransferableInput](api_platformvm_inputs.transferableinput)›

  ↳ **AssetAmountDestination**

## Index

### Constructors

- [constructor](api_platformvm_utxos.assetamountdestination#constructor)

### Properties

- [amountkey](api_platformvm_utxos.assetamountdestination#protected-amountkey)
- [amounts](api_platformvm_utxos.assetamountdestination#protected-amounts)
- [change](api_platformvm_utxos.assetamountdestination#protected-change)
- [changeAddresses](api_platformvm_utxos.assetamountdestination#protected-changeaddresses)
- [destinations](api_platformvm_utxos.assetamountdestination#protected-destinations)
- [inputs](api_platformvm_utxos.assetamountdestination#protected-inputs)
- [outputs](api_platformvm_utxos.assetamountdestination#protected-outputs)
- [senders](api_platformvm_utxos.assetamountdestination#protected-senders)

### Methods

- [addAssetAmount](api_platformvm_utxos.assetamountdestination#addassetamount)
- [addChange](api_platformvm_utxos.assetamountdestination#addchange)
- [addInput](api_platformvm_utxos.assetamountdestination#addinput)
- [addOutput](api_platformvm_utxos.assetamountdestination#addoutput)
- [assetExists](api_platformvm_utxos.assetamountdestination#assetexists)
- [canComplete](api_platformvm_utxos.assetamountdestination#cancomplete)
- [getAllOutputs](api_platformvm_utxos.assetamountdestination#getalloutputs)
- [getAmounts](api_platformvm_utxos.assetamountdestination#getamounts)
- [getAssetAmount](api_platformvm_utxos.assetamountdestination#getassetamount)
- [getChangeAddresses](api_platformvm_utxos.assetamountdestination#getchangeaddresses)
- [getChangeOutputs](api_platformvm_utxos.assetamountdestination#getchangeoutputs)
- [getDestinations](api_platformvm_utxos.assetamountdestination#getdestinations)
- [getInputs](api_platformvm_utxos.assetamountdestination#getinputs)
- [getOutputs](api_platformvm_utxos.assetamountdestination#getoutputs)
- [getSenders](api_platformvm_utxos.assetamountdestination#getsenders)

## Constructors

### constructor

\+ **new AssetAmountDestination**(`destinations`: Buffer[], `senders`: Buffer[], `changeAddresses`: Buffer[]): _[AssetAmountDestination](api_platformvm_utxos.assetamountdestination)_

_Inherited from [StandardAssetAmountDestination](common_assetamount.standardassetamountdestination).[constructor](common_assetamount.standardassetamountdestination#constructor)_

_Defined in [src/common/assetamount.ts:190](https://github.com/chain4travel/caminojs/blob/3883166/src/common/assetamount.ts#L190)_

**Parameters:**

| Name              | Type     |
| ----------------- | -------- |
| `destinations`    | Buffer[] |
| `senders`         | Buffer[] |
| `changeAddresses` | Buffer[] |

**Returns:** _[AssetAmountDestination](api_platformvm_utxos.assetamountdestination)_

## Properties

### `Protected` amountkey

• **amountkey**: _object_

_Inherited from [StandardAssetAmountDestination](common_assetamount.standardassetamountdestination).[amountkey](common_assetamount.standardassetamountdestination#protected-amountkey)_

_Defined in [src/common/assetamount.ts:118](https://github.com/chain4travel/caminojs/blob/3883166/src/common/assetamount.ts#L118)_

---

### `Protected` amounts

• **amounts**: _[AssetAmount](common_assetamount.assetamount)[]_ = []

_Inherited from [StandardAssetAmountDestination](common_assetamount.standardassetamountdestination).[amounts](common_assetamount.standardassetamountdestination#protected-amounts)_

_Defined in [src/common/assetamount.ts:114](https://github.com/chain4travel/caminojs/blob/3883166/src/common/assetamount.ts#L114)_

---

### `Protected` change

• **change**: _[TransferableOutput](api_platformvm_outputs.transferableoutput)[]_ = []

_Inherited from [StandardAssetAmountDestination](common_assetamount.standardassetamountdestination).[change](common_assetamount.standardassetamountdestination#protected-change)_

_Defined in [src/common/assetamount.ts:121](https://github.com/chain4travel/caminojs/blob/3883166/src/common/assetamount.ts#L121)_

---

### `Protected` changeAddresses

• **changeAddresses**: _Buffer[]_ = []

_Inherited from [StandardAssetAmountDestination](common_assetamount.standardassetamountdestination).[changeAddresses](common_assetamount.standardassetamountdestination#protected-changeaddresses)_

_Defined in [src/common/assetamount.ts:117](https://github.com/chain4travel/caminojs/blob/3883166/src/common/assetamount.ts#L117)_

---

### `Protected` destinations

• **destinations**: _Buffer[]_ = []

_Inherited from [StandardAssetAmountDestination](common_assetamount.standardassetamountdestination).[destinations](common_assetamount.standardassetamountdestination#protected-destinations)_

_Defined in [src/common/assetamount.ts:115](https://github.com/chain4travel/caminojs/blob/3883166/src/common/assetamount.ts#L115)_

---

### `Protected` inputs

• **inputs**: _[TransferableInput](api_platformvm_inputs.transferableinput)[]_ = []

_Inherited from [StandardAssetAmountDestination](common_assetamount.standardassetamountdestination).[inputs](common_assetamount.standardassetamountdestination#protected-inputs)_

_Defined in [src/common/assetamount.ts:119](https://github.com/chain4travel/caminojs/blob/3883166/src/common/assetamount.ts#L119)_

---

### `Protected` outputs

• **outputs**: _[TransferableOutput](api_platformvm_outputs.transferableoutput)[]_ = []

_Inherited from [StandardAssetAmountDestination](common_assetamount.standardassetamountdestination).[outputs](common_assetamount.standardassetamountdestination#protected-outputs)_

_Defined in [src/common/assetamount.ts:120](https://github.com/chain4travel/caminojs/blob/3883166/src/common/assetamount.ts#L120)_

---

### `Protected` senders

• **senders**: _Buffer[]_ = []

_Inherited from [StandardAssetAmountDestination](common_assetamount.standardassetamountdestination).[senders](common_assetamount.standardassetamountdestination#protected-senders)_

_Defined in [src/common/assetamount.ts:116](https://github.com/chain4travel/caminojs/blob/3883166/src/common/assetamount.ts#L116)_

## Methods

### addAssetAmount

▸ **addAssetAmount**(`assetID`: Buffer, `amount`: BN, `burn`: BN): _void_

_Inherited from [StandardAssetAmountDestination](common_assetamount.standardassetamountdestination).[addAssetAmount](common_assetamount.standardassetamountdestination#addassetamount)_

_Defined in [src/common/assetamount.ts:125](https://github.com/chain4travel/caminojs/blob/3883166/src/common/assetamount.ts#L125)_

**Parameters:**

| Name      | Type   |
| --------- | ------ |
| `assetID` | Buffer |
| `amount`  | BN     |
| `burn`    | BN     |

**Returns:** _void_

---

### addChange

▸ **addChange**(`output`: [TransferableOutput](api_platformvm_outputs.transferableoutput)): _void_

_Inherited from [StandardAssetAmountDestination](common_assetamount.standardassetamountdestination).[addChange](common_assetamount.standardassetamountdestination#addchange)_

_Defined in [src/common/assetamount.ts:139](https://github.com/chain4travel/caminojs/blob/3883166/src/common/assetamount.ts#L139)_

**Parameters:**

| Name     | Type                                                            |
| -------- | --------------------------------------------------------------- |
| `output` | [TransferableOutput](api_platformvm_outputs.transferableoutput) |

**Returns:** _void_

---

### addInput

▸ **addInput**(`input`: [TransferableInput](api_platformvm_inputs.transferableinput)): _void_

_Inherited from [StandardAssetAmountDestination](common_assetamount.standardassetamountdestination).[addInput](common_assetamount.standardassetamountdestination#addinput)_

_Defined in [src/common/assetamount.ts:131](https://github.com/chain4travel/caminojs/blob/3883166/src/common/assetamount.ts#L131)_

**Parameters:**

| Name    | Type                                                         |
| ------- | ------------------------------------------------------------ |
| `input` | [TransferableInput](api_platformvm_inputs.transferableinput) |

**Returns:** _void_

---

### addOutput

▸ **addOutput**(`output`: [TransferableOutput](api_platformvm_outputs.transferableoutput)): _void_

_Inherited from [StandardAssetAmountDestination](common_assetamount.standardassetamountdestination).[addOutput](common_assetamount.standardassetamountdestination#addoutput)_

_Defined in [src/common/assetamount.ts:135](https://github.com/chain4travel/caminojs/blob/3883166/src/common/assetamount.ts#L135)_

**Parameters:**

| Name     | Type                                                            |
| -------- | --------------------------------------------------------------- |
| `output` | [TransferableOutput](api_platformvm_outputs.transferableoutput) |

**Returns:** _void_

---

### assetExists

▸ **assetExists**(`assetHexStr`: string): _boolean_

_Inherited from [StandardAssetAmountDestination](common_assetamount.standardassetamountdestination).[assetExists](common_assetamount.standardassetamountdestination#assetexists)_

_Defined in [src/common/assetamount.ts:163](https://github.com/chain4travel/caminojs/blob/3883166/src/common/assetamount.ts#L163)_

**Parameters:**

| Name          | Type   |
| ------------- | ------ |
| `assetHexStr` | string |

**Returns:** _boolean_

---

### canComplete

▸ **canComplete**(): _boolean_

_Inherited from [StandardAssetAmountDestination](common_assetamount.standardassetamountdestination).[canComplete](common_assetamount.standardassetamountdestination#cancomplete)_

_Defined in [src/common/assetamount.ts:183](https://github.com/chain4travel/caminojs/blob/3883166/src/common/assetamount.ts#L183)_

**Returns:** _boolean_

---

### getAllOutputs

▸ **getAllOutputs**(): _[TransferableOutput](api_platformvm_outputs.transferableoutput)[]_

_Inherited from [StandardAssetAmountDestination](common_assetamount.standardassetamountdestination).[getAllOutputs](common_assetamount.standardassetamountdestination#getalloutputs)_

_Defined in [src/common/assetamount.ts:179](https://github.com/chain4travel/caminojs/blob/3883166/src/common/assetamount.ts#L179)_

**Returns:** _[TransferableOutput](api_platformvm_outputs.transferableoutput)[]_

---

### getAmounts

▸ **getAmounts**(): _[AssetAmount](common_assetamount.assetamount)[]_

_Inherited from [StandardAssetAmountDestination](common_assetamount.standardassetamountdestination).[getAmounts](common_assetamount.standardassetamountdestination#getamounts)_

_Defined in [src/common/assetamount.ts:143](https://github.com/chain4travel/caminojs/blob/3883166/src/common/assetamount.ts#L143)_

**Returns:** _[AssetAmount](common_assetamount.assetamount)[]_

---

### getAssetAmount

▸ **getAssetAmount**(`assetHexStr`: string): _[AssetAmount](common_assetamount.assetamount)_

_Inherited from [StandardAssetAmountDestination](common_assetamount.standardassetamountdestination).[getAssetAmount](common_assetamount.standardassetamountdestination#getassetamount)_

_Defined in [src/common/assetamount.ts:159](https://github.com/chain4travel/caminojs/blob/3883166/src/common/assetamount.ts#L159)_

**Parameters:**

| Name          | Type   |
| ------------- | ------ |
| `assetHexStr` | string |

**Returns:** _[AssetAmount](common_assetamount.assetamount)_

---

### getChangeAddresses

▸ **getChangeAddresses**(): _Buffer[]_

_Inherited from [StandardAssetAmountDestination](common_assetamount.standardassetamountdestination).[getChangeAddresses](common_assetamount.standardassetamountdestination#getchangeaddresses)_

_Defined in [src/common/assetamount.ts:155](https://github.com/chain4travel/caminojs/blob/3883166/src/common/assetamount.ts#L155)_

**Returns:** _Buffer[]_

---

### getChangeOutputs

▸ **getChangeOutputs**(): _[TransferableOutput](api_platformvm_outputs.transferableoutput)[]_

_Inherited from [StandardAssetAmountDestination](common_assetamount.standardassetamountdestination).[getChangeOutputs](common_assetamount.standardassetamountdestination#getchangeoutputs)_

_Defined in [src/common/assetamount.ts:175](https://github.com/chain4travel/caminojs/blob/3883166/src/common/assetamount.ts#L175)_

**Returns:** _[TransferableOutput](api_platformvm_outputs.transferableoutput)[]_

---

### getDestinations

▸ **getDestinations**(): _Buffer[]_

_Inherited from [StandardAssetAmountDestination](common_assetamount.standardassetamountdestination).[getDestinations](common_assetamount.standardassetamountdestination#getdestinations)_

_Defined in [src/common/assetamount.ts:147](https://github.com/chain4travel/caminojs/blob/3883166/src/common/assetamount.ts#L147)_

**Returns:** _Buffer[]_

---

### getInputs

▸ **getInputs**(): _[TransferableInput](api_platformvm_inputs.transferableinput)[]_

_Inherited from [StandardAssetAmountDestination](common_assetamount.standardassetamountdestination).[getInputs](common_assetamount.standardassetamountdestination#getinputs)_

_Defined in [src/common/assetamount.ts:167](https://github.com/chain4travel/caminojs/blob/3883166/src/common/assetamount.ts#L167)_

**Returns:** _[TransferableInput](api_platformvm_inputs.transferableinput)[]_

---

### getOutputs

▸ **getOutputs**(): _[TransferableOutput](api_platformvm_outputs.transferableoutput)[]_

_Inherited from [StandardAssetAmountDestination](common_assetamount.standardassetamountdestination).[getOutputs](common_assetamount.standardassetamountdestination#getoutputs)_

_Defined in [src/common/assetamount.ts:171](https://github.com/chain4travel/caminojs/blob/3883166/src/common/assetamount.ts#L171)_

**Returns:** _[TransferableOutput](api_platformvm_outputs.transferableoutput)[]_

---

### getSenders

▸ **getSenders**(): _Buffer[]_

_Inherited from [StandardAssetAmountDestination](common_assetamount.standardassetamountdestination).[getSenders](common_assetamount.standardassetamountdestination#getsenders)_

_Defined in [src/common/assetamount.ts:151](https://github.com/chain4travel/caminojs/blob/3883166/src/common/assetamount.ts#L151)_

**Returns:** _Buffer[]_
