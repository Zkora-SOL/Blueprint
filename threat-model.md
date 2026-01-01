# Z-Kora Threat Model
---


## Out-of-Scope Threats (Not Mitigated)


Z-Kora does NOT attempt to protect against:


- Network-level traffic analysis
- Global passive adversaries
- Compromised user devices or browsers
- Social engineering attacks
- Key theft due to poor user security practices


These risks must be addressed through complementary tools or user education.


---


## On-Chain Threats


- Smart contract bugs
- Incorrect verifier implementation
- Replay attacks


**Mitigations:**
- Extensive testing
- Formal verification where possible
- External security audits


---


## Off-Chain Threats


- Relayer censorship
- Metadata leakage through RPC endpoints
- Availability attacks


**Mitigations:**
- Permissionless relayer model
- Optional self-relaying
- Support for multiple RPC providers


---


## User Responsibility Model


Users are responsible for:
- Securing private keys
- Verifying frontend authenticity
- Understanding privacy limitations


Z-Kora cannot protect users from compromised environments.


---


## Incident Response & Upgradability


- Critical issues may require contract upgrades
- Emergency pauses may be implemented where strictly necessary
- Governance mechanisms will be documented separately


---


## Summary


Z-Kora provides **cryptographic privacy guarantees** within clearly defined security boundaries. By explicitly stating assumptions and non-goals, the protocol avoids false promises and enables realistic risk assessment by users and auditors.
