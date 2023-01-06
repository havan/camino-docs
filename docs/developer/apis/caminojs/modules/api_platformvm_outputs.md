# Module: API-PlatformVM-Outputs

## Index

### Classes

- [AmountOutput](../classes/api_platformvm_outputs.amountoutput)
- [ParseableOutput](../classes/api_platformvm_outputs.parseableoutput)
- [SECPOwnerOutput](../classes/api_platformvm_outputs.secpowneroutput)
- [SECPTransferOutput](../classes/api_platformvm_outputs.secptransferoutput)
- [StakeableLockOut](../classes/api_platformvm_outputs.stakeablelockout)
- [TransferableOutput](../classes/api_platformvm_outputs.transferableoutput)

### Variables

- [bintools](api_platformvm_outputs#const-bintools)
- [serialization](api_platformvm_outputs#const-serialization)

### Functions

- [SelectOutputClass](api_platformvm_outputs#const-selectoutputclass)

## Variables

### `Const` bintools

• **bintools**: _[BinTools](../classes/utils_bintools.bintools)_ = BinTools.getInstance()

_Defined in [src/apis/platformvm/outputs.ts:19](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/outputs.ts#L19)_

---

### `Const` serialization

• **serialization**: _[Serialization](../classes/utils_serialization.serialization)_ = Serialization.getInstance()

_Defined in [src/apis/platformvm/outputs.ts:20](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/outputs.ts#L20)_

## Functions

### `Const` SelectOutputClass

▸ **SelectOutputClass**(`outputid`: number, ...`args`: any[]): _[Output](../classes/common_output.output)_

_Defined in [src/apis/platformvm/outputs.ts:29](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/outputs.ts#L29)_

Takes a buffer representing the output and returns the proper Output instance.

**Parameters:**

| Name       | Type   | Description                                                           |
| ---------- | ------ | --------------------------------------------------------------------- |
| `outputid` | number | A number representing the inputID parsed prior to the bytes passed in |
| `...args`  | any[]  | -                                                                     |

**Returns:** _[Output](../classes/common_output.output)_

An instance of an [Output](src_common#output)-extended class.
