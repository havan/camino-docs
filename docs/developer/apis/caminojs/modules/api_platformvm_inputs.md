# Module: API-PlatformVM-Inputs

## Index

### Classes

- [AmountInput](../classes/api_platformvm_inputs.amountinput)
- [ParseableInput](../classes/api_platformvm_inputs.parseableinput)
- [SECPTransferInput](../classes/api_platformvm_inputs.secptransferinput)
- [StakeableLockIn](../classes/api_platformvm_inputs.stakeablelockin)
- [TransferableInput](../classes/api_platformvm_inputs.transferableinput)

### Variables

- [serialization](api_platformvm_inputs#const-serialization)

### Functions

- [SelectInputClass](api_platformvm_inputs#const-selectinputclass)

## Variables

### `Const` serialization

• **serialization**: _[Serialization](../classes/utils_serialization.serialization)_ = Serialization.getInstance()

_Defined in [src/apis/platformvm/inputs.ts:22](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/inputs.ts#L22)_

## Functions

### `Const` SelectInputClass

▸ **SelectInputClass**(`inputid`: number, ...`args`: any[]): _[Input](../classes/common_inputs.input)_

_Defined in [src/apis/platformvm/inputs.ts:31](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/inputs.ts#L31)_

Takes a buffer representing the output and returns the proper [Input](../classes/common_inputs.input) instance.

**Parameters:**

| Name      | Type   | Description                                                           |
| --------- | ------ | --------------------------------------------------------------------- |
| `inputid` | number | A number representing the inputID parsed prior to the bytes passed in |
| `...args` | any[]  | -                                                                     |

**Returns:** _[Input](../classes/common_inputs.input)_

An instance of an [Input](../classes/common_inputs.input)-extended class.
