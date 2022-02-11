# LeTemps dataset

### Profile

| <!-- -->    | <!-- -->    |
|-------------|-------------|
| **Original dataset**    | updated soon  |
| **Document type**       | newspaper (mid-19C to mid 20C) |
| **Languages**           |French |
| **Annotation guidelines** | Aligned on Quaero guidelines, also refer to the paper.|
| **Annotation tool**     | brat |
| **Original format and tagging scheme** | brat format |
| **Annotations**          | NERC |
| **Version (used in HIPE-2022)**   | v1.0 |
| **Paper**               |[link](https://infoscience.epfl.ch/record/221391)  |


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

The _letemps_ dataset can be used for:    

- **Tasks**: NERC-Coarse, NERC-Fine.
- **Challenges**: Multilingual Newspaper Coarse, Multilingual Newspaper Fine, Global Adaptation Coarse.


### Specificities and important information

- **Guidelines:** _letemps_ annotation guidelines are compatible with the Quaero guidelines, and to some extent with HIPE-2020 impresso guidelines.
- **Documents:** _letemps_ documents corresponds to newspaper articles.
- **Sentence splitting:** performed automatically on OCRed text (performances not perfect).

