# TopRes19th dataset

### Dataset profile

| <!-- -->    | <!-- -->    |
|-------------|-------------|
| **Original dataset**    |[https://doi.org/10.23636/r7d4-kw08](https://doi.org/10.23636/r7d4-kw08)  |
| **Document type**       | newspaper (19C) |
| **Languages**           | English |
| **Annotation guidelines** | see README in original release and below |
| **Annotation tool**     | [INCEpTION](https://inception-project.github.io/) |
| **Original format and tagging scheme** | WebAnno 2.3 |
| **Annotations**          | NERC, EL (towards Wikipedia) |
| **Version (used in HIPE-2022)**   | v2 |
| **Related publication**               |[A Dataset for Toponym Resolution in Nineteenth-Century English Newspapers](https://openhumanitiesdata.metajnl.com/articles/10.5334/johd.56/)  |
| **License**              |[CC BY-NC-SA 4.0 Attribution-NonCommercial-ShareAlike](https://creativecommons.org/licenses/by-nc-sa/4.0/)  |


### Entity tagset 

The topres19th dataset focuses exclusively on toponyms.

| Coarse-grained tagset | Fine-grained tagset | Nesting applies | Linking applies | 
| ------| ------------| --------| --------|
|LOC    | _        | no      | yes     |
|BUILDING  | -     | no      | yes     |
| STREET  | -      | no      | yes     |
| ALIEN | -        | no      | yes     |
| OTHER | -        | no      | yes     |
| FICTION | -      | no      | yes     |


Type explanation (from original release guidelines):

- `LOC`:  Refers to a real world place regardless of scale (region, city, neighborhood) with the exception of the additional, separate categories listed below;
- `BUILDING`: Names of buildings (e.g. schools, hospitals, factories, palaces, etc.). Optional link to Wikipedia article if it exists.
-  `STREET`: Streets, squares, etc. Optional link to Wikipedia article if it exists.
-  `ALIEN`: Extraterrestrial locations (e.g. the moon). Optional link to Wikipedia article if it exists.
-  `OTHER`: Others, as in famous trees (https://en.wikipedia.org/wiki/Lone_Cypress) or battlefields (https://en.wikipedia.org/wiki/Battle_of_Waterloo). Optional link to Wikipedia article if it exists.
-  `FICTION`: If it is a fictional/mythical place (e.g. Lilliput). Optional link to Wikipedia article if it exists.


### HIPE-2022 Tasks and Challenges

The *topres19th* dataset can be used for:    

- **Tasks**: NERC-Coarse,  NEL.
- **Challenges**: Multilingual Newspaper Coarse, Global Adaptation Coarse.


### Specificities and important information
 
- **Documents:** *topres19th* documents corresponds to newspaper articles.
- **Metadata:** *topres19th* has rich metadata, reported in the HIPE-2022 converted files.
- **Sentence splitting:** performed automatically on OCRed text (performances not perfect).
- **Entity linking and metonymic sense:** originally towards Wikipedia, mapped to Wikidata during HIPE-2022 conversion.
- **Known glitches:**
	-  none at present

