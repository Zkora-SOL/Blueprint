# Z-Kora Architecture
- Updating on-chain state without revealing private inputs


**Key Properties:**
- Deterministic
- Transparent verification
- No access to plaintext user data


---


## Core Data Flows


### Private Payment Flow (ZK-Pay)


1. User creates a payment intent locally
2. ZK circuit generates a proof of validity
3. Encrypted transaction data is prepared
4. Relayer submits proof to the smart contract
5. Contract verifies proof and updates state
6. Funds are transferred privately


At no point are sender, receiver, or amount revealed on-chain.


---


### Identity Proof Flow (ZK-ID)


1. User holds identity credentials off-chain
2. User generates a selective disclosure proof
3. Proof is submitted to verifier contract
4. Contract verifies required attributes only


No raw identity data is stored on-chain.


---


## Storage Architecture (ZK-Storage)


- Files are encrypted client-side
- Encrypted files are stored on decentralized storage (e.g., IPFS)
- Access is controlled via ZK-based access proofs
- Smart contracts only verify access rights, not content


---


## Design Decisions & Rationale


- **Client-side proof generation:** minimizes trust and leakage
- **Off-chain relayers:** improve UX without custody
- **On-chain verification only:** keeps blockchain interactions minimal
- **Modularity:** each module can evolve independently


---


## Privacy & Security Boundaries


Z-Kora guarantees:
- No plaintext sensitive data on-chain
- No custodial control over user assets
- Cryptographic privacy, not policy-based privacy


Z-Kora does not guarantee:
- Network-level anonymity
- Protection against compromised user devices


---


## Future Extensions


- Decentralized relayer network
- Hardware-based proof acceleration
- Cross-chain privacy interoperability


---


## Summary


Z-Kora’s architecture is designed to make privacy a **default property** of Web3 interactions. By combining client-side cryptography, off-chain coordination, and on-chain verification, Z-Kora delivers scalable and composable privacy infrastructure.
