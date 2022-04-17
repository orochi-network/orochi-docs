---
description: >-
  Orochi đRNG is a component of Orochi Computation Layer that will be the source
  of trustless randomness. It provides randomness for Orochi Computation Layer
  and all supported blockchains.
---

# 🐉 Orochi Decentralized RNG

## Problem

* There is no trustless source of randomness, even the advanced approach like [drand](https://drand.love)
* It's cost too munch to feeding and verify a randomness
* There is no penalty for malfunction participants and colluding parties
* Most of distributed RNG is built with the fail-stop mechanism it's also no penalty to secret withholding&#x20;

## Architecture

All components will be implemented as a Go module and this approach help other project to reuse our source code.

![Architecture of Orochi đRNG full-node](<.gitbook/assets/image (1).png>)
