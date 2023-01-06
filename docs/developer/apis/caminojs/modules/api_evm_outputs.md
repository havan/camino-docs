# Module: API-EVM-Outputs

## Index

### Classes

- [AmountOutput](../classes/api_evm_outputs.amountoutput)
- [EVMOutput](../classes/api_evm_outputs.evmoutput)
- [SECPTransferOutput](../classes/api_evm_outputs.secptransferoutput)
- [TransferableOutput](../classes/api_evm_outputs.transferableoutput)

### Variables

- [bintools](api_evm_outputs#const-bintools)

### Functions

- [SelectOutputClass](api_evm_outputs#const-selectoutputclass)

## Variables

### `Const` bintools

• **bintools**: _[BinTools](../classes/utils_bintools.bintools)_ = BinTools.getInstance()

_Defined in [src/apis/evm/outputs.ts:18](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/outputs.ts#L18)_

## Functions

### `Const` SelectOutputClass

▸ **SelectOutputClass**(`outputID`: number, ...`args`: any[]): _[Output](../classes/common_output.output)_

_Defined in [src/apis/evm/outputs.ts:27](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/outputs.ts#L27)_

Takes a buffer representing the output and returns the proper Output instance.

**Parameters:**

| Name       | Type   | Description                                                            |
| ---------- | ------ | ---------------------------------------------------------------------- |
| `outputID` | number | A number representing the outputID parsed prior to the bytes passed in |
| `...args`  | any[]  | -                                                                      |

**Returns:** _[Output](../classes/common_output.output)_

An instance of an [Output](src_common#output)-extended class.
