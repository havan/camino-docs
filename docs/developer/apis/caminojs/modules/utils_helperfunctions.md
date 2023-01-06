# Module: Utils-HelperFunctions

## Index

### Functions

- [MaxWeightFormula](utils_helperfunctions#maxweightformula)
- [NodeIDStringToBuffer](utils_helperfunctions#nodeidstringtobuffer)
- [UnixNow](utils_helperfunctions#unixnow)
- [bufferToNodeIDString](utils_helperfunctions#buffertonodeidstring)
- [bufferToPrivateKeyString](utils_helperfunctions#buffertoprivatekeystring)
- [calcBytesCost](utils_helperfunctions#calcbytescost)
- [costExportTx](utils_helperfunctions#costexporttx)
- [costImportTx](utils_helperfunctions#costimporttx)
- [privateKeyStringToBuffer](utils_helperfunctions#privatekeystringtobuffer)

## Functions

### MaxWeightFormula

▸ **MaxWeightFormula**(`staked`: BN, `cap`: BN): _BN_

_Defined in [src/utils/helperfunctions.ts:18](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/helperfunctions.ts#L18)_

**Parameters:**

| Name     | Type |
| -------- | ---- |
| `staked` | BN   |
| `cap`    | BN   |

**Returns:** _BN_

---

### NodeIDStringToBuffer

▸ **NodeIDStringToBuffer**(`pk`: string): _Buffer_

_Defined in [src/utils/helperfunctions.ts:67](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/helperfunctions.ts#L67)_

Takes a nodeID string and produces a nodeID [Buffer](https://github.com/feross/buffer).

**Parameters:**

| Name | Type   | Description              |
| ---- | ------ | ------------------------ |
| `pk` | string | A string for the nodeID. |

**Returns:** _Buffer_

---

### UnixNow

▸ **UnixNow**(): _BN_

_Defined in [src/utils/helperfunctions.ts:25](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/helperfunctions.ts#L25)_

Function providing the current UNIX time using a [BN](https://github.com/indutny/bn.js/).

**Returns:** _BN_

---

### bufferToNodeIDString

▸ **bufferToNodeIDString**(`pk`: Buffer): _string_

_Defined in [src/utils/helperfunctions.ts:58](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/helperfunctions.ts#L58)_

Takes a nodeID buffer and produces a nodeID string with prefix.

**Parameters:**

| Name | Type   | Description                                                  |
| ---- | ------ | ------------------------------------------------------------ |
| `pk` | Buffer | A [Buffer](https://github.com/feross/buffer) for the nodeID. |

**Returns:** _string_

---

### bufferToPrivateKeyString

▸ **bufferToPrivateKeyString**(`pk`: Buffer): _string_

_Defined in [src/utils/helperfunctions.ts:34](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/helperfunctions.ts#L34)_

Takes a private key buffer and produces a private key string with prefix.

**Parameters:**

| Name | Type   | Description                                                       |
| ---- | ------ | ----------------------------------------------------------------- |
| `pk` | Buffer | A [Buffer](https://github.com/feross/buffer) for the private key. |

**Returns:** _string_

---

### calcBytesCost

▸ **calcBytesCost**(`c`: [C](../interfaces/utils_networks.c), `len`: number): _number_

_Defined in [src/utils/helperfunctions.ts:88](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/helperfunctions.ts#L88)_

**Parameters:**

| Name  | Type                                |
| ----- | ----------------------------------- |
| `c`   | [C](../interfaces/utils_networks.c) |
| `len` | number                              |

**Returns:** _number_

---

### costExportTx

▸ **costExportTx**(`c`: [C](../interfaces/utils_networks.c), `tx`: [UnsignedTx](../classes/api_evm_transactions.unsignedtx)): _number_

_Defined in [src/utils/helperfunctions.ts:92](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/helperfunctions.ts#L92)_

**Parameters:**

| Name | Type                                                     |
| ---- | -------------------------------------------------------- |
| `c`  | [C](../interfaces/utils_networks.c)                      |
| `tx` | [UnsignedTx](../classes/api_evm_transactions.unsignedtx) |

**Returns:** _number_

---

### costImportTx

▸ **costImportTx**(`c`: [C](../interfaces/utils_networks.c), `tx`: [UnsignedTx](../classes/api_evm_transactions.unsignedtx)): _number_

_Defined in [src/utils/helperfunctions.ts:77](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/helperfunctions.ts#L77)_

**Parameters:**

| Name | Type                                                     |
| ---- | -------------------------------------------------------- |
| `c`  | [C](../interfaces/utils_networks.c)                      |
| `tx` | [UnsignedTx](../classes/api_evm_transactions.unsignedtx) |

**Returns:** _number_

---

### privateKeyStringToBuffer

▸ **privateKeyStringToBuffer**(`pk`: string): _Buffer_

_Defined in [src/utils/helperfunctions.ts:43](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/helperfunctions.ts#L43)_

Takes a private key string and produces a private key [Buffer](https://github.com/feross/buffer).

**Parameters:**

| Name | Type   | Description                   |
| ---- | ------ | ----------------------------- |
| `pk` | string | A string for the private key. |

**Returns:** _Buffer_
