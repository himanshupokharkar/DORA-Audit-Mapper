# Known Limitations

This document lists known gaps, design constraints, and edge cases
in the DORA Audit Mapper knowledge base and system prompt. Read
before relying on the tool for audit scope sign-off.

---

## 1. Unloaded Instruments

The following RTS and ITS are referenced in chunk metadata but have
not yet been chunked and loaded into the knowledge base. When any of
these instruments is relevant, the system will surface it in the
"Expanded by" column as "(not yet loaded)" and flag it in the
Coverage Assessment.

| Instrument | Relevance |
|---|---|
| RTS on Subcontracting (EU 2025/532) | Sub-outsourcing chain analysis and Art.30(2)(a) subcontracting determination for third-party risk audits |
| ITS on Register of Information | Field-by-field testing of the Art.28(3) Register of Information |
| RTS on ICT Third-Party Service Provider Policy (EU 2024/1773) | Content testing of the Art.28(2) CIF policy |
| RTS on Critical ICT Third-Party Providers | CTPP-side oversight regime |
| ITS on Incident Reporting Templates | Standard forms and templates for Art.19 notifications |
| RTS on Joint Examination Teams (EU 2025/420) | JET procedures for TLPT cross-border coordination |

**Impact:** Mappings for third-party risk and incident reporting audits
will have medium confidence on the detailed policy and template
requirements until these instruments are loaded. The system is honest
about this — it tells you what is missing.

---

## 2. TLPT RTS Annexes I-VIII Not Chunked

The RTS on TLPT (EU 2025/1190) contains eight Annexes specifying
required deliverable templates. These Annexes are referenced in the
main RTS article text but have not been chunked as individual
obligations.

**Impact:** For design-effectiveness TLPT audits, the auditor must
obtain Annexes I-VIII separately and reconcile entity deliverables
against them manually. The system will not surface specific Annex
requirements as testable obligations.

---

## 3. Art.3 Definitions Not In Main Mapping Scope

The 65 DORA Article 3 definition chunks are loaded in a separate file
(referenced but not included in the main knowledge base upload
instructions). Key defined terms are referenced in chunk text but
the definition chunks are not actively retrieved during mapping.

**Impact:** If the auditor needs to verify a specific DORA defined
term (e.g. "critical or important function", "major ICT-related
incident"), they should look up Art.3 directly rather than relying
on the mapping output.

---

## 4. Section 3 Uses Article-Level Grouping

In some mapping outputs, Section 3 (Cross-Referenced RTS/ITS
Provisions) groups multiple paragraphs of the same RTS article into
a single row rather than listing each paragraph separately.

**Impact:** Minor — the auditor may need to read the full RTS article
rather than being directed to a specific paragraph. The Article Text
Appendix reproduces the full article text so this information is
available within the same output.

---

## 5. Sectoral Interplay Not Fully Mapped

DORA Chapter V (third-party risk) operates alongside Solvency II
Art.49 (insurance), CRD VI (credit institutions), MiFID II (investment
firms), and PSD2 (payment services). The DORA knowledge base covers
the DORA-side obligations only.

**Impact:** For insurance undertakings, credit institutions, and
payment service providers, the auditor must reconcile DORA obligations
against existing sectoral outsourcing registers and guidelines
(particularly EIOPA guidelines on outsourcing to cloud service
providers, EBA outsourcing guidelines). The system surfaces this as
an awareness gap in Coverage Assessment for affected entity types.

---

## 6. LLM Quality Variability

The system prompt has been validated on Claude Sonnet 4.6. Output
quality on other models (GPT-4, Gemini) is expected to be similar
for straightforward topics but may degrade on:

- Very large mappings (TLPT, incident management) where context
  window usage is high
- Cross-document retrieval where multiple large knowledge base files
  must be searched simultaneously
- Sub-point extraction accuracy in the Article Text Appendix

**Recommendation:** Use Claude Sonnet 4 or higher for production
audit use. Validate a sample output before relying on a new model.

---

## 7. Not Legal Advice

The mappings produced are a starting point for audit scope
identification, not legal interpretation of DORA provisions. Where
a provision is ambiguous, the mapping reflects the most common
regulatory reading but should be reviewed by a qualified professional
before use in a regulated context.

Provisions tagged "Conditional" are based on the trigger conditions
identified in the chunk metadata. Real-world trigger evaluation may
require facts not available to the system (e.g. whether a specific
third-party contract supports a critical function).

---

## 8. Metadata Bugs Fixed In Current Version

Six metadata tagging errors were identified during diagnostic testing
and fixed in the current knowledge base files. The pattern in each
case was: a chunk whose operative text imposed an entity obligation
but was mis-tagged as Empowerment, Procedural, or Scope.

Fixed chunks:
- DORA-ART11-P10 (Empowerment → Conditional)
- DORA-ART19-P6 (Conditional → Procedural)
- DORA-ART27-P3 (Empowerment → Direct)
- DORA-ART31-P12 (Empowerment → Conditional)
- DORA-ART42-P3 (Procedural → Direct)
- INC-RPT-ART5-P5 (Scope → Conditional)

If you identify further metadata errors, please open a GitHub issue
with the chunk ID, current tag, and the operative text that suggests
a different tag.
