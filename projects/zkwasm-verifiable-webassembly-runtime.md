---
description: >-
  High performance verifiable runtime, that allow all kind of nextgen
  application to be executed and verify with semi zero-cost.
---

# 🦸 zkWASM: Verifiable WebAssembly Runtime

## Problem

* Blockchain is a synchronous system, it can not handle asynchronous events meanwhile game logic need to handle asynchronous events and process all requests in the real-time.&#x20;
* EVM and blockchain aren't suitable for real-time interactive, in some cases WebAssembly cloud be 2,000 times faster than EVM. EVM has never ever reach the semi-native performance.
* Blockchain can't achieve instant finality that's why the latency is around 60-90 secs for blockchain to finalize its state.

## zkWASM: Verifiable WebAssembly Runtime

* **High Performance:** WebAssembly itself was designed to archive semi-native performance
* **Seamless:** WebAssembly is architecture/operating system independent. All popular programing language can be compiled to WebAssembly opcodes, it doesn't require a new toolchain for WebAssembly.
* **Verifiable:** Applying **Succinct Non-Interactive Argument of Knowledge** (SNARK), allowed us to proving the computation process to generate validity proof along side with the result. We can verify the correctness of the computational process with a lower cost.
