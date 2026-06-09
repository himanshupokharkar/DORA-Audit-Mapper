# DORA Regulation Mapping — ICT Incident Management, Classification, and Reporting

**Example output from DORA Audit Mapper v8**
**System prompt:** v8_PUBLIC | **Knowledge base:** 652 chunks across 5 instruments
**Model tested on:** Claude Sonnet 4.6
**Note:** This example includes an audit objective (compliance review) to demonstrate
how v8 tailors the Coverage Assessment when an objective is voluntarily provided.
The five-section mapping in Sections 1-5 is identical regardless of audit objective.

---

> **Article Text Appendix:** The full verbatim text of all articles cited in Sections 1–4 is
> generated automatically by v8 at the end of every mapping. It is omitted here for
> readability. When you run this mapping yourself, the complete appendix spanning Main DORA,
> RTS ICT-RMF, RTS Incident Classification, and RTS Incident Reporting will appear automatically.

---

## DORA Regulation Mapping — ICT Incident Management, Classification, and Reporting (End-to-End)

### Audit Context

- Entity type: Credit institution, non-microenterprise, not designated as significant under Regulation (EU) No 1024/2013 (SSM)
- Audit topic: ICT incident management, classification, and reporting (end-to-end)
- Audit objective: Compliance review
- Scope exclusions applied: Title III of RTS ICT-RMF (Arts 28–41) and DORA Art.16(1) simplified-framework provisions filtered out. DORA Art.19(1)(c) significant-CI routing to ECB excluded (entity not designated significant under SSM).

### Section 1 — Directly Applicable Provisions

| Citation | Obligation Summary | Why Applicable | Expanded by |
|---|---|---|---|
| Art.10(1) [Main DORA] | Have mechanisms to promptly detect anomalous activities, ICT network performance issues and incidents; identify potential material single points of failure; regularly test all detection mechanisms. | Foundation of detection capability. | RTS on ICT Risk Management [loaded] |
| Art.10(2) [Main DORA] | Detection mechanisms shall enable multiple control layers, define alert thresholds and criteria, including automatic alert mechanisms for response staff. | Specifies how detection feeds response. | RTS on ICT Risk Management [loaded] |
| Art.10(3) [Main DORA] | Devote sufficient resources to monitor user activity, ICT anomalies and incidents, in particular cyber-attacks. | Resource-allocation obligation. | RTS on ICT Risk Management [loaded] |
| Art.13(1) [Main DORA] | Have capabilities and staff to gather information on vulnerabilities, cyber threats and incidents and analyse their likely impact on digital operational resilience. | Underpins incident intake and threat-intelligence integration. | RTS on ICT Risk Management [loaded] |
| Art.13(2) [Main DORA] | Put in place post-incident reviews after a major ICT-related incident disrupts core activities; analyse causes and identify improvements. | Lessons-learned obligation; entity is non-microenterprise. | RTS on ICT Risk Management [loaded] |
| Art.17(1) [Main DORA] | Define, establish and implement an ICT-related incident management process to detect, manage and notify ICT-related incidents. | Core process obligation — anchors classification and reporting duties. | ITS on Incident Reporting (not yet loaded) |
| Art.17(2) [Main DORA] | Record all ICT-related incidents and significant cyber threats; establish procedures for consistent monitoring, handling and follow-up; identify, document and address root causes. | Record-keeping and follow-up duty. | ITS on Incident Reporting (not yet loaded) |
| Art.17(3) [Main DORA] | Process shall include: early-warning indicators; identify/track/log/categorise/classify procedures; roles; communication and escalation plans; management-body reporting of major incidents; incident response procedures. | Specifies mandatory components of the incident management process. | ITS on Incident Reporting (not yet loaded) |
| Art.18(1) [Main DORA] | Classify ICT-related incidents and determine impact based on six criteria: clients/counterparts/transactions and reputational impact; duration; geographical spread; data losses; criticality of services; economic impact. | Foundational classification obligation. | RTS on Incident Classification [loaded]; ITS on Incident Reporting (not yet loaded) |
| Art.18(2) [Main DORA] | Classify cyber threats as significant based on criticality of services at risk, number/relevance of clients or counterparts targeted, and geographical spread. | Required for cyber-threat track. | RTS on Incident Classification [loaded]; ITS on Incident Reporting (not yet loaded) |
| Art.19(5) [Main DORA] | Where reporting obligations are outsourced to a third party, the entity remains fully responsible for fulfilment. | Residual-responsibility obligation. | ITS on Incident Reporting (not yet loaded); RTS on Incident Reporting [loaded] |
| Art.22 [RTS ICT-RMF] (incident management policy) | Develop, document and implement an ICT-related incident policy: document Art.17 process; establish contacts; support detection mechanisms; retain evidence; analyse significant/recurring incidents and patterns. | RTS-level policy obligation expanding Art.17. | RTS on Incident Classification [loaded] |
| Art.23(1) [RTS ICT-RMF] | Set clear roles and responsibilities to detect and respond to incidents and anomalous activities. | RACI obligation for incident response. | — |
| Art.23(2) [RTS ICT-RMF] | Detection mechanism shall enable: collection/monitoring/analysis of internal/external factors and cyber threats; identify anomalies with alerting tools; prioritise alerts; record/analyse anomalous activity. | Operative content of Art.10(1) detection mechanism. | — |
| Art.23(3) [RTS ICT-RMF] | Protect any recording of anomalous activities against tampering and unauthorised access at rest, in transit and in use. | Evidence-integrity obligation supporting forensic readiness. | — |
| Art.23(4) [RTS ICT-RMF] | Log all relevant information for each detected anomalous activity: date/time of occurrence, date/time of detection, type of activity. | Logging granularity obligation. | — |
| Art.23(5) [RTS ICT-RMF] | Consider four trigger criteria for the Art.10(2) detection/response process: indications of malicious activity; data losses; adverse impact on transactions/operations; ICT system/network unavailability. | Operational threshold criteria for invoking incident response. | — |
| Art.23(6) [RTS ICT-RMF] | For the purposes of paragraph 5, also consider the criticality of the services affected. | Adds criticality lens to the trigger criteria. | — |
| Art.1(1) [RTS Incident Classification] | The number of clients affected shall reflect all clients unable to use the service or adversely impacted, including third-party beneficiaries explicitly covered by the contract. | Defines the population for Art.9(1) numerical thresholds. | — |
| Art.1(2) [RTS Incident Classification] | The number of financial counterparts affected shall reflect all affected counterparts in a contractual arrangement with the entity. | Defines counterpart population. | — |
| Art.1(3) [RTS Incident Classification] | Assess relevance by extent to which client/counterpart impact affects implementation of business objectives and potential impact on market efficiency. | Qualitative relevance test feeding Art.9(1)(f). | — |
| Art.1(4) [RTS Incident Classification] | Take into account all affected transactions involving a monetary amount where at least one part is carried out in the Union. | Scope rule for transaction-based thresholds. | — |
| Art.2(1) [RTS Incident Classification] | Reputational impact occurs where at least one criterion is met: media reflection; repetitive complaints; inability/likely inability to meet regulatory requirements; material loss/likely loss of clients or counterparts. | Defines qualitative reputational impact test. | — |
| Art.2(2) [RTS Incident Classification] | Take into account the visibility the incident has gained or is likely to gain in relation to each Art.2(1) criterion. | Proportionality factor for reputational assessment. | — |
| Art.4 [RTS Incident Classification] | Assess impact in other Member States: clients/counterparts in other MS; branches/group entities in other MS; FMIs/third-party providers affecting entities in other MS. | Operationalises DORA Art.18(1)(c). | — |
| Art.5 [RTS Incident Classification] | Take into account: availability (data inaccessible); authenticity (compromised source); integrity (non-authorised modification); confidentiality (access/disclosure to unauthorised party). | Operationalises DORA Art.18(1)(d). | — |
| Art.6 [RTS Incident Classification] | Assess whether incident: (a) affects ICT services/NIS supporting critical or important functions; (b) affects supervised financial services; (c) constitutes successful malicious unauthorised access to NIS. Point (c) is an automatic trigger. | Operationalises DORA Art.18(1)(e); gateway to Art.8(1) major-incident rule. | — |
| Art.7(1) [RTS Incident Classification] | Include: expropriated funds; software/hardware replacement; staff costs; non-compliance fees; customer redress; forgone revenues; communications; advisory/legal/forensic costs. | Includable cost taxonomy. | — |
| Art.7(2) [RTS Incident Classification] | Exclude: general maintenance; post-incident upgrades/improvements/risk assessment initiatives; insurance premiums. | Defines boundary of cost calculation. | — |
| Art.7(4) [RTS Incident Classification] | Sum up costs and losses referred to in paragraph 1 when assessing economic impact. | Aggregation rule. | — |
| Art.8(1) [RTS Incident Classification] | Incident is major where it affected critical services (Art.6) and either (a) Art.9(5)(b) threshold met; or (b) two or more other Art.9(1)–(6) thresholds met. | Primary classification decision point. | — |
| Art.8(2) [RTS Incident Classification] | Assess existence of recurring incidents on a monthly basis. Does not apply to microenterprises or Art.16(1) entities — applies to this entity. | Standalone Direct monthly assessment duty. | — |
| Art.9(1) [RTS Incident Classification] | Threshold met where: >10% affected clients; >100,000 clients; >30% affected counterparts; >10% transactions by count or value; relevant clients/counterparts affected. | Quantitative thresholds for Art.18(1)(a). | — |
| Art.9(2) [RTS Incident Classification] | Threshold met where any condition in Art.2(1)(a)–(d) is fulfilled. | Reputational threshold. | — |
| Art.9(3) [RTS Incident Classification] | Threshold met where: duration > 24 hours; or downtime > 2 hours for services supporting critical or important functions. | Time-based thresholds. | — |
| Art.9(4) [RTS Incident Classification] | Threshold met where incident has impact in two or more Member States under Art.4. | Geographical threshold. | — |
| Art.9(5) [RTS Incident Classification] | Threshold met where: (a) Art.5 impact has adverse impact on business objectives or regulatory compliance; or (b) any successful malicious unauthorised access to NIS resulting in data losses (automatic trigger). | Data-loss threshold including automatic malicious-access trigger. | — |
| Art.9(6) [RTS Incident Classification] | Threshold met where costs and losses have exceeded or are likely to exceed €100,000. | Monetary threshold for economic impact. | — |
| Art.1(1) [RTS Incident Reporting] | Initial notification, intermediate and final reports shall include: submission type; entity name and LEI; submitting entity ID; LEIs in aggregated reports; communication contact details; parent undertaking; currency. | Universal header fields. | — |
| Art.2(1) [RTS Incident Reporting] | Initial notification shall contain at least: incident reference code; detection/classification date and time; description; classification criteria from Arts 1–8 of 2024/1772; impacted Member States; discovery method; origin; BCP activation; reclassification info. | Substantive content of initial notification. | — |
| Art.3(1) [RTS Incident Reporting] | Intermediate report shall contain at least: CA reference; occurrence date/time; recovery date/time; how Arts 1–8 criteria fulfilled; type of incident; threats/techniques; functional areas affected; infrastructure components; client financial interest impact; reporting to other authorities; recovery actions; IOCs. | Substantive content of intermediate report. | — |
| Art.4(1) [RTS Incident Reporting] | Final report shall contain all of: root causes; resolution and root-cause-addressed timestamps; resolution information; resolution-authority-relevant info; direct/indirect costs and losses and financial recoveries; recurring-incident information. | Closure-report substantive content. | RTS on Incident Classification [loaded] |
| Art.5(1) [RTS Incident Reporting] | Submit: (a) initial report within 4 hours of classification as major and no later than 24 hours from awareness; (b) intermediate report within 72 hours of initial; (c) final report no later than one month after latest intermediate. | Core deadline framework. | — |
| Art.6(1) [RTS Incident Reporting] | Where the entity voluntarily notifies a significant cyber threat, the notification shall cover: general entity info; detection date/time; threat description; potential impact; classification criteria; threat status; preventive actions; notification to other authorities; IOCs. | Mandatory content where voluntary notification is made. | RTS on Incident Classification [loaded] |

### Section 2 — Conditionally Applicable Provisions

| Citation | Obligation Summary | Trigger Condition | Audit Action | Expanded by |
|---|---|---|---|---|
| Art.19(1)(a) [Main DORA] (core reporting obligation) | Report major ICT-related incidents to the relevant CA using Art.20 templates; where technical impossibility, notify CA via alternative means. | Major ICT incident classified under Art.18. | Test classification outputs against thresholds; confirm CA submission via templates. | ITS on Incident Reporting (not yet loaded); RTS on Incident Reporting [loaded] |
| Art.19(3) [Main DORA] (client notification) | Where a major incident impacts financial interests of clients, inform clients without undue delay about the incident and mitigation measures. | Major incident impacts financial interests of clients. | Evaluate whether trigger was met for sampled incidents and test timeliness and content of client notifications. | ITS on Incident Reporting (not yet loaded); RTS on Incident Reporting [loaded] |
| Art.19(4) [Main DORA] (initial/intermediate/final reports) | Submit: (a) initial notification; (b) intermediate report when status or handling changes; (c) final report when root cause analysis complete. | Major ICT incident classified under Art.18. | Test that all three reports were submitted in line with Art.5 deadlines. | ITS on Incident Reporting (not yet loaded); RTS on Incident Reporting [loaded] |
| Art.19(6) [Main DORA] (onward provision by CA) | Upon receipt of initial notification and each report, the CA shall in a timely manner provide details to: EBA/ESMA/EIOPA; ECB; CSIRTs; resolution authorities; other relevant public authorities. | Major incident classified under Art.18 (entity-side trigger; onward provision itself is a CA duty). | Awareness — entity submission triggers onward routing. | ITS on Incident Reporting (not yet loaded); RTS on Incident Reporting [loaded] |
| Art.23 [Main DORA] (payment-related incidents) | Chapter III requirements apply also to operational or security payment-related incidents concerning credit institutions. | Entity is a credit institution — trigger satisfied. | Confirm payment-related incidents are routed through Chapter III framework; confirm interaction with parallel PSD2-derived reporting. | ITS on Incident Reporting (not yet loaded) |
| Art.1(5) [RTS Incident Classification] | Where actual numbers of clients/counterparts/transactions cannot be determined, estimate based on available data from comparable reference periods. | Actual figures cannot be determined at time of reporting. | Test that any estimates are documented, reasoned and based on comparable reference periods. | — |
| Art.3(1) [RTS Incident Classification] | Measure incident duration from occurrence to resolution; fallbacks where occurrence or resolution time cannot be determined. | Primary rule applies; conditional fallbacks where occurrence/resolution time unknown. | Test methodology against the four scenarios; confirm fallback logic is documented. | — |
| Art.3(2) [RTS Incident Classification] | Measure service downtime from moment service fully/partially unavailable to moment regular activities restored; conditional extension for post-restoration delays. | Primary rule applies; conditional extension for post-restoration delay. | Test that downtime measurement reflects post-restoration delays where present. | — |
| Art.7(3) [RTS Incident Classification] | Calculate costs and losses based on data available at time of reporting; where actual amounts cannot be determined, estimate. | Actual cost/loss amounts cannot be determined at time of reporting. | Test that any estimated cost figures are reasoned and updated in subsequent reports. | — |
| Art.8(2) [RTS Incident Classification] (recurring incidents aggregation rule) | Recurring incidents considered one major incident where: occurred ≥2 times within 6 months; same apparent root cause; collectively fulfil Art.8(1). | Recurring incidents pattern matches the three-condition test. | Test recurring-incident assessment process; confirm monthly aggregation has been performed. | — |
| Art.10(1) [RTS Incident Classification] (significant cyber threat) | Cyber threat is significant where all three met: (a) if materialised could affect critical functions; (b) high probability of materialisation; (c) if materialised could meet Art.6, Art.9(1) or Art.9(4) thresholds. | All three cumulative conditions met. | Test classification of cyber threats against the three-condition cumulative test. | — |
| Art.5(2) [RTS Incident Reporting] (late classification) | Where entity did not classify as major within 24 hours of awareness but classifies later, submit initial notification within 4 hours from the later classification. | Classification as major occurs after the 24-hour-from-awareness window. | Where classification was delayed, test that the 4-hour-from-classification rule was applied. | — |
| Art.5(3) [RTS Incident Reporting] (delay notification) | Where unable to submit within Art.5(1) limits, inform the CA without undue delay (no later than the respective time limit) and explain the reasons. | Entity unable to submit within Art.5(1) deadline. | Test that any deadline failures were accompanied by a within-deadline delay notice and documented reason. | — |
| Art.5(4) [RTS Incident Reporting] (weekend/bank holiday derogation — final report only for this entity) | Where submission deadline falls on a weekend or bank holiday, entity may submit by noon of the next working day. The Art.5(5) carve-out disapplies this for credit institutions for initial notifications and intermediate reports. | Deadline falls on a weekend or MS bank holiday. | For final reports submitted on the next working day, confirm noon-deadline compliance; confirm derogation NOT used for initial/intermediate reports. | — |

### Section 3 — Cross-Referenced RTS/ITS Provisions

| Citation | Expands which DORA article | What it adds | Expanded by |
|---|---|---|---|
| Art.22 [RTS ICT-RMF] (also in Section 1) | Art.17 [Main DORA] | Specifies the mandatory components of the ICT-related incident policy. | RTS on Incident Classification [loaded] |
| Art.23(1)–(6) [RTS ICT-RMF] (also in Section 1) | Art.10, Art.17 [Main DORA] | Specifies detection mechanism content, alert prioritisation, evidence protection, logging granularity and trigger criteria. | — |
| Art.1(1)–(4) [RTS Incident Classification] (also in Section 1) | Art.18(1)(a) [Main DORA] | Defines client, counterpart, transaction and relevance populations. | — |
| Art.1(5) [RTS Incident Classification] (also in Section 2) | Art.18(1)(a) [Main DORA] | Adds estimation fallback for client/counterpart/transaction quantification. | — |
| Art.2(1)–(2) [RTS Incident Classification] (also in Section 1) | Art.18(1)(a) [Main DORA] | Defines the qualitative reputational impact criteria and visibility weighting. | — |
| Art.3(1)–(2) [RTS Incident Classification] (also in Section 2) | Art.18(1)(b) [Main DORA] | Specifies duration and downtime measurement methodology including fallback rules. | — |
| Art.4 [RTS Incident Classification] (also in Section 1) | Art.18(1)(c) [Main DORA] | Operationalises the geographical spread assessment with three impact channels. | — |
| Art.5 [RTS Incident Classification] (also in Section 1) | Art.18(1)(d) [Main DORA] | Operationalises data-loss criterion across availability, authenticity, integrity, confidentiality. | — |
| Art.6 [RTS Incident Classification] (also in Section 1) | Art.18(1)(e) [Main DORA] | Defines criticality of services affected including automatic malicious-access trigger. | — |
| Art.7(1), 7(2), 7(4) [RTS Incident Classification] (also in Section 1) | Art.18(1)(f) [Main DORA] | Defines includable costs, excluded costs and aggregation rule. | — |
| Art.7(3) [RTS Incident Classification] (also in Section 2) | Art.18(1)(f) [Main DORA] | Adds the cost-estimation rule at time of reporting. | — |
| Art.8(1) [RTS Incident Classification] (also in Section 1) | Art.19(1) [Main DORA] | Establishes the primary major-incident gateway rule. | — |
| Art.8(2) [RTS Incident Classification] (also in Section 1 and Section 2) | Art.19(1), Art.20 [Main DORA] | Adds the monthly assessment duty (Direct) and recurring-incidents aggregation rule (Conditional). | — |
| Art.9(1)–(6) [RTS Incident Classification] (also in Section 1) | Art.18(1) [Main DORA] | Sets numerical/qualitative materiality thresholds for each Art.18(1) criterion. | — |
| Art.10(1) [RTS Incident Classification] (also in Section 2) | Art.18(2), Art.19(2) [Main DORA] | Specifies the three-condition cumulative test for classifying a significant cyber threat. | — |
| Art.1(1) [RTS Incident Reporting] (also in Section 1) | Art.19(4) [Main DORA] | Establishes universal report header fields. | — |
| Art.2(1) [RTS Incident Reporting] (also in Section 1) | Art.19(4)(a) [Main DORA] | Specifies the substantive content of the initial notification. | RTS on Incident Classification [loaded] |
| Art.3(1) [RTS Incident Reporting] (also in Section 1) | Art.19(4)(b) [Main DORA] | Specifies the substantive content of intermediate reports. | RTS on Incident Classification [loaded] |
| Art.4(1) [RTS Incident Reporting] (also in Section 1) | Art.19(4)(c) [Main DORA] | Specifies the substantive content of final reports including root causes, costs and recurring-incident information. | RTS on Incident Classification [loaded] |
| Art.5(1) [RTS Incident Reporting] (also in Section 1) | Art.19(4) [Main DORA] | Establishes the 4-hour/24-hour/72-hour/one-month deadline framework. | — |
| Art.5(2), 5(3), 5(4) [RTS Incident Reporting] (also in Section 2) | Art.19(4) [Main DORA] | Adds late-classification, delay-notification and weekend-derogation rules. | — |
| Art.6(1) [RTS Incident Reporting] (also in Section 1) | Art.19(2) [Main DORA] | Specifies the substantive content of voluntary cyber threat notifications. | RTS on Incident Classification [loaded] |

### Section 4 — Indirect or Awareness Items

| Citation | Reason for Awareness | Expanded by |
|---|---|---|
| Art.4(2) [Main DORA] (proportionality — Chapter III) | Chapter III obligations are subject to proportionality based on entity size, risk profile and complexity. Calibrates how the entity scales its incident response capability. | RTS on Simplified ICT Risk Management (not yet loaded) |
| Art.19(2) [Main DORA] (Permissive — voluntary cyber threat notification) | The entity *may* voluntarily notify significant cyber threats to the relevant CA where it deems the threat relevant to the financial system, service users or clients. Auditor should be aware whether the entity has chosen to make such notifications and whether content matches Art.6(1) of 2025/301. | RTS on Incident Reporting [loaded] (Art.6); ITS on Incident Reporting (not yet loaded) |

### Section 5 — Excluded From Scope

| Citation | Obligation Type | Reason for Exclusion |
|---|---|---|
| Art.2 [Main DORA] | Scope | Defines DORA applicability; not an obligation. |
| Art.3 Definitions [Main DORA] | Definition | Interpretive provisions; not obligations. |
| Art.18(3) [Main DORA] | Empowerment | ESA mandate to develop the RTS on incident classification; not an entity obligation. |
| Art.18(4) [Main DORA] | Empowerment | ESA development considerations for the Art.18(3) RTS; not an entity obligation. |
| Art.19(1)(b) [Main DORA] (multi-CA designation) | Procedural | Member State duty to designate a single CA; entity not the addressee. |
| Art.19(1)(c) [Main DORA] (significant CI routing to ECB) | Entity-type | Applies only to credit institutions classified as significant under Reg 1024/2013 Art.6(4); entity is not designated significant under SSM. |
| Art.19(1)(d) [Main DORA] (Member State CSIRT discretion) | Procedural | Member State option to require parallel CSIRT notification; entity not the addressee. |
| Art.19(7) [Main DORA] | Procedural | Duty on EBA/ESMA/EIOPA and ECB to assess cross-MS relevance; entity not the addressee. |
| Art.19(8) [Main DORA] | Procedural | Duty on competent authority; entity not the addressee. |
| Art.20 [Main DORA] | Empowerment | ESA mandate to develop RTS/ITS on reporting content and templates. |
| Art.21(1)–(3) [Main DORA] | Empowerment | ESA joint-report obligation on single EU incident-reporting hub feasibility. |
| Art.22(1) [Main DORA] | Procedural | Duty on competent authority; entity not the addressee. |
| Art.22(2) [Main DORA] | Procedural | Duty on the ESAs through the Joint Committee; entity not the addressee. |
| Art.11 [RTS Incident Classification] | Procedural | Duty on competent authorities; entity not the addressee. |
| Art.12 [RTS Incident Classification] | Procedural | Duty on competent authorities; entity not the addressee. |
| Art.13 [RTS Incident Classification] | Scope | Operational entry-into-force provision; not an obligation. |
| Art.5(5) [RTS Incident Reporting] | Scope | Tagged Scope in the knowledge base — defines which entities the Art.5(4) derogation does not apply to. Substantively affects this entity as a credit institution — treat as effectively Conditional in working papers. See Coverage Assessment. |
| Art.5(6) [RTS Incident Reporting] | Procedural | Discretion of competent authority; entity should monitor but provision is on the CA. |
| Art.38 [RTS ICT-RMF] | Entity-type | Title III simplified framework provisions; entity is not under Art.16(1). |

### Coverage Assessment

- Total provisions retrieved: 76
- Section 1 — Directly applicable: 41
- Section 2 — Conditionally applicable: 14
- Section 3 — Cross-referenced RTS/ITS: 21 (all also appearing in Sections 1 or 2)
- Section 4 — Indirect or awareness: 2
- Section 5 — Excluded from scope: 19
- Documents not yet loaded but referenced:
  - ITS on Incident Reporting (Commission Implementing Regulation under DORA Art.20(b)) — sets standard forms and templates; referenced throughout but not loaded
  - RTS on Simplified ICT Risk Management — referenced from DORA Art.4(2) metadata; not in scope for this entity
- Confidence: **High** — Chapter III of DORA and its three loaded RTS (Incident Classification 2024/1772, Incident Reporting 2025/301, ICT-RMF Arts 22–23) provide a near-complete obligation set for an end-to-end incident-management audit of a standard-framework credit institution
- Metadata-substance discrepancies flagged:
  - **INC-RPT Art.5(5)** is tagged Scope in the knowledge base but the operative text disapplies the Art.5(4) weekend derogation for credit institutions in respect of initial notifications and intermediate reports. The auditor should treat it as effectively Conditional in working papers
- Audit-objective considerations (compliance review):
  - **Process and policy compliance:** test the documented ICT-related incident policy (RTS ICT-RMF Art.22) and incident management process (DORA Art.17(1)–(3)) contain every element listed, with named owners and management-body reporting evidence
  - **Classification decisions:** for each sampled incident, attest against the Art.8(1) primary gateway rule and the six Art.9 thresholds; test the monthly recurring-incidents assessment (Art.8(2)) and any aggregation determinations
  - **Report content compliance:** for each major incident, attest initial notification (Arts 1 and 2 of 2025/301), intermediate report (Arts 1 and 3) and final report (Arts 1 and 4) contain every mandatory field
  - **Timeliness compliance:** attest each report against the Art.5(1) deadlines; confirm the entity did NOT use the Art.5(4) weekend derogation for initial/intermediate reports
  - **Client notification compliance:** attest the without-undue-delay client notification under DORA Art.19(3) was made with mitigation-measure content
  - **Outsourcing compliance:** if reporting is outsourced (DORA Art.19(5)), attest the outsourcing arrangement preserves residual entity responsibility
  - **Voluntary cyber threat notifications:** where the entity made voluntary notifications under DORA Art.19(2), attest content against RTS 2025/301 Art.6(1) and the three-condition classification test under Art.10(1) of 2024/1772
- Gaps to flag for manual review:
  - The **ITS on Incident Reporting** sets the standard forms, templates and procedures; obtain and reconcile entity templates against it
  - **DORA Art.23 payment-related incidents:** confirm interaction with any parallel PSD2-derived reporting and that the entity does not double-report or omit overlapping disclosures
  - **Cross-border impact assessment** under Art.4 of 2024/1772 may require coordination with other group entities; confirm the aggregated-reporting mechanism was properly used where applicable
