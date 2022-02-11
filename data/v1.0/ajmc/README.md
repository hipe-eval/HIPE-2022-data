# Annotated 19C Classical Commentaries

## Description

This dataset consists of NE-annotated historical commentaries in the field of Classics, and was created in the context of the [Ajax MultiCommentary project](https://mromanello.github.io/ajax-multi-commentary/). We annotated a set of Knowledge Entities (KEs) of domain-specific interest, according to some newly-developed [annotation guidelines](./annotation-guidelines-classics-KEs.pdf). Such KEs feature a few domain-specific entity types such as works, material objects (e.g. manuscripts) and bibliographic references, in addition to more universal entities like persons, locations and organizations.

List of annotated entities (coarse level):
- Person\* (`pers`)
- Location (`loc`)
- Organisation (`org`)
- Date (`date`)
- Work\* (`work`)
- Scope (`scope`)
- Object\* (`object`)

Entities marked with an asterisk (\*) are further classified into sub-types. For example, a *person* entity can be: a) mythological entity (`pers.myth`), b) author (`pers.author`), c) editor (`pers.editor`) or d) other (`pers.other`). See the [annotation guidelines](./annotation-guidelines-classics-KEs.pdf) for the full list of entity sub-types.

## Composition

[Commentaries](https://en.wikipedia.org/wiki/Commentary_(philology)) are a specific genre of scholarly publications that focus on one specific text (or part of it) and aim to provide the reader with in-depth information to understand this text. From an information extraction point of view, commentaries are very rich in terms of KEs as they contain mentions of mythological characters (heroes, gods, etc.), scholars, works of primary and secondary literature – all this in a style which favours conciseness and makes abundant usage of abbreviations.

For this dataset, we annotated randomly selected pages from three 19th century commentaries written in German, English and French about an Ancient Greek tragedy by Sophocles, the *Ajax*. As to the quality of the OCR, we used the output of the OCR engine Tesseract (see [this paper](https://arxiv.org/abs/2110.06817) for further details on OCR quality evaluation of these commentaries). An example of a commentary page is shown in the image below.

![](./commentary-layout-regions.png)

When sampling data for annotation, we kept only pages belonging to the introduction, preface or the commentary itself, and excluded very short pages (less than 100 tokens). 

## Format

This dataset comes in the CoNLL-like HIPE TSV format (for further details see the [HIPE 2020 Task Participation Guidelines](https://doi.org/10.5281/zenodo.3677171), p. 8). Sentence boundaries are indicated by the `EndOfLine` flag, contained in the `MISC` column, and correspond to manually identified linguistic sentences (see Guidelines, section 4). Hyphenated words were manually identified and re-composed (i.e. de-hyphenated).

Annotated data come in two flavours, corresponding to two different sets of tasks: 
1) *NER and EL*: data contains annotations of universal entities, both coarse and fine grained, as well as entity links (see sample file).
2) *Citation mining*: data contains annotations of bibliographic references to both primary and secondary sources, according to the taxonomy described in the Annotation Guidelines section 2.3 (see sample file). 

**NB**: the two files are fully aligned, meaning line e.g. 100 in both files refers to the same annotated token. As such, information from both files can be used in a multi-task learning scenario. 

## Statistics

Not available yet. 

## License

The digitized commentaries are available in the Internet Archive and released in the Public Domain. This annotated dataset is published under a [Creative Commons CC BY license (v. 4.0)](https://creativecommons.org/licenses/by/4.0/). 

## Domain specificity

TBD

- data sparsity
- entity linking/importance of context
- abbreviations: not commonly found in Wikidata, but they can be found in hucitlib (partly linked to Wikidata), see below. 

## Related resources

**hucitlib knowledge base.** Commentators make abundant use of very concise abbreviations when referring e.g. to ancient authors (`pers.author`) and their works (`work.primlit`). Such abbreviations constitute a substantial challenge, especially for entity linking. An external resource that can be used in this respect is the [`hucitlib` knowledge base](https://hucitlib.readthedocs.io/) which is partially linked to Wikidata and provides abbreviations and variant names/titles for classical authors and their works.  