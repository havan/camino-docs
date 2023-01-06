# Module: Utils-Networks

## Index

### Classes

- [Networks](../classes/utils_networks.networks)

### Interfaces

- [C](../interfaces/utils_networks.c)
- [Network](../interfaces/utils_networks.network)
- [P](../interfaces/utils_networks.p)
- [X](../interfaces/utils_networks.x)

### Object literals

- [AvaxMainNetwork](utils_networks#const-avaxmainnetwork)
- [TestNetwork](utils_networks#const-testnetwork)

## Object literals

### `Const` AvaxMainNetwork

### ▪ **AvaxMainNetwork**: _object_

_Defined in [src/utils/networks.ts:124](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/networks.ts#L124)_

### hrp

• **hrp**: _string_ = "avax"

_Defined in [src/utils/networks.ts:125](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/networks.ts#L125)_

▪ **C**: _object_

_Defined in [src/utils/networks.ts:154](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/networks.ts#L154)_

- **alias**: _string_ = CChainAlias

- **blockchainID**: _string_ = "2q9e4r6Mu3U68nU1fYjgbR6JvwrRx36CohpAX5UQxse55x1Q5"

- **chainID**: _number_ = 43114

- **costPerSignature**: _number_ = 1000

- **gasPrice**: _BN‹›_ = GWEI.mul(new BN(225))

- **maxGasPrice**: _BN‹›_ = GWEI.mul(new BN(1000))

- **minGasPrice**: _BN‹›_ = GWEI.mul(new BN(25))

- **txBytesGas**: _number_ = 1

- **txFee**: _BN‹›_ = MILLIAVAX

- **vm**: _string_ = CChainVMName

▪ **P**: _object_

_Defined in [src/utils/networks.ts:136](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/networks.ts#L136)_

- **alias**: _string_ = PChainAlias

- **blockchainID**: _string_ = DefaultPlatformChainID

- **createChainTx**: _BN‹›_ = ONEAVAX

- **createSubnetTx**: _BN‹›_ = ONEAVAX

- **creationTxFee**: _BN‹›_ = CENTIAVAX

- **maxConsumption**: _number_ = 0.12

- **maxStakeDuration**: _number_ = 365 _ 24 _ 60 \* 60

- **maxStakingDuration**: _BN‹›_ = new BN(31536000)

- **maxSupply**: _BN‹›_ = new BN(720000000).mul(ONEAVAX)

- **minConsumption**: _number_ = 0.1

- **minDelegationFee**: _BN‹›_ = new BN(2)

- **minDelegationStake**: _BN‹›_ = ONEAVAX.mul(new BN(25))

- **minStake**: _BN‹›_ = ONEAVAX.mul(new BN(2000))

- **minStakeDuration**: _number_ = 2 _ 7 _ 24 _ 60 _ 60

- **txFee**: _BN‹›_ = MILLIAVAX

- **vm**: _string_ = PChainVMName

▪ **X**: _object_

_Defined in [src/utils/networks.ts:126](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/networks.ts#L126)_

- **alias**: _string_ = XChainAlias

- **avaxAssetAlias**: _string_ = "AVAX"

- **avaxAssetID**: _string_ = "FvwEAhmxKfeiG8SnEvq42hc6whRyY3EFYAvebMqDNDGCgxN5Z"

- **blockchainID**: _string_ = "2oYMBNV4eNHyqk2fjjV5nVQLDbtmNJzq5s3qs3Lo6ftnC6FByM"

- **creationTxFee**: _BN‹›_ = CENTIAVAX

- **mintTxFee**: _BN‹›_ = MILLIAVAX

- **txFee**: _BN‹›_ = MILLIAVAX

- **vm**: _string_ = XChainVMName

---

### `Const` TestNetwork

### ▪ **TestNetwork**: _object_

_Defined in [src/utils/networks.ts:79](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/networks.ts#L79)_

### hrp

• **hrp**: _string_ = TestHRP

_Defined in [src/utils/networks.ts:80](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/networks.ts#L80)_

▪ **C**: _object_

_Defined in [src/utils/networks.ts:109](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/networks.ts#L109)_

- **alias**: _string_ = CChainAlias

- **blockchainID**: _string_ = TestCBlockchainID

- **chainID**: _number_ = 43112

- **costPerSignature**: _number_ = 1000

- **gasPrice**: _BN‹›_ = GWEI.mul(new BN(225))

- **maxGasPrice**: _BN‹›_ = GWEI.mul(new BN(1000))

- **minGasPrice**: _BN‹›_ = GWEI.mul(new BN(25))

- **txBytesGas**: _number_ = 1

- **txFee**: _BN‹›_ = MILLIAVAX

- **vm**: _string_ = CChainVMName

▪ **P**: _object_

_Defined in [src/utils/networks.ts:91](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/networks.ts#L91)_

- **alias**: _string_ = PChainAlias

- **blockchainID**: _string_ = DefaultPlatformChainID

- **createChainTx**: _BN‹›_ = ONEAVAX

- **createSubnetTx**: _BN‹›_ = ONEAVAX

- **creationTxFee**: _BN‹›_ = CENTIAVAX

- **maxConsumption**: _number_ = 0.12

- **maxStakeDuration**: _number_ = 365 _ 24 _ 60 \* 60

- **maxStakingDuration**: _BN‹›_ = new BN(31536000)

- **maxSupply**: _BN‹›_ = new BN(720000000).mul(ONEAVAX)

- **minConsumption**: _number_ = 0.1

- **minDelegationFee**: _BN‹›_ = new BN(2)

- **minDelegationStake**: _BN‹›_ = ONEAVAX

- **minStake**: _BN‹›_ = ONEAVAX

- **minStakeDuration**: _number_ = 24 _ 60 _ 60

- **txFee**: _BN‹›_ = MILLIAVAX

- **vm**: _string_ = PChainVMName

▪ **X**: _object_

_Defined in [src/utils/networks.ts:81](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/networks.ts#L81)_

- **alias**: _string_ = XChainAlias

- **avaxAssetAlias**: _string_ = "AVAX"

- **avaxAssetID**: _string_ = TestAvaxAssetID

- **blockchainID**: _string_ = TestXBlockchainID

- **creationTxFee**: _BN‹›_ = CENTIAVAX

- **mintTxFee**: _BN‹›_ = MILLIAVAX

- **txFee**: _BN‹›_ = MILLIAVAX

- **vm**: _string_ = XChainVMName
