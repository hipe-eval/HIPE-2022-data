# Newseye dataset

### Dataset profile

| <!-- -->    | <!-- -->    |
|-------------|-------------|
| **Original dataset**    |[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.4573313.svg)](https://doi.org/10.5281/zenodo.4573313)|
| **Document type**       | newspaper (mid-19C to mid 20C) |
| **Languages**           |Finnish, French, German, Swedish |
| **Annotation guidelines** |[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.4574199.svg)](https://doi.org/10.5281/zenodo.4574199)  |
| **Annotation tool**     |transkribus |
| **Original format and tagging scheme** |`.tsv, IOB` |
| **Annotations**          | NERC, EL (towards Wikidata, unknown dump) |
| **Version (used in HIPE-2022)**   | v1.0 |
| **Related publication**               |[A Multilingual Dataset for Named Entity Recognition, Entity Linking and Stance Detection in Historical Newspapers](https://dl.acm.org/doi/abs/10.1145/3404835.3463255)  |
| **License** | [![License: CC BY 4.0](https://img.shields.io/badge/License-CC_BY_4.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)|


### Entity tagset 

| Coarse-grained tagset | Fine-grained tagset | Nesting applies | Linking applies | 
| ------| ------------| --------| --------|
|PER    | PERS.author | yes     | yes     |
|LOC    | -           | yes     | yes     |
|ORG    | -           | yes     | yes     |
|HumanProd | -        | yes     | yes     |


### HIPE-2022 Tasks and Challenges

The *newseye* dataset can be used for:    

- **Tasks**: NERC-Coarse, NERC-Fine, NEL.
- **Challenges**: Multilingual Newspaper Coarse, Multilingual Newspaper Fine, Global Adaptation Coarse.


### Specificities and important information

- **Annotation guidelines:** mostly compatible with *hipe2020* dataset (except for the consideration of metonymic sense for entity linking, see participation guidelines p. 12).
- **Documents:** newseye documents corresponds to newspaper pages.
- **Document IDs:** document ID were added during HIPE-2022 conversion and are composed of: `split_language_docNumber (in file)`. 
- **Sentence splitting:** performed automatically on OCRed text (performances not perfect).
- **Entity linking and metonymic sense:** only one linking annotation exists per linked entity. 
- **Known glitches:**
	-  309 lines/tokens across all datasets in all languages contain the `###` subword marker.
	-  at conversion time, some missing tab (`\t`) and malformed Wikidata QID were manually corrected.


	
**HIPE-2022 v1.0 release notes**

-  Some parts (mainly tables) of some German documents seem to be missing annotations. This will be fixed for the next HIPE-2022 release. 

**HIPE-2022 v2.0 release notes**

- In the document metadata of each file, the value of `# hipe2022:document_id` has (sligtly) changed: the number in `train_[lg]_[nb]` is now the sequence number of the document in the file (it was by mistake the token sequential number in previous release). Newseye orginal data does not have document id, it is an addition from HIPE-2022.
- The train set of Newseye German data contained quite some parts with no annotations. Therefore we removed the following documents from the file `HIPE-2022-v2.0-newseye-train-de.tsv`: 
    - documents `train_de_3`, `train_de_4` and `train_de_7`, which do not have any NE annotation;
    - document `train_de_6`, which has less than 20 entities for 10,000 tokens.
    
Also, please note that `train_de_10` has a large chunk of ca. 100,000 non-annotated tokens at the beginning. 
	
	











