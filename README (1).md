---
description: >-
  Orand is a component of Orochi Computation Layer that will be the source of
  trustless randomness. It provides randomness for Orochi Computation Layer and
  all supported blockchains.
---

# ☢ Orand: Decentralized Random Number Generator

## Problem

* There is no trustless source of randomness, even the advanced approach like [drand](https://drand.love)
* The cost is overwhelming  to feeding and verify a randomness
* There is no penalty for malfunction participants and colluding parties
* Most of distributed RNG is built with the fail-stop mechanism it's also no penalty to withholding secret
* Randomness values aren't accessible during the runtime

## Orand

A **Decentralized Random Number Generator** by Orochi Network. Allowed randomness to be generated and fed to any smart contracts on EVM compatible blockchains.

### Orand v1.0 is providing:

**Verifiable randomness:** We're using Verifiable Random Function (VRF) to generate randomness the process described here [https://www.rfc-editor.org/rfc/rfc6979](https://www.rfc-editor.org/rfc/rfc6979). Curve **secp256k1** was used to minimizing verification cost for smart contract.

**Depersity:** A distributed system with many participants/nodes will join to generate randomness by using **Multi Party Computation** (MPC)

**Unpredictability:** A VRF will perform with the input is previous randomness and it’s also require half of participants to participate in MPC

**High throughput:** Game server could request randomness from the **Orand** system. The result will be provided as soon as half of participants participate in the MPC.

**Cheap and secure randomness:** For the free tier, randomnesses will be given freely for the first 20,000 randomnesses every month.

**Fault Proof:** If the game server tries to delay the feeding process to manipulate the result, a fault proof will be committed so sue the game server.

**Multi-chain:** All EVM compatible blockchains can be supported

## Architecture

All components will be implemented as a module and this approach help other project to reuse our source code.

![](<.gitbook/assets/image (2).png>)
