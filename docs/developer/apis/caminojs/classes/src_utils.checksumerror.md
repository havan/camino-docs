# Class: ChecksumError

## Hierarchy

↳ [AvalancheError](src_utils.avalancheerror)

↳ **ChecksumError**

## Index

### Constructors

- [constructor](src_utils.checksumerror#constructor)

### Properties

- [errorCode](src_utils.checksumerror#errorcode)
- [message](src_utils.checksumerror#message)
- [name](src_utils.checksumerror#name)
- [stack](src_utils.checksumerror#optional-stack)

### Methods

- [getCode](src_utils.checksumerror#getcode)

## Constructors

### constructor

\+ **new ChecksumError**(`m`: string): _[ChecksumError](src_utils.checksumerror)_

_Overrides [AvalancheError](src_utils.avalancheerror).[constructor](src_utils.avalancheerror#constructor)_

_Defined in [src/utils/errors.ts:158](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/errors.ts#L158)_

**Parameters:**

| Name | Type   |
| ---- | ------ |
| `m`  | string |

**Returns:** _[ChecksumError](src_utils.checksumerror)_

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
