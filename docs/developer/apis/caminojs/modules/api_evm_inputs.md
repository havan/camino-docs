# Module: API-EVM-Inputs

## Index

### Classes

- [AmountInput](../classes/api_evm_inputs.amountinput)
- [EVMInput](../classes/api_evm_inputs.evminput)
- [SECPTransferInput](../classes/api_evm_inputs.secptransferinput)
- [TransferableInput](../classes/api_evm_inputs.transferableinput)

### Functions

- [SelectInputClass](api_evm_inputs#const-selectinputclass)

## Functions

### `Const` SelectInputClass

▸ **SelectInputClass**(`inputID`: number, ...`args`: any[]): _[Input](../classes/common_inputs.input)_

_Defined in [src/apis/evm/inputs.ts:32](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/inputs.ts#L32)_

Takes a buffer representing the output and returns the proper [Input](../classes/common_inputs.input) instance.

**Parameters:**

| Name      | Type   | Description                                                           |
| --------- | ------ | --------------------------------------------------------------------- |
| `inputID` | number | A number representing the inputID parsed prior to the bytes passed in |
| `...args` | any[]  | -                                                                     |

**Returns:** _[Input](../classes/common_inputs.input)_

An instance of an [Input](../classes/common_inputs.input)-extended class.
