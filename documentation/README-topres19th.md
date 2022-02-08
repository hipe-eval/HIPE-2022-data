# TopRes19th dataset

### Profile

| <!-- -->    | <!-- -->    |
|-------------|-------------|
| **Original dataset**    |[https://doi.org/10.23636/b1c4-py78](https://doi.org/10.23636/b1c4-py78)  |
| **Document type**       | newspaper (19C) |
| **Languages**           | English |
| **Annotation guidelines** | see README in original release and below |
| **Annotation tool**     | INCEpTION |
| **Original format and tagging scheme** | WebAnno 2.3 |
| **Annotations**          | NERC, EL (towards Wikipedia) |
| **Version (used in HIPE-2022)**   | v2 |
| **Paper**               |[link](https://openhumanitiesdata.metajnl.com/articles/10.5334/johd.56/)  |


### Entity tagset 

The _topres19th_ dataset focuses exclusively on toponyms.

| Coarse-grained tagset | Fine-grained tagset | Nesting applies | Linking applies | 
| ------| ------------| --------| --------|
|LOC    | _        | no      | yes     |
|BUILDING  | -     | no      | yes     |
| STREET  | -      | no      | yes     |
| ALIEN | -        | no      | yes     |
| OTHER | -        | no      | yes     |
| UNKNOWN | -      | no      | yes?    |
| FICTION | -      | no      | yes     |


Type explanation (from original release guidelines):

- `LOC`:  Refers to a real world place regardless of scale (region, city, neighborhood) with the exception of the additional, separate categories listed below;
- `BUILDING`: Names of buildings (e.g. schools, hospitals, factories, palaces, etc.). Optional link to Wikipedia article if it exists.
-  `STREET`: Streets, squares, etc. Optional link to Wikipedia article if it exists.
-  `ALIEN`: Extraterrestrial locations (e.g. the moon). Optional link to Wikipedia article if it exists.
-  `OTHER`: Others, as in famous trees (https://en.wikipedia.org/wiki/Lone_Cypress) or battlefields (https://en.wikipedia.org/wiki/Battle_of_Waterloo). Optional link to Wikipedia article if it exists.
-  `UNKNOWN`: If the location has no Wikipedia entry OR if you cannot determine what place it is, but are confident that it is a place. No link to Wikipedia.
-  `FICTION`: If it is a fictional/mythical place (e.g. Lilliput). Optional link to Wikipedia article if it exists.


### HIPE-2022 Tasks and Challenges

The _topres19th_ dataset can be used for:    

- **Tasks**: NERC-Coarse,  NEL.
- **Challenges**: Multilingual Newspaper Coarse, Global Adaptation Coarse.


### Specificities and important information

- **Guidelines:** topres19th annotation guidelines are ad hoc. 
- **Documents:** topres19th documents corresponds to newspaper articles.
- **Metadata:** topres19th has rich metadata, reported in the HIPE-2022 converted files.
- **Sentence splitting:** performed automatically on OCRed text (performances not perfect).
- **Entity linking and metonymic sense:** originally towards Wikipedia, mapped to Wikidata during HIPE-2022 conversion.
- **Known glitches:**
	-  ...

