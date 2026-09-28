# Wittgenstein Apartment: Behavioral Predicate Resource

**Release:** v1.0  
**Author:** Furkan Yaşar  
**Resource type:** Sense-level behavioral predicate resource  
**License:** Wittgenstein Apartment Academic & Derivative Research License v1.0 (WA-ADRL-1.0)  
**Canonical archive / DOI:** https://doi.org/10.5281/zenodo.23015862  
**Hugging Face:** https://huggingface.co/datasets/Kon-tiki-ship/wittgenstein-apartment-behavioral-predicate-resource  
**Homepage:** https://www.furkanyasar.me

Wittgenstein Apartment (WA) is a sense-level behavioral predicate resource designed to bridge lexical-semantic representations of human action with character-relative action repertoires and downstream narrative, simulation, and planning systems.

Release v1.0 contains **2,904 active Action Senses**, organized through **541 Behavioral Predicate Families** and **14 behavioral Superclasses**. The resource also includes lexical background, goal relations, execution/context metadata, and eight downstream Functional Projection views.

WA separates three representational questions:

1. **Behavioral identity** — What exact action is this?
2. **Character repertoire** — Should a character be assumed to have access to this action without additional character-specific evidence?
3. **Situational executability** — Can the action be carried out in the current scene and world conditions?

---

## Canonical Release

The archival, citable v1.0 release is deposited on Zenodo:

**DOI:** [10.5281/zenodo.23015862](https://doi.org/10.5281/zenodo.23015862)

This GitHub repository is a public research mirror and project-facing repository for the same v1.0 resource family.

Hugging Face dataset mirror:

https://huggingface.co/datasets/Kon-tiki-ship/wittgenstein-apartment-behavioral-predicate-resource

---

## Release v1.0 at a Glance

| Metric | Value |
|---|---:|
| Active Action Senses | 2,904 |
| Character Specific Action Senses | 2,469 |
| Basic Human Action Senses | 435 |
| Behavioral Predicate Families | 541 |
| Behavioral Superclasses | 14 |
| WordNet Background Records | 2,890 |
| Goal Relation Rows | 4,193 |
| Active Senses with at Least One Goal Relation | 2,739 |
| Non-Goal Exceptions | 151 |
| Functional Projection Rows | 1,392 |
| Unique Projected Action Senses | 1,361 |
| Functional Projection Views | 8 |

The 14 Superclasses are:

`CARE`, `COGNITION`, `COMBAT`, `COMMUNICATION`, `ECONOMY`, `EMOTION`, `LEISURE`, `LOCOMOTION`, `MANIPULATION`, `PERCEPTION`, `SOCIAL`, `STATE_MAINT`, `SURVIVAL`, and `TRANSPORT`.

---

## Core Representation Model

```text
Superclass
    ↓
Behavioral Predicate Family
    ↓
Action Sense
```

- **Superclass** provides a broad behavioral domain.
- **Behavioral Predicate Family** provides an intensional grouping of related action senses with shared behavioral constraints.
- **Action Sense** is the smallest stable behavioral identity used as the primary cross-layer unit.

The principal cross-file join key is:

```text
Action Sense ID
```

Action-level metadata includes fields such as Task Structure, Scene Dependency, Scene Gate Type, Affordance Gates, Action Anatomy, lexical background, goal relations, and downstream Functional Projection metadata.

---

## Basic Human Action and Character Specific Action

### Basic Human Action (BHA)

BHA represents a **default-open repertoire**: actions that do not normally require additional character-specific evidence before being considered available to a character model.

### Character Specific Action (CSA)

CSA represents an **evidence-gated repertoire**: actions whose inclusion normally requires positive evidence such as skill, training, occupation, institutional authority, specialized practice, biography, or another marked character property.

The distinction concerns **repertoire assumptions**, not a universal claim about whether a human being is physically capable of performing an action.

---

## Functional Projections

The companion Functional Projections workbook provides eight operational views over the same semantic authority:

- `SPEAK`
- `COMBAT`
- `INSPECT`
- `MOVE`
- `MAKE`
- `USE`
- `TAKE`
- `GIVE`

Release v1.0 contains **1,392 projection rows** covering **1,361 unique Action Senses**.

Functional Projection does not redefine Action Sense identity. The semantic fields are inherited from the Behavioral Predicate Resource; projection-specific fields provide downstream retrieval and routing surfaces.

---

## Repository Structure

```text
.
├── README.md
├── data/
│   ├── Wittgenstein_Apartment_Behavioral_Predicate_Resource_v1.0.xlsx
│   ├── Wittgenstein_Apartment_Behavioral_Predicate_Resource_v1.0.json
│   ├── Wittgenstein_Apartment_Behavioral_Predicate_Resource_v1.0.jsonl
│   ├── Wittgenstein_Apartment_Functional_Projections_v1.0.xlsx
│   ├── Wittgenstein_Apartment_Functional_Projections_v1.0.json
│   └── Wittgenstein_Apartment_Functional_Projections_v1.0.jsonl
├── figures/
│   ├── Figure_1_Representational_Gap.png
│   ├── Figure_2_Core_Architecture.png
│   ├── Figure_3_Executable_Action_Space.png
│   └── Figure_4_Goal_Relations_and_Projection.png
├── paper/
│   ├── Wittgenstein_Apartment_Article_EN_Submission_Master_v1.0.pdf
│   └── Wittgenstein_Apartment_Article_EN_Submission_Master_v1.0.docx
├── CITATION.cff
├── LICENSE.txt
├── checksums.sha256
└── release_metadata.json
```

---

## Data Files

### Behavioral Predicate Resource

`data/Wittgenstein_Apartment_Behavioral_Predicate_Resource_v1.0.xlsx`

Primary workbook containing:

- `00_SUMMARY`
- `01_Character_Specific`
- `02_Basic_Human`
- `03_Family_Definition`
- `A_WORDNET_BACKGROUND`
- `B_GOAL_ONTOLOGY`
- `C_NON_GOAL_EXCEPTIONS`

### Functional Projections

`data/Wittgenstein_Apartment_Functional_Projections_v1.0.xlsx`

Companion workbook containing:

- `00_SUMMARY`
- `01_SPEAK`
- `02_COMBAT`
- `03_INSPECT`
- `04_MOVE`
- `05_MAKE`
- `06_USE`
- `07_TAKE`
- `08_GIVE`

---

## JSON and JSONL Exports

The JSON representations preserve workbook organization at the sheet level. The JSONL exports are row-oriented and retain source sheet and source-row provenance.

Example JSONL record:

```json
{
  "sheet": "01_Character_Specific",
  "row_number": 2,
  "data": {
    "Action Sense ID": "WA.ACT.000001",
    "Superclass": "CARE",
    "Family Name": "CHILD_CARE"
  }
}
```

---

## Intended Research Uses

Potential non-commercial scholarly uses include:

- lexical-semantic analysis
- computational narrative and character modeling
- automated planning and domain authoring research
- game and simulation research
- knowledge representation
- digital humanities
- ontology and knowledge-graph mappings
- creation of derivative research datasets and annotations

---

## License and Reuse

The dataset/resource files are released under the **Wittgenstein Apartment Academic & Derivative Research License v1.0 (WA-ADRL-1.0)**.

Without prior permission, the license permits non-commercial academic and research use, including:

- inspection and analysis;
- modification, annotation, normalization, mapping, translation, enrichment, and extension;
- creation and publication of derivative non-commercial research datasets, ontologies, mappings, and knowledge graphs;
- academic articles, theses, dissertations, conference papers, technical reports, and teaching use;
- non-commercial academic redistribution with attribution and the canonical DOI preserved.

**AI/model training requires prior written permission.**

**Commercial use requires prior written permission.**

See [`LICENSE.txt`](LICENSE.txt) for the complete terms.

---

## Scope and Known Limitations

Release v1.0 is a frozen research release. Known limitations are preserved and documented rather than silently normalized.

- **14 active Action Senses** are retained as known WordNet and/or goal-layer coverage exceptions.
- **151 active senses** are explicitly represented as Non-Goal Exceptions.
- Fully materialized per-character `ALLOWED`, `CONDITIONAL`, `HIGH_COST`, and `NOT_ALLOWED` assignments are not included as a character-instance dataset in v1.0.
- Some family naming and identifier inconsistencies remain documented limitations rather than being retrospectively reclassified.
- World Layer artifacts and interactive authoring interfaces are separate research directions and are not part of this v1.0 behavioral dataset release.

---

## Companion Paper

**Furkan Yaşar.**  
*Wittgenstein Apartment: A Sense-Level Behavioral Predicate Resource for Character-Relative Action Representation.*  
Author manuscript, 2026.

Repository copies:

- `paper/Wittgenstein_Apartment_Article_EN_Submission_Master_v1.0.pdf`
- `paper/Wittgenstein_Apartment_Article_EN_Submission_Master_v1.0.docx`

The dataset DOI above is the canonical citation for the v1.0 data release. A separate publication DOI may be added if the manuscript is later deposited as a preprint or published by a journal.

---

## Citation

Please cite the canonical Zenodo release:

> Yaşar, F. (2026). *Wittgenstein Apartment Behavioral Predicate Resource v1.0* (Version 1.0) [Data set]. Zenodo. https://doi.org/10.5281/zenodo.23015862

Machine-readable citation metadata are provided in [`CITATION.cff`](CITATION.cff).

---

## Author and Contact

**Furkan Yaşar**  
Independent Researcher · Istanbul, Türkiye  
Website: https://www.furkanyasar.me  
Correspondence: furkanyasar1924@gmail.com

---

## Release Status

**v1.0 — Public Research Resource**  
Release date: **2026-09-28**

Future corrections or extensions should be published as separately versioned releases rather than silently replacing the archived v1.0 record.
