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

## Architecture

All components will be implemented as a module and this approach help other project to reuse our source code.

![](<.gitbook/assets/image (2).png>)
