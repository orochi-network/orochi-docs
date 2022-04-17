---
description: >-
  Orochi đRNG is a component of Orochi Computation Layer that will be the source
  of trustless randomness. It provides randomness for Orochi Computation Layer
  and all supported blockchains.
---

# Orochi Decentralized RNG

## Problem

* There is no trustless source of randomness, even the advanced approach like [drand](https://drand.love)
* It's cost too munch to feeding and verify a randomness
* There is no penalty for malfunction participants and colluding parties
* Most of distributed RNG is built with the fail-stop mechanism it's also no penalty to secret withholding&#x20;

## Architecture

All components will be implemented as a Go module and this approach help other project to reuse our source code.

![Architecture of Orochi đRNG full-node](<../.gitbook/assets/image (1).png>)

###

### Components

* Verifiable Random Function (VRF)\
  We're still using VRF to draw the randomness, it prevent the distributor to generate&#x20;

### Verifiable Random Function (VRF)

This component provides the abilities to draw a verifiable randomness, we assume that all node's public keys are accessible by the other in the same network.

We have G is a key-pair generator

$$
(SK,PK)=G(1^k)
$$

Generating a randomness

$$
(r,\pi_x)=f_{sk}(x)
$$

Verifying a randomness

$$
g_{PK}(r,\pi_x)\in\{0,1\}
$$

