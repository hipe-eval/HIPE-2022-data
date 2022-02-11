# Newseye dataset

### Profile

| <!-- -->    | <!-- -->    |
|-------------|-------------|
| **Original dataset**    |[https://zenodo.org/record/4573313](https://zenodo.org/record/4573313)  |
| **Document type**       | newspaper (mid-19C to mid 20C) |
| **Languages**           |Finnish, French, German, Swedish |
| **Annotation guidelines** |[https://zenodo.org/record/4574199](https://zenodo.org/record/4574199)  |
| **Annotation tool**     |transkribus |
| **Original format and tagging scheme** |`.tsv, IOB` |
| **Annotations**          | NERC, EL (towards Wikidata, unknown dump) |
| **Version (used in HIPE-2022)**   | v1.0 |
| **Paper**               |[link](https://dl.acm.org/doi/abs/10.1145/3404835.3463255)  |
| **License** | [Creative Commons Attribution 4.0 International](https://creativecommons.org/licenses/by/4.0/legalcode)|


### Entity tagset 

| Coarse-grained tagset | Fine-grained tagset | Nesting applies | Linking applies | 
| ------| ------------| --------| --------|
|PER    | PERS.author | yes     | yes     |
|LOC    | -           | yes     | yes     |
|ORG    | -           | yes     | yes     |
|HumanProd | -        | yes     | yes     |


### HIPE-2022 Tasks and Challenges

The _newseye_ dataset can be used for:    

- **Tasks**: NERC-Coarse, NERC-Fine, NEL.
- **Challenges**: Multilingual Newspaper Coarse, Multilingual Newspaper Fine, Global Adaptation Coarse.


### Specificities and important information

- **Guidelines:** _newseye_ annotation guidelines are compatible with the HIPE-2020 impresso guidelines (except for the consideration of metonymic sense for entity linking, see below).
- **Documents:** _newseye_ documents corresponds to newspaper pages.
- **Document IDs:** document ID were added during HIPE-2022 conversion and are composed of: `split_language_docNumber (in file)`. 
- **Sentence splitting:** performed automatically on OCRed text (performances not perfect).
- **Entity linking and metonymic sense:** only one linking annotation exists per linked entity. 
- **Known glitches:**
	-  309 lines/tokens across all datasets in all languages contain the `###` subword marker.

	
	
	











