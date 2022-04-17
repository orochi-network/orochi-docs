---
description: We're going to describe the process to generate the randomness
---

# 🤖 Protocol

## Epoch

Assuming that we have $$n$$ participants denote $$P_1, P_2, ... P_n$$. Each participant play two roles in our system dealer and verifier. Each participant have their own key-pair $$\{SK_i,PK_i\}$$ and the public key $$PK_i$$ is available to all other participants.

### Draw

All participants $$P_i$$ will need to generate their secret and also randomness by using VRF with$$x$$ is the grand randomness of previous epoch. In the genesis epoch $$x$$ can be&#x20;

choose by any participant.&#x20;

$$
\{r_i,\pi_{x}\}=f_{SK_{i}}(x)
$$

### Split

Each participant $$P_i$$ will use the PVSS to split the randomness&#x20;

Gossip

Virtual Voting

Audit

Conclusion

