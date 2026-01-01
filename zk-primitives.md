# Z-Kora Zero-Knowledge Primitives
### Plonk (and variants)
- Universal trusted setup
- More flexible circuit upgrades
- Slightly higher verification cost


The choice of proof system may vary by module and network.


---


## Circuit Design Philosophy


Z-Kora circuits follow these principles:


- **Minimal disclosure:** Only prove what is strictly necessary
- **Composable logic:** Circuits can be reused across modules
- **Constraint efficiency:** Optimize for verification cost
- **Explicit assumptions:** No hidden trust or shortcuts


Circuits are treated as **security-critical components**.


---


## Core ZK Primitives in Z-Kora


### Membership Proofs


Used to prove that a user belongs to a valid set (e.g., shielded pool, identity set) without revealing which member they are.


### Balance & State Validity Proofs


Used to prove:
- Inputs equal outputs
- No double-spending occurs
- State transitions are valid


Without revealing actual balances.


### Selective Disclosure Proofs


Allow users to prove specific attributes (e.g., uniqueness, eligibility) without exposing full identity data.


### Access Control Proofs


Used in encrypted storage to prove access rights without revealing file contents or metadata.


---


## Privacy Guarantees


Z-Kora provides cryptographic guarantees that:
- Sensitive inputs are never revealed on-chain
- Proofs cannot be reverse-engineered to recover private data
- Verifiers learn nothing beyond statement validity


---


## Limitations & Non-Goals


Z-Kora does NOT guarantee:
- Network-layer anonymity
- Protection against malicious user devices
- Privacy against global traffic analysis


These risks are considered out of scope for the protocol.


---


## Auditing & Verification


- All circuits are open for review
- Formal verification is encouraged where applicable
- External audits are required before mainnet deployment


---


## Summary


Zero-knowledge primitives are the **core security foundation** of Z-Kora. By using ZK proofs as first-class components, Z-Kora enables privacy-preserving payments, identity, and data interactions without sacrificing decentralization or verifiability.
