# CuneiAchai — Evidence Model

**Status:** Draft / Initial Baseline  
**Publication Status:** Public Case Study Record  

---

## 1. Purpose

The CuneiAchai Evidence Model defines how the project will distinguish source support, human review, uncertainty, and validation.

The model is intentionally conservative. A value is not considered validated merely because it exists in the dataset or because an external source was cited at record level.

---

## 2. Evidence Is Field-Specific

Evidence should ultimately be evaluated at the smallest practical unit.

Depending on the data, this may be:

- inscription
- sentence
- token
- cuneiform form
- transliteration
- lemma
- grammatical annotation
- translation
- metadata field

A single record may therefore contain fields with different evidence states.

---

## 3. Provenance vs Evidence vs Validation

These are separate concepts:

```text
PROVENANCE
Where did this information come from?

        ↓

EVIDENCE
What supports this information?

        ↓

VALIDATION
Has the information passed the project's defined review criteria?

        ↓

PUBLICATION
Is this information released at the current publication boundary?
```

None of these states should be inferred solely from another state.

---

## 4. Initial Evidence States

The following vocabulary is provisional:

### `SOURCE_REFERENCED`

An identifiable external source has been associated with the information.

### `CROSS_CHECKED`

The information has been compared against at least one relevant independent or alternative reference where appropriate.

### `HUMAN_REVIEWED`

A human review has been performed according to the applicable review scope.

### `VALIDATED`

The information has passed the defined validation criteria for its data class.

### `UNCERTAIN`

Available evidence does not justify a sufficiently confident single interpretation.

### `UNVERIFIED`

The required evidence or review has not yet been established.

These states may later be replaced or refined after the first corpus audit.

---

## 5. Evidence Types

Potential evidence types include:

```text
PRIMARY_INSCRIPTION
SCHOLARLY_EDITION
SCHOLARLY_REFERENCE
LEXICAL_REFERENCE
GRAMMATICAL_REFERENCE
SECONDARY_REFERENCE
COMPARATIVE_SOURCE
HUMAN_ANALYSIS
PROGRAMMATIC_CHECK
```

The final controlled vocabulary will be established after source inventory and domain review.

---

## 6. Confidence Is Not Validation

The project should avoid using a single numeric confidence score as a substitute for evidence.

For example:

```text
Confidence = high
```

does not by itself mean:

```text
Validation = complete
```

If a confidence score is introduced later, its meaning and calculation must be documented.

---

## 7. Conflicting Evidence

When credible sources disagree, the disagreement should not be silently removed.

The preferred process is:

```text
Source A ─┐
          ├── Comparison → Difference identified
Source B ─┘
                    ↓
              Human assessment
                    ↓
          Selected interpretation
          or preserved uncertainty
```

The basis for a material selection should be traceable.

---

## 8. AI-Assisted Evidence

AI output is not an independent source of scholarly evidence.

Where AI assistance contributes to a candidate lemma, normalization, interpretation, or other transformation, the project should distinguish:

```text
External Evidence
       ↓
AI-Assisted Candidate
       ↓
Human Decision
       ↓
Project Data
```

An AI suggestion may trigger investigation; it does not automatically establish validation.

---

## 9. Release Gate

A future public dataset release should define minimum evidence requirements by data class.

For example, the release gate may require stronger evidence for:

- cuneiform/transliteration alignment
- lexical analysis
- morphology
- translations

than for purely descriptive project metadata.

The actual thresholds will be defined only after the audit.

---

## 10. Current State

The current corpus does not yet have complete field-level evidence metadata.

This document therefore defines the intended direction rather than claiming that the model is already implemented throughout the dataset.
