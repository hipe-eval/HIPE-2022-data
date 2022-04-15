# AjMC dataset

### Dataset profile

| <!-- -->    | <!-- -->    |
|-------------|-------------|
| **Original dataset**    | not available yet |
| **Document type**       | commentary (19C) |
| **Languages**           | English, French, German |
| **Annotation guidelines** | [link](https://doi.org/10.5281/zenodo.6368101) |
| **Annotation tool**     | [INCEpTION](https://inception-project.github.io/) |
| **Original format and tagging scheme** |`.tsv, IOB` |
| **Annotations**          | NERC, EL (towards Wikidata) |
| **Version (used in HIPE-2022)**   | `v0.2` |
| **Related publication**               | – |
| **License** | [![License: CC BY 4.0](https://img.shields.io/badge/License-CC_BY_4.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/) |


### Description

This dataset consists of NE-annotated historical commentaries in the field of Classics, and was created in the context of the [Ajax MultiCommentary project](https://mromanello.github.io/ajax-multi-commentary/). We annotated a set of Named Entities (NEs) of domain-specific interest, according to some newly-developed [annotation guidelines](https://doi.org/10.5281/zenodo.6368101). Such NEs feature a few domain-specific entity types such as works, material objects (e.g. manuscripts) and bibliographic references, in addition to more universal entities like persons, locations and organizations. Entity linking is performed against [Wikidata](http://wikidata.org/).

## Composition

[Commentaries](https://en.wikipedia.org/wiki/Commentary_(philology)) are a specific genre of scholarly publications that focus on one specific text (or part of it) and aim to provide the reader with in-depth information to understand this text. From an information extraction point of view, commentaries are very rich in terms of NEs as they contain mentions of mythological characters (heroes, gods, etc.), scholars, works of primary and secondary literature – all this in a style which favours conciseness and makes abundant usage of abbreviations.

For this dataset, we annotated randomly selected pages from three 19th century commentaries written in German, English and French about an Ancient Greek tragedy by Sophocles, the *Ajax*. As to the quality of the OCR, we used the output of the OCR engine Tesseract (see [this paper](https://arxiv.org/abs/2110.06817) for further details on OCR quality evaluation of these commentaries). An example of a commentary page is shown in [this image](ajmc-commentary-layout-regions.png).


### Entity tagset

| Coarse-grained tagset | Fine-grained tagset | Nesting applies | Linking applies | 
| ------| ------------| --------| --------|
| pers | pers.author | yes     | yes\*   |
|  | pers.editor | yes     | yes\*     |
|  | pers.myth | yes     | yes\*     |
|  | pers.other | yes     | yes\*     |
| work | work.primlit | yes | yes\* |
|  | work.seclit | yes | yes\* |
|  | work.fragm | yes | yes\* |
| loc | - | yes | yes\* |
| object | object.manuscr | yes | no |
|  | object.museum | yes | no |
| date | - | yes | no |
| scope | - | yes | no |


**\*** unless token flagged as `InSecondaryReference` (flags are contained in the `MISC` column).

### HIPE-2022 Tasks and Challenges

The *ajmc* dataset can be used for:    

- **Tasks**: NERC-Coarse, NERC-Fine, NEL.
- **Challenges**: Multilingual Classical Commentary Challenge, Global Adaptation Challenge.


### Specificities and important information

- **Documents:** *ajmc* documents correspond to pages of classical commentaries (only pages contanining introduction/preface or commentary sections were selected).
- **Sentence splitting:** annotated manually (see Guidelines, section 4).

### Data release notes

**HIPE-2022-data v2.1**
- Thorough data cleaning: added missing OCR transcriptions, added some missing Wikidata IDs, fixed some erroneous entity types, added some missing mentions.

**HIPE-2022-data v2.0**
- This release contains dev and train set for all languages (EN, DE, FR). 
- It also includes the mappings of OCR/gold transcript for those entities that are affected by OCR noise. These mappings will be of particurlar use for entity linking, where the impact of OCR noise on short entities is much higher than on other entities. These mappings are contained in three files named `ajmc-entity-ocr-correction-{LANG}.tsv` and located in the corpus' root directory. Each file contains the following columns:
    - `entity_surface`: entity surface form as in the original OCR 
    - `gold_transcript`: manual transcription (of entity surface form)
    - `levenshtein_norm`: normalised levennshtein distance between `entity_surface` and `gold_transcript`
    - `entity_fine_type`: fine-grained NE type
    - `wikidata_id`: entity's Wikidata ID when entity is not NIL (otherwise empty value)
    - `frequency`: the number of times that the same OCR error pattern occurs in dev and train sets (e.g. the abbreviation of Aeschylus' name is wrongly recognised Aſch. -> Äſch. 15 times in the DE corpus).

**HIPE-2022-data v1.0**

- This release contains only a data sample (EN, DE). Train and dev sets will be included in the next HIPE-2022 release.

### Domain specificity

This dataset raises some challenges for NER and EL that are related to its domain-specific nature: 

- *data sparsity*: the fact that some entity types are under-represented in this dataset (e.g. `date`) calls for approaches to deal with data sparsity (e.g. data augmentation, meta-learning);
- *dependance on context*: the overall context of a commentary has a direct impact on how entity mentions are crafted, especially in terms of conciseness of the referents. This is especially relevant for EL as capturing the global document context becomes essential to select the correct linking candidate. To give a concrete example, a scholar commenting on a tragedy by Sophocles will probably omit the ancient author's name when referring to other works by Sophocles. To refer to a line of Sophocles' play *Philoctetes* she may write "*Ph.* 100" instead of the more easily intelligible "Soph. *Philoct.* 110".

### Related resources

**Hucitlib Knowledge Base.** Commentators make abundant use of very concise abbreviations when referring e.g. to ancient authors (`pers.author`) and their works (`work.primlit`). Such abbreviations constitute a substantial challenge, especially for entity linking. An external resource that can be used in this respect is the [`hucitlib` knowledge base](https://hucitlib.readthedocs.io/) which is partially linked to Wikidata and provides abbreviations and variant names/titles for classical authors and their works.