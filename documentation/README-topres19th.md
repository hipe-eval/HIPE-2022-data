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

| Coarse-grained tagset | Fine-grained tagset | Nesting applies | Linking applies | Present in HIPE 2022 data |
| ------| ------------| --------| --------| -------------|
|LOC    | _        | no      | yes     | yes |
|BUILDING  | -     | no      | yes     | yes |
| STREET  | -      | no      | yes     | yes |
| ALIEN | -        | no      | yes     | no |
| OTHER | -        | no      | yes     | no |
| FICTION | -      | no      | yes     | no |

Note: Due to data sparseness the tags ALIEN, OTHER and FICTION and their corresponding annotations (6 in total for the training/dev data) were removed in HIPE 2022.

TopRes19th toponym classes correspond to (descriptions taken from the README of the original dataset release v2):

* `BUILDING`: names of buildings, such as the 'British Museum'.
* `STREET`: streets, roads, and other odonyms, such as 'Great Russell St'.
* `LOC`: any other real world places regardless of type or scale, such as 'Bloomsbury', 'London' or 'Great Britain'.
* `ALIEN`: extraterrestrial locations, such as 'Venus'.
* `FICTION`: fictional or mythical places, such as 'Hell'.
* `OTHER`: other types of entities with coordinates, such as events, like the 'Battle of Waterloo'.


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

