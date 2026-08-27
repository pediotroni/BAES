# CuneiAchai — Provenance

**Status:** Initial Baseline  
**Publication Status:** Public Case Study Record  

---

## 1. Purpose

This document establishes the initial provenance model for CuneiAchai.

The purpose is to distinguish the origin of information from transformations, annotations, and validation performed during project development.

---

## 2. Project Creator

The CuneiAchai dataset is created and curated by **Babak Varjamand**.

---

## 3. Source Material

Project material has been collected from multiple reference sources available on the Internet.

The project does not assume that the existence of a source reference establishes correctness of every derived field.

A future source registry should identify, where practical:

- Source identifier
- Author / organization
- Title or description
- URL or bibliographic reference
- Access date where relevant
- Material used
- Applicable rights / licensing information where known

---

## 4. Provenance Categories

CuneiAchai will distinguish at least the following provenance categories:

### `SOURCE_DERIVED`

Information transcribed, extracted, or otherwise derived from an external reference source.

### `HUMAN_CREATED`

Information, interpretation, annotation, organization, or transformation created by the project author.

### `AI_ASSISTED`

Information or transformation for which an AI system provided assistance, suggestion, analysis, or candidate output.

### `PROGRAMMATIC_TRANSFORMATION`

Information produced through deterministic or rule-based software processing, including Python-based normalization.

### `DERIVED`

Information calculated or inferred from other project data through a documented transformation.

### `VALIDATED`

Information that has subsequently passed a defined validation process. This is an evidence/validation state, not merely an origin category.

---

## 5. Current Workflow Provenance

Based on the current project history, the workflow can be represented as:

```text
External Sources
      ↓
Collection
      ↓
Python-based Normalization
      ↓
AI Assistance where applicable
      ↓
Human Curation / Annotation
      ↓
Integrated Working Dataset
      ↓
Future Validation
```

The exact historical sequence of every operation is not yet reconstructed at field level.

---

## 6. AI Assistance

AI assistance has been used in normalization and in lemma-related work.

AI assistance is not treated as independent scholarly authority.

Where AI-assisted content becomes significant to a published result, the project should preserve enough information to distinguish the AI contribution from human decisions and source evidence.

---

## 7. Transformation Ownership

The project distinguishes underlying historical/source material from the project's own organization and transformations.

In particular:

```text
Underlying Source Material
        ≠
CuneiAchai Integration
        ≠
CuneiAchai Annotations
        ≠
CuneiAchai Engineering Artifacts
```

This distinction is important for attribution, licensing, provenance, and publication decisions.

---

## 8. Current Provenance Limitations

Field-level provenance is not yet complete.

The current project therefore does not claim that every value can already be traced through a complete machine-readable provenance chain.

Completing this model is a future engineering objective.

---

## 9. Provenance Principle

> **Every significant published claim should be distinguishable by origin, transformation, and validation status wherever practical.**
