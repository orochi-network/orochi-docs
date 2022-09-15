---
description: >-
  Orocle is a Decentralized Oracle, a component of Orochi Computation Layer.
  Orocle establishes the interaction between smart contract and reality.
---

# 🪄 Orocle: Decentralized Oracle

## Problem

* The latency is too high, it took around 5-9mins to complete feeding process
* The sampling process isn't verifiable
* Oracle work like a third party service, Oracle doesn't accessible during the runtime

## Orocle' Features

**Orocle** v1.0 is providing:

**Verifiable:** sampling Using cryptography to prove and verify sampling process

**Depersity:** A system with many participants will join to sampling data by using Multi Party Computation (MPC)

**Low-cost:** With free tier, we allow users to request data or interact freely with 2,000 request/month Verifiable input All input will be sign with secp26k1 (ECDSA)

**Fault Proof:** If the game server tries to delay the feeding process to manipulate the result, a fault proof will be committed by Orochi Network so sue the game server.

**Multi-chain:** All EVM compatible blockchains can be supported

