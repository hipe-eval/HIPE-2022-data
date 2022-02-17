# LeTemps dataset

### Dataset profile

| <!-- -->    | <!-- -->    |
|-------------|-------------|
| **Original dataset**    | [https://zenodo.org/record/6046853](https://zenodo.org/record/6046853)  |
| **Document type**       | newspaper (mid-19C to mid 20C) |
| **Languages**           |French |
| **Annotation guidelines** | Aligned on Quaero guidelines, see publication. |
| **Annotation tool**     | brat |
| **Original format and tagging scheme** | brat format |
| **Annotations**          | NERC |
| **Version (used in HIPE-2022)**   | v1.0 |
| **Related publication**               |[Diachronic evaluation of NER systems on old newspapers](https://infoscience.epfl.ch/record/221391)  |
| **License** | [![License: CC BY-NC-SA 4.0](https://img.shields.io/badge/License-CC_BY--NC--SA_4.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc-sa/4.0/) |

### Entity tagset 

| Coarse-grained tagset | Fine-grained tagset | Nesting applies | Linking applies | 
| ------| ------------| --------| --------|
| pers  | pers.ind    | yes     | no      |
|       | pers.coll   |  yes     | no     |
| loc   | loc.adm.town |  yes     | no    |
|       | loc.adm.reg |  yes     | no    |
|       | loc.adm.nat |  yes     | no    |
|       | loc.adm.sup |  yes     | no    |
|       | loc.phys.geo |  yes     | no    |
|       | loc.phys.hydro |  yes     | no    |
|       | loc.oro |  yes     | no    |
|       | loc.fac |  yes     | no    |
|       | loc.add.phys |  yes     | no    |
|       | loc.add.elec |  yes     | no    |
|       |  loc.unk |  yes     | no    |




### HIPE-2022 Tasks and Challenges

The *letemps* dataset can be used for:    

- **Tasks**: NERC-Coarse, NERC-Fine.
- **Challenges**: Multilingual Newspaper Coarse, Multilingual Newspaper Fine, Global Adaptation Coarse.


### Specificities and important information

- **Guidelines:** letemps annotation guidelines are compatible with the Quaero guidelines, and to some extent with HIPE-2020 impresso guidelines.
- **Documents:** *letemps* documents corresponds to newspaper articles.
- **Sentence splitting:** performed automatically on OCRed text (performances not perfect).
- **About person function and title annotations**: *letemps* dataset is very similar to *hipe2020* and *newseye*.  For the type PERS a noticeable difference is that *letemps* annotations do not include function (e.g. *general, mayor*) in person names, but do include titles (e.g. *M.*, *Madame*). Both *hipe2020* and *newseye* include functions and titles as part of person name annotations.

