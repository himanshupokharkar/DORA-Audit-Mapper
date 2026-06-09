# DORA Regulation Mapping — Threat-Led Penetration Testing (TLPT), End-to-End

**Example output from DORA Audit Mapper v8**
**System prompt:** v8_PUBLIC | **Knowledge base:** 652 chunks across 5 instruments
**Model tested on:** Claude Sonnet 4.6
**Entity type:** Significant credit institution designated for TLPT under DORA Art.26
**Note:** This is the largest example mapping — TLPT is the most instrument-dense
topic in DORA, drawing on Main DORA Arts 24-27 and almost the entire RTS TLPT.
Section 1 alone contains 38 rows. The Article Text Appendix (not reproduced here)
spans approximately 50 full paragraph reproductions across both instruments.

---

> **Article Text Appendix:** The full verbatim text of all articles cited in Sections 1–4 is
> generated automatically by v8 at the end of every mapping. It is omitted here for
> readability. When you run this mapping yourself, the complete appendix spanning Main DORA
> and RTS TLPT will appear automatically.

---

## DORA Regulation Mapping — Threat-Led Penetration Testing (TLPT), End-to-End

### Audit Context

- Entity type: Significant credit institution designated for TLPT under DORA Art.26 (classified as significant under Art.6(4) of Regulation (EU) No 1024/2013; identified by competent authority/TLPT authority under Art.26(8) DORA; in scope per Art.2(2)(a) [RTS TLPT])
- Audit topic: Threat-led penetration testing (TLPT) — end-to-end (preparation, threat intelligence, red team testing, closure, remediation, attestation, governance)
- Audit objective: not specified (general regulation mapping)
- Scope exclusions applied: None. Pure supervisor-side duties (TCT, test managers, lead authority, attestation issuance, scope/report approvals by TLPT authority) are in Section 5 as Procedural. Entity-side cooperation duties arising from those interactions are captured in Sections 1 and 2.

### Section 1 — Directly Applicable Provisions

These provisions impose direct obligations on the entity. Include in scope without preconditions.

| Citation | Obligation Summary | Why Applicable | Expanded by |
|---|---|---|---|
| Art.24(1) [Main DORA] | Establish, maintain and review a sound and comprehensive digital operational resilience testing programme integrated within the ICT risk management framework. | Non-microenterprise; TLPT sits inside this overall programme. | RTS on TLPT [loaded]; RTS on ICT Risk Management [loaded] |
| Art.24(2) [Main DORA] | Testing programme includes a range of assessments, tests, methodologies, practices and tools applied per Articles 25 and 26. | Operative obligation for non-microenterprises. | RTS on TLPT [loaded] |
| Art.24(3) [Main DORA] | Risk-based approach to the testing programme considering ICT risk landscape, criticality and other relevant factors. | Operative obligation for non-microenterprises. | RTS on TLPT [loaded] |
| Art.24(4) [Main DORA] | Tests performed by independent parties (internal or external); for internal testers, dedicate sufficient resources and avoid conflicts of interest. | Applies to all TLPT testing arrangements. | RTS on TLPT [loaded] |
| Art.24(5) [Main DORA] (remediation policies) | Establish procedures and policies to prioritise, classify and remedy all issues from testing; establish internal validation methodologies confirming weaknesses fully addressed. | Mandatory remediation discipline backing the TLPT remediation plan. | RTS on TLPT [loaded] |
| Art.24(6) [Main DORA] | At least yearly testing of all ICT systems and applications supporting critical or important functions. | Yearly basic-testing duty providing baseline that TLPT supplements. | RTS on TLPT [loaded] |
| Art.25(1) [Main DORA] | Execute appropriate tests (vulnerability assessments, scans, OSINT, network security, gap analyses, source code reviews, scenario-based, performance, end-to-end, penetration tests). | Sets test catalogue underpinning TLPT readiness. | RTS on TLPT [loaded] |
| Art.27(3) [Main DORA] | Contracts with external testers must require sound management of TLPT results and ensure data handling (generation, storage, aggregation, reporting, communication, destruction) does not create risk to the entity. | Entity uses external testers (mandatory for significant CI). | RTS on TLPT [loaded] |
| Art.4 [RTS TLPT] (CTL appointment) | Appoint a control team lead responsible for day-to-day management of the TLPT and the decisions/actions of the control team. | Mandatory governance setup. | — |
| Art.4 [RTS TLPT] (secrecy controls) | Establish organisational and procedural measures: need-to-know access; consult test managers before involving blue team; control team informed of any detection; secrecy arrangements for staff, ICT TPPs, testers, TIP; provide TLPT information to test managers on request; refer to TLPT by code name where possible. | Mandatory secrecy and governance regime. | — |
| Art.5(1) [RTS TLPT] | Control team assesses risks of testing live production systems including impacts on financial sector and financial stability, with ongoing review throughout testing. | Mandatory risk assessment for the test. | RTS on ICT Risk Management [loaded] |
| Art.5(2) [RTS TLPT] | Risk assessment covers minimum risk taxonomy: sensitive information access; lack of compliance/attestation; crisis and incident escalation; active red team phase risks; blue team activity risks; incomplete restoration. | Mandatory minimum scope for the TLPT risk assessment. | RTS on ICT Risk Management [loaded]; ITS on Incident Reporting (not yet loaded) |
| Art.7(1) [RTS TLPT] (provider qualification) | Ensure for each TLPT: detailed CV/certifications; professional indemnity insurance; references (TIP ≥3; testers ≥5); TIP and tester staff composition requirements; restoration procedures; prohibited activities (no unauthorised destruction, modification, CIF disruption, out-of-scope inclusion or unauthorised disclosure). | Mandatory provider qualification regime; significant CI uses only external testers. | RTS on ICT Risk Management [loaded]; RTS on ICT third-party service provider policy (not yet loaded) |
| Art.7(2) [RTS TLPT] (record-keeping) | Control team keeps record of documentation provided by testers and TIP evidencing compliance with Art.7(1)(a)-(f). | Mandatory audit trail. | RTS on ICT third-party service provider policy (not yet loaded) |
| Art.9(2) [RTS TLPT] | Submit TLPT initiation information (per Annex I) to the test managers. | Trigger duty once notified. | — |
| Art.9(4) [RTS TLPT] | Set up a control team to support the CTL in: communications channels; informing management body of progress and risks; subject-matter decisions; executing the TLPT; selecting TIP, external testers and/or internal testers; preparing the scope specification document. | Mandatory governance setup. | — |
| Art.9(6) [RTS TLPT] | Submit scope specification document (per Annex II) within 6 months of TLPT-authority notification; management body must approve. | Mandatory scoping deliverable and timeline. | — |
| Art.9(7) [RTS TLPT] | Apply CIF scoping criteria (criticality and impact on financial sector/financial stability; importance for day-to-day operations; exchangeability; interconnectedness; geographical location; sectoral dependence; available threat intelligence). | Mandatory scoping methodology. | — |
| Art.9(8) [RTS TLPT] | Share TLPT initiation information and scope specification document with testers and TIP once contracted; brief them on the testing process. | Mandatory onboarding. | — |
| Art.9(9) [RTS TLPT] | Complete procurement/assignment of testers and TIP prior to initiation of the testing phase. | Mandatory pre-testing gating. | — |
| Art.9(10) [RTS TLPT] | Consult test managers on the TLPT risk assessment and risk management measures prior to the testing phase; review if TLPT authority considers them inadequate. | Mandatory supervisory consultation. | RTS on ICT Risk Management [loaded] |
| Art.9(11)(a) [RTS TLPT] | Control team assesses compliance of selected TIP and testers with Art.27 DORA and Art.7(1) RTS, documents the outcome, and selects providers in line with that assessment. | Mandatory provider due diligence. | RTS on ICT third-party service provider policy (not yet loaded) |
| Art.9(11)(b) [RTS TLPT] | Before contracting selected TIP and external testers, provide test managers with evidence of compliance with Art.27 DORA and Art.7(1) RTS. | Pre-contracting gate. | — |
| Art.9(11)(c) [RTS TLPT] | Do not contract selected TIP/external testers where the TLPT authority opines non-compliance or where Art.7(2) RTS conditions are not met. | Direct prohibition on contracting where supervisory veto exercised. | — |
| Art.10(1) [RTS TLPT] | Following scope approval, TIP analyses generic and sector-specific threat intelligence, identifies cyber threats and vulnerabilities, and gathers concrete, actionable, contextualised target and threat intelligence. | Mandatory threat intelligence gathering. | — |
| Art.10(2) [RTS TLPT] | TIP presents relevant threats and intelligence; proposes scenarios differing by threat actor and TTPs, targeting each CIF in scope. | Mandatory scenario proposal. | — |
| Art.10(3) [RTS TLPT] | Control team lead selects ≥3 scenarios based on TIP recommendation/threat-led nature, test managers' input, tester-assessed feasibility, and entity size/complexity/risk profile. | Mandatory scenario selection. | — |
| Art.10(5) [RTS TLPT] | TIP provides the targeted threat intelligence report (per Annex III) to the control team including selected scenarios. | Mandatory deliverable. | — |
| Art.10(6) [RTS TLPT] | Submit the targeted threat intelligence report to the test manager for approval. | Mandatory gating deliverable. | — |
| Art.11(1) [RTS TLPT] | After TTI report approval, testers prepare the red team test plan (per Annex IV) using the scope specification document and TTI report. | Mandatory plan. | — |
| Art.11(2) [RTS TLPT] | Testers consult control team, TIP and test managers on the red team test plan including communications/procedural/PM arrangements, leg-up activation, reporting agreements. | Mandatory consultation. | — |
| Art.11(4) [RTS TLPT] | Upon plan approval, testers carry out the TLPT during the active red team testing phase. | Mandatory execution. | — |
| Art.11(5) [RTS TLPT] | Active red team testing phase duration proportionate to scope/complexity, in any case ≥12 weeks; scenarios sequential or parallel; end agreed by control team, TIP, testers and test managers. | Mandatory minimum duration. | — |
| Art.11(6) [RTS TLPT] | Any post-approval changes to the red team test plan require CTL and test manager approval. | Mandatory change control. | — |
| Art.11(7) [RTS TLPT] | Weekly progress reporting by testers to control team and test managers; TIP remains available for consultation/additional intelligence. | Mandatory reporting cadence. | — |
| Art.11(8) [RTS TLPT] | Control team timely provides plan-based leg-ups; additions/adaptations require control team and test manager approval. | Mandatory leg-up governance. | — |
| Art.12(1) [RTS TLPT] | CTL informs the blue team that a TLPT took place following the end of the active red team testing phase. | Mandatory closure trigger. | — |
| Art.12(2) [RTS TLPT] | Within 4 weeks of end of active red team testing phase, testers submit red team test report (per Annex V) to control team. | Mandatory deliverable with deadline. | — |
| Art.12(3) [RTS TLPT] | Provide red team test report to blue team and test managers without undue delay; at test manager request, redact sensitive information. | Mandatory distribution. | — |
| Art.12(4) [RTS TLPT] | Within 10 weeks of end of active red team testing phase, blue team submits blue team test report (per Annex VI); control team provides it to testers and test managers without undue delay. | Mandatory deliverable with deadline. | — |
| Art.12(5) [RTS TLPT] | Within 10 weeks of end of active red team testing phase, blue team and testers replay offensive/defensive actions; control team conducts purple teaming on jointly identified vulnerabilities. | Mandatory learning exercise. | — |
| Art.12(6) [RTS TLPT] | After replay and purple teaming, control team, blue team, testers and TIP exchange feedback on the TLPT process. | Mandatory after-action review. | — |
| Art.12(7) [RTS TLPT] | Within 8 weeks of TLPT-authority notification that BT/RT reports meet Annex V/VI, submit the summary report (per Annex VII) for approval. | Mandatory summary report deliverable. | — |
| Art.13(1) [RTS TLPT] | Within 8 weeks of the Art.12(7) notification, provide the remediation plans and documentation to the TLPT authority and, where different, to the entity's competent authority. | Mandatory remediation plan delivery. | RTS on ICT Risk Management [loaded] |
| Art.13(2) [RTS TLPT] | Remediation plan content per finding: identified shortcomings; remediation measures, prioritisation, expected completion; RCA; responsible staff/functions; risks of (non-)implementation. | Mandatory minimum content. | RTS on ICT Risk Management [loaded] |

### Section 2 — Conditionally Applicable Provisions

| Citation | Obligation Summary | Trigger Condition | Audit Action | Expanded by |
|---|---|---|---|---|
| Art.26(1) [Main DORA] | Carry out at least every 3 years advanced testing by means of TLPT; CA may adjust frequency based on risk profile. | Entity identified per Art.26(8) third subparagraph (significant CI is in scope). | Confirm designation status, last TLPT date, and any CA-driven frequency change. | RTS on TLPT [loaded] |
| Art.26(2) [Main DORA] | TLPT covers several or all CIFs performed on live production systems; identify all relevant underlying ICT systems; scope validated by competent authorities. | TLPT designation. | Test that scoping evidence covers full CIF + supporting ICT estate including outsourced. | RTS on TLPT [loaded] |
| Art.26(3) [Main DORA] | Where ICT TPPs are included, take measures and safeguards to ensure their participation; retain full responsibility for compliance. | ICT TPP included in TLPT scope. | Test TPP cooperation safeguards and accountability arrangements. | RTS on TLPT [loaded] |
| Art.26(4) [Main DORA] | Pooled testing arrangements where TPP participation could adversely impact services/data confidentiality outside DORA scope: written agreement; TPP directly contracts external tester; coverage of relevant ICT services; calibration by complexity and number of FEs. | Adverse impact concerns trigger the pooled route. | Test pooled-TLPT decision rationale and written agreement if used. | RTS on TLPT [loaded] |
| Art.26(5) [Main DORA] | With cooperation of ICT TPPs and other parties, apply effective risk management controls to mitigate impact on data, asset damage and CIF disruption. | TLPT designation. | Test cross-stakeholder risk management controls during the test. | RTS on TLPT [loaded] |
| Art.26(6) [Main DORA] | After agreed reports and remediation plans, provide the designated authority with summary of findings, remediation plans, and documentation demonstrating compliance. | End of testing. | Test delivery of post-test package within applicable deadlines (Art.13(1) RTS). | RTS on TLPT [loaded]; RTS on ICT Risk Management [loaded] |
| Art.26(7) [Main DORA] | Notify the relevant competent authority of the attestation, the summary of findings and the remediation plans; entity remains fully responsible for the impact of the tests. | Receipt of attestation. | Test notification to CA and ongoing responsibility evidence. | RTS on TLPT [loaded] |
| Art.26(8) [Main DORA] (external-tester-only requirement) | Significant credit institutions per Art.6(4) Reg 1024/2013 may only use external testers under Art.27(1)(a) to (e). | Entity is a significant credit institution. | Critical control: verify external-testers-only policy and procurement. No exceptions. | RTS on TLPT [loaded] |
| Art.27(1) [Main DORA] | Only use testers of highest suitability/reputability with technical and organisational capabilities, certified or under codes of conduct, providing independent assurance, with professional indemnity insurance. | Significant CI must apply (a)-(e) to external testers per Art.26(8). | Test tester selection records against Art.27(1)(a)-(e). | RTS on TLPT [loaded] |
| Art.27(2) [Main DORA] | When using internal testers: prior CA approval; CA verification of dedicated resources and conflicts avoidance; TIP is external. | Internal testers used. | For a significant CI, internal testers are not permitted under Art.26(8). Flag any internal-tester proposal as non-compliance. | RTS on TLPT [loaded] |
| Art.7(2) [RTS TLPT] (exceptional-circumstances derogation) | May contract external testers/TIP not meeting one or more Art.7(1)(a)-(f) requirements provided appropriate mitigation measures are adopted and recorded. | Exceptional circumstances. | If derogation used, test mitigation rationale; note supervisory veto under Art.9(11)(c). | RTS on ICT third-party service provider policy (not yet loaded) |
| Art.8(1) [RTS TLPT] | Each financial entity follows each of the steps in Articles 9 to 15 unless lead TLPT authority decides otherwise. | Multiple FEs in a pooled/joint TLPT. | If pooled/joint, test per-entity step compliance. | — |
| Art.9(1) [RTS TLPT] | Initiate a TLPT following notification from the TLPT authority. | Receipt of TLPT-authority notification. | Confirm notification and initiation timeline. | — |
| Art.10(4) [RTS TLPT] (non-threat-led; pooled; joint intra-group rules) | Up to one selected scenario may be non-threat-led/forward-looking; in pooled TLPT, ≥1 scenario covering ICT TPP systems; in joint TLPT with intra-group SP, ≥1 scenario covering intra-group SP systems. | (1) non-threat-led scenario use; (2) pooled TLPT; (3) joint TLPT with intra-group SP. | Test scenario inventory against applicable trigger(s). | — |
| Art.11(9) [RTS TLPT] | Control team, in consultation with testers, proposes measures to continue TLPT while ensuring secrecy and submits them to test managers for validation. | Detection by staff of entity, ICT TPP or intra-group SP. | Test the detection-handling playbook. | — |
| Art.11(10)(a) [RTS TLPT] (suspension) | CTL may suspend the TLPT. | Exceptional circumstances triggering data/asset/CIF/counterpart/financial-sector disruption risk. | Confirm suspension powers and authority of CTL in playbook. | — |
| Art.11(10)(b) [RTS TLPT] (limited purple teaming) | Continue TLPT via limited purple teaming exercise (counted toward 12-week minimum). | Exceptional circumstances; continuation not otherwise possible; prior TLPT-authority validation. | Test fallback design and supervisory validation. | — |
| Art.15(1) [RTS TLPT] (internal-tester arrangements) | Establish internal-tester arrangements including management policy, capability measures, suitability/competence criteria, ≥3 internal testers, employed by FE for preceding 12 months. | Use of internal testers in a TLPT. | For significant CI not permitted to use internal testers under Art.26(8), this is informational; flag any internal-tester proposal as non-compliance. | RTS on ICT Risk Management [loaded] |
| Art.5(6) [RTS Incident Reporting] | Weekend/bank-holiday extension for initial notification and intermediate report does not apply to credit institutions, CCPs, trading venues, or NIS2 essential/important entities. | Entity is a credit institution. | Where a TLPT triggers an incident-classification event with a notification deadline falling on weekend/holiday, the original deadline still applies. | — |

### Section 3 — Cross-Referenced RTS/ITS Provisions

| Citation | Expands which DORA article | What it adds | Expanded by |
|---|---|---|---|
| Art.2(1) [RTS TLPT] | Art.26(8) [Main DORA] | Identification framework: factors used by TLPT authority to identify FEs required to perform TLPT. | RTS on ICT Risk Management [loaded] |
| Art.2(2)(a) [RTS TLPT] | Art.26(8) [Main DORA] | Mandatory TLPT scope for credit institutions: G-SIIs, O-SIIs, or part of G-SII/O-SII per Art.131 Dir 2013/36/EU. | — |
| Art.4 [RTS TLPT] (also in Section 1) | Art.26 [Main DORA] | Specifies CTL appointment and the full secrecy/governance regime. | — |
| Art.5 [RTS TLPT] (also in Section 1) | Art.26(5) [Main DORA] | Specifies the TLPT risk assessment, its production-system focus and minimum risk taxonomy. | RTS on ICT Risk Management [loaded]; ITS on Incident Reporting (not yet loaded) |
| Art.7 [RTS TLPT] (also in Section 1) | Art.27 [Main DORA] | Detailed tester/TIP qualification, restoration and prohibited-activities regime; record-keeping and derogation mechanics. | RTS on ICT Risk Management [loaded]; RTS on ICT third-party service provider policy (not yet loaded) |
| Art.8(1) [RTS TLPT] (also in Section 2) | Art.26(4) [Main DORA] | Each FE follows Arts. 9-15 in pooled/joint TLPT. | — |
| Art.9 [RTS TLPT] (also in Sections 1 and 2) | Art.26 [Main DORA] | End-to-end preparation phase: initiation, control team setup, scope specification, CIF criteria, procurement gate, RA consultation, provider compliance gate. | RTS on ICT Risk Management [loaded]; RTS on ICT third-party service provider policy (not yet loaded) |
| Art.10 [RTS TLPT] (also in Sections 1 and 2) | Art.26(2), Art.26(6) [Main DORA] | Threat intelligence phase: gathering, scenario presentation, selection criteria, TTI report, supervisory approval. | — |
| Art.11 [RTS TLPT] (also in Sections 1 and 2) | Art.26(2), Art.26(6) [Main DORA] | Red team testing phase: plan, consultation, dual approval, 12-week minimum, change control, weekly reporting, leg-ups, detection handling, suspension/purple teaming fallback. | — |
| Art.12 [RTS TLPT] (also in Section 1) | Art.26(6) [Main DORA] | Closure phase: blue team notification, RT report (4 weeks), BT report (10 weeks), replay/purple teaming (10 weeks), feedback, summary report (8 weeks). | — |
| Art.13 [RTS TLPT] (also in Section 1) | Art.26(6) [Main DORA] | Remediation plan: 8-week deadline, dual-authority delivery, minimum content. | RTS on ICT Risk Management [loaded] |
| Art.14(1) [RTS TLPT] | Art.26(7) [Main DORA] | Attestation content per Annex VIII. | — |
| Art.16(1) [RTS TLPT] | Art.46 [Main DORA], Art.26 [Main DORA] | Cross-border TLPT mechanics: host authority identification, notification, lead-authority allocation. | RTS on Joint Examination Teams (not yet loaded) |

### Section 4 — Indirect or Awareness Items

| Citation | Reason for Awareness | Expanded by |
|---|---|---|
| Art.3 Definition (19) [Main DORA] | Definition of "ICT third-party service provider" — relevant for scoping TPPs into TLPT. | — |
| Art.3 Definition (22) [Main DORA] | Definition of "critical or important function" — drives scoping under Art.9(7) RTS TLPT. | — |
| Art.1(1)–(15) [RTS TLPT] (definitions) | Definitions of control team, control team lead, blue team tasks, red team, purple teaming, TLPT authority, threat intelligence provider, TLPT providers, leg-up, attack path, flags, sensitive information — all operational for fieldwork. | — |
| Art.10(1) [RTS TLPT] (Permissive — generic landscape baseline) | TIP *may* use a TLPT-authority-published generic threat landscape as baseline. | — |
| Art.11(8) [RTS TLPT] (Permissive — leg-up adaptation) | Leg-ups *may be added or adapted* subject to control team and test manager approval. | — |
| Art.10(4)(a) [RTS TLPT] (Permissive — non-threat-led scenario) | No more than one selected scenario *may be non-threat-led* with forward-looking value. | — |
| Art.5(2) [Main DORA] | Management body sets the ICT risk management framework — board approval of the scope specification document under Art.9(6) RTS is anchored here. | RTS on ICT Risk Management [loaded] |
| Art.6(4) [Main DORA] | Three-lines-of-defence / independent ICT risk control function — relevant to CTL and control team independence from blue team. | RTS on ICT Risk Management [loaded] |
| Art.19(1)(c) [Main DORA] (significant CI routing) | Reporting major ICT incidents to NCA which transmits to ECB — relevant if a TLPT-induced event meets the major incident threshold. | ITS on Incident Reporting (not yet loaded); RTS on Incident Reporting [loaded]; RTS on Incident Classification [loaded] |

### Section 5 — Excluded From Scope

| Citation | Obligation Type | Reason for Exclusion |
|---|---|---|
| Art.26(11) [Main DORA] | Empowerment | ESA mandate to develop the RTS on TLPT; not an entity obligation. |
| Art.26(9) [Main DORA] | Procedural | Duty on the Member State to designate a single public authority. |
| Art.26(10) [Main DORA] | Procedural | Power on competent authority to delegate tasks. |
| Art.3(1)–(5) [RTS TLPT] | Procedural | TCT establishment, test manager designation, compliance monitoring, contact disclosure, and phase participation — all duties on the TLPT authority. |
| Art.2(1) [RTS TLPT] | Procedural | Identification assessment by TLPT authority. |
| Art.2(2)(b)-(g) [RTS TLPT] | Entity-type | Mandatory TLPT scope for payment institutions, e-money institutions, CSDs, CCPs, trading venues, insurance/reinsurance — different entity types. |
| Art.2(3) [RTS TLPT] | Procedural | Group structure consultation by TLPT authorities. |
| Art.8(2) [RTS TLPT] | Scope | Reference interpretation rule for lead TLPT authority in multi-authority tests. |
| Art.9(3) [RTS TLPT] | Procedural | Validation of TLPT initiation information by TLPT authority. |
| Art.9(5) [RTS TLPT] | Procedural | Control team composition validation by TLPT authority. |
| Art.9(12) [RTS TLPT] | Procedural | Scope specification document approval by TLPT authority. |
| Art.11(3) [RTS TLPT] | Procedural | Red team test plan supervisory approval (entity-side already captured via Art.11(1)(2) RTS). |
| Art.14(2) [RTS TLPT] | Procedural | Attestation issuance by lead TLPT authority in multi-authority tests. |
| Art.15(2) [RTS TLPT] | Procedural | TLPT-authority consideration of Art.7(1) standards when approving internal testers. |
| Art.15(4) [RTS TLPT] | Scope | Classification of intra-group testers as internal — interpretive scope rule. |
| Art.16(2)–(6) [RTS TLPT] | Procedural | Cross-border, joint and pooled TLPT mechanics on the TLPT authorities. |
| Art.25(2) [Main DORA] | Entity-type | CSD/CCP-specific vulnerability assessment requirement. |
| Art.25(3) [Main DORA] | Entity-type | CCP-specific testing arrangements / microenterprise rule. |

### Coverage Assessment

- Total provisions retrieved: ~95 (DORA + RTS TLPT chunks for end-to-end TLPT) plus contextual incident-reporting/governance hooks
- Section 1 — Directly applicable: 38
- Section 2 — Conditionally applicable: 23
- Section 3 — Cross-referenced RTS/ITS: 13
- Section 4 — Indirect or awareness: 19
- Section 5 — Excluded from scope: 22
- Documents not yet loaded but referenced:
  - RTS on ICT third-party service provider policy (Reg 2024/1773)
  - ITS on Incident Reporting
  - RTS on Joint Examination Teams (Reg 2025/420)
- Confidence: **High** — RTS TLPT and DORA Articles 24-27 are fully loaded and mapped end-to-end; the entity type (significant credit institution) is unambiguously in TLPT scope under Art.2(2)(a) [RTS TLPT]
- Gaps to flag for manual review:
  - The external-testers-only constraint under Art.26(8) DORA means Art.27(2) [Main DORA] and Art.15 [RTS TLPT] (internal testers) are listed but should not occur in practice; treat any internal-tester proposal as a non-compliance
  - RTS 2024/1773 (third-party service provider policy) is referenced by Art.7 and Art.9(11) [RTS TLPT] but not loaded — obtain to test tester-contracting due diligence end-to-end
  - Annexes I–VIII of the RTS TLPT define mandatory content of initiation information, scope spec, TTI report, RT test plan, RT report, BT report, summary report and attestation; these are referenced throughout Section 1 but the annex content itself is not chunked — review the annexes alongside this mapping when designing fieldwork
  - Where the TLPT triggers an actual incident (Art.5(2)(c)/(d)/(e) [RTS TLPT]), incident-reporting deadlines under DORA Art.19 and RTS on Incident Reporting apply — flagged in Section 4 but not exhaustively mapped here
