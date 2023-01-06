# Module: API-EVM-Transactions

## Index

### Classes

- [Tx](../classes/api_evm_transactions.tx)
- [UnsignedTx](../classes/api_evm_transactions.unsignedtx)

### Functions

- [SelectTxClass](api_evm_transactions#const-selecttxclass)

## Functions

### `Const` SelectTxClass

▸ **SelectTxClass**(`txTypeID`: number, ...`args`: any[]): _[EVMBaseTx](../classes/api_evm_basetx.evmbasetx)_

_Defined in [src/apis/evm/tx.ts:32](https://github.com/chain4travel/caminojs/blob/3883166/src/apis/evm/tx.ts#L32)_

Takes a buffer representing the output and returns the proper [EVMBaseTx](../classes/api_evm_basetx.evmbasetx) instance.

**Parameters:**

| Name       | Type   | Description                    |
| ---------- | ------ | ------------------------------ |
| `txTypeID` | number | The id of the transaction type |
| `...args`  | any[]  | -                              |

**Returns:** _[EVMBaseTx](../classes/api_evm_basetx.evmbasetx)_

An instance of an [EVMBaseTx](../classes/api_evm_basetx.evmbasetx)-extended class.
