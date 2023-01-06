# Class: DB

A class for interacting with the [store2 module](https://github.com/nbubna/store)

This class should never be instantiated directly. Instead, invoke the "DB.getInstance()" static
function to grab the singleton instance of the database.

```js
const db = DB.getInstance();
const blockchaindb = db.getNamespace("mychain");
```

## Hierarchy

- **DB**

## Index

### Constructors

- [constructor](utils_db.db#private-constructor)

### Properties

- [instance](utils_db.db#static-private-instance)
- [store](utils_db.db#static-private-store)

### Methods

- [getInstance](utils_db.db#static-getinstance)
- [getNamespace](utils_db.db#static-getnamespace)

## Constructors

### `Private` constructor

\+ **new DB**(): _[DB](utils_db.db)_

_Defined in [src/utils/db.ts:21](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/db.ts#L21)_

**Returns:** _[DB](utils_db.db)_

## Properties

### `Static` `Private` instance

▪ **instance**: _[DB](utils_db.db)_

_Defined in [src/utils/db.ts:19](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/db.ts#L19)_

---

### `Static` `Private` store

▪ **store**: _StoreType_ = store

_Defined in [src/utils/db.ts:21](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/db.ts#L21)_

## Methods

### `Static` getInstance

▸ **getInstance**(): _[DB](utils_db.db)_

_Defined in [src/utils/db.ts:28](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/db.ts#L28)_

Retrieves the database singleton.

**Returns:** _[DB](utils_db.db)_

---

### `Static` getNamespace

▸ **getNamespace**(`ns`: string): _StoreAPI_

_Defined in [src/utils/db.ts:40](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/db.ts#L40)_

Gets a namespace from the database singleton.

**Parameters:**

| Name | Type   | Description            |
| ---- | ------ | ---------------------- |
| `ns` | string | Namespace to retrieve. |

**Returns:** _StoreAPI_
