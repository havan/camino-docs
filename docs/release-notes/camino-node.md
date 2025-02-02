---
sidebar_position: 2
---

# Camino-Node Releases

:::warning OBSOLETE

The [camino-node repository](https://github.com/chain4travel/camino-node) is
obsolete.

Development has been transitioned from the
[`camino-node`](https://github.com/chain4travel/camino-node) repository to the
[`caminogo`](https://github.com/chain4travel/caminogo) repository as of the `v1.1.0`
release. For release notes, please refer to the [this page](./caminogo.md).

:::

## v1.0.1

[View on GitHub](https://github.com/chain4travel/camino-node/releases/tag/v1.0.1)

- [Dependencies, Version] caminoethvm -> caminogo (Athens 1.0.1) by @evlekht
- [[PVM] Returns pre-Athens rewardsImportTx logic for pre-Athens txs] by @evlekht
- [[PVM, Spend] Allow spend to deposit unlocked tokens for different owner] by @evlekht
- [[Dependency, fix] Fix state sync version (fork leftover)] by @evlekht

**Full Changelog**: https://github.com/chain4travel/camino-node/compare/v1.0.0...v1.0.1

## v1.0.0

<p><span class="alert alert--info pill">Athens Phase</span></p>

[View on GitHub](https://github.com/chain4travel/camino-node/releases/tag/v1.0.0)

- Official Athens Phase Release

**caminogo**

- Athens Upgrade
- AddDepositOffer allows creation of deposit offers
- Whitelist / Owner controlled deposit offers
- AddressStateTx upgrade to make it MsigAlias capable
- Fix AddValidatorTx RewardOwner
- Fix bootstrap of SystemUnlockDepositTx (empty Creds[0])
- Fix AddddressStateTx Roles
- Admin API secret (dns attack)

**camino-node**

- Bump dependencies
- Adjust Config flags for admin api secret
- 1.9.16 avax to dev by @evlekht in #65
- update git version in dockerfile by @mo-c4t in #67
- Admin API DNS Rebinding mitigation by @DerTiedemann in #62
- Fix Validator reconnection when public IP changes

**Full Changelog**: https://github.com/chain4travel/camino-node/compare/v0.4.9...v1.0.0

## v0.4.9

[View on GitHub](https://github.com/chain4travel/camino-node/releases/tag/v0.4.9)

- caminogo: Fix bootstrap issues after RewardValTx
- caminogo: Change Deposit API (query with timestamp) and strings for uint64 result types.

**Full Changelog**: https://github.com/chain4travel/camino-node/compare/v0.4.9-rc1...v0.4.9

## v0.4.9-rc1

[View on GitHub](https://github.com/chain4travel/camino-node/releases/tag/v0.4.9-rc1)

- CaminoAddValidator NodeOwnerAuth
- Because we faced issues with the current UnsortedCredential checker, a subnetAuth was added to the CaminoAddValidatorTx.
- This authentication must handle credentials which verifies the Registered NodeID owner

**Full Changelog**: https://github.com/chain4travel/camino-node/compare/v0.4.8-rc1...v0.4.9-rc1

## v0.4.8-rc1

[View on GitHub](https://github.com/chain4travel/camino-node/releases/tag/v0.4.8-rc1)

- Version 0.4.8 (== compatibility)
- Add RewardOwner into Deposit (state)
- Multiple Owners getClaimables
- PVM Service: Remove APIOwner, instead use existing platformapi.Owner
- Fixed NodeIDs for Columbus by @Noctunus in #64

**Full Changelog**: https://github.com/chain4travel/camino-node/compare/v0.4.7-rc1...v0.4.8-rc1

## v0.4.7-rc1

[View on GitHub](https://github.com/chain4travel/camino-node/releases/tag/v0.4.7-rc1)

- General genesis update by @Noctunus in #63
- ClaimTx Rework (CaminoGo)

**Full Changelog**: https://github.com/chain4travel/camino-node/compare/v0.4.6-rc2...v0.4.7-rc1

## v0.4.6-rc2

[View on GitHub](https://github.com/chain4travel/camino-node/releases/tag/v0.4.6-rc2)

- caminogo: fix camino beacon (missing port)

**Full Changelog**: https://github.com/chain4travel/camino-node/compare/v0.4.6-rc1...v0.4.6-rc2

## v0.4.6-rc1

[View on GitHub](https://github.com/chain4travel/camino-node/releases/tag/v0.4.6-rc1)

- Camino genesis generation by @Noctunus in #60
- caminojs: genesis files / version bump 0.4.6 (== compatibility)
- caminojs: reward UTXO sorting

**Full Changelog**: https://github.com/chain4travel/camino-node/compare/v0.4.5-rc1...v0.4.6-rc1

## v0.4.5-rc1

[View on GitHub](https://github.com/chain4travel/camino-node/releases/tag/v0.4.5-rc1)

- Update of the genesis file (kopernikus) by @pnowosie in #58
- CaminoGo
  - CrossTransferOut to specify Import receiver already on export time
  - PlatformVM: Implement BaseTx to enable P -> P transfer

**Full Changelog**: https://github.com/chain4travel/camino-node/compare/v0.4.4-rc1...v0.4.5-rc1

## v0.4.4-rc1

[View on GitHub](https://github.com/chain4travel/camino-node/releases/tag/v0.4.4-rc1)

- Cleanup Release
- **This version is NOT compatible to earlier camino-node versions**
- Simplify DepositOffer DB storage
- Update Columbus Genesis

**Full Changelog**: https://github.com/chain4travel/camino-node/compare/v0.4.3-rc3...v0.4.4-rc1

## v0.4.3-rc2

[View on GitHub](https://github.com/chain4travel/camino-node/releases/tag/v0.4.3-rc2)

- Fix UnlockDeposit
- Rework MultisigAlias handling
- Updated genesis files (columbus / kopernikus)
- API changes for rewards (deposit / treasury differentation)
- Forbid Export of MultisigAlias funds
- Implement Auto-UnlockDeposit
- LRU cache for MSigAliases (16384)
- Revert SigIndex math.Uint32 magic number
- RegisterNodeTx: Forbid registration of already registered node

(Includes changelog from unreleased version of `v0.4.3-rc1`)

**Full Changelog**: https://github.com/chain4travel/camino-node/compare/v0.4.2-rc2...v0.4.3-rc2

## v0.4.2-rc2

[View on GitHub](https://github.com/chain4travel/camino-node/releases/tag/v0.4.2-rc2)

- Genesis generator update
- Publickey recovery tests
- allow to choose P/X destination of the free funds
- Regenerated kopernikus & columbus json files
- Deposit offers read from xls instead of template
- Dependencies and formatting
- Threshold moved to Multisig workbook
- Validation of missed columns: KYC, consortium
- Regenerated genesis files
- [Dependencies] Latest fixes
- [GENESIS] Additional checks for the genesis generator tool
- Fix broken links in README
- Updated columbus genesis to the latest state
- [DEPENDENCIES] caminoethvm (GasFee / ExportLimit) -> caminogo (claim)

**Full Changelog**: https://github.com/chain4travel/camino-node/compare/v0.4.2-rc1...v0.4.2-rc2

## v0.4.2-rc1

[View on GitHub](https://github.com/chain4travel/camino-node/releases/tag/v0.4.2-rc1)

- Genesis generator update
- Publickey recovery tests
- allow to choose P/X destination of the free funds
- Regenerated kopernikus & columbus json files
- Deposit offers read from xls instead of template
- Dependencies and formatting
- Threshold moved to Multisig workbook
- Validation of missed columns: KYC, consortium
- Regenerated genesis files
- [Dependencies] Latest fixes
- [GENESIS] Additional checks for the genesis generator tool
- Fix broken links in README
- Updated columbus genesis to the latest state
- [DEPENDENCIES] caminoethvm (GasFee / ExportLimit) -> caminogo (claim)
- Peak3d/bump

**Full Changelog**: https://github.com/chain4travel/camino-node/compare/v0.4.1-rc2...v0.4.2-rc1

## v0.4.1-rc2

[View on GitHub](https://github.com/chain4travel/camino-node/releases/tag/v0.4.1-rc2)

- Split genesis `platformAllocation` to only stake `maxStakingAmount`
- Add depositTx inputs for already bonded UTXOs

**Full Changelog**: https://github.com/chain4travel/camino-node/compare/v0.4.1-rc1...v0.4.1-rc2

---

## v0.4.1-rc1

:::caution WARNING

This branch has bugs. Please use [v0.4.1-rc2](#v041-rc2) instead.

:::

[View on GitHub](https://github.com/chain4travel/camino-node/releases/tag/v0.4.1-rc1)

Based on avalanchego v1.9.4 (Banff)

#### PlatformVM:

- DepositBond mode instead stake/delegate (for camino networks)
- AddressStates for KYC / ConsortiumMembers
- Registration NodeID `<->` Consortium member
- Multisigaddresses

#### X-Chain:

- Unchanged

#### C-Chain

- Fixed Base Fee
- KYC over predeployed admin Smart Contract
- Contract deploy restricted to KYC verified addresses

**Full Changelog**: https://github.com/chain4travel/camino-node/compare/v0.4.0-alpha2...v0.4.1-rc1

---

## v0.4.0-alpha2

[View on GitHub](https://github.com/chain4travel/camino-node/releases/tag/v0.4.0-alpha2)

**Full Changelog**: https://github.com/chain4travel/camino-node/compare/v0.4.0-alpha1...v0.4.0-alpha2

---

## v0.4.0-alpha1

[View on GitHub](https://github.com/chain4travel/camino-node/releases/tag/v0.4.0-alpha1)

#### What's Changed

- Disable ansible_lint / artifacts only on release
- Fix CI Tests
- Add .editorconfig

**Full Changelog**: https://github.com/chain4travel/camino-node/compare/v0.3.0-alpha1...v0.4.0-alpha1

---

## v0.3.0-alpha1

[View on GitHub](https://github.com/chain4travel/camino-node/releases/tag/v0.3.0-alpha1)

#### What's Changed

This release is based on latest avalanche-network runner and has only slight modifications to get camino-node instead avalanchego running.

**Full Changelog**: https://github.com/chain4travel/camino-node/compare/v0.2.1-rc2...v0.3.0-alpha1

---

## v0.2.1-rc2

[View on GitHub](https://github.com/chain4travel/camino-node/releases/tag/v0.2.1-rc2)

- Build with [CaminoEthVM](./caminoethvm.md#v012-rc2) v0.1.2-rc2

---

## v0.2.1-rc1

[View on GitHub](https://github.com/chain4travel/camino-node/releases/tag/v0.2.1-rc1)

- Based On [CaminoGo](./caminogo.md#v0_2_0) v0.2.0
- Build with [CaminoEthVM](./caminoethvm.md#v0_1_2-rc1) v0.1.2-rc1
