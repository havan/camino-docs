# Module: API-AVM-Operations

## Index

### Classes

- [NFTMintOperation](../classes/api_avm_operations.nftmintoperation)
- [NFTTransferOperation](../classes/api_avm_operations.nfttransferoperation)
- [Operation](../classes/api_avm_operations.operation)
- [SECPMintOperation](../classes/api_avm_operations.secpmintoperation)
- [TransferableOperation](../classes/api_avm_operations.transferableoperation)
- [UTXOID](../classes/api_avm_operations.utxoid)

### Variables

- [bintools](api_avm_operations#const-bintools)
- [buffer](api_avm_operations#const-buffer)
- [cb58](api_avm_operations#const-cb58)
- [decimalString](api_avm_operations#const-decimalstring)
- [hex](api_avm_operations#const-hex)
- [serialization](api_avm_operations#const-serialization)

### Functions

- [SelectOperationClass](api_avm_operations#const-selectoperationclass)

## Variables

### `Const` bintools

• **bintools**: _[BinTools](../classes/utils_bintools.bintools)_ = BinTools.getInstance()

_Defined in [src/apis/avm/ops.ts:29](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L29)_

---

### `Const` buffer

• **buffer**: _[SerializedType](utils_serialization#serializedtype)_ = "Buffer"

_Defined in [src/apis/avm/ops.ts:32](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L32)_

---

### `Const` cb58

• **cb58**: _[SerializedType](utils_serialization#serializedtype)_ = "cb58"

_Defined in [src/apis/avm/ops.ts:31](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L31)_

---

### `Const` decimalString

• **decimalString**: _[SerializedType](utils_serialization#serializedtype)_ = "decimalString"

_Defined in [src/apis/avm/ops.ts:34](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L34)_

---

### `Const` hex

• **hex**: _[SerializedType](utils_serialization#serializedtype)_ = "hex"

_Defined in [src/apis/avm/ops.ts:33](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L33)_

---

### `Const` serialization

• **serialization**: _[Serialization](../classes/utils_serialization.serialization)_ = Serialization.getInstance()

_Defined in [src/apis/avm/ops.ts:30](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L30)_

## Functions

### `Const` SelectOperationClass

▸ **SelectOperationClass**(`opid`: number, ...`args`: any[]): _[Operation](../classes/api_avm_operations.operation)_

_Defined in [src/apis/avm/ops.ts:43](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/ops.ts#L43)_

Takes a buffer representing the output and returns the proper [Operation](../classes/api_avm_operations.operation) instance.

**Parameters:**

| Name      | Type   | Description                                                                |
| --------- | ------ | -------------------------------------------------------------------------- |
| `opid`    | number | A number representing the operation ID parsed prior to the bytes passed in |
| `...args` | any[]  | -                                                                          |

**Returns:** _[Operation](../classes/api_avm_operations.operation)_

An instance of an [Operation](../classes/api_avm_operations.operation)-extended class.
