# Module: API-AVM-Inputs

## Index

### Classes

- [AmountInput](../classes/api_avm_inputs.amountinput)
- [SECPTransferInput](../classes/api_avm_inputs.secptransferinput)
- [TransferableInput](../classes/api_avm_inputs.transferableinput)

### Functions

- [SelectInputClass](api_avm_inputs#const-selectinputclass)

## Functions

### `Const` SelectInputClass

▸ **SelectInputClass**(`inputid`: number, ...`args`: any[]): _[Input](../classes/common_inputs.input)_

_Defined in [src/apis/avm/inputs.ts:28](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/avm/inputs.ts#L28)_

Takes a buffer representing the output and returns the proper [Input](../classes/common_inputs.input) instance.

**Parameters:**

| Name      | Type   | Description                                                           |
| --------- | ------ | --------------------------------------------------------------------- |
| `inputid` | number | A number representing the inputID parsed prior to the bytes passed in |
| `...args` | any[]  | -                                                                     |

**Returns:** _[Input](../classes/common_inputs.input)_

An instance of an [Input](../classes/common_inputs.input)-extended class.
