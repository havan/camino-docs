# Class: AssetAmount

Class for managing asset amounts in the UTXOSet fee calcuation

## Hierarchy

- **AssetAmount**

## Index

### Constructors

- [constructor](common_assetamount.assetamount#constructor)

### Properties

- [amount](common_assetamount.assetamount#protected-amount)
- [assetID](common_assetamount.assetamount#protected-assetid)
- [burn](common_assetamount.assetamount#protected-burn)
- [change](common_assetamount.assetamount#protected-change)
- [finished](common_assetamount.assetamount#protected-finished)
- [spent](common_assetamount.assetamount#protected-spent)
- [stakeableLockChange](common_assetamount.assetamount#protected-stakeablelockchange)
- [stakeableLockSpent](common_assetamount.assetamount#protected-stakeablelockspent)

### Methods

- [getAmount](common_assetamount.assetamount#getamount)
- [getAssetID](common_assetamount.assetamount#getassetid)
- [getAssetIDString](common_assetamount.assetamount#getassetidstring)
- [getBurn](common_assetamount.assetamount#getburn)
- [getChange](common_assetamount.assetamount#getchange)
- [getSpent](common_assetamount.assetamount#getspent)
- [getStakeableLockChange](common_assetamount.assetamount#getstakeablelockchange)
- [getStakeableLockSpent](common_assetamount.assetamount#getstakeablelockspent)
- [isFinished](common_assetamount.assetamount#isfinished)
- [spendAmount](common_assetamount.assetamount#spendamount)

## Constructors

### constructor

\+ **new AssetAmount**(`assetID`: Buffer, `amount`: BN, `burn`: BN): _[AssetAmount](common_assetamount.assetamount)_

_Defined in [src/common/assetamount.ts:98](https://github.com/chain4travel/caminojs/blob/3883166/src/common/assetamount.ts#L98)_

**Parameters:**

| Name      | Type   |
| --------- | ------ |
| `assetID` | Buffer |
| `amount`  | BN     |
| `burn`    | BN     |

**Returns:** _[AssetAmount](common_assetamount.assetamount)_

## Properties

### `Protected` amount

• **amount**: _BN_ = new BN(0)

_Defined in [src/common/assetamount.ts:19](https://github.com/chain4travel/caminojs/blob/3883166/src/common/assetamount.ts#L19)_

---

### `Protected` assetID

• **assetID**: _Buffer_ = Buffer.alloc(32)

_Defined in [src/common/assetamount.ts:17](https://github.com/chain4travel/caminojs/blob/3883166/src/common/assetamount.ts#L17)_

---

### `Protected` burn

• **burn**: _BN_ = new BN(0)

_Defined in [src/common/assetamount.ts:21](https://github.com/chain4travel/caminojs/blob/3883166/src/common/assetamount.ts#L21)_

---

### `Protected` change

• **change**: _BN_ = new BN(0)

_Defined in [src/common/assetamount.ts:31](https://github.com/chain4travel/caminojs/blob/3883166/src/common/assetamount.ts#L31)_

---

### `Protected` finished

• **finished**: _boolean_ = false

_Defined in [src/common/assetamount.ts:37](https://github.com/chain4travel/caminojs/blob/3883166/src/common/assetamount.ts#L37)_

---

### `Protected` spent

• **spent**: _BN_ = new BN(0)

_Defined in [src/common/assetamount.ts:24](https://github.com/chain4travel/caminojs/blob/3883166/src/common/assetamount.ts#L24)_

---

### `Protected` stakeableLockChange

• **stakeableLockChange**: _boolean_ = false

_Defined in [src/common/assetamount.ts:34](https://github.com/chain4travel/caminojs/blob/3883166/src/common/assetamount.ts#L34)_

---

### `Protected` stakeableLockSpent

• **stakeableLockSpent**: _BN_ = new BN(0)

_Defined in [src/common/assetamount.ts:27](https://github.com/chain4travel/caminojs/blob/3883166/src/common/assetamount.ts#L27)_

## Methods

### getAmount

▸ **getAmount**(): _BN_

_Defined in [src/common/assetamount.ts:47](https://github.com/chain4travel/caminojs/blob/3883166/src/common/assetamount.ts#L47)_

**Returns:** _BN_

---

### getAssetID

▸ **getAssetID**(): _Buffer_

_Defined in [src/common/assetamount.ts:39](https://github.com/chain4travel/caminojs/blob/3883166/src/common/assetamount.ts#L39)_

**Returns:** _Buffer_

---

### getAssetIDString

▸ **getAssetIDString**(): _string_

_Defined in [src/common/assetamount.ts:43](https://github.com/chain4travel/caminojs/blob/3883166/src/common/assetamount.ts#L43)_

**Returns:** _string_

---

### getBurn

▸ **getBurn**(): _BN_

_Defined in [src/common/assetamount.ts:55](https://github.com/chain4travel/caminojs/blob/3883166/src/common/assetamount.ts#L55)_

**Returns:** _BN_

---

### getChange

▸ **getChange**(): _BN_

_Defined in [src/common/assetamount.ts:59](https://github.com/chain4travel/caminojs/blob/3883166/src/common/assetamount.ts#L59)_

**Returns:** _BN_

---

### getSpent

▸ **getSpent**(): _BN_

_Defined in [src/common/assetamount.ts:51](https://github.com/chain4travel/caminojs/blob/3883166/src/common/assetamount.ts#L51)_

**Returns:** _BN_

---

### getStakeableLockChange

▸ **getStakeableLockChange**(): _boolean_

_Defined in [src/common/assetamount.ts:67](https://github.com/chain4travel/caminojs/blob/3883166/src/common/assetamount.ts#L67)_

**Returns:** _boolean_

---

### getStakeableLockSpent

▸ **getStakeableLockSpent**(): _BN_

_Defined in [src/common/assetamount.ts:63](https://github.com/chain4travel/caminojs/blob/3883166/src/common/assetamount.ts#L63)_

**Returns:** _BN_

---

### isFinished

▸ **isFinished**(): _boolean_

_Defined in [src/common/assetamount.ts:71](https://github.com/chain4travel/caminojs/blob/3883166/src/common/assetamount.ts#L71)_

**Returns:** _boolean_

---

### spendAmount

▸ **spendAmount**(`amt`: BN, `stakeableLocked`: boolean): _boolean_

_Defined in [src/common/assetamount.ts:77](https://github.com/chain4travel/caminojs/blob/3883166/src/common/assetamount.ts#L77)_

**Parameters:**

| Name              | Type    | Default |
| ----------------- | ------- | ------- |
| `amt`             | BN      | -       |
| `stakeableLocked` | boolean | false   |

**Returns:** _boolean_
