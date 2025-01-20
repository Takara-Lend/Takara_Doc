# 🔴 Sei V2 EVM

[Sei](https://www.sei.io/) v2 is introduced as the pioneering blockchain that utilizes a parallelized Ethereum Virtual Machine (EVM), marking a substantial evolution from its predecessor.

## Key Features of Sei v2

**Parallelization:**

Optimistic parallelization is a feature of Sei v2, enabling developers to perform parallel transactions without defining dependencies. To preserve determinism, conflicting transactions that affect the same state will be replayed consecutively.

**Backward Compatibility:**

Sei v2 aims to achieve backward compatibility with Ethereum by smoothly redeploying important Ethereum smart contracts on Sei with no code modifications. Ethereum transaction processing will be possible thanks to the automatic import of Geth by the Sei chain binary.

**Optimized State Storage (SeiDB):**

Sei v2 re-architects the storage layer by breaking the IAVL tree into two components: state store and state commitment. The goals of the new storage architecture are to facilitate new node synchronization, decrease state bloat, and enhance read/write performance. PebbleDB will replace GoLevelDB in Sei v2 to increase read/write performance during multi-threaded access.

**Interoperability:**

Transactions across different components of Sei (Cosmwasm, EVM, bank, staking) can communicate seamlessly. Different sorts of transactions are processed by Sei native, which creates a more cohesive developer experience.

**Performance Metrics:**

Sei v2 supports finality and block times of 390 ms along with 28,300 batched transactions per second. Performance tests conducted in a cluster of twenty nodes show encouraging outcomes for optimistic parallelization with SeiDB.
