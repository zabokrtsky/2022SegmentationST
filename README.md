# The 2022 SIGMORPHON Shared task on Morphological Segmentation.

Morphemes (prefixes, suffixes, root words) are linguistic descriptions, defined as the smallest meaningful unit of words. Our proposed shared task is morpheme
segmentation that converts a text into a sequence of morphemes. In order to prepare a dataset for this task, we integrated all basic types of morphological
databases (including UniMorph (Kirov et al., 2018b; McCarthy et al., 2020) – inflectional morphology; MorphyNet (Batsuren et al., 2021) – derivational morphology; Universal
Dependencies (Nivre et al., 2017) and ten editions of Wiktionary – compound morphology and root words). In the future, we expect the NLP community will
benefit a lot by innovating subword-based tokenization with this task. 

+ ***Part 1***: [Word-level morpheme segmentation](https://github.com/sigmorphon/2022SegmentationST#)
+ ***Part 2***: [Sentence-level morpheme segmentation](https://github.com/sigmorphon/2022SegmentationST#)

## Part 1: Word-level Morpheme Segmentation
At the word level, participants will be asked to segment a given word into a sequence of morphemes. Input words contains all types of word forms: root words, derived words, inflected words, and compound words.

### Data
Training and development data are UTF-8-encoded tab-separated values files. Each example occupies a single line and consists of input word, the corresponding morpheme sequence, and the corresponding morphological category (optional information should be used only to oversample or undersample training data). The following shows three lines of English data:
    
    inaccuracies  in@@ accurate @@cy @@s  110
    dictionary  dictionary  000
    screwdriver screw @@drive @@er  011

First example is a derived word with prefix (in-) and suffixes (-cy and -s), and second example is a root word. Third example is a compound word. In the test datasets, we will provide only first column of data as input words. 

### Languages
Development languages are:
1.  `ces`: Czech
2.  `deu`: German
3.  `eng`: English
4.  `fra`: French
5.  `hun`: Hungarian
6.  `spa`: Spanish
7.  `ita`: Italian
8.  `lat`: Latin
9.  `rus`: Russian

### Data Statistics

| word class | English | Spanish | Hungarian | French | Italian | Russian | Czech | Latin | German |
|:-----:|---------|---------|-----------|--------|---------|---------|-------|-------|--------|
|  100  |  126544 |  502229 |    436753 | 122529 |  253455 |  221760 |     - |   TBD |    TBD |
|  010  |  203102 |   18449 |     23717 |  61465 |   41092 |   72970 |     - |   TBD |    TBD |
|  101  |   13790 |     458 |    124479 |    581 |     317 |    1909 |     - |   TBD |    TBD |
|  000  |  101938 |   15843 |      6266 |  32509 |   21037 |    2921 |     - |   TBD |    TBD |
|  011  |    5381 |      82 |      1657 |    521 |     140 |     328 |     - |   TBD |    TBD |
|  110  |  106570 |  346862 |    289812 | 163297 |  237104 |  481409 |     - |   TBD |    TBD |
|  001  |   16990 |     248 |      4398 |   1586 |     431 |     259 |     - |   TBD |    TBD |
|  111  |    3059 |     343 |     47541 |    309 |     158 |    2658 |     - |   TBD |    TBD |
| total words |  577374 |  884514 |    934623 | 382797 |  553734 |  784214 | 38682 |   TBD |    TBD |

### Word category description
For some of the development languages, we are providing the word categories so that participant can deal with imbalanced situation of morphological categories. 

| word class | Description                      | English example                        |
|------------|----------------------------------|----------------------------------------|
| 100        | Inflection only                  | played ==> play @@ed                   |
| 010        | Derivation only                  | player ==> play @@er                   |
| 101        | Inflection and Compound          | wheelbands ==> wheel @@band @@s        |
| 000        | Root words                       | progress ==> progress                  |
| 011        | Derivation and Compound          | tankbuster ==> tank @@bust @@er        |
| 110        | Inflection and Derivation        | urbanizes ==> urban @@ize @@s          |
| 001        | Compound only                    | hotpot ==> hot @@pot                   |
| 111        | Inflection, Derivation, Compound | trackworkers ==> track @@work @@er @@s |

## Part 2: Sentence-level Morpheme Segmentation
At the sentence level, participating systems are expected to predict a sequence of morphemes for a given sentence.
The following shows two lines of English data:

    Six weeks of basic training. Six week @@s of base @@ic train @@ing .
    Fistfights, please. Fist @@fight @@s , please .

The following shows two lines of Mongolian data:

    Гэрт эмээ хоол хийв. Гэр @@т эмээ хоол хийх @@в .
    Би өдөр эмээ уусан. Би өдөр эм @@ээ уух @@сан .

In above example, `эмээ` is a hononym of two different words, first means a `grandmother` and second is `medicine`. Depending on the context, the second homonym word is inflectional form of `medicine` and it is segmentable.

### Languages
Development languages are:
1.  `ces`: Czech
2.  `eng`: English
3.  `hun`: Hungarian
4.  `mon`: Mongolian

### Data Statistics

|           | train | dev  | test |
|-----------|-------|------|------|
| Czech     | 1000  | 500  | 500  |
| English   | 11007 | 1783 | 1846 |
| Hungarian | TBD   | TBD  | TBD  |
| Mongolian | 1000  | 500  | 500  |

## Task Details

## Evaluation

We will provide python evaluation scripts, reporting the following evaluation measures:

- Accuracy - fraction of correctly predicted morphemes.
- Edit distance - average Levenshtein distance between the predicted output and the gold instance.

## Timeline

### Development Phase

- February 21, 2022: Training splits for development languages are released.
- February 28, 2022: Development splits for development languages are released.
- March 5, 2022: Baseline code, and results released.

### Generalization Phase

- April 8, 2022: Training and development splits for surprise languages released.

### Evaluation Phase

- April 15, 2022: Test splits for development and surprise languages are released.
- April 29, 2022: Participants' submissions due.

### Write-up Phase

- May 13, 2022: Participants' draft system description papers due.
- May 20, 2022: Participants' camera-ready system description papers due.

## Organizers

- Khuyagbaatar Batsuren (National University of Mongolia)
- Gábor Bella (University of Trento)
- Viktor Martinović (University of Vienna)
- Aryaman Arora (Georgetown University)
- Kyle Gorman (Graduate center, City University Of New York)
- Zdeněk Žabokrtský (Charles University)
- Amarsanaa Ganbold (National University of Mongolia)
- Šárka Dohnalová (Charles University)
- Magda Ševčíková (Charles University)
- Kateřina Pelegrinová (University of Ostrava)
- Fausto Giunchiglia (University of Trento)
- Ryan Cotterell (ETH Zürich)
- Ekaterina Vylomova (University of Melbourne)

## References

Kirov, C., Cotterell, R., Sylak-Glassman, J., Walther, G., Vylomova, E., Xia, P., Faruqui, M., Mielke, S., McCarthy, A., Kübler, S., Yarowsky, D., Eisner, J., and Hulden, M. (2018). [UniMorph 2.0: Universal Morphology](https://arxiv.org/abs/1810.11101). Proceedings of LREC 2018.

McCarthy, A.D., Kirov, C., Grella, M., Nidhi, A., Xia, P., Gorman, K., Vylomova, E., Mielke, S.J., Nicolai, G., Silfverberg, M. and Arkhangelskij, T., (2020). [UniMorph 3.0: Universal Morphology.](https://aclanthology.org/2020.lrec-1.483/). Proceedings of LREC 2020.

Batsuren, K., Bella, G. and Giunchiglia, F., (2021). [MorphyNet: a Large Multilingual Database of Derivational and Inflectional Morphology.](https://aclanthology.org/2021.sigmorphon-1.5/) In Proceedings of SIGMORPHON 2021 (pp. 39-48).

Nivre, J., Agić, Ž., Ahrenberg, L., Antonsen, L., Aranzabe, M.J., Asahara, M., Ateyah, L., Attia, M., Atutxa, A., Augustinus, L. and Badmaeva, E., (2017). [Universal Dependencies 2.1.](https://hal.inria.fr/hal-01682188?gathStatIcon=true)

