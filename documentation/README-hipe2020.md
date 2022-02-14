# HIPE-2020 dataset

### Dataset profile

| <!-- -->    | <!-- -->    |
|-------------|-------------|
| **Original dataset**    | [![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.6046853.svg)](https://doi.org/10.5281/zenodo.6046853) |
| **Document type**       | newspaper (mid-19C to mid 20C) |
| **Languages**           | English, French, German |
| **Annotation guidelines** |[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.3585750.svg)](https://doi.org/10.5281/zenodo.3585750)|
| **Annotation tool**     | [INCEpTION](https://inception-project.github.io/) |
| **Original format and tagging scheme** |`.tsv, IOB` |
| **Annotations**          | NERC, EL (towards Wikidata, dump of [2019.11.13](https://files.ifi.uzh.ch/cl/siclemat/impresso/clef-hipe-2020/wikidata-2019-11-13.nt.bz2) ) |
| **Version (used in HIPE-2022)**   | `v1.4` |
| **Related publication**               |[Overview of CLEF-HIPE-2020](https://dl.acm.org/doi/abs/10.1007/978-3-030-58219-7_21), [Extended Overview of CLEF-HIPE-2020](https://infoscience.epfl.ch/record/281054)|
| **License** | [![License: CC BY-NC-SA 4.0](https://img.shields.io/badge/License-CC_BY--NC--SA_4.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc-sa/4.0/)|


 

### Entity tagset 

| Coarse-grained tagset | Fine-grained tagset | Nesting applies | Linking applies | 
| ------| ------------| --------| --------|
| pers | pers.ind | yes     | yes     |
|  | pers.coll | yes     | yes     |
|  | pers.ind.articleauthor | yes     | yes     |
| org | org.adm | yes     | yes     |
|  | org.ent | yes     | yes     |
|  | org.ent.pressagency | yes     | yes     |
| prod | prod.media | yes     | yes     |
|  | prod.doctr | yes     | yes     |
| time | time.date.abs | yes     | yes     |
| loc | loc.adm.town | yes     | yes     |
| | loc.adm.reg | yes     | yes     |
|  | loc.adm.nat | yes     | yes     |
|  | loc.adm.sup | yes     | yes     |
|  | loc.phys.geo | yes     | yes     |
|  | loc.phys.hydro | yes     | yes     |
|  | loc.phys.astro | yes     | yes     |
|  | loc.oro | yes     | yes     |
|  | loc.fac | yes     | yes     |
|  | loc.add.phys | yes     | yes     |
|  | loc.add.elec | yes     | yes     |
|  | loc.unk | yes     | yes     |


### HIPE-2022 Tasks and Challenges

The *hipe2020* dataset can be used for:    

- **Tasks**: NERC-Coarse, NERC-Fine, NEL.
- **Challenges**: Multilingual Newspaper Coarse, Multilingual Newspaper Fine, Global Adaptation Coarse.


### Specificities and important information

- **Annotation guidelines:** mostly compatible with *letemps* and *newseye* datasets.
- **Documents:** *hipe2020* documents corresponds to newspaper articles.
- **Train set:** for this dataset, there is no training set. Only a dev set that is representative for the test set in terms of newspapers and periods.
- **Sentence splitting:** performed automatically on OCRed text using pySBD (performances not perfect).
- **Metonymic sense:** literal and metonymic annotations are in separated columns. 
- **Known glitches:**
	 - some negative offsets in Partial are wrong/off

**HIPE-2022 v1.0 release notes**
