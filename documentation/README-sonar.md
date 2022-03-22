# SoNAR dataset

### Dataset profile

| <!-- -->    | <!-- -->    |
|-------------|-------------|
| **Original dataset**    | DOI not available yet  |
| **Document type**       | newspaper (mid-19C to mid 20C) |
| **Languages**           | German |
| **Annotation guidelines** |[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.5116015.svg)](https://doi.org/10.5281/zenodo.5116015)  |
| **Annotation tool**     | [neat](https://github.com/qurator-spk/neat/blob/master/README.md#22-data-format) |
| **Original format and tagging scheme** |`.tsv, IOB` |
| **Annotations**          | NERC, EL  |
| **Version (used in HIPE-2022)**   | v1.0 with many corrections from the HIPE 2022 team|
| **Related publication**               |[Named Entity Linking mit Wikidata und GND](https://doi.org/10.1515/9783110691597-012)  |
| **License** | [![License: CC BY 4.0](https://img.shields.io/badge/License-CC_BY_4.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)|


### Entity tagset 

| Coarse-grained tagset | Fine-grained tagset | Nesting applies | Linking applies | 
| ------| ------------| --------| --------|
|PER    | -  | no     | yes     |
|LOC    | -           | no     | yes     |
|ORG    | -           | no     | yes     |

N.B. SoNAR guidelines indicate other possible entity types but they are not present in the data.

### HIPE-2022 Tasks and Challenges

The *sonar* dataset can be used for:    

- **Tasks**: NERC-Coarse,  NEL.
- **Challenges**: Multilingual Newspaper Coarse, Global Adaptation Coarse.


### Specificities and important information

- **Documents:** sonar documents corresponds to newspaper articles (UPDATE)
- **Train set:** for this dataset, there is no training set. Only a dev set that is representative for the test set in terms of newspapers and periods.
- **Sentence splitting:** performed automatically on OCRed text (performances not perfect) (UPDATE).
- **Entity linking and metonymic sense:** only one linking annotation exists per linked entity. 
- **Known glitches:**
    - no embedded entities (the guidelines specify them), which sometimes can lead to inconsistent annotations for complex entities (e.g. company names with a person or location inside) 
    - the annotation guidelines have not been strictly followed in the original version v1.0
    - the original NEL information was not manually disambiguated; the HIPE 2022 team corrected them according to our understanding of the intended SoNAR annotations. 
    - the original data contained discontinuous NER spans, probably due to retokenization that treated all punctuation symbols as separate tokens (including abbreviation periods)

### Data release notes

**HIPE-2022 v2.0 release notes**
- EL annotation is now part of the release.
- Thorough revision of NER and NEL annotation have been done by the HIPE team.
- Due to time limits, we could not revise all dev set pages completely to the end of the page. The material that could not be revised was removed from the dev set. Meaning, although there is a bit less material in the dev set now, it is fully revised.

**HIPE-2022 v1.0 release notes**

- EL annotation are not present in current sonar file and will be added in the next release.