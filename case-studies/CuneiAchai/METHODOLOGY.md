# CuneiAchai — Methodology

**Status:** In Progress  
**Publication Status:** Public Case Study Record  

---

## 1. Purpose

This document records the current methodological approach used to construct and maintain the CuneiAchai corpus.

It is a living engineering document. Details may be refined as the underlying dataset and its evidence model are audited.

---

## 2. Source Collection

Project material has been collected from multiple reference sources available on the Internet.

The source collection process is intended to bring relevant textual, transliteration, translation, lexical, grammatical, and historical information into a common working environment.

The project does not assume that information from different sources is automatically equivalent or mutually consistent.

Source reconciliation is therefore an explicit future work item.

---

## 3. Normalization

Python-based programming has been used to normalize and process collected material into a unified structure.

AI assistance has been used during parts of the normalization workflow.

The current methodological principle is:

```text
Source Material
      ↓
Programmatic Processing
      ↓
AI-Assisted Operations where applicable
      ↓
Human Control / Curation
      ↓
Normalized Working Dataset
```

The precise transformation rules and scripts are to be documented as the project matures.

---

## 4. Corpus Integration

The project seeks to represent related information as a connected record rather than as isolated lists.

A conceptual record may connect:

```text
Inscription
   ├── Text
   ├── Transliteration
   ├── Translation
   ├── Metadata
   └── Tokens
          ├── Cuneiform
          ├── Transliteration
          ├── Lemma
          ├── POS
          ├── Morphology
          └── Meaning
```

This structure is intended to support traceability between inscription-level and token-level information.

---

## 5. Annotation

The current dataset contains linguistic and lexical annotations including, where applicable:

- Lemma
- Part of speech
- Sub-category
- Case
- Person/number
- Lexical meaning
- Other grammatical information

According to the current project history, most annotation and curation has been performed by the project author. AI assistance has specifically been used for lemma-related work.

The annotation taxonomy remains subject to validation against appropriate linguistic references.

---

## 6. Translation

The working corpus contains Persian and English translations where available.

Translations should be treated as data requiring provenance rather than as automatically authoritative interpretations.

Where multiple translations or interpretations exist, the future evidence model should allow the alternatives and their sources to remain distinguishable.

---

## 7. Human Control

Human review and project authority remain responsible for the admission of information into the working corpus.

AI assistance does not independently authorize a dataset change or establish scholarly validity.

This reflects the BAES distinction between AI execution/assistance and human engineering authority.

---

## 8. Reproducibility

Where practical, transformation processes should eventually be reproducible through documented scripts, inputs, outputs, and version information.

The current public case study does not claim that every historical transformation is already reproducible.

Establishing this capability is part of the ongoing engineering work.

---

## 9. Methodological Constraints

The current project has several known methodological constraints:

- Source material may use different conventions.
- Historical and linguistic interpretations may differ between sources.
- Normalization can introduce transformation decisions.
- AI-assisted processing may introduce errors.
- Current records do not yet have a complete formal evidence/validation status model.
- The complete working dataset is not currently public.

These constraints are not treated as defects to conceal; they are part of the current project state.

---

## 10. Future Methodological Work

The methodology is expected to evolve through:

1. Source inventory
2. Source classification
3. Transformation-rule documentation
4. Schema refinement
5. Cross-source reconciliation
6. Linguistic validation
7. Consistency testing
8. Provenance completion
9. Versioned releases
10. Publication review

Changes should be recorded when they materially affect the corpus or its interpretation.
