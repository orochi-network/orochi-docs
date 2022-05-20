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

### References

* [https://doi.org/10.1007/s00145-019-09331-1](https://doi.org/10.1007/s00145-019-09331-1)
* [https://eprint.iacr.org/2004/310.pdf](https://eprint.iacr.org/2004/310.pdf)
* [https://dash.harvard.edu/bitstream/handle/1/5028196/Vadhan\_VerifRandomFunction.pdf](https://dash.harvard.edu/bitstream/handle/1/5028196/Vadhan\_VerifRandomFunction.pdf)
* [https://github.com/coniks-sys/coniks-go/blob/master/crypto/vrf/vrf.go](https://github.com/coniks-sys/coniks-go/blob/master/crypto/vrf/vrf.go)
