# Module: API-AVM-Outputs

## Index

### Classes

- [AmountOutput](../classes/api_avm_outputs.amountoutput)
- [NFTMintOutput](../classes/api_avm_outputs.nftmintoutput)
- [NFTOutput](../classes/api_avm_outputs.nftoutput)
- [NFTTransferOutput](../classes/api_avm_outputs.nfttransferoutput)
- [SECPMintOutput](../classes/api_avm_outputs.secpmintoutput)
- [SECPTransferOutput](../classes/api_avm_outputs.secptransferoutput)
- [TransferableOutput](../classes/api_avm_outputs.transferableoutput)

### Variables

- [bintools](api_avm_outputs#const-bintools)
- [serialization](api_avm_outputs#const-serialization)

### Functions

- [SelectOutputClass](api_avm_outputs#const-selectoutputclass)

## Variables

### `Const` bintools

• **bintools**: _[BinTools](../classes/utils_bintools.bintools)_ = BinTools.getInstance()

_Defined in [src/apis/avm/outputs.ts:18](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/outputs.ts#L18)_

---

### `Const` serialization

• **serialization**: _[Serialization](../classes/utils_serialization.serialization)_ = Serialization.getInstance()

_Defined in [src/apis/avm/outputs.ts:19](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/outputs.ts#L19)_

## Functions

### `Const` SelectOutputClass

▸ **SelectOutputClass**(`outputid`: number, ...`args`: any[]): _[Output](../classes/common_output.output)_

_Defined in [src/apis/avm/outputs.ts:28](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/outputs.ts#L28)_

Takes a buffer representing the output and returns the proper Output instance.

**Parameters:**

| Name       | Type   | Description                                                           |
| ---------- | ------ | --------------------------------------------------------------------- |
| `outputid` | number | A number representing the inputID parsed prior to the bytes passed in |
| `...args`  | any[]  | -                                                                     |

**Returns:** _[Output](../classes/common_output.output)_

An instance of an [Output](src_common#output)-extended class.
