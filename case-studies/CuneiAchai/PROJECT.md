# CuneiAchai — Project Definition

**Status:** In Progress  
**Publication Status:** Public Case Study Record  
**Dataset Status:** Restricted / Development  

---

## 1. Purpose

CuneiAchai is an ongoing research and data-engineering project for organizing Achaemenid Old Persian cuneiform material into a structured corpus suitable for linguistic research and future computational/AI applications.

The project is maintained as a BAES case study in order to preserve a traceable engineering record and to evaluate BAES concepts in a real research context.

---

## 2. Project Origin

The project work represented by the current corpus began approximately in **2025**.

The project evolved through the collection, normalization, integration, and annotation of material obtained from multiple reference sources available on the Internet.

The exact historical evolution of individual artifacts will be documented as provenance information becomes available.

---

## 3. Project Objective

The current objective is to construct an integrated and machine-readable representation of Old Persian cuneiform material in which textual, linguistic, historical, and source information can be related within a consistent data structure.

The intended structure connects, where available:

```text
Inscription
    ↓
Text
    ↓
Tokens
    ↓
Cuneiform / Transliteration
    ↓
Lexical and Morphological Annotation
    ↓
Translation
    ↓
Metadata and Sources
```

The project may later support AI/NLP research, but an AI application is not currently treated as proof of corpus correctness.

---

## 4. Current Data Characteristics

The current working material includes, where available:

- Original cuneiform representation
- Transliteration
- Persian translation
- English translation
- Historical/descriptive information
- Inscription metadata
- Tokenization
- Lemma
- Part of speech
- Sub-category information
- Case
- Person/number information
- Other grammatical or lexical annotations
- Word meanings
- Source references

The exact schema remains subject to audit and refinement.

---

## 5. Human and AI Roles

The dataset has been created and curated by **Babak Rasti M.**.

The current development history indicates a **human-controlled, AI-assisted workflow**.

In particular:

- Python programming has been used for normalization and data processing.
- AI assistance has been used during normalization.
- AI assistance has also been used for lemma-related work.
- Other corpus content and annotations have been produced/curated by the project author according to the current project history.

The public case study does not treat AI-generated or AI-assisted output as independently authoritative evidence.

---

## 6. Sources

Project material has been collected from multiple reference sources available on the Internet.

Source provenance is an ongoing work item. The project will distinguish, where practical, between:

1. External source material
2. Data derived or transcribed from sources
3. Transformations performed by the project
4. Human-created annotations
5. AI-assisted transformations or suggestions
6. Validation results

A source being used by the project does not imply that the project owns the underlying source material.

---

## 7. Validation Position

The current project is **not declared fully validated**.

This status is deliberate. The corpus is considered a development/research artifact and remains subject to linguistic, source, structural, and consistency review.

The project therefore avoids treating the current dataset as a perfect or final scholarly corpus.

---

## 8. Versioning

The project did not previously maintain a formal public dataset versioning scheme.

A formal baseline and subsequent versioning policy will be established after the initial evidence and data-model audit.

No historical version numbers are being invented retroactively.

---

## 9. Publication Boundary

The complete master/working dataset is currently restricted from public publication.

The public case-study repository is intended to expose the engineering record without automatically exposing the complete underlying dataset.

This boundary may change through an explicit publication decision.

---

## 10. Non-Claims

At the current stage, CuneiAchai does not claim:

- Complete scholarly validation
- Universal correctness
- Exhaustive coverage of all relevant Old Persian material
- Exclusive ownership of underlying historical/source material
- Uniqueness relative to every existing corpus or database

Any future claim of uniqueness, completeness, or scholarly status must be supported by appropriate evidence.

---

## 11. Next Engineering Objectives

The immediate objectives are:

1. Establish the current data-model baseline.
2. Establish detailed provenance requirements.
3. Define evidence and validation states.
4. Audit structural consistency.
5. Reconcile source-derived information where required.
6. Establish a formal dataset versioning scheme.
7. Define the public/private publication boundary.
8. Record significant findings and corrections through traceable artifacts.

