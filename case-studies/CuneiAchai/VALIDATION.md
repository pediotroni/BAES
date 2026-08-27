# CuneiAchai — Validation Framework

**Status:** Initial Baseline  
**Publication Status:** Public Case Study Record  
**Dataset Validation:** Not Complete

---

## 1. Purpose

This document defines the initial approach for evaluating the correctness, consistency, provenance, and reliability of CuneiAchai data.

It does not certify the current corpus as correct or complete.

---

## 2. Current Validation Position

The CuneiAchai corpus is a development/research artifact.

The project does not currently declare the dataset to be fully validated, complete, or error-free.

This is a deliberate status rather than a claim that every record is known to be incorrect or unverified.

---

## 3. Validation Dimensions

Future validation should distinguish at least the following dimensions:

### Source Validation

Can the relevant value be traced to an identifiable source?

### Textual Validation

Does the cuneiform representation correspond to the referenced material?

### Transliteration Validation

Does the transliteration correspond to the cuneiform representation according to the applicable convention/source?

### Translation Validation

Can the translation be supported by the referenced source or an explicit linguistic analysis?

### Lexical Validation

Are lemma and lexical meaning supported by appropriate linguistic evidence?

### Morphological Validation

Are case, person/number, tense/aspect/mood, and related annotations supported?

### Structural Validation

Is the record internally consistent and correctly represented according to the schema?

### Cross-Source Validation

Where multiple sources exist, are differences identified and reconciled rather than silently merged?

---

## 4. Evidence States

The following states are proposed as an initial vocabulary and are not yet final normative definitions:

```text
SOURCE_REFERENCED
CROSS_CHECKED
HUMAN_REVIEWED
VALIDATED
UNCERTAIN
UNVERIFIED
```

Evidence state and publication state must remain separate.

---

## 5. Validation Workflow

A future validation workflow may follow this pattern:

```text
Record
  ↓
Source Identification
  ↓
Structural Checks
  ↓
Text / Transliteration Checks
  ↓
Linguistic Checks
  ↓
Cross-Source Comparison
  ↓
Human Review
  ↓
Validation Decision
  ↓
Traceable Record
```

The actual sequence may vary by data type.

---

## 6. Automated Validation

Python-based validation should eventually be used where deterministic checks are appropriate.

Potential automated checks include:

- Schema validity
- Required-field presence
- Field-name consistency
- Duplicate detection
- Token count consistency
- Cuneiform/token alignment
- Transliteration/token alignment
- Controlled vocabulary validation
- Metadata consistency
- Source-reference integrity

Automated validation cannot by itself establish the scholarly correctness of linguistic interpretations.

---

## 7. Human Validation

Human review remains necessary for questions that require linguistic, historical, or interpretive judgment.

AI output should not be treated as a substitute for such validation.

---

## 8. Uncertainty

Uncertainty should be recorded rather than silently resolved when the available evidence does not justify a single conclusion.

Where sources disagree, the project should preserve the disagreement when practical and record the basis for any selected interpretation.

---

## 9. Corrections

A discovered error should be corrected through a traceable process where the correction materially affects the dataset or its interpretation.

The project should preserve sufficient history to identify what changed and why.

---

## 10. Validation Limitations

The current framework is preliminary.

No complete validation pass has yet been declared for the corpus.

The validation vocabulary, evidence thresholds, reviewer requirements, and release gates will be refined after the initial dataset audit.

---

## 11. Validation Principle

> **Do not convert uncertainty into certainty merely to make the dataset appear complete.**
