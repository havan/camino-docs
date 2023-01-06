# Class: EVMOutputError

## Hierarchy

↳ [AvalancheError](src_utils.avalancheerror)

↳ **EVMOutputError**

## Index

### Constructors

- [constructor](src_utils.evmoutputerror#constructor)

### Properties

- [errorCode](src_utils.evmoutputerror#errorcode)
- [message](src_utils.evmoutputerror#message)
- [name](src_utils.evmoutputerror#name)
- [stack](src_utils.evmoutputerror#optional-stack)

### Methods

- [getCode](src_utils.evmoutputerror#getcode)

## Constructors

### constructor

\+ **new EVMOutputError**(`m`: string): _[EVMOutputError](src_utils.evmoutputerror)_

_Overrides [AvalancheError](src_utils.avalancheerror).[constructor](src_utils.avalancheerror#constructor)_

_Defined in [src/utils/errors.ts:207](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/errors.ts#L207)_

**Parameters:**

| Name | Type   |
| ---- | ------ |
| `m`  | string |

**Returns:** _[EVMOutputError](src_utils.evmoutputerror)_

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
