# DORA Regulation Mapping — Encryption and Cryptographic Controls

**Example output from DORA Audit Mapper v8**
**System prompt:** v8_PUBLIC | **Knowledge base:** 652 chunks across 5 instruments
**Model tested on:** Claude Sonnet 4.6

---

## DORA Regulation Mapping — Encryption and Cryptographic Controls

### Audit Context

- Entity type: Investment firm, non-microenterprise, standard framework
- Audit topic: Encryption and cryptographic controls
- Audit objective: not specified (general regulation mapping)
- Scope exclusions applied: Title III of RTS ICT-RMF (Arts 28–41) and DORA Art.16(1) provisions filtered out — entity is not under the simplified framework

### Section 1 — Directly Applicable Provisions

These provisions impose direct obligations on the entity. Include them in scope without preconditions.

| Citation | Obligation Summary | Why Applicable | Expanded by |
|---|---|---|---|
| Art.9(1) [Main DORA] | Continuously monitor and control the security and functioning of ICT systems through appropriate security tools, policies and procedures. | Foundational protection obligation under which cryptographic controls operate. | RTS on ICT Risk Management [loaded] |
| Art.9(2) [Main DORA] | Design, procure and implement ICT security policies, procedures, protocols and tools to maintain high standards of availability, authenticity, integrity and confidentiality of data at rest, in use or in transit. | Direct anchor for the encryption obligation — explicitly references confidentiality and integrity of data across all three states. | RTS on ICT Risk Management [loaded] |
| Art.9(3) [Main DORA] | Use ICT solutions and processes that ensure security of the means of transfer of data, minimise risk of corruption/unauthorised access, prevent breaches of confidentiality, and protect data from management risks. | Establishes outcome requirements that cryptographic controls and secure transmission protocols must achieve. | RTS on ICT Risk Management [loaded] |
| Art.9(4) [Main DORA] | Develop information security policy; implement strong authentication and protection measures of cryptographic keys whereby data is encrypted based on data classification and ICT risk assessment results. | Operative paragraph that explicitly mandates cryptographic key protection and risk-based encryption. | RTS on ICT Risk Management [loaded] |
| Art.2(1) [RTS ICT-RMF] | Ensure ICT security policies, information security and related procedures, protocols and tools referred to in DORA Art.9(2) are embedded in the ICT risk management framework. | Umbrella provision under which the encryption policy must be integrated rather than maintained in isolation. | — |
| Art.6(1) [RTS ICT-RMF] | Develop, document and implement a policy on encryption and cryptographic controls as part of the ICT security policies referred to in DORA Art.9(2). | Direct foundational obligation requiring an encryption and cryptographic controls policy. | — |
| Art.6(2)(a) [RTS ICT-RMF] | Design the encryption policy on the basis of approved data classification and ICT risk assessment, with rules covering: data at rest and in transit; data in use where necessary; encryption of internal network connections and external traffic; and cryptographic key management. | Specifies the mandatory minimum content of the encryption policy. | — |
| Art.6(3)(a) [RTS ICT-RMF] | Include in the encryption policy criteria for selecting cryptographic techniques and use practices, taking into account leading practices and EU/international standards and the ICT asset classification under DORA Art.8(1). | Direct obligation on cryptographic technique selection criteria. | — |
| Art.6(4)(a) [RTS ICT-RMF] | Include provisions for updating or changing cryptographic technology on the basis of developments in cryptanalysis, ensuring continued resilience against cyber threats. | Cryptographic agility obligation — must be documented in the policy. | — |
| Art.6(5) [RTS ICT-RMF] | Include in the encryption policy a requirement to record the adoption of mitigation and monitoring measures adopted under paragraphs 3 and 4 and to provide a reasoned explanation. | Documentation and rationale obligation — applies whenever paragraphs 3 or 4 compensating measures are triggered. | — |
| Art.7(1) [RTS ICT-RMF] | Include in the cryptographic key management policy requirements for managing keys through their whole lifecycle: generating, renewing, storing, backing up, archiving, retrieving, transmitting, retiring, revoking and destroying. | Direct lifecycle obligation covering every phase of cryptographic key handling. | — |
| Art.7(2) [RTS ICT-RMF] | Identify and implement controls to protect cryptographic keys throughout their lifecycle against loss, unauthorised access, disclosure and modification, designed on the basis of data classification and ICT risk assessment. | Direct protection obligation for keys at every lifecycle stage. | — |
| Art.7(3) [RTS ICT-RMF] | Develop and implement methods to replace cryptographic keys in the case of loss, compromise or damage. | Direct obligation to maintain a key replacement/recovery capability. | — |
| Art.7(4) [RTS ICT-RMF] | Create and maintain an up-to-date register for all certificates and certificate-storing devices for at least ICT assets supporting critical or important functions. | Direct register and inventory obligation for certificates. | — |
| Art.7(5) [RTS ICT-RMF] | Ensure prompt renewal of certificates in advance of their expiration. | Direct certificate-lifecycle obligation preventing service disruption from expired certificates. | — |
| Art.11(2) [RTS ICT-RMF] (data and system security — encryption-relevant elements) | The data and system security procedure shall contain elements including: access restrictions; secure configuration baselines; authorised software/storage media controls; secure deletion and disposal of data/media containing confidential information; DLP controls; teleworking and endpoint security; and third-party security requirements. | Operationalises encryption-supporting controls tied to data classification. | — |
| Art.13 [RTS ICT-RMF] (network security management, including encryption of network connections) | Develop, document and implement policies on network security management including, at point (e), the encryption of network connections passing over corporate, public, domestic, third-party and wireless networks, taking into account data classification, ICT risk assessment and the Art.6(2) encryption policy. | Directly mandates network-connection encryption and links back to the Art.6 encryption policy. | — |
| Art.14(1) [RTS ICT-RMF] | Develop, document and implement policies to protect information in transit — ensuring CIA+A of data during network transmission; preventing/detecting data leakages and securing transfers with external parties; and implementing confidentiality/non-disclosure arrangements. | Direct obligation specifically governing protection of information in transit. | — |
| Art.14(2) [RTS ICT-RMF] | Design the policies to protect information in transit on the basis of approved data classification and ICT risk assessment results. | Design-input obligation linking in-transit protection to the data classification framework. | — |

### Section 2 — Conditionally Applicable Provisions

These provisions apply only when their specific trigger is met. Evaluate the trigger before including in scope.

| Citation | Obligation Summary | Trigger Condition | Audit Action | Expanded by |
|---|---|---|---|---|
| Art.6(2)(b) [RTS ICT-RMF] (compensating control for data in use) | Where encryption of data in use is not possible, process data in use in a separated and protected environment, or take equivalent measures to ensure CIA+A. | Encryption of data in use is not technically possible. | Identify which processes the entity has determined cannot be encrypted in use; test the separation/equivalent-measures control and the Art.6(5) recording. | — |
| Art.6(3)(b) [RTS ICT-RMF] (compensating measures — non-leading-practice cryptography) | Where the entity cannot adhere to leading practices, standards or the most reliable techniques, adopt mitigation and monitoring measures ensuring resilience against cyber threats. | Entity cannot adhere to leading cryptographic practices or use the most reliable techniques. | Identify any algorithm/protocol exceptions; test mitigation/monitoring measures and the Art.6(5) recording. | — |
| Art.6(4)(b) [RTS ICT-RMF] (compensating measures — non-updatable cryptography) | Entities unable to update or change the cryptographic technology shall adopt mitigation and monitoring measures ensuring resilience against cyber threats. | Entity cannot update or change cryptographic technology (e.g. legacy infrastructure constraints). | Identify cryptographic assets that cannot be updated; test mitigation/monitoring measures and the Art.6(5) recording. | — |

### Section 3 — Cross-Referenced RTS/ITS Provisions

| Citation | Expands which DORA article | What it adds | Expanded by |
|---|---|---|---|
| Art.6(1) [RTS ICT-RMF] (also in Section 1) | Art.9(2) [Main DORA] | Imposes the standalone obligation to maintain a documented encryption and cryptographic controls policy. | — |
| Art.6(2)(a) [RTS ICT-RMF] (also in Section 1) | Art.9(2) [Main DORA] | Specifies the mandatory coverage of the encryption policy across data states and key management. | — |
| Art.6(2)(b) [RTS ICT-RMF] (also in Section 2) | Art.9(2) [Main DORA] | Adds the compensating-control regime where encryption of data in use is not feasible. | — |
| Art.6(3)(a) [RTS ICT-RMF] (also in Section 1) | Art.9(2) [Main DORA] | Adds technique-selection criteria referencing leading practices and Reg (EU) No 1025/2012 standards. | — |
| Art.6(3)(b) [RTS ICT-RMF] (also in Section 2) | Art.9(2) [Main DORA] | Adds compensating mitigation/monitoring where leading practices cannot be followed. | — |
| Art.6(4)(a) [RTS ICT-RMF] (also in Section 1) | Art.9(2) [Main DORA] | Adds the cryptographic agility / cryptanalysis-driven update obligation. | — |
| Art.6(4)(b) [RTS ICT-RMF] (also in Section 2) | Art.9(2) [Main DORA] | Adds compensating measures where cryptographic technology cannot be updated. | — |
| Art.6(5) [RTS ICT-RMF] (also in Section 1) | Art.9(2) [Main DORA] | Adds the requirement to record mitigation measures and provide reasoned explanation. | — |
| Art.7(1) [RTS ICT-RMF] (also in Section 1) | Art.9(2), Art.9(4)(d) [Main DORA] | Specifies the whole-lifecycle scope of the cryptographic key management policy. | — |
| Art.7(2) [RTS ICT-RMF] (also in Section 1) | Art.9(2), Art.9(4)(d) [Main DORA] | Specifies key-protection controls and their design basis. | — |
| Art.7(3) [RTS ICT-RMF] (also in Section 1) | Art.9(2) [Main DORA] | Specifies the key replacement obligation for loss/compromise/damage. | — |
| Art.7(4) [RTS ICT-RMF] (also in Section 1) | Art.9(2) [Main DORA] | Specifies the certificate-and-device register obligation. | — |
| Art.7(5) [RTS ICT-RMF] (also in Section 1) | Art.9(2) [Main DORA] | Specifies the prompt-renewal obligation for certificates. | — |
| Art.11(2) [RTS ICT-RMF] (also in Section 1) | Art.9(2), Art.9(4)(a) [Main DORA] | Specifies data-and-system security controls including secure deletion, media disposal, DLP and endpoint security. | — |
| Art.13 [RTS ICT-RMF] (also in Section 1) | Art.9(2), Art.9(4)(b) [Main DORA] | Specifies network-connection encryption requirements and links to the Art.6 encryption policy. | — |
| Art.14(1) [RTS ICT-RMF] (also in Section 1) | Art.9(2), Art.9(3)(a) [Main DORA] | Specifies the operational requirements for protecting information in transit. | — |
| Art.14(2) [RTS ICT-RMF] (also in Section 1) | Art.9(2) [Main DORA] | Specifies that in-transit protection design must be driven by data classification and ICT risk assessment. | — |

### Section 4 — Indirect or Awareness Items

| Citation | Reason for Awareness | Expanded by |
|---|---|---|
| Art.4(1) [Main DORA] (proportionality — Chapter II) | Governs how the encryption obligations under Chapter II must be applied — scaled to entity size, risk profile, and complexity. Auditor should be aware of how the entity has documented its proportionality stance for cryptographic controls. | RTS on Simplified ICT Risk Management (not yet loaded) |
| Art.8(1) [Main DORA] (data classification as input) | Encryption policy design under Art.6(2)(a) [RTS ICT-RMF] and in-transit protection design under Art.14(2) [RTS ICT-RMF] both depend on an approved data classification. Awareness ensures the auditor tests the upstream classification before testing encryption coverage. | RTS on ICT Risk Management [loaded] |
| Art.1 [RTS ICT-RMF] (proportionality elements) | Lists encryption and cryptography as one of the elements explicitly subject to size-and-risk-profile-based calibration. Awareness item when assessing whether scaled-down cryptographic controls are appropriately justified. | — |

### Section 5 — Excluded From Scope

| Citation | Obligation Type | Reason for Exclusion |
|---|---|---|
| Art.2(1), Art.2(2) [Main DORA] | Scope | Defines DORA applicability; not an obligation. |
| Art.3 Definition (60) [Main DORA] (microenterprise definition) | Definition | Interpretive provision; entity is non-microenterprise so the definition does not change scope here. |
| Art.4(3) [Main DORA] | Procedural | Duty on competent authorities to consider proportionality when reviewing the framework; entity is not the addressee. |
| Art.15 [Main DORA] | Empowerment | ESA mandate to develop the RTS on ICT Risk Management; not an entity obligation. |
| Art.16(1) [Main DORA] | Entity-type | Defines applicability of the simplified framework; entity is standard-framework, not simplified. |
| Art.28 (paragraphs 1–6) [RTS ICT-RMF] (simplified framework governance) | Entity-type | Title III — applies only to Art.16(1) entities; entity not in scope. |
| Art.29(1), Art.29(2) [RTS ICT-RMF] | Entity-type | Title III simplified framework information security; not applicable. |
| Art.33 [RTS ICT-RMF] | Entity-type | Title III simplified framework access control; not applicable. |
| Art.34 [RTS ICT-RMF] | Entity-type | Title III simplified framework ICT operations security; not applicable. |
| Art.35(1) [RTS ICT-RMF] | Entity-type | Title III simplified framework safeguards; not applicable. |

### Coverage Assessment

- Total provisions retrieved: 31
- Section 1 — Directly applicable: 19
- Section 2 — Conditionally applicable: 3
- Section 3 — Cross-referenced RTS/ITS: 17 (all also appearing in Sections 1 or 2)
- Section 4 — Indirect or awareness: 3
- Section 5 — Excluded from scope: 10
- Documents not yet loaded but referenced: RTS on Simplified ICT Risk Management (not yet loaded) — referenced via Art.4(1) [Main DORA]; not in scope for this entity, so no impact on testable obligations
- Confidence: **High** — the encryption topic is concentrated in DORA Art.9 and RTS ICT-RMF Arts 6, 7, 11, 13 and 14, all fully loaded with clean Title II Direct obligations applicable to a non-microenterprise investment firm under the standard framework
- Gaps to flag for manual review:
  - The Art.6(5) recording obligation links to compensating measures under Art.6(3) and Art.6(4); test that any conditional-fallback use is fully documented per Art.6(5), even where the trigger appears minor
  - Where the firm relies on ICT third-party providers for cryptographic services (HSM-as-a-service, cloud KMS, certificate authorities), DORA Chapter V third-party risk management obligations apply alongside these obligations; consider a separate third-party-risk mapping if the audit scope extends to outsourced cryptography
  - Art.6(3)(a) cites "standards as defined in Article 2, point (1), of Regulation (EU) No 1025/2012" — confirm the entity's documented technique-selection criteria reference appropriate harmonised standards
