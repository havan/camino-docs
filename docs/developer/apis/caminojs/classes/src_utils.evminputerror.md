# Class: EVMInputError

## Hierarchy

↳ [AvalancheError](src_utils.avalancheerror)

↳ **EVMInputError**

## Index

### Constructors

- [constructor](src_utils.evminputerror#constructor)

### Properties

- [errorCode](src_utils.evminputerror#errorcode)
- [message](src_utils.evminputerror#message)
- [name](src_utils.evminputerror#name)
- [stack](src_utils.evminputerror#optional-stack)

### Methods

- [getCode](src_utils.evminputerror#getcode)

## Constructors

### constructor

\+ **new EVMInputError**(`m`: string): _[EVMInputError](src_utils.evminputerror)_

_Overrides [AvalancheError](src_utils.avalancheerror).[constructor](src_utils.avalancheerror#constructor)_

_Defined in [src/utils/errors.ts:200](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/errors.ts#L200)_

**Parameters:**

| Name | Type   |
| ---- | ------ |
| `m`  | string |

**Returns:** _[EVMInputError](src_utils.evminputerror)_

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
