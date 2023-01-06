# Class: StandardAssetAmountDestination ‹**TO, TI**›

## Type parameters

▪ **TO**: _[StandardTransferableOutput](common_output.standardtransferableoutput)_

▪ **TI**: _[StandardTransferableInput](common_inputs.standardtransferableinput)_

## Hierarchy

- **StandardAssetAmountDestination**

  ↳ [AssetAmountDestination](api_evm_utxos.assetamountdestination)

  ↳ [AssetAmountDestination](api_avm_utxos.assetamountdestination)

  ↳ [AssetAmountDestination](api_platformvm_utxos.assetamountdestination)

## Index

### Constructors

- [constructor](common_assetamount.standardassetamountdestination#constructor)

### Properties

- [amountkey](common_assetamount.standardassetamountdestination#protected-amountkey)
- [amounts](common_assetamount.standardassetamountdestination#protected-amounts)
- [change](common_assetamount.standardassetamountdestination#protected-change)
- [changeAddresses](common_assetamount.standardassetamountdestination#protected-changeaddresses)
- [destinations](common_assetamount.standardassetamountdestination#protected-destinations)
- [inputs](common_assetamount.standardassetamountdestination#protected-inputs)
- [outputs](common_assetamount.standardassetamountdestination#protected-outputs)
- [senders](common_assetamount.standardassetamountdestination#protected-senders)

### Methods

- [addAssetAmount](common_assetamount.standardassetamountdestination#addassetamount)
- [addChange](common_assetamount.standardassetamountdestination#addchange)
- [addInput](common_assetamount.standardassetamountdestination#addinput)
- [addOutput](common_assetamount.standardassetamountdestination#addoutput)
- [assetExists](common_assetamount.standardassetamountdestination#assetexists)
- [canComplete](common_assetamount.standardassetamountdestination#cancomplete)
- [getAllOutputs](common_assetamount.standardassetamountdestination#getalloutputs)
- [getAmounts](common_assetamount.standardassetamountdestination#getamounts)
- [getAssetAmount](common_assetamount.standardassetamountdestination#getassetamount)
- [getChangeAddresses](common_assetamount.standardassetamountdestination#getchangeaddresses)
- [getChangeOutputs](common_assetamount.standardassetamountdestination#getchangeoutputs)
- [getDestinations](common_assetamount.standardassetamountdestination#getdestinations)
- [getInputs](common_assetamount.standardassetamountdestination#getinputs)
- [getOutputs](common_assetamount.standardassetamountdestination#getoutputs)
- [getSenders](common_assetamount.standardassetamountdestination#getsenders)

## Constructors

### constructor

\+ **new StandardAssetAmountDestination**(`destinations`: Buffer[], `senders`: Buffer[], `changeAddresses`: Buffer[]): _[StandardAssetAmountDestination](common_assetamount.standardassetamountdestination)_

_Defined in [src/common/assetamount.ts:190](https://github.com/chain4travel/caminojs/blob/3883166/src/common/assetamount.ts#L190)_

**Parameters:**

| Name              | Type     |
| ----------------- | -------- |
| `destinations`    | Buffer[] |
| `senders`         | Buffer[] |
| `changeAddresses` | Buffer[] |

**Returns:** _[StandardAssetAmountDestination](common_assetamount.standardassetamountdestination)_

## Properties

### `Protected` amountkey

• **amountkey**: _object_

_Defined in [src/common/assetamount.ts:118](https://github.com/chain4travel/caminojs/blob/3883166/src/common/assetamount.ts#L118)_

---

### `Protected` amounts

• **amounts**: _[AssetAmount](common_assetamount.assetamount)[]_ = []

_Defined in [src/common/assetamount.ts:114](https://github.com/chain4travel/caminojs/blob/3883166/src/common/assetamount.ts#L114)_

---

### `Protected` change

• **change**: _TO[]_ = []

_Defined in [src/common/assetamount.ts:121](https://github.com/chain4travel/caminojs/blob/3883166/src/common/assetamount.ts#L121)_

---

### `Protected` changeAddresses

• **changeAddresses**: _Buffer[]_ = []

_Defined in [src/common/assetamount.ts:117](https://github.com/chain4travel/caminojs/blob/3883166/src/common/assetamount.ts#L117)_

---

### `Protected` destinations

• **destinations**: _Buffer[]_ = []

_Defined in [src/common/assetamount.ts:115](https://github.com/chain4travel/caminojs/blob/3883166/src/common/assetamount.ts#L115)_

---

### `Protected` inputs

• **inputs**: _TI[]_ = []

_Defined in [src/common/assetamount.ts:119](https://github.com/chain4travel/caminojs/blob/3883166/src/common/assetamount.ts#L119)_

---

### `Protected` outputs

• **outputs**: _TO[]_ = []

_Defined in [src/common/assetamount.ts:120](https://github.com/chain4travel/caminojs/blob/3883166/src/common/assetamount.ts#L120)_

---

### `Protected` senders

• **senders**: _Buffer[]_ = []

_Defined in [src/common/assetamount.ts:116](https://github.com/chain4travel/caminojs/blob/3883166/src/common/assetamount.ts#L116)_

## Methods

### addAssetAmount

▸ **addAssetAmount**(`assetID`: Buffer, `amount`: BN, `burn`: BN): _void_

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

▸ **addChange**(`output`: TO): _void_

_Defined in [src/common/assetamount.ts:139](https://github.com/chain4travel/caminojs/blob/3883166/src/common/assetamount.ts#L139)_

**Parameters:**

| Name     | Type |
| -------- | ---- |
| `output` | TO   |

**Returns:** _void_

---

### addInput

▸ **addInput**(`input`: TI): _void_

_Defined in [src/common/assetamount.ts:131](https://github.com/chain4travel/caminojs/blob/3883166/src/common/assetamount.ts#L131)_

**Parameters:**

| Name    | Type |
| ------- | ---- |
| `input` | TI   |

**Returns:** _void_

---

### addOutput

▸ **addOutput**(`output`: TO): _void_

_Defined in [src/common/assetamount.ts:135](https://github.com/chain4travel/caminojs/blob/3883166/src/common/assetamount.ts#L135)_

**Parameters:**

| Name     | Type |
| -------- | ---- |
| `output` | TO   |

**Returns:** _void_

---

### assetExists

▸ **assetExists**(`assetHexStr`: string): _boolean_

_Defined in [src/common/assetamount.ts:163](https://github.com/chain4travel/caminojs/blob/3883166/src/common/assetamount.ts#L163)_

**Parameters:**

| Name          | Type   |
| ------------- | ------ |
| `assetHexStr` | string |

**Returns:** _boolean_

---

### canComplete

▸ **canComplete**(): _boolean_

_Defined in [src/common/assetamount.ts:183](https://github.com/chain4travel/caminojs/blob/3883166/src/common/assetamount.ts#L183)_

**Returns:** _boolean_

---

### getAllOutputs

▸ **getAllOutputs**(): _TO[]_

_Defined in [src/common/assetamount.ts:179](https://github.com/chain4travel/caminojs/blob/3883166/src/common/assetamount.ts#L179)_

**Returns:** _TO[]_

---

### getAmounts

▸ **getAmounts**(): _[AssetAmount](common_assetamount.assetamount)[]_

_Defined in [src/common/assetamount.ts:143](https://github.com/chain4travel/caminojs/blob/3883166/src/common/assetamount.ts#L143)_

**Returns:** _[AssetAmount](common_assetamount.assetamount)[]_

---

### getAssetAmount

▸ **getAssetAmount**(`assetHexStr`: string): _[AssetAmount](common_assetamount.assetamount)_

_Defined in [src/common/assetamount.ts:159](https://github.com/chain4travel/caminojs/blob/3883166/src/common/assetamount.ts#L159)_

**Parameters:**

| Name          | Type   |
| ------------- | ------ |
| `assetHexStr` | string |

**Returns:** _[AssetAmount](common_assetamount.assetamount)_

---

### getChangeAddresses

▸ **getChangeAddresses**(): _Buffer[]_

_Defined in [src/common/assetamount.ts:155](https://github.com/chain4travel/caminojs/blob/3883166/src/common/assetamount.ts#L155)_

**Returns:** _Buffer[]_

---

### getChangeOutputs

▸ **getChangeOutputs**(): _TO[]_

_Defined in [src/common/assetamount.ts:175](https://github.com/chain4travel/caminojs/blob/3883166/src/common/assetamount.ts#L175)_

**Returns:** _TO[]_

---

### getDestinations

▸ **getDestinations**(): _Buffer[]_

_Defined in [src/common/assetamount.ts:147](https://github.com/chain4travel/caminojs/blob/3883166/src/common/assetamount.ts#L147)_

**Returns:** _Buffer[]_

---

### getInputs

▸ **getInputs**(): _TI[]_

_Defined in [src/common/assetamount.ts:167](https://github.com/chain4travel/caminojs/blob/3883166/src/common/assetamount.ts#L167)_

**Returns:** _TI[]_

---

### getOutputs

▸ **getOutputs**(): _TO[]_

_Defined in [src/common/assetamount.ts:171](https://github.com/chain4travel/caminojs/blob/3883166/src/common/assetamount.ts#L171)_

**Returns:** _TO[]_

---

### getSenders

▸ **getSenders**(): _Buffer[]_

_Defined in [src/common/assetamount.ts:151](https://github.com/chain4travel/caminojs/blob/3883166/src/common/assetamount.ts#L151)_

**Returns:** _Buffer[]_
