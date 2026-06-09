# Design Decisions

This document explains the key design choices behind the DORA Audit
Mapper, including why certain approaches were taken and what
alternatives were considered. Useful for anyone who wants to extend,
fork, or challenge the methodology.

---

## 1. Paragraph-Level Granularity, Not Article-Level

**Decision:** Each paragraph of each article is a separate chunk with
its own metadata.

**Why:** DORA articles often contain multiple paragraphs with
materially different obligations, entity scopes, and triggers. If
Art.28 were a single chunk, the system could not distinguish between
Art.28(1) (Direct on all entities) and Art.28(2) (Conditional on
non-microenterprises) or Art.28(8) (Conditional on CIF-supporting
contracts). Paragraph granularity is the minimum unit at which
entity scope and obligation type can be accurately tagged.

**Alternative considered:** Article-level chunks with metadata
summarising all paragraphs. Rejected because it prevents accurate
entity-type filtering and conditional-trigger identification.

---

## 2. Sub-Chunking For Mixed-Obligation Paragraphs

**Decision:** Where one paragraph contains both a primary obligation
and a conditional fallback (e.g. "entity shall do X; where X is not
possible, entity shall do Y"), the paragraph is split into two chunks:
one Direct and one Conditional.

**Why:** Without sub-chunking, either the Direct or the Conditional
obligation would be mis-classified. The split allows the system to
place the primary obligation in Section 1 and the fallback in
Section 2, with the (a)/(b) sub-letter suffix making it clear they
are parts of the same parent paragraph.

**Applied to:** DORA Art.30(3)(a-g), RTS ICT-RMF Art.6(2), Art.6(3),
Art.6(4), and others.

---

## 3. Eight-Category Obligation Taxonomy

**Decision:** Eight obligation types (Direct, Conditional, Indirect,
Permissive, Definition, Empowerment, Procedural, Scope) rather than
a simpler binary (in scope / not in scope).

**Why:** The taxonomy drives the five-section output structure. It
allows the system to route each chunk to the correct section
automatically, to distinguish between obligations the auditor must
test (Direct, Conditional) and those they should be aware of but not
test (Indirect, Permissive) and those that have been considered and
excluded (Definition, Empowerment, Procedural, Scope).

The Permissive category is particularly important — "the entity may"
provisions are not obligations but are relevant context for the
auditor assessing whether the entity has made a design choice.

---

## 4. Section 5 Always Populated

**Decision:** Section 5 (Excluded From Scope) must always show every
excluded chunk, not just the most relevant ones.

**Why:** Audit transparency. The auditor must be able to verify that
the system considered and deliberately excluded each provision, not
that it failed to retrieve it. An empty Section 5 would be suspicious
for any DORA topic given how many supervisor duties and ESA
empowerments DORA contains.

**Trade-off:** Section 5 can be long (28+ rows for third-party risk,
31+ rows for TLPT). Accepted because completeness is more important
than brevity for audit working papers.

---

## 5. Article Text Appendix — Sections 1-4 Only

**Decision:** The Article Text Appendix reproduces verbatim text for
every article cited in Sections 1-4. Section 5 articles are excluded.

**Why:** Section 5 articles have been deliberately excluded from the
audit scope. Reproducing their full text would imply they are in
scope. Section 5 rows already contain enough information (obligation
type, reason for exclusion) for the auditor to verify the exclusion
rationale.

**Alternative considered:** Appendix for all five sections. Rejected
because it inflates the appendix with text the auditor has no reason
to act on.

---

## 6. Audit Objective Is Optional

**Decision (v7+):** The audit objective is not required to produce a
regulation mapping. If provided, it tailors the Coverage Assessment
only. The five-section mapping is identical regardless.

**Why:** The core value of the tool is regulation-to-topic mapping.
The audit objective influences how the auditor tests, not which
regulations apply. Adding it as a required input creates unnecessary
friction for auditors who just want the regulatory scope.

**Earlier approach (v1-v6):** Audit objective was required. Rejected
because it blocked the basic mapping use case and produced only minor
output differences (Coverage Assessment language only).

---

## 7. "Expanded By" Column Always Populated

**Decision:** The "Expanded by" column surfaces every linked
secondary instrument for each chunk, regardless of whether the
instrument is loaded or not, and regardless of how relevant the
linkage appears to the audit topic.

**Why:** The auditor decides relevance, not the system. Filtering
linkages by relevance would require the system to make a judgement
call about which RTS the auditor is likely to care about — a call
that should belong to the professional conducting the audit.

**Impact:** The "(not yet loaded)" entries in the "Expanded by"
column are the system's honest acknowledgement of its own gaps,
surfaced at the point of use rather than buried in documentation.

---

## 8. No Vector Database — Claude Project Setup

**Decision:** The knowledge base is loaded as plain text files in a
Claude Project rather than a vector database with embedding-based
retrieval.

**Why:** For 652 chunks across five files (approximately 1MB of
text), Claude's native context window is sufficient for the retrieval
quality needed. A vector database would add complexity and
infrastructure cost without materially improving the regulatory
reasoning quality.

**Limitation:** This approach does not scale beyond approximately
2,000-3,000 chunks. As additional RTS/ITS are loaded, performance
should be monitored. If context limits become a constraint, moving
to a hybrid retrieval architecture (Chroma or similar for retrieval,
Claude for reasoning) is the recommended upgrade path.

---

## 9. Source Labels Not Chunk IDs In Output

**Decision:** Visible citations use article references and source
labels (e.g. `Art.17(2) [Main DORA]`) rather than chunk IDs (e.g.
`DORA-ART17-P2`).

**Why:** Chunk IDs are internal implementation details. The auditor
reading the output needs to reference DORA and the RTS in official
documents — and official documents use article numbers, not chunk
IDs. Source labels tie the citation directly to the regulatory
instrument.

**Chunk IDs remain visible:** In the knowledge base files themselves,
for maintainers performing metadata enrichment or bug fixes. The
system prompt can also reveal chunk IDs on explicit request.

---

## 10. MIT License With Public Domain Note

**Decision:** MIT license with an explicit note that DORA regulatory
text reproduced in the knowledge base files is public domain EU
official material.

**Why:** The intellectual property in this repository is the
chunking, metadata structure, system prompt design, and methodology
— not the regulatory text. The regulatory text is official EU law
published in the Official Journal and is not proprietary. Being
explicit about this distinction avoids any ambiguity for users who
want to use the knowledge base files in commercial audit contexts.
