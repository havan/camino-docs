# Class: ChainIdError

## Hierarchy

↳ [AvalancheError](src_utils.avalancheerror)

↳ **ChainIdError**

## Index

### Constructors

- [constructor](src_utils.chainiderror#constructor)

### Properties

- [errorCode](src_utils.chainiderror#errorcode)
- [message](src_utils.chainiderror#message)
- [name](src_utils.chainiderror#name)
- [stack](src_utils.chainiderror#optional-stack)

### Methods

- [getCode](src_utils.chainiderror#getcode)

## Constructors

### constructor

\+ **new ChainIdError**(`m`: string): _[ChainIdError](src_utils.chainiderror)_

_Overrides [AvalancheError](src_utils.avalancheerror).[constructor](src_utils.avalancheerror#constructor)_

_Defined in [src/utils/errors.ts:74](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/errors.ts#L74)_

**Parameters:**

| Name | Type   |
| ---- | ------ |
| `m`  | string |

**Returns:** _[ChainIdError](src_utils.chainiderror)_

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
