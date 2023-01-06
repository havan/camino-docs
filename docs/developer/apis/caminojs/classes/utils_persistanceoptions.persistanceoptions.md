# Class: PersistanceOptions

A class for defining the persistance behavior of this an API call.

## Hierarchy

- **PersistanceOptions**

## Index

### Constructors

- [constructor](utils_persistanceoptions.persistanceoptions#constructor)

### Properties

- [mergeRule](utils_persistanceoptions.persistanceoptions#protected-mergerule)
- [name](utils_persistanceoptions.persistanceoptions#protected-name)
- [overwrite](utils_persistanceoptions.persistanceoptions#protected-overwrite)

### Methods

- [getMergeRule](utils_persistanceoptions.persistanceoptions#getmergerule)
- [getName](utils_persistanceoptions.persistanceoptions#getname)
- [getOverwrite](utils_persistanceoptions.persistanceoptions#getoverwrite)

## Constructors

### constructor

\+ **new PersistanceOptions**(`name`: string, `overwrite`: boolean, `mergeRule`: [MergeRule](../modules/utils_constants#mergerule)): _[PersistanceOptions](utils_persistanceoptions.persistanceoptions)_

_Defined in [src/utils/persistenceoptions.ts:31](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/persistenceoptions.ts#L31)_

**`remarks`**
The merge rules are as follows:

- "intersection" - the intersection of the set
- "differenceSelf" - the difference between the existing data and new set
- "differenceNew" - the difference between the new data and the existing set
- "symDifference" - the union of the differences between both sets of data
- "union" - the unique set of all elements contained in both sets
- "unionMinusNew" - the unique set of all elements contained in both sets, excluding values only found in the new set
- "unionMinusSelf" - the unique set of all elements contained in both sets, excluding values only found in the existing set

**Parameters:**

| Name        | Type                                              | Default | Description                                      |
| ----------- | ------------------------------------------------- | ------- | ------------------------------------------------ |
| `name`      | string                                            | -       | The namespace of the database the data           |
| `overwrite` | boolean                                           | false   | True if the data should be completey overwritten |
| `mergeRule` | [MergeRule](../modules/utils_constants#mergerule) | -       | -                                                |

**Returns:** _[PersistanceOptions](utils_persistanceoptions.persistanceoptions)_

## Properties

### `Protected` mergeRule

• **mergeRule**: _[MergeRule](../modules/utils_constants#mergerule)_ = "union"

_Defined in [src/utils/persistenceoptions.ts:16](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/persistenceoptions.ts#L16)_

---

### `Protected` name

• **name**: _string_ = undefined

_Defined in [src/utils/persistenceoptions.ts:12](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/persistenceoptions.ts#L12)_

---

### `Protected` overwrite

• **overwrite**: _boolean_ = false

_Defined in [src/utils/persistenceoptions.ts:14](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/persistenceoptions.ts#L14)_

## Methods

### getMergeRule

▸ **getMergeRule**(): _[MergeRule](../modules/utils_constants#mergerule)_

_Defined in [src/utils/persistenceoptions.ts:31](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/persistenceoptions.ts#L31)_

Returns the [MergeRule](../modules/utils_constants#mergerule) of the instance

**Returns:** _[MergeRule](../modules/utils_constants#mergerule)_

---

### getName

▸ **getName**(): _string_

_Defined in [src/utils/persistenceoptions.ts:21](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/persistenceoptions.ts#L21)_

Returns the namespace of the instance

**Returns:** _string_

---

### getOverwrite

▸ **getOverwrite**(): _boolean_

_Defined in [src/utils/persistenceoptions.ts:26](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/persistenceoptions.ts#L26)_

Returns the overwrite rule of the instance

**Returns:** _boolean_
