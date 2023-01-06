# Class: SECPMintOutputError

## Hierarchy

↳ [AvalancheError](src_utils.avalancheerror)

↳ **SECPMintOutputError**

## Index

### Constructors

- [constructor](src_utils.secpmintoutputerror#constructor)

### Properties

- [errorCode](src_utils.secpmintoutputerror#errorcode)
- [message](src_utils.secpmintoutputerror#message)
- [name](src_utils.secpmintoutputerror#name)
- [stack](src_utils.secpmintoutputerror#optional-stack)

### Methods

- [getCode](src_utils.secpmintoutputerror#getcode)

## Constructors

### constructor

\+ **new SECPMintOutputError**(`m`: string): _[SECPMintOutputError](src_utils.secpmintoutputerror)_

_Overrides [AvalancheError](src_utils.avalancheerror).[constructor](src_utils.avalancheerror#constructor)_

_Defined in [src/utils/errors.ts:193](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/errors.ts#L193)_

**Parameters:**

| Name | Type   |
| ---- | ------ |
| `m`  | string |

**Returns:** _[SECPMintOutputError](src_utils.secpmintoutputerror)_

## Properties

### errorCode

• **errorCode**: _string_

_Inherited from [AvalancheError](src_utils.avalancheerror).[errorCode](src_utils.avalancheerror#errorcode)_

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

## Methods

### getCode

▸ **getCode**(): _string_

_Inherited from [AvalancheError](src_utils.avalancheerror).[getCode](src_utils.avalancheerror#getcode)_

_Defined in [src/utils/errors.ts:55](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/errors.ts#L55)_

**Returns:** _string_
