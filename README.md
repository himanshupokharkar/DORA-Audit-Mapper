# DORA Audit Mapper

An open-source structured knowledge base and methodology for mapping
DORA (Digital Operational Resilience Act, Regulation EU 2022/2554)
regulatory obligations to specific audit scopes — and converting them
into Excel testing workbooks for audit fieldwork.

Designed for IT auditors who need to identify which DORA provisions
apply to a given audit topic and entity type, without manually
re-deriving scope from scratch every time.

---

## What This Repository Contains

- **652 paragraph-level chunks** across DORA main regulation and four
  Regulatory Technical Standards
- A **production-tested system prompt (v8)** that converts an audit
  scope into a structured five-section mapping with a full Article
  Text Appendix
- An **Excel conversion prompt** that turns any mapping output into a
  formatted audit testing workbook
- A **sample Excel testing workbook** showing what fieldwork output
  looks like for an incident management audit
- A **methodology document** for chunking and tagging new RTS or ITS
  documents as they are published
- **Reusable user prompts** for common audit-mapping queries
- **Worked examples** showing real mapping output across four audit
  topics

This is regulatory knowledge plus a workflow, not a software
application. It works with any large language model that accepts
system prompts and structured text input.

---

## Coverage At A Glance

| Document | Chunks | Source Label |
|---|---|---|
| DORA main regulation (EU 2022/2554) | 335 | `[Main DORA]` |
| RTS on ICT Risk Management Framework (EU 2024/1774) | 122 | `[RTS ICT-RMF]` |
| RTS on Threat-Led Penetration Testing (EU 2025/1190) | 107 | `[RTS TLPT]` |
| RTS on Incident Classification (EU 2024/1772) | 29 | `[RTS Incident Classification]` |
| RTS on Incident Reporting (EU 2025/301) | 59 | `[RTS Incident Reporting]` |
| **Total** | **652** | |

Each chunk carries 17 metadata fields including obligation type,
entity scope, condition triggers, and cross-references to other
instruments.

---

## Why This Exists

DORA went into force on 17 January 2025. The regulation is broad,
its scope varies by entity type, and it is expanded by multiple
RTS and ITS documents that often impose nested or conditional
obligations.

Manually scoping a DORA audit means reading the primary regulation
plus the relevant RTS, deciding which provisions apply to your
specific entity, separating direct obligations from supervisor
duties, identifying conditional triggers, and tracking
cross-document linkages.

This repository captures that work in a reusable form. The output
is consistent, traceable to source articles, and structured to
support audit working papers.

---

## How To Use

### Step 1 — Set Up The Mapping Tool

1. **Choose your LLM**: Claude (recommended), GPT-4, Gemini, or any
   model that accepts system prompts and large context. Developed and
   tested on Claude Sonnet 4.6 via Claude.ai Pro.

2. **Create a Project** (Claude.ai): In Claude.ai, create a new
   Project called "DORA Audit Mapper". Use Projects so the knowledge
   base files persist across sessions.

3. **Load the system prompt**: Copy the contents of
   `prompts/DORA_Audit_Mapper_System_Prompt_v8_PUBLIC.txt` into the
   Project Instructions field.

4. **Load the knowledge base files**: Upload all five files from
   `knowledge-base/` into the Project Knowledge section.

### Step 2 — Run A Mapping

Use one of the prompt templates in
`prompts/DORA_Audit_Mapper_User_Prompts_v3.txt`. You need three
inputs:

- **Audit topic** — e.g. "ICT incident classification and reporting"
- **Entity type** — e.g. "non-microenterprise credit institution"
- **Scope exclusions** — or confirm "none"

Audit objective is optional. If provided, it tailors the Coverage
Assessment section. The five-section regulation mapping is identical
regardless.

The system produces a structured five-section mapping with a full
Article Text Appendix containing verbatim regulatory text for every
cited article.

### Step 3 — Convert To Excel Testing Workbook (Optional)

To convert any mapping output into an Excel audit testing workbook:

1. Copy the full mapping output (including the Article Text Appendix)
2. Open a new claude.ai chat (not your Project)
3. Open `prompts/DORA_Excel_Conversion_Prompt.txt`
4. Paste the prompt into the chat, replacing `[PASTE YOUR FULL
   MAPPING OUTPUT HERE]` with your copied mapping
5. Download the Excel file

The Excel workbook contains four sheets:
- **Audit Context** — engagement details, fillable fields
- **Testing Programme** — one row per article, with columns for
  testing procedure, evidence, result, observations and follow-up
- **Coverage Assessment** — gaps, confidence, and audit
  considerations from the mapping
- **Excluded Items** — provisions considered but excluded, with
  reasons

See `examples/DORA_Testing_Workbook_Sample_Incident_Management.xlsx`
for a worked example.

---

## The Five-Section Output Format

Every mapping follows the same structure:

| Section | Contents |
|---|---|
| **Section 1 — Directly Applicable** | Direct obligations on the entity — audit without preconditions |
| **Section 2 — Conditionally Applicable** | Conditional obligations with their triggers — evaluate trigger before audit |
| **Section 3 — Cross-Referenced RTS/ITS** | RTS/ITS provisions that expand Section 1 and 2 obligations |
| **Section 4 — Indirect or Awareness** | Indirect obligations and Permissive provisions — awareness only |
| **Section 5 — Excluded From Scope** | Empowerments, supervisor duties, definitions, scope provisions — shown so auditors can verify what was considered |

Plus a Coverage Assessment summarising counts, confidence, and gaps.
Plus an Article Text Appendix with verbatim regulatory text for every
cited article in Sections 1-4.

---

## Eight-Category Obligation Taxonomy

Every chunk is tagged with one of eight obligation types:

| Type | Meaning | Where It Appears In Output |
|---|---|---|
| Direct | Operative obligation on entity | Section 1 |
| Conditional | Applies when trigger met | Section 2 |
| Indirect | Implied via cross-reference | Section 4 |
| Permissive | Entity *may* do something | Section 4 |
| Definition | Interpretive provision | Section 5 |
| Empowerment | Mandate to ESA | Section 5 |
| Procedural | Duty on authority | Section 5 |
| Scope | Defines applicability | Section 5 |

---

## Repository Structure

```
DORA-Audit-Mapper/
├── README.md                          ← this file
├── LICENSE                            ← MIT
│
├── knowledge-base/
│   ├── 01_Main_DORA_Knowledge_Base.md
│   ├── 02_RTS_ICT_Risk_Management_Framework.md
│   ├── 03_RTS_Threat_Led_Penetration_Testing.md
│   ├── 04_RTS_Incident_Classification.md
│   └── 05_RTS_Incident_Reporting.md
│
├── prompts/
│   ├── DORA_Audit_Mapper_System_Prompt_v8_PUBLIC.txt
│   ├── DORA_Audit_Mapper_User_Prompts_v3.txt
│   └── DORA_Excel_Conversion_Prompt.txt
│
├── methodology/
│   └── DORA_Knowledge_Base_Creator_Methodology.txt
│
├── examples/
│   ├── 01_encryption_mapping.md
│   ├── 02_incident_management_mapping.md
│   ├── 03_tlpt_mapping.md
│   ├── 04_third_party_risk_mapping.md
│   └── DORA_Testing_Workbook_Sample_Incident_Management.xlsx
│
└── docs/
    ├── known_limitations.md
    └── design_decisions.md
```

---

## What This Does Not Cover

Honest disclosure of gaps so users know where to supplement:

- **RTS on Subcontracting (EU 2025/532)** — not yet loaded; relevant
  for third-party risk audits involving sub-outsourcing of critical
  functions
- **ITS on Register of Information** — not yet loaded; needed for
  field-by-field testing of Article 28(3) register compliance
- **RTS on ICT Third-Party Service Provider Policy (EU 2024/1773)**
  — not yet loaded; needed for testing the CIF policy under Art.28(2)
- **RTS on Critical ICT Third-Party Providers** — not yet loaded;
  relevant for CTPP-side oversight audits
- **ITS on Incident Reporting Templates** — not yet loaded; needed
  to test template compliance at field level
- **TLPT RTS Annexes I-VIII** — referenced but not individually
  chunked; relevant for design-effectiveness TLPT audits
- **Guidelines and Q&A** — informal supervisory guidance not in scope

The system prompt flags references to unloaded instruments in the
"Expanded by" column so auditors always know what to supplement
manually.

---

## Methodology

The 17-field chunk structure and eight obligation categories were
developed iteratively over multiple cycles of diagnostic testing,
documented in the methodology file.

Key design principles:

1. **Paragraph-level granularity, not article-level inheritance** —
   each numbered paragraph is its own chunk with its own metadata
2. **Sub-chunking for mixed-obligation paragraphs** — where one
   paragraph contains both a primary obligation and a conditional
   fallback, they are split into separate chunks
3. **Source-traceable citations** — every output cites article
   reference plus source label; chunk IDs never appear in user output
4. **Auditor decides relevance** — the system surfaces all linkages
   in the "Expanded by" column rather than filtering by AI judgement
5. **Honest gap surfacing** — Coverage Assessment always lists
   unloaded instruments and metadata discrepancies so the auditor
   knows exactly what the system could and could not retrieve

See `methodology/DORA_Knowledge_Base_Creator_Methodology.txt` for
the complete process.

---

## Contributing

This is an open project. Contributions welcome in three forms:

1. **New RTS/ITS knowledge base files** — follow the methodology
   document and submit a pull request
2. **Enrichment of existing files** — better keywords, sub-chunking
   improvements, metadata corrections
3. **Tested example mappings** — real audit scopes plus mapping
   output, with personal or entity-specific data removed

Please open an issue first to discuss substantive changes.

---

## Status And Limitations

**Status**: Production-tested across five audit topics (encryption,
incident management, TLPT, third-party risk, BCP testing). Validated
on Claude Sonnet 4.6 with all five knowledge base files loaded.

**Quality of mappings**: Strong for the five loaded instruments.
Quality drops in domains covered by unloaded instruments — see
Coverage section above.

**Not a substitute for**:
- Professional regulatory advice
- Legal interpretation of DORA provisions
- Official supervisory guidance from EBA, ESMA, or EIOPA

The mappings produced are a starting point for audit scoping, not
the final scope. Auditor judgement remains required.

---

## License

MIT License — see LICENSE file. You are free to use, modify, and
share this work commercially and non-commercially, provided
attribution is preserved.

The DORA regulation text and RTS/ITS text reproduced in the knowledge
base files is official EU regulatory material published in the Official
Journal of the European Union and is in the public domain.

---

## About

Built by [Himanshu Pokharkar], Senior IT auditor, London.

For feedback, questions, or contributions:
- LinkedIn: [https://www.linkedin.com/in/himanshupokharkar/]
- Portfolio: [https://www.himanshupokharkar.com/]
- GitHub issues: please use the Issues tab on this repository

If this saves you time on a real DORA audit, I would value hearing
about it.
