# Module: API-PlatformVM-Transactions

## Index

### Classes

- [Tx](../classes/api_platformvm_transactions.tx)
- [UnsignedTx](../classes/api_platformvm_transactions.unsignedtx)

### Functions

- [SelectTxClass](api_platformvm_transactions#const-selecttxclass)

## Functions

### `Const` SelectTxClass

▸ **SelectTxClass**(`txtype`: number, ...`args`: any[]): _[BaseTx](../classes/api_platformvm_basetx.basetx)_

_Defined in [src/apis/platformvm/tx.ts:33](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/platformvm/tx.ts#L33)_

Takes a buffer representing the output and returns the proper [BaseTx](../classes/api_avm_basetx.basetx) instance.

**Parameters:**

| Name      | Type   | Description                    |
| --------- | ------ | ------------------------------ |
| `txtype`  | number | The id of the transaction type |
| `...args` | any[]  | -                              |

**Returns:** _[BaseTx](../classes/api_platformvm_basetx.basetx)_

An instance of an [BaseTx](../classes/api_avm_basetx.basetx)-extended class.
