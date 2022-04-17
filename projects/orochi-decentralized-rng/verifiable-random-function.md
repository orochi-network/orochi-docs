---
description: >-
  This component provides the abilities to draw a verifiable randomness, we
  assume that all node's public keys are accessible by the other in the same
  network.
---

# 🀄 Verifiable Random Function

**Denote**

| Denote    | Description                                                         |
| --------- | ------------------------------------------------------------------- |
| $$SK$$    | Secret key                                                          |
| $$PK$$    | Public key or verify key                                            |
| $$G$$     | Key generator method                                                |
| $$r$$     | Verifiable randomness                                               |
| $$\pi_x$$ | Corresponding proof for $$x$$                                       |
| $$f$$     | Verifiable Random Function                                          |
| $$g$$     | Proving function which's use to verify $$(r,\pi_x)$$by using $$PK$$ |

We have

$$
(SK,PK)=G(1^k)
$$

Generating a randomness

$$
(r,\pi_x)=f_{SK}(x)
$$

Verifying a randomness

$$
g_{PK}(x,r,\pi_x)\in\{0,1\}
$$
