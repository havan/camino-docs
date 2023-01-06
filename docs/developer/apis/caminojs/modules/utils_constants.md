# Module: Utils-Constants

## Index

### Type aliases

- [MergeRule](utils_constants#mergerule)

### Variables

- [AVAXGWEI](utils_constants#const-avaxgwei)
- [AVAXSTAKECAP](utils_constants#const-avaxstakecap)
- [CChainAlias](utils_constants#const-cchainalias)
- [CChainVMName](utils_constants#const-cchainvmname)
- [CENTIAVAX](utils_constants#const-centiavax)
- [DECIAVAX](utils_constants#const-deciavax)
- [DefaultEVMLocalGenesisAddress](utils_constants#const-defaultevmlocalgenesisaddress)
- [DefaultEVMLocalGenesisPrivateKey](utils_constants#const-defaultevmlocalgenesisprivatekey)
- [DefaultLocalGenesisPrivateKey](utils_constants#const-defaultlocalgenesisprivatekey)
- [DefaultNetworkID](utils_constants#const-defaultnetworkid)
- [DefaultPlatformChainID](utils_constants#const-defaultplatformchainid)
- [DummyBlockchainID](utils_constants#const-dummyblockchainid)
- [DummyPlatformChainID](utils_constants#const-dummyplatformchainid)
- [GWEI](utils_constants#const-gwei)
- [MICROAVAX](utils_constants#const-microavax)
- [MILLIAVAX](utils_constants#const-milliavax)
- [NANOAVAX](utils_constants#const-nanoavax)
- [NodeIDPrefix](utils_constants#const-nodeidprefix)
- [ONEAVAX](utils_constants#const-oneavax)
- [PChainAlias](utils_constants#const-pchainalias)
- [PChainVMName](utils_constants#const-pchainvmname)
- [PrivateKeyPrefix](utils_constants#const-privatekeyprefix)
- [TestAvaxAssetID](utils_constants#const-testavaxassetid)
- [TestCBlockchainID](utils_constants#const-testcblockchainid)
- [TestCChainID](utils_constants#const-testcchainid)
- [TestHRP](utils_constants#const-testhrp)
- [TestNetworkID](utils_constants#const-testnetworkid)
- [TestXBlockchainID](utils_constants#const-testxblockchainid)
- [WEI](utils_constants#const-wei)
- [XChainAlias](utils_constants#const-xchainalias)
- [XChainVMName](utils_constants#const-xchainvmname)
- [mnemonic](utils_constants#const-mnemonic)

## Type aliases

### MergeRule

Ƭ **MergeRule**: _"intersection" | "differenceSelf" | "differenceNew" | "symDifference" | "union" | "unionMinusNew" | "unionMinusSelf" | "ERROR"_

_Defined in [src/utils/constants.ts:62](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/constants.ts#L62)_

Rules used when merging sets

## Variables

### `Const` AVAXGWEI

• **AVAXGWEI**: _BN_ = NANOAVAX.clone()

_Defined in [src/utils/constants.ts:56](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/constants.ts#L56)_

---

### `Const` AVAXSTAKECAP

• **AVAXSTAKECAP**: _BN_ = ONEAVAX.mul(new BN(3000000))

_Defined in [src/utils/constants.ts:57](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/constants.ts#L57)_

---

### `Const` CChainAlias

• **CChainAlias**: _string_ = "C"

_Defined in [src/utils/constants.ts:13](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/constants.ts#L13)_

---

### `Const` CChainVMName

• **CChainVMName**: _string_ = "evm"

_Defined in [src/utils/constants.ts:16](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/constants.ts#L16)_

---

### `Const` CENTIAVAX

• **CENTIAVAX**: _BN_ = ONEAVAX.div(new BN(100))

_Defined in [src/utils/constants.ts:49](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/constants.ts#L49)_

---

### `Const` DECIAVAX

• **DECIAVAX**: _BN_ = ONEAVAX.div(new BN(10))

_Defined in [src/utils/constants.ts:48](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/constants.ts#L48)_

---

### `Const` DefaultEVMLocalGenesisAddress

• **DefaultEVMLocalGenesisAddress**: _string_ = "0x8db97C7cEcE249c2b98bDC0226Cc4C2A57BF52FC"

_Defined in [src/utils/constants.ts:42](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/constants.ts#L42)_

---

### `Const` DefaultEVMLocalGenesisPrivateKey

• **DefaultEVMLocalGenesisPrivateKey**: _string_ = "0x56289e99c94b6912bfc12adc093c9b51124f0dc54ac7a766b2bc5ccf558d8027"

_Defined in [src/utils/constants.ts:40](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/constants.ts#L40)_

---

### `Const` DefaultLocalGenesisPrivateKey

• **DefaultLocalGenesisPrivateKey**: _string_ = "ewoqjP7PxY4yr3iLTpLisriqt94hdyDFNgchSxGGztUrTXtNN"

_Defined in [src/utils/constants.ts:38](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/constants.ts#L38)_

---

### `Const` DefaultNetworkID

• **DefaultNetworkID**: _1_ = 1

_Defined in [src/utils/constants.ts:8](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/constants.ts#L8)_

---

### `Const` DefaultPlatformChainID

• **DefaultPlatformChainID**: _string_ = "11111111111111111111111111111111LpoYY"

_Defined in [src/utils/constants.ts:23](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/constants.ts#L23)_

---

### `Const` DummyBlockchainID

• **DummyBlockchainID**: _"aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa"_ = "aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa"

_Defined in [src/utils/constants.ts:31](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/constants.ts#L31)_

---

### `Const` DummyPlatformChainID

• **DummyPlatformChainID**: _string_ = "11111111111111111111111111111111LpoXX"

_Defined in [src/utils/constants.ts:33](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/constants.ts#L33)_

---

### `Const` GWEI

• **GWEI**: _BN_ = WEI.mul(new BN(1000000000))

_Defined in [src/utils/constants.ts:55](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/constants.ts#L55)_

---

### `Const` MICROAVAX

• **MICROAVAX**: _BN_ = ONEAVAX.div(new BN(1000000))

_Defined in [src/utils/constants.ts:51](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/constants.ts#L51)_

---

### `Const` MILLIAVAX

• **MILLIAVAX**: _BN_ = ONEAVAX.div(new BN(1000))

_Defined in [src/utils/constants.ts:50](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/constants.ts#L50)_

---

### `Const` NANOAVAX

• **NANOAVAX**: _BN_ = ONEAVAX.div(new BN(1000000000))

_Defined in [src/utils/constants.ts:52](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/constants.ts#L52)_

---

### `Const` NodeIDPrefix

• **NodeIDPrefix**: _string_ = "NodeID-"

_Defined in [src/utils/constants.ts:11](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/constants.ts#L11)_

---

### `Const` ONEAVAX

• **ONEAVAX**: _BN_ = new BN(1000000000)

_Defined in [src/utils/constants.ts:47](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/constants.ts#L47)_

---

### `Const` PChainAlias

• **PChainAlias**: _string_ = "P"

_Defined in [src/utils/constants.ts:14](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/constants.ts#L14)_

---

### `Const` PChainVMName

• **PChainVMName**: _string_ = "platformvm"

_Defined in [src/utils/constants.ts:17](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/constants.ts#L17)_

---

### `Const` PrivateKeyPrefix

• **PrivateKeyPrefix**: _string_ = "PrivateKey-"

_Defined in [src/utils/constants.ts:10](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/constants.ts#L10)_

---

### `Const` TestAvaxAssetID

• **TestAvaxAssetID**: _"2fombhL7aGPwj3KH4bfrmJwW6PVnMobf9Y2fn9GwxiAAJyFDbe"_ = "2fombhL7aGPwj3KH4bfrmJwW6PVnMobf9Y2fn9GwxiAAJyFDbe"

_Defined in [src/utils/constants.ts:21](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/constants.ts#L21)_

---

### `Const` TestCBlockchainID

• **TestCBlockchainID**: _"2CA6j5zYzasynPsFeNoqWkmTCt3VScMvXUZHbfDJ8k3oGzAPtU"_ = "2CA6j5zYzasynPsFeNoqWkmTCt3VScMvXUZHbfDJ8k3oGzAPtU"

_Defined in [src/utils/constants.ts:27](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/constants.ts#L27)_

---

### `Const` TestCChainID

• **TestCChainID**: _42112_ = 42112

_Defined in [src/utils/constants.ts:29](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/constants.ts#L29)_

---

### `Const` TestHRP

• **TestHRP**: _"local"_ = "local"

_Defined in [src/utils/constants.ts:19](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/constants.ts#L19)_

---

### `Const` TestNetworkID

• **TestNetworkID**: _12345_ = 12345

_Defined in [src/utils/constants.ts:20](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/constants.ts#L20)_

---

### `Const` TestXBlockchainID

• **TestXBlockchainID**: _"2eNy1mUFdmaxXNj1eQHUe7Np4gju9sJsEtWQ4MX3ToiNKuADed"_ = "2eNy1mUFdmaxXNj1eQHUe7Np4gju9sJsEtWQ4MX3ToiNKuADed"

_Defined in [src/utils/constants.ts:25](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/constants.ts#L25)_

---

### `Const` WEI

• **WEI**: _BN_ = new BN(1)

_Defined in [src/utils/constants.ts:54](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/constants.ts#L54)_

---

### `Const` XChainAlias

• **XChainAlias**: _string_ = "X"

_Defined in [src/utils/constants.ts:12](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/constants.ts#L12)_

---

### `Const` XChainVMName

• **XChainVMName**: _string_ = "avm"

_Defined in [src/utils/constants.ts:15](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/constants.ts#L15)_

---

### `Const` mnemonic

• **mnemonic**: _string_ = "output tooth keep tooth bracket fox city sustain blood raise install pond stem reject long scene clap gloom purpose mean music piece unknown light"

_Defined in [src/utils/constants.ts:44](https://github.com/chain4travel/caminojs/blob/3883166/src/utils/constants.ts#L44)_
