# Class: AvalancheError

## Hierarchy

- [Error](src_utils.avalancheerror#static-error)

  ↳ **AvalancheError**

  ↳ [AddressError](src_utils.addresserror)

  ↳ [GooseEggCheckError](src_utils.gooseeggcheckerror)

  ↳ [ChainIdError](src_utils.chainiderror)

  ↳ [NoAtomicUTXOsError](src_utils.noatomicutxoserror)

  ↳ [SymbolError](src_utils.symbolerror)

  ↳ [NameError](src_utils.nameerror)

  ↳ [TransactionError](src_utils.transactionerror)

  ↳ [CodecIdError](src_utils.codeciderror)

  ↳ [CredIdError](src_utils.crediderror)

  ↳ [TransferableOutputError](src_utils.transferableoutputerror)

  ↳ [TransferableInputError](src_utils.transferableinputerror)

  ↳ [InputIdError](src_utils.inputiderror)

  ↳ [OperationError](src_utils.operationerror)

  ↳ [InvalidOperationIdError](src_utils.invalidoperationiderror)

  ↳ [ChecksumError](src_utils.checksumerror)

  ↳ [OutputIdError](src_utils.outputiderror)

  ↳ [UTXOError](src_utils.utxoerror)

  ↳ [InsufficientFundsError](src_utils.insufficientfundserror)

  ↳ [ThresholdError](src_utils.thresholderror)

  ↳ [SECPMintOutputError](src_utils.secpmintoutputerror)

  ↳ [EVMInputError](src_utils.evminputerror)

  ↳ [EVMOutputError](src_utils.evmoutputerror)

  ↳ [FeeAssetError](src_utils.feeasseterror)

  ↳ [StakeError](src_utils.stakeerror)

  ↳ [TimeError](src_utils.timeerror)

  ↳ [DelegationFeeError](src_utils.delegationfeeerror)

  ↳ [SubnetOwnerError](src_utils.subnetownererror)

  ↳ [BufferSizeError](src_utils.buffersizeerror)

  ↳ [AddressIndexError](src_utils.addressindexerror)

  ↳ [PublicKeyError](src_utils.publickeyerror)

  ↳ [MergeRuleError](src_utils.mergeruleerror)

  ↳ [Base58Error](src_utils.base58error)

  ↳ [PrivateKeyError](src_utils.privatekeyerror)

  ↳ [NodeIdError](src_utils.nodeiderror)

  ↳ [HexError](src_utils.hexerror)

  ↳ [TypeIdError](src_utils.typeiderror)

  ↳ [TypeNameError](src_utils.typenameerror)

  ↳ [UnknownTypeError](src_utils.unknowntypeerror)

  ↳ [Bech32Error](src_utils.bech32error)

  ↳ [EVMFeeError](src_utils.evmfeeerror)

  ↳ [InvalidEntropy](src_utils.invalidentropy)

  ↳ [ProtocolError](src_utils.protocolerror)

  ↳ [SubnetIdError](src_utils.subnetiderror)

  ↳ [SubnetThresholdError](src_utils.subnetthresholderror)

  ↳ [SubnetAddressError](src_utils.subnetaddresserror)

## Index

### Constructors

- [constructor](src_utils.avalancheerror#constructor)

### Properties

- [errorCode](src_utils.avalancheerror#errorcode)
- [message](src_utils.avalancheerror#message)
- [name](src_utils.avalancheerror#name)
- [stack](src_utils.avalancheerror#optional-stack)
- [Error](src_utils.avalancheerror#static-error)

### Methods

- [getCode](src_utils.avalancheerror#getcode)

## Constructors

### constructor

\+ **new AvalancheError**(`m`: string, `code`: string): _[AvalancheError](src_utils.avalancheerror)_

_Defined in [src/utils/errors.ts:48](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/errors.ts#L48)_

**Parameters:**

| Name   | Type   |
| ------ | ------ |
| `m`    | string |
| `code` | string |

**Returns:** _[AvalancheError](src_utils.avalancheerror)_

## Properties

### errorCode

• **errorCode**: _string_

_Defined in [src/utils/errors.ts:48](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/errors.ts#L48)_

---

### message

• **message**: _string_

_Inherited from [AvalancheError](src_utils.avalancheerror).[message](src_utils.avalancheerror#message)_

Defined in node_modules/typescript/lib/lib.es5.d.ts:1029

---

### name

• **name**: _string_

_Inherited from [AvalancheError](src_utils.avalancheerror).[name](src_utils.avalancheerror#name)_

Defined in node_modules/typescript/lib/lib.es5.d.ts:1028

---

### `Optional` stack

• **stack**? : _string_

_Inherited from [AvalancheError](src_utils.avalancheerror).[stack](src_utils.avalancheerror#optional-stack)_

Defined in node_modules/typescript/lib/lib.es5.d.ts:1030

---

### `Static` Error

▪ **Error**: _ErrorConstructor_

Defined in node_modules/typescript/lib/lib.es5.d.ts:1039

## Methods

### getCode

▸ **getCode**(): _string_

_Defined in [src/utils/errors.ts:55](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/errors.ts#L55)_

**Returns:** _string_
