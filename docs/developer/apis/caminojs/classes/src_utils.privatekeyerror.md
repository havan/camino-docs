# Class: PrivateKeyError

## Hierarchy

↳ [AvalancheError](src_utils.avalancheerror)

↳ **PrivateKeyError**

## Index

### Constructors

- [constructor](src_utils.privatekeyerror#constructor)

### Properties

- [errorCode](src_utils.privatekeyerror#errorcode)
- [message](src_utils.privatekeyerror#message)
- [name](src_utils.privatekeyerror#name)
- [stack](src_utils.privatekeyerror#optional-stack)

### Methods

- [getCode](src_utils.privatekeyerror#getcode)

## Constructors

### constructor

\+ **new PrivateKeyError**(`m`: string): _[PrivateKeyError](src_utils.privatekeyerror)_

_Overrides [AvalancheError](src_utils.avalancheerror).[constructor](src_utils.avalancheerror#constructor)_

_Defined in [src/utils/errors.ts:284](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/errors.ts#L284)_

**Parameters:**

| Name | Type   |
| ---- | ------ |
| `m`  | string |

**Returns:** _[PrivateKeyError](src_utils.privatekeyerror)_

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
