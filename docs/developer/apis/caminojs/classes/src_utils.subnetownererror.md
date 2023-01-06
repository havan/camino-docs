# Class: SubnetOwnerError

## Hierarchy

↳ [AvalancheError](src_utils.avalancheerror)

↳ **SubnetOwnerError**

## Index

### Constructors

- [constructor](src_utils.subnetownererror#constructor)

### Properties

- [errorCode](src_utils.subnetownererror#errorcode)
- [message](src_utils.subnetownererror#message)
- [name](src_utils.subnetownererror#name)
- [stack](src_utils.subnetownererror#optional-stack)

### Methods

- [getCode](src_utils.subnetownererror#getcode)

## Constructors

### constructor

\+ **new SubnetOwnerError**(`m`: string): _[SubnetOwnerError](src_utils.subnetownererror)_

_Overrides [AvalancheError](src_utils.avalancheerror).[constructor](src_utils.avalancheerror#constructor)_

_Defined in [src/utils/errors.ts:242](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/errors.ts#L242)_

**Parameters:**

| Name | Type   |
| ---- | ------ |
| `m`  | string |

**Returns:** _[SubnetOwnerError](src_utils.subnetownererror)_

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
