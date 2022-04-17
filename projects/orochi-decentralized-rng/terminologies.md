---
description: >-
  We will try to describe all terminologies here, that help you to understand
  the protocol and all denotes.
---

# 🗒 Terminologies

<details>

<summary>Dealer</summary>

Who's generate randomness and contribute their randomness to construct the grand randomness.

</details>

<details>

<summary>Verifier</summary>

Who's observe the process and verify distributed shares from the randomness. They can receive reward by committing dishonest dealer/verifier.

</details>

<details>

<summary>Participant</summary>

Who's participate in Orochi đRNG protocol they played two roles **Dealer** and **Verifier**

</details>

<details>

<summary>Public Verifiable Secret Sharing (PVSS)</summary>

A mechanism to split secret into share and allows any one to verify the shares of a secret without reveal the secret.

</details>

<details>

<summary>Verifiable Random Function (VRF)</summary>

Generating a randomness for a corresponding key-pair, the generated value is verifiable

</details>

<details>

<summary>Grand Randomness</summary>

The value which was constructed by combine all randomnesses.

</details>

<details>

<summary>Randomness</summary>

Orochi đRNG will use VRF to draw the randomness, this process is necessary to prevent participants to contribute low entropy randomness and detect dishonest participant.

</details>

<details>

<summary>Randomness shares</summary>

Orochi đRNG will use PVSS to split the randomness into shares. At the genesis of each epoch no one know enough share to reconstruct Grand Randomness till the end of epoch.

</details>

<details>

<summary>đRNG</summary>

This term is promoted by Orochi Network to represent for Decentralized RNG.

</details>
