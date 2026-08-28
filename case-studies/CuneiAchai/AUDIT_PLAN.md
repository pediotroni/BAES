# CuneiAchai — Initial Audit Plan

**Status:** Planned  
**Dataset:** Restricted / Not Publicly Released

---

## 1. Purpose

This document defines the first structured audit of the existing CuneiAchai working dataset.

The objective is not to rewrite or improve the dataset before understanding it. The objective is to determine what currently exists, how it is structured, what can be evidenced, and where uncertainty or inconsistency exists.

---

## 2. Audit Principle

> **Inspect first. Modify second.**

The existing working dataset should be treated as an evidence-bearing development artifact. No broad cleanup should be performed before the original structure and transformations have been characterized.

---

## 3. Audit Stages

### Stage A — Structural Audit

Determine:

- Actual file format(s)
- Record count
- Field inventory
- Nested structures
- Optional fields
- Repeated fields
- Field-name inconsistencies
- Data-type inconsistencies
- Duplicate or near-duplicate records
- Encoding and Unicode integrity

### Stage B — Corpus-Level Audit

Determine:

- Inscription coverage represented by the dataset
- Record organization
- Sentence/inscription boundaries
- Tokenization conventions
- Relationship between inscription-level and token-level data

### Stage C — Linguistic-Annotation Audit

Inspect:

- Transliteration conventions
- Lemma conventions
- POS taxonomy
- Morphological fields
- Case labels
- Person/number labels
- Proper-name handling
- Lexical meanings

### Stage D — Alignment Audit

Check relationships among:

```text
Cuneiform
    ↕
Transliteration
    ↕
Tokens
    ↕
Lemma / Morphology
    ↕
Translation
```

The purpose is to identify mismatches rather than assume alignment.

### Stage E — Source and Provenance Audit

Determine:

- Which information is source-derived
- Which source supports which data class
- Where source references are record-level only
- Where field-level provenance is available
- Where provenance is missing

### Stage F — Validation Audit

Determine which records or fields already have meaningful review evidence and which require further validation.

The audit must not equate "not yet fully validated" with "known incorrect."

---

## 4. Representative Sampling

The first audit will use a representative subset of the private working dataset rather than requiring publication of the complete dataset.

The sample should contain multiple data shapes and, where practical:

- short records
- long records
- multiple inscriptions
- different grammatical constructions
- records with complete annotations
- records with optional/missing annotations
- records containing proper names
- records from different source contexts

---

## 5. Audit Outputs

The initial audit should produce:

1. Field inventory
2. Schema observations
3. Data-quality findings
4. Inconsistency list
5. Provenance gaps
6. Linguistic-review candidates
7. Validation candidates
8. Proposed schema changes
9. Recommended automated checks
10. A decision on the first formal dataset baseline

---

## 6. Preservation Rule

Before any destructive normalization or correction, preserve the current working state.

Corrections should be traceable and should not erase the ability to determine what was changed.

---

## 7. Publication Rule

The audit may use private/restricted data without requiring the complete dataset to become public.

Only artifacts explicitly approved for publication should be added to the public BAES case study.

---

## 8. Immediate Next Action

Provide a representative extract of the existing working dataset for structural and schema inspection.

The extract should preserve the actual field names and nesting of the working data.

No manual cleanup is required before inspection.
