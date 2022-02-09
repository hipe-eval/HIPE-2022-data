# HIPE-2022-data

[HIPE 2022 shared task](https://hipe-eval.github.io/HIPE-2022/) is a [CLEF 2022 Evaluation Lab](https://clef2022.clef-initiative.eu/) which focuses on the tasks of **named entity recognition and classification (NERC) and entity linking (EL) in multilingual historical documents**. Following the first [CLEF-HIPE-2020](https://impresso.github.io/CLEF-HIPE-2020) evaluation lab on historical newspapers in three languages, HIPE-2022 is based on diverse datasets and aims at confronting systems with the challenges of **dealing with more languages, learning domain-specific entities, and adapting to diverse annotation tag sets**. The main objective is to gain new insights into the _transferability_ of named entity processing approaches across languages, time periods, document types, and annotation tag sets.

Please refer to:    
- :computer: the [website](https://hipe-eval.github.io/HIPE-2022/) for general information on the shared task and registration;    
- :notebook: the [participation guidelines]() for detailed information on the tasks, datasets and evaluation settings.

**CONTENTS**

- [Primary datasets](README.md#primary-datasets)    
- [HIPE-2022 releases (structure, format, tagging scheme)](README.md#HIPE-2022-releases)   
- [HIPE-2022 NE annotation types](README.md#HIPE-2022-NE-annotation-types)
- [Entity tagsets](README.md#HIPE-2022-primary-dataset-entity-tagsets)      
- [Primary datasets to HIPE-2022: mapping overview](README.md#Primary-datasets-to-HIPE-2022:-mapping-overview)
- [References](README.md#acknowledgments)
- [Acknowledgments](README.md#acknowledgments)    



## Primary datasets

HIPE-2022 primary datasets are composed of historical newspapers and classic commentaries covering ca. 200 years, feature several languages and different entity tag sets and annotation schemes. They originate from several European cultural heritage projects, from HIPE organisers’ previous research project, and from the previous HIPE-2020 campaign. Some are already published, others are released for the first time for HIPE-2022.

| Dataset alias | README | Document type | Languages |  Suitable for | Project | 
|---------|---------|---------------|-----------| ---------------|---------------|
| ajmc       | [link](documentation/README-ajmc.md)  | classical commentaries | de, fr, en | NERC and EL | AjMC |
| hipe2020   | [link](documentation/README-hipe2020.md)| historical newspapers | de, fr, en | NERC and EL | [CLEF-HIPE-2020](https://impresso.github.io/CLEF-HIPE-2020)|
| letemps    | [link](documentation/README-letemps.md) | historical newspapers    | fr | NERC  | LeTemps |
| topres19th | [link](documentation/README-topres19th.md) | historical newspapers | en | NERC and EL |[Living with Machines](https://livingwithmachines.ac.uk/) |
| newseye    | [link](documentation/README-newseye.md)|  historical newspapers | de, fi, fr, sv | NERC and EL |  [NewsEye](https://www.newseye.eu/) | 
| sonar      | [link](documentation/README-sonar.md) | historical newspapers  | de | NERC and EL |  [SoNAR](https://sonar.fh-potsdam.de/)  |

**Licenses:** The primary datasets which compose HIPE-2022 data are released under different licenses, please refer to each dataset specific README.


## HIPE-2022 releases 

A HIPE-2022 release corresponds to a single package composed of neatly structured and homogeneously formatted datasets of diverse origins. Primary datasets undergo the following preparation steps:
- conversion to the HIPE format (with correction of data inconsistencies and metadata consolidation);
- rearrangement or composition of train and dev splits.

### Directory structure and naming conventions

HIPE-2022 data directory is organised per HIPE release version, dataset and language, as follows:

```
data
└── vx.x
  └── dataset1
  │   ├── lg1
  │   │   ├── HIPE-2022-vx.x-dataset1-train-lg1.tsv
  │   │   ├── HIPE-2022-vx.x-dataset1-dev-lg1.tsv
  │   └── lg2
  │       ├── HIPE-2022-vx.x-dataset2-train-lg2.tsv
  │       ├── HIPE-2022-vx.x-dataset2-dev-lg2.tsv
  └── dataset2
  │   ├── lg1
  │   │   ├── HIPE-2022-vx.x-dataset2-train-lg1.tsv
  │   │   ├── ...
  └── ...
```

**Files and file naming conventions**

- Training and development datasets consist of UTF-8, tab-separated-values files.
- There is one `.tsv` file per dataset, language and dataset split.
- Files contain information needed for all tasks (NERC-Coarse, NERC-Fine, and entity linking).
- Files are named according to this schema:
  `HIPE-2022-<hipeversion>-<dataset-alias>-<split>-<language>.tsv` where `# split = sample|train|dev|dev2|test|`. For example, the file `HIPE-2022-v1.0-newseye-dev-sv.tsv` contains NE-annotated documents of the Swedish part of the newseye corpus which are meant as development set, in HIPE format and from HIPE-2022 release v1.0. 
     

**Versioning**  

- HIPE-2022 release are versioned with a two-part version number (Major.Minor) which is part of 1) the data directory structure and 2) the filename of each file.     
- Each HIPE-2022 release has an equivalent git repository release, with release notes.    
- The version of each specific dataset is mentioned in document metadata (see below).    


### HIPE format and tagging scheme

HIPE format is a simple tab-separated column textual format using an [IOB]( https://en.wikipedia.org/wiki/Inside–outside–beginning_(tagging)) tagging scheme (inside-outside-beginning format), in a similar fashion to that of the [CoNLL-U](https://universaldependencies.org/format.html) format. 

**File structure**

Files encode annotations needed for all tasks (NERC-Coarse, NERC-Fine and NEL) and contain the following lines:   

- empty lines, which mark the boundaries between documents;    
- comment lines, which give further information and start with the character `#`;    
- annotated lines, which contain a token followed by tab-separated annotations.    

A file contains all the documents of one dataset/language/split. Documents are separated with empty lines and are preceded with several metadata comment lines. The notion of document varies from one dataset to another, please refer to dataset-specific READMEs.

**Document metadata**

Primary datasets provide different document metadata, with different granularity. This information is kept in HIPE-2022 files in the form of "metadata blocks". HIPE-2022 metadata blocks encode as much information as necessary to ensure that each document is 'self-contained' with respect to HIPE-2022 settings.

Metadata blocks uses name spacing to distinguish between mandatory HIPE-2022 metadata and dataset-specific (optional) metadata:


```
# hipe2022:document_id     = [value: identifier for the document inside a dataset]
# hipe2022:date            = [value: original document publication date (YYYY-MM-DD, with YYYY-01-01 if month or date are not available)]
# hipe2022:language        = [value: iso two-letter language code]
# hipe2022:dataset         = [value: dataset alias as in file name]
# hipe2022:original_source = [value: path to source file in original dataset release] 
# DATASET:doi              = [value: DOI url of primary dataset release (if available)]   
# DATASET:version          = [value: version of primary dataset as indicated in latest release]   
# to be continued....
```

**Columns**

Each annotated line consists of 10 columns:

- `TOKEN`: the annotated token.
- `NE-COARSE-LIT`: the coarse type (IOB-type) of the entity mention token, according to the literal sense.
- `NE-COARSE-METO`: the coarse type (IOB-type) of the entity mention token, according to the metonymic sense.
- `NE-FINE-LIT`: the fine-grained type (IOB-type.subtype.subtype) of the entity mention token, according to the literal sense.
- `NE-FINE-METO`: the fine-grained type (IOB-type.subtype.subtype) of the entity mention token, according to the metonymic sense.
- `NE-FINE-COMP`: the component type of the entity mention token.
- `NE-NESTED`: the coarse type of the nested entity (if any).
- `NEL-LIT`: the Wikidata Qid of the literal sense, or `NIL`.
- `NEL-METO`: the Wikidata Qid of the metonymic sense, or `NIL`.
- `MISC`: a flag which can take the following values:
    - `NoSpaceAfter`, to indicate the absence of white space after the token.
    - `EndOfLine`, to indicate the end of a layout line.
    - `EndOfSentence`, to indicate the end of a sentence.
    - `Partial-START:END`, to indicate the character on/offsets of mentions that do not cover the full token (esp. for German compounds).

Non-specified values are marked by the underscore character (`_`). 

Since they were created according to different annotation schemes, datasets do not systematically include all columns. Applicable columns for a dataset are specified in each document metadata. When a column does not apply for a specific dataset, all its values are `_`.     


## HIPE-2022 NE annotation types

HIPE-2022 annotation scheme originates from the CLEF-HIPE-2020 shared task and contains detailed named entity annotation types (reflected in the IOB file columns and presented above). All HIPE-2022 primary datasets do not necessarily have all annotation types. 

Datasets and their annotation types:


| NE annotation type | ajmc | hipe2020 | letemps  | topres19th | newseye | sonar |
|---------|---------|---------|---------|---------|---------|---------|
|  NE-COARSE-LIT  | x  | x  |  x | x  | x  |  x |
|  NE-COARSE-METO |    |    |    |    |    |    | 
|  NE-FINE-LIT    |    |    |    |    |    |    | 
|  NE-FINE-METO   |    |    |    |    |    |    | 
|  NE-FINE-COMP   |    |    |    |    |    |    | 
|  NE-NESTED      |    |    |    |    |    |    | 
|  NEL-LIT        |  x |  x |    |  x | x  |  x | 
|  NEL-METO       |    |    |    |    |    |    |


Given its wide scope in terms of languages and datasets, **HIPE-2022 tasks only focuses on a selection of NE annotation types** (in contrast to CLEF-HIPE-2020 which focused on fine-grained NE processing).

Overview of HIPE-2022 tasks and their annotation types:


| HIPE-2022 Tasks  | NE annotation types | 
| -------| -------|
| NERC-Coarse | NE-COARSE-LIT |
| NERC-Fine | NE-FINE-LIT, NE-NESTED|
| NEL | NEL-LIT | 

The annotation types `NE-COARSE-METO, NE-FINE-METO, NE-FINE-COMP` are not considered in HIPE-2022 tasks and evaluation scenarios but are left in the IOB files when present with a dataset, for systems to use this information if beneficial.


## HIPE-2022 Primary Dataset Entity Tagsets

HIPE-2022 datasets feature different entity tagsets. In practice, datasets are converted to the HIPE *format*, but the entity tagsets are left untouched.



## Additional resources

To be updated soon.


## Primary datasets to HIPE-2022: mapping overview

![](./documentation/HIPE2022-Dataset-Mapping.png)

## References

## Acknowledgements






