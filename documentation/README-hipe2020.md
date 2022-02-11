# HIPE-2020 dataset

### Dataset profile

| <!-- -->    | <!-- -->    |
|-------------|-------------|
| **Original dataset**    | UPDATE ZENODO LINK |
| **Document type**       | newspaper (mid-19C to mid 20C) |
| **Languages**           | English, French, German |
| **Annotation guidelines** |[impresso HIPE-2020 NE Annotation Guidelines](https://zenodo.org/record/3585750)  |
| **Annotation tool**     | [neat](https://github.com/qurator-spk/neat/blob/master/README.md#22-data-format) |
| **Original format and tagging scheme** |`.tsv, IOB` |
| **Annotations**          | NERC, EL (towards Wikidata, dump of [2019.11.13](https://files.ifi.uzh.ch/cl/siclemat/impresso/clef-hipe-2020/wikidata-2019-11-13.nt.bz2) ) |
| **Version (used in HIPE-2022)**   | v1.4 |
| **Paper**               |[Overview of CLEF-HIPE-2020](https://dl.acm.org/doi/abs/10.1007/978-3-030-58219-7_21), [Extended Overview of CLEF-HIPE-2020](https://infoscience.epfl.ch/record/281054)|
| **License** | UPDATE |


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

- **Tasks**: NERC-Coarse,  NEL.
- **Challenges**: Multilingual Newspaper Coarse (MNC), Multilingual Newspaper Fine (MNF), Global Adaptation Coarse (GAC).


### Specificities and important information

- **Documents:** *hipe2020* documents corresponds to newspaper articles.
- **Sentence splitting:** performed automatically on OCRed text using pySBD (performances not perfect).
- **Metonymic sense:** literal and metonymic annotations are in separated columns. 
- **Known glitches:**
	 - none at present

**HIPE-2022 v1.0 release notes**
