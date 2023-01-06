# Class: Serialization

## Hierarchy

- **Serialization**

## Index

### Constructors

- [constructor](utils_serialization.serialization#private-constructor)

### Properties

- [bintools](utils_serialization.serialization#private-bintools)
- [instance](utils_serialization.serialization#static-private-instance)

### Methods

- [bufferToType](utils_serialization.serialization#buffertotype)
- [decoder](utils_serialization.serialization#decoder)
- [deserialize](utils_serialization.serialization#deserialize)
- [encoder](utils_serialization.serialization#encoder)
- [serialize](utils_serialization.serialization#serialize)
- [typeToBuffer](utils_serialization.serialization#typetobuffer)
- [getInstance](utils_serialization.serialization#static-getinstance)

## Constructors

### `Private` constructor

\+ **new Serialization**(): _[Serialization](utils_serialization.serialization)_

_Defined in [src/utils/serialization.ts:155](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/serialization.ts#L155)_

**Returns:** _[Serialization](utils_serialization.serialization)_

## Properties

### `Private` bintools

• **bintools**: _[BinTools](utils_bintools.bintools)_

_Defined in [src/utils/serialization.ts:160](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/serialization.ts#L160)_

---

### `Static` `Private` instance

▪ **instance**: _[Serialization](utils_serialization.serialization)_

_Defined in [src/utils/serialization.ts:155](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/serialization.ts#L155)_

## Methods

### bufferToType

▸ **bufferToType**(`vb`: Buffer, `type`: [SerializedType](../modules/utils_serialization#serializedtype), ...`args`: any[]): _any_

_Defined in [src/utils/serialization.ts:180](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/serialization.ts#L180)_

Convert [Buffer](https://github.com/feross/buffer) to [SerializedType](../modules/utils_serialization#serializedtype)

**Parameters:**

| Name      | Type                                                            | Description                                                     |
| --------- | --------------------------------------------------------------- | --------------------------------------------------------------- |
| `vb`      | Buffer                                                          | [Buffer](https://github.com/feross/buffer)                      |
| `type`    | [SerializedType](../modules/utils_serialization#serializedtype) | [SerializedType](../modules/utils_serialization#serializedtype) |
| `...args` | any[]                                                           | -                                                               |

**Returns:** _any_

type of [SerializedType](../modules/utils_serialization#serializedtype)

---

### decoder

▸ **decoder**(`value`: string, `encoding`: [SerializedEncoding](../modules/utils_serialization#serializedencoding), `intype`: [SerializedType](../modules/utils_serialization#serializedtype), `outtype`: [SerializedType](../modules/utils_serialization#serializedtype), ...`args`: any[]): _any_

_Defined in [src/utils/serialization.ts:308](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/serialization.ts#L308)_

Convert value to type of [SerializedType](../modules/utils_serialization#serializedtype) or [SerializedEncoding](../modules/utils_serialization#serializedencoding)

**Parameters:**

| Name       | Type                                                                    | Description                                                             |
| ---------- | ----------------------------------------------------------------------- | ----------------------------------------------------------------------- |
| `value`    | string                                                                  | -                                                                       |
| `encoding` | [SerializedEncoding](../modules/utils_serialization#serializedencoding) | [SerializedEncoding](../modules/utils_serialization#serializedencoding) |
| `intype`   | [SerializedType](../modules/utils_serialization#serializedtype)         | [SerializedType](../modules/utils_serialization#serializedtype)         |
| `outtype`  | [SerializedType](../modules/utils_serialization#serializedtype)         | [SerializedType](../modules/utils_serialization#serializedtype)         |
| `...args`  | any[]                                                                   | -                                                                       |

**Returns:** _any_

type of [SerializedType](../modules/utils_serialization#serializedtype) or [SerializedEncoding](../modules/utils_serialization#serializedencoding)

---

### deserialize

▸ **deserialize**(`input`: [Serialized](../interfaces/common_interfaces.serialized), `output`: [Serializable](utils_serialization.serializable)): _void_

_Defined in [src/utils/serialization.ts:345](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/serialization.ts#L345)_

**Parameters:**

| Name     | Type                                                     |
| -------- | -------------------------------------------------------- |
| `input`  | [Serialized](../interfaces/common_interfaces.serialized) |
| `output` | [Serializable](utils_serialization.serializable)         |

**Returns:** _void_

---

### encoder

▸ **encoder**(`value`: any, `encoding`: [SerializedEncoding](../modules/utils_serialization#serializedencoding), `intype`: [SerializedType](../modules/utils_serialization#serializedtype), `outtype`: [SerializedType](../modules/utils_serialization#serializedtype), ...`args`: any[]): _any_

_Defined in [src/utils/serialization.ts:279](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/serialization.ts#L279)_

Convert value to type of [SerializedType](../modules/utils_serialization#serializedtype) or [SerializedEncoding](../modules/utils_serialization#serializedencoding)

**Parameters:**

| Name       | Type                                                                    | Description                                                             |
| ---------- | ----------------------------------------------------------------------- | ----------------------------------------------------------------------- |
| `value`    | any                                                                     | -                                                                       |
| `encoding` | [SerializedEncoding](../modules/utils_serialization#serializedencoding) | [SerializedEncoding](../modules/utils_serialization#serializedencoding) |
| `intype`   | [SerializedType](../modules/utils_serialization#serializedtype)         | [SerializedType](../modules/utils_serialization#serializedtype)         |
| `outtype`  | [SerializedType](../modules/utils_serialization#serializedtype)         | [SerializedType](../modules/utils_serialization#serializedtype)         |
| `...args`  | any[]                                                                   | -                                                                       |

**Returns:** _any_

type of [SerializedType](../modules/utils_serialization#serializedtype) or [SerializedEncoding](../modules/utils_serialization#serializedencoding)

---

### serialize

▸ **serialize**(`serialize`: [Serializable](utils_serialization.serializable), `vm`: string, `encoding`: [SerializedEncoding](../modules/utils_serialization#serializedencoding), `notes`: string): _[Serialized](../interfaces/common_interfaces.serialized)_

_Defined in [src/utils/serialization.ts:327](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/serialization.ts#L327)_

**Parameters:**

| Name        | Type                                                                    | Default   |
| ----------- | ----------------------------------------------------------------------- | --------- |
| `serialize` | [Serializable](utils_serialization.serializable)                        | -         |
| `vm`        | string                                                                  | -         |
| `encoding`  | [SerializedEncoding](../modules/utils_serialization#serializedencoding) | "display" |
| `notes`     | string                                                                  | undefined |

**Returns:** _[Serialized](../interfaces/common_interfaces.serialized)_

---

### typeToBuffer

▸ **typeToBuffer**(`v`: any, `type`: [SerializedType](../modules/utils_serialization#serializedtype), ...`args`: any[]): _Buffer_

_Defined in [src/utils/serialization.ts:220](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/serialization.ts#L220)_

Convert [SerializedType](../modules/utils_serialization#serializedtype) to [Buffer](https://github.com/feross/buffer)

**Parameters:**

| Name      | Type                                                            | Description                                                             |
| --------- | --------------------------------------------------------------- | ----------------------------------------------------------------------- |
| `v`       | any                                                             | type of [SerializedType](../modules/utils_serialization#serializedtype) |
| `type`    | [SerializedType](../modules/utils_serialization#serializedtype) | [SerializedType](../modules/utils_serialization#serializedtype)         |
| `...args` | any[]                                                           | -                                                                       |

**Returns:** _Buffer_

[Buffer](https://github.com/feross/buffer)

---

### `Static` getInstance

▸ **getInstance**(): _[Serialization](utils_serialization.serialization)_

_Defined in [src/utils/serialization.ts:165](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/serialization.ts#L165)_

Retrieves the Serialization singleton.

**Returns:** _[Serialization](utils_serialization.serialization)_
