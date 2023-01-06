# Class: Networks

A class for storing predefined / fetched networks

## Hierarchy

- **Networks**

## Index

### Constructors

- [constructor](utils_networks.networks#constructor)

### Properties

- [registry](utils_networks.networks#registry)

### Methods

- [getNetwork](utils_networks.networks#getnetwork)
- [registerNetwork](utils_networks.networks#registernetwork)

## Constructors

### constructor

\+ **new Networks**(): _[Networks](utils_networks.networks)_

_Defined in [src/utils/networks.ts:172](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/networks.ts#L172)_

**Returns:** _[Networks](utils_networks.networks)_

## Properties

### registry

• **registry**: _Map‹string, [Network](../interfaces/utils_networks.network)›_ = new Map()

_Defined in [src/utils/networks.ts:172](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/networks.ts#L172)_

## Methods

### getNetwork

▸ **getNetwork**(`networkID`: number): _[Network](../interfaces/utils_networks.network)_

_Defined in [src/utils/networks.ts:183](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/networks.ts#L183)_

**Parameters:**

| Name        | Type   |
| ----------- | ------ |
| `networkID` | number |

**Returns:** _[Network](../interfaces/utils_networks.network)_

---

### registerNetwork

▸ **registerNetwork**(`networkID`: number, `network`: [Network](../interfaces/utils_networks.network)): _void_

_Defined in [src/utils/networks.ts:179](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/networks.ts#L179)_

**Parameters:**

| Name        | Type                                            |
| ----------- | ----------------------------------------------- |
| `networkID` | number                                          |
| `network`   | [Network](../interfaces/utils_networks.network) |

**Returns:** _void_
