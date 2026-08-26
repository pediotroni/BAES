# BAES — External Critical Review

**Reviewer:** Engineer Ali Taheri (مهندس علی طاهری)  
**Review source:** Fable  
**Review date:** 2026-08-21  
**Reviewed repository:** `babakvarjamand/BAES`  
**Reviewed baseline:** Repository state reported as of the 2026-08-20 commit  
**Review stance:** Adversarial but fair  
**Status:** External review — received and preserved as submitted; not yet adjudicated by BAES governance

> **Provenance note:** This document records the critical review supplied to the BAES project by Engineer Ali Taheri. The review was produced after Ali provided the BAES repository to **Fable** and asked it to conduct a critical review. The content below is preserved as an external critique rather than presented as an official BAES position.
>
> **Important scope note:** The review evaluated the public repository available to Fable. At the time of review, the BAES Foundation material was not publicly released and therefore was not available to the reviewer as part of the public evidence base. Consequently, observations concerning missing principles, requirements, ontology elements, and implementation mechanisms must be interpreted in light of that publication boundary.

## 1. Restatement

BAES proposes that any situation where a human and an AI work together toward an outcome should be treated as an engineered system with an explicit chain: human intent → authority → delegation → AI participation → actions → evidence → evaluation → outcome. Its headline rule is that “AI must not autonomously expand human-defined intent, scope, or objectives,” and its second rule is that “authority may be delegated; engineering responsibility is not transferred.” It wants to be vendor-, technology- and domain-neutral, and to build itself through a standards-body-style staged process (ontology → specification → evidence → validation → review → release).

Today it consists of framing documents, folder scaffolding, and six blank templates. No principle, requirement, ontology element, research record, or case study has been published.

## 2. Falsifiable Claims

| # | Claim | Type | Compliance test stated? |
|---|---|---|---|
| C1 | “AI capability is advancing faster than the engineering structures used to manage complex Human–AI collaboration.” | Empirical | No evidence cited |
| C2 | Engineering structures for collaboration “remain fragmented.” | Empirical | No survey of existing structures |
| C3 | “Capability ≠ Authority”, “Execution ≠ Decision” | Definitional | n/a |
| C4 | “AI must not autonomously expand human-defined intent, scope, or objectives.” | Normative | No — “scope”, “expand”, “autonomously” undefined |
| C5 | “Authority may be delegated; engineering responsibility is not transferred.” | Normative / definitional | No — “responsibility” undefined |
| C6 | Actions should be “sufficiently traceable to support review and reconstruction.” | Normative | No — “sufficiently” undefined |
| C7 | BAES is “domain-general” | Aspirational | Untested; zero domains exercised |
| C8 | “BAES is developed according to the engineering principles it seeks to establish.” | Empirical (self-referential) | Partly checkable; see §5 |
| C9 | Uncontrolled scope expansion is “an important failure mode” | Empirical | Plausible; no incident data cited |
| C10 | “Concept Status ≠ Evidence Validity” | Methodological | n/a |
| C11 | Engineering Inquiry identifies ambiguity “before execution” | Definitional | Mechanism undefined |
| C12 | MOU / Datum / Coordinate relationships form “a rigorous reference framework” | Aspirational | Appears only as a heading; undefined |

The review concludes that every normative claim (C4–C6) lacks a test. The documents acknowledge this repeatedly (“the exact normative requirements… remain under development”). That is honest, but it means the project currently asserts zero checkable requirements.

## 3. Prior Art and Overlap

| BAES concept | Nearest existing equivalent | What BAES adds | Assessment |
|---|---|---|---|
| Human Engineering Authority | EU AI Act Art. 14 (human oversight); ISO/IEC 42001 §5; NIST AI RMF GOVERN 1–3; “meaningful human control” | Applies it at task level rather than system/organisation level | Mostly terminological; task-level framing is a modest shift |
| Delegated / Execution / Scope Authority | Principal-agent theory; least privilege; capability-based security; OAuth scopes; MCP/agent tool permissions | Vocabulary for kinds of authority an agent can hold | Terminological; security already has finer-grained models |
| No Autonomous Scope Expansion | OWASP LLM Top 10 “Excessive Agency”; agent confirmation gates; corrigibility and side-effect literature; specification gaming | Elevates it to a standard’s central principle | Emphasis somewhat new; concept itself is not |
| Traceability / Reviewability | ISO/IEC 42001 A.6.2.8; ISO/IEC 23894 §6; IEEE 7001-2021; OpenTelemetry GenAI semantic conventions; EU AI Act Art. 12 | Nothing yet; no schema or required fields | Terminological |
| Evidence before normative claims | ISO/IEC Directives Part 1; IETF “rough consensus and running code”; W3C Process | Nothing; standard practice restated as principle | Terminological |
| Engineering Inquiry | Clarification/escalation policies; HITL; requirements elicitation | A named construct | Potentially substantive if it becomes a decision rule |
| Concept status ≠ evidence validity | GRADE; ISO stage codes vs. TRL | Nothing new | Terminological |
| MOU / Datum / Coordinate | No identifiable equivalent | Unknown | Cannot assess |

The review notes that ISO/IEC 22989 already defines much of the vocabulary BAES lists, and argues that BAES should cite its neighboring standards and frameworks rather than appear unaware of them.

## 4. Uniqueness Verdict

**Overall novelty: 3 / 10**

| Dimension | Score | Reason |
|---|---:|---|
| Problem framing | 6 / 10 | “Engineer the collaboration, not the model or the organisation” is a real gap between model-centric and org-centric frameworks |
| Conceptual vocabulary | 2 / 10 | Every term has an established equivalent; several are less precise than the equivalent |
| Methodology | 3 / 10 | Standards-body process applied to a one-person project; public development from day zero is the main distinctive aspect |

**Strongest argument for redundancy:** ISO/IEC 42001 + 22989 + 23894, EU AI Act Arts. 12 and 14, and OWASP agentic guidance together already cover authority, oversight, logging, and excessive agency.

**Strongest argument against redundancy:** None of those documents, according to the review, gives a per-task artifact recording what a specific human asked, what authority was granted for that task, what the agent did, and where it stopped to ask. The review identifies a possible niche in a compact, tool-neutral task-level “delegation record” standard.

## 5. Structural Critique

### 5.1 Domain Generality

The review argues that BAES claims a breadth similar to ISO 9001 or ISO/IEC 42001 while attempting to constrain AI behavior across domains. It warns that behavioral norms may become domain-bound and suggests either a management-system orientation or a thin domain-neutral core with domain profiles.

### 5.2 Operationalisability of the Core Principle

The review identifies three scenarios in which “AI must not autonomously expand human-defined intent, scope, or objectives” may be ambiguous:

1. **Safety deviation:** The stated intent is to deploy v2.3, but the AI discovers that migration deletes user data. The principle does not clearly prioritize intent fidelity versus harm avoidance.
2. **Intrinsic sub-goals:** Fixing a login test may require changing a shared authentication helper used elsewhere. It is unclear whether that constitutes scope expansion.
3. **Ambiguous intent under time pressure:** “Clean up this dataset” may permit multiple interpretations with materially different methodological consequences.

The review proposes a classification such as **proceed / proceed-and-log-assumption / ask / halt**, keyed to reversibility, blast radius, and confidence.

### 5.3 Authority Taxonomy

The review argues that Human Engineering / Governance / Execution / Delegated / Scope Authority are not a clean partition because “delegated” describes a mode of acquisition while the others describe kinds of authority. It proposes two axes:

- **What authority covers:** intent-setting, scope-setting, action-execution, acceptance/approval
- **How authority is held:** original vs. delegated, with constraints such as bounds, revocability, and duration

It suggests these could be expressed as a single authority-grant record.

### 5.4 Convergence Risk

The review notes an eight-phase roadmap with no dates or exit criteria, a single visible author and commit, and argues that an ISO-style staged process applied by one maintainer could take years without external forcing functions.

It also criticizes the Restricted publication tier because withheld material prevents external readers from evaluating the substantive work.

### 5.5 Self-Conformance

The review states that BAES claims to follow its own principles but that the public repository did not contain corresponding decision, change, or review records for the observed changes. It characterizes the public record as insufficiently traceable under BAES’s own stated philosophy.

### 5.6 Repetition

The review identifies repeated presentations of authority, scope, delegation, evidence, traceability, governance, and reviewability across multiple documents, as well as repeated variants of the same diagram. It argues that repetition can make conceptual volume appear greater than conceptual maturity.

## 6. Adoption Analysis

The review finds the initial adopter unclear and asks what changes on “Monday morning” for a team using BAES.

It proposes the following candidate conformance checklist:

- Intent recorded before AI participation and attributed to a named human.
- Authorized scope and explicit out-of-scope list recorded.
- Authority grant recorded, including action classes allowed without approval, requiring approval, and forbidden.
- Significant AI actions logged with reference to the applicable authority grant.
- Deviations classified and logged.
- Evidence cited for conclusions.
- Human acceptance of outcome recorded.
- Record sufficient for an outside reader to reconstruct the sequence.

The review identifies a **minimum viable artifact**: a single “Delegation Record” in Markdown or JSON containing these fields.

It states that this artifact cannot be constructed from the public documents alone because the fields are the reviewer’s synthesis rather than explicit requirements in the repository.

## 7. Risks

| Risk | Review observation |
|---|---|
| Eponymous naming | A standard bearing its author’s name may signal ownership and deter co-authors. |
| Licensing | “Under consideration” blocks straightforward reuse and adoption. |
| Single-maintainer governance | Roles described in governance documentation are currently concentrated in one person; the review asks how contributors can progress toward authority. |
| No machine-readable ontology | A prose-only ontology cannot be readily validated, diffed, or implemented. |
| No worked example | Empty templates do not demonstrate whether the concepts survive a real task. |
| Restricted-tier opacity | External readers cannot evaluate material they cannot see. |
| Unexplained constructs | “MOU / Datum / Coordinate Discovery” is cited as an unexplained credibility cost. |

## 8. Improvement Plan Proposed by the Review

1. Publish one fully worked case study, including at least one scope-expansion incident and its handling.
2. Define a **Delegation Record** as the minimum conformance artifact, using explicit MUST/SHOULD language.
3. Publish the core ontology as JSON Schema, optionally OWL/SKOS.
4. Replace the absolute scope-expansion rule with a deviation decision rule based on reversibility × blast radius × confidence, yielding proceed / log-assumption / ask / halt.
5. Publish mapping tables to ISO/IEC 42001, 22989, 23894, NIST AI RMF, EU AI Act Arts. 12 and 14, and IEEE 7001.
6. Define a threat model covering prompt injection, tool misuse, silent scope creep, fabricated evidence, approval fatigue, and authority laundering through sub-agents.
7. Narrow the scope statement to task-level delegation between humans and agentic AI systems, then re-earn generality through domain profiles.
8. Select a license and add exit criteria and target dates to roadmap phases.
9. Demonstrate self-conformance through decision/change records and traceable commit messages.
10. Consolidate repeated concepts, establish a glossary, and reconsider eponymous naming; define or remove “MOU / Datum / Coordinate.”

## 9. The Question the Author Most Needs to Answer

> **What is the smallest artifact a team can produce for one real task today that would let an outside reviewer say “this collaboration was BAES-conformant, and here is the exact point where it was not”?**

## Appendix — Review Prompt Used by Fable

The following is the review prompt supplied with the external critique:

> You are a senior standards reviewer with experience in ISO/IEC JTC 1, NIST, and IEEE working groups, plus hands-on experience building agentic AI systems. Review the attached project, BAES (Babak AI Engineering Standard), a proposed vendor-neutral standard for governing Human–AI collaboration.
>
> Be adversarial but fair. Do not praise anything you cannot justify with a specific reference to the text. Do not pad.
>
> Work through these sections in order:
>
> 1. ONE-PARAGRAPH RESTATEMENT
> 2. FALSIFIABLE CLAIMS — extract every claim; mark definitional / empirical / normative / aspirational; flag normative claims lacking a compliance test.
> 3. PRIOR ART AND OVERLAP — compare concept-by-concept against NIST AI RMF 1.0, ISO/IEC 42001, 23894, 22989, EU AI Act Art. 14, IEEE 7001, OWASP LLM/Agentic Top 10, vendor agent safety guidance, MCP/agent permission models, HITL / principal-agent / meaningful-human-control literature.
> 4. UNIQUENESS VERDICT — 0–10 overall; separately score problem framing, vocabulary, methodology.
> 5. STRUCTURAL CRITIQUE — domain-generality vs testability; operationalisability of “no autonomous scope expansion”; authority taxonomy; convergence risk; repetition.
> 6. ADOPTION ANALYSIS — who adopts; what changes Monday morning; conformance checklist; minimum viable artifact.
> 7. RISKS — naming, licensing, single-maintainer governance, no machine-readable ontology, no worked example.
> 8. IMPROVEMENT PLAN — ≤10 prioritised actions.
> 9. THE QUESTION THE AUTHOR MOST NEEDS TO ANSWER — one sentence.
>
> Output in Markdown.

---

## BAES Governance Status

This document is an **external review record**, not a BAES specification or normative decision. No criticism in this document is automatically accepted as a BAES requirement. Each material point must be independently evaluated through BAES’s governance and evidence process.

**Disposition:** Pending formal response.
