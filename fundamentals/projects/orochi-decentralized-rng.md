---
description: >-
  Orochi đRNG is a component of Orochi Computation Layer that will be the source
  of trustless randomness. It provides randomness for Orochi Computation Layer
  and all supported blockchains.
---

# Orochi Decentralized RNG

## Overview

All components will be implemented as a Go module and this approach help other project to reuse our source code.

![Architecture of Orochi đRNG full-node](<../../.gitbook/assets/image (1).png>)

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

