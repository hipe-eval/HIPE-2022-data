# HIPE-2022-data
This repository contains the data for the [HIPE 2022 shared task](https://hipe-eval.github.io/HIPE-2022/).

### About

HIPE-2022 is a [CLEF 2022 Evaluation Lab](https://clef2022.clef-initiative.eu/) which focuses on **named entity recognition and classification (NERC) and entity linking (EL) in historical documents** covering the period from the 18th to the 20th century and featuring several languages.    

Following the first [CLEF-HIPE-2020](https://impresso.github.io/CLEF-HIPE-2020) evaluation lab on historical newspapers in three languages, HIPE-2022 features more diverse datasets and aims at confronting systems with the challenges of **dealing with more languages, learning domain-specific entities, and adapting to diverse annotation tag sets**. The main objective is to gain new insights into the _transferability_ of named entity processing approaches across languages, time periods, document types, and annotation tag sets.

Please refer to:
- the [website](https://hipe-eval.github.io/HIPE-2022/) for general information on the shared task and registration (open until Friday, 22 April 2022)
- the [participation guidelines]() for detailed information on the tasks, datasets and evaluation settings.

### Datasets

HIPE-2022 is based on a set of different NE-annotated datasets, assembled and prepared for the purpose of the shared task.

The datasets are composed of historical newspapers and classic commentaries covering ca. 200 years, feature several languages and different NE tag sets and annotation schemes. They originate from several European cultural heritage projects,  from HIPE organisers’ previous research project, and from the previous HIPE-2020 campaign. Some are already published, others are released for the first time for this shared task.

Here is an overview of the datasets; a generic description is provided below, and a detailed description of each dataset is available in the dedicated README.



| Project | Dataset alias | Document type | Languages | Main types | Suitable for | README |
|---------|---------|---------------|-----------| ---------------|---------------|---------------|
| AjMC | ajmc  | classical commentaries | de, fr, en | | NERC and EL |[link](data/ajmc/README.md) |
| [CLEF-HIPE-2020](https://impresso.github.io/CLEF-HIPE-2020) | hipe2020 | historical newspapers | de, fr, en | | NERC and EL |[link](data/hipe2020/README.md) |
| LeTemps | letemps  | historical newspapers    | fr | |NERC  | [link](data/letemps/README.md) |
| [Living with Machines](https://livingwithmachines.ac.uk/) | topRes19th | historical newspapers | en | | NERC and EL |[link](data/topRes19th/README.md) |
| [NewsEye](https://www.newseye.eu/)| newseye |  historical newspapers | de, fi, fr, sv | |NERC and EL | [link](data/newseye/README.md) | 
| [SoNAR](https://sonar.fh-potsdam.de/) | sonar  | historical newspapers    | de | |NERC and EL | [link](data/sonar/README.md) |

​    

These datasets are prepared for the shared task as follows:

- conversion to the HIPE format (with correction of data inconsistencies and metadata consolidation);
- rearrangement or composition of train and dev splits.



#### HIPE format and tagging scheme

HIPE format is a simple tab-separated verticalized textual format using an [IOB]( https://en.wikipedia.org/wiki/Inside–outside–beginning_(tagging)) tagging scheme (inside-outside-beginning format), in a similar fashion to that of the [CoNLL-U](https://universaldependencies.org/format.html) format. 





#### Naming conventions and directory structure



#### Mapping from original to HIPE-2022



### Additional resources



