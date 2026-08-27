# CuneiAchai — Data Model

**Status:** Draft / Initial Baseline  
**Publication Status:** Public Case Study Record  

---

## 1. Purpose

This document describes the current conceptual data model observed in the CuneiAchai working corpus.

It is intentionally a **conceptual baseline**, not a declaration that the current dataset schema is final.

---

## 2. Record-Level Model

The current corpus represents an inscription-related record with several information layers:

```text
Inscription Record
│
├── Cuneiform Text
├── Transliteration
├── Persian Translation
├── English Translation
├── Description
├── Sources
├── Classification / Type
├── Inscription Metadata
└── Tokens
```

---

## 3. Inscription Metadata

The current sample demonstrates metadata fields such as:

- Source identifier
- Inscription name
- Location
- King / ruler
- Approximate date
- Inscription type

The final metadata model should distinguish controlled vocabulary fields from free-text fields.

---

## 4. Token Model

A token may currently contain:

```text
Token
├── Cuneiform
├── Transliteration
├── Lemma
├── POS
├── Sub-POS
├── Case
├── Person / Number
└── Meaning
```

Not every token necessarily requires every field.

Optionality and cardinality will be formalized after a broader dataset audit.

---

## 5. Linguistic Layers

The model currently mixes several linguistic layers that should remain conceptually distinguishable:

### Orthographic / Script Layer

- Cuneiform representation

### Transliteration Layer

- Scholarly transliteration

### Lexical Layer

- Lemma
- Meaning

### Morphological Layer

- Case
- Person / number
- Other grammatical attributes

### Syntactic / Grammatical Layer

- Part of speech
- Sub-category
- Future syntactic relations where supported

### Translation Layer

- Persian translation
- English translation

This separation is important because a single textual form may have multiple analytical interpretations.

---

## 6. Provenance Layer

The final model should be capable of distinguishing the provenance of individual fields or annotations where this is materially important.

Conceptually:

```text
Field / Annotation
      ↓
Origin
      ↓
Source / Human / AI-assisted / Derived
      ↓
Evidence
      ↓
Validation Status
```

The current working dataset does not yet expose this level of provenance for every field.

---

## 7. Evidence and Validation Layer

Evidence status should not be embedded implicitly in the existence of a field.

The future model should support explicit status information such as:

```text
Source Referenced
Cross-Checked
Human Reviewed
Validated
Uncertain
Unverified
```

These labels are provisional and will be formally defined after the evidence-model audit.

---

## 8. Data Integrity Requirements

The model should eventually support automated checks for:

- Missing required fields
- Invalid field names
- Inconsistent field types
- Duplicate records
- Token/text alignment problems
- Transliteration/cuneiform count mismatches where applicable
- Inconsistent metadata
- Invalid controlled vocabulary values
- Broken source references

The existence of these requirements does not imply that all checks are currently implemented.

---

## 9. Schema Evolution

The current conceptual model is expected to evolve.

Schema changes should preserve traceability and should not silently alter the meaning of existing records.

A formal schema version will be established after the first complete structural audit.

---

## 10. Current Status

The model is sufficiently defined to document the current corpus structure, but it is **not yet declared a final CuneiAchai schema**.

The next step is to compare this conceptual model against a representative sample of the actual corpus and identify missing, ambiguous, duplicated, or overloaded fields.
