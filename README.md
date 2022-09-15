---
description: >-
  We defines the next form of the gaming industry. Orochi Network is the first
  Computation Layer solution that revamps latency and improve processing
  performance.
---

# 💕 Orochi Network

{% hint style="info" %}
**Good to know:** Orochi Network provides missing components to "run" the game in the decentralized fashion. It covers wide range of needs from trustless randomness to verifiable computation.
{% endhint %}

## Getting Started

### Unique selling points:

**High performance:** Orochi Network provides semi-native performance with Verifiable WebAssembly Runtime.

**Zero latency:** Orochi Network makes all critical components to be available at the runtime that reduces latency significantly.

**Non-blocking:** Orochi Network terminated third party interactive there is no need for awaiting the third party responses.

**Decentralized:** Orochi Network uses validity proof to secure the network and prove the computation process thus our network doesn't require third party trust.

**Seamless:** Orochi Network has an embedded WebAssembly runtime that can execute arbitrary given WebAssembly opcodes. It doesn't require a unique toolchain to compile a program to be compatible with Orochi Network’s runtime.

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

{% content-ref url="README (1).md" %}
[README (1).md](<README (1).md>)
{% endcontent-ref %}
