# SoNAR dataset

### Dataset profile

| <!-- -->    | <!-- -->    |
|-------------|-------------|
| **Original dataset**    | not available yet  |
| **Document type**       | newspaper (mid-19C to mid 20C) |
| **Languages**           | German |
| **Annotation guidelines** |[https://zenodo.org/record/5116015#.YgTt0N_MKUk](https://zenodo.org/record/5116015#.YgTt0N_MKUk)  |
| **Annotation tool**     | [neat](https://github.com/qurator-spk/neat/blob/master/README.md#22-data-format) |
| **Original format and tagging scheme** |`.tsv, IOB` |
| **Annotations**          | NERC, EL (towards Wikidata, unknown dump) |
| **Version (used in HIPE-2022)**   | v1.0 |
| **Paper**               |[link](https://doi.org/10.1515/9783110691597-012)  |
| **License** | [Creative Commons Attribution 4.0 (CC-BY)](https://creativecommons.org/licenses/by/4.0/)|


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
- **Challenges**: Multilingual Newspaper Coarse (MNC), Multilingual Newspaper Fine (MNF), Global Adaptation Coarse (GAC).


### Specificities and important information

- **Documents:** sonar documents corresponds to newspaper articles (UPDATE)
- **Sentence splitting:** performed automatically on OCRed text (performances not perfect) (UPDATE).
- **Entity linking and metonymic sense:** only one linking annotation exists per linked entity. 
- **Known glitches:**
	 - none at present

**HIPE-2022 v1.0 release notes**

- EL annotation are not present in current sonar file and will be added in the next release.