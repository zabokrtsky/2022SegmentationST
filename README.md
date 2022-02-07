# The 2022 SIGMORPHON Shared task on Morphological Segmentation.

Morphemes (prefixes, suffixes, root words) are linguistic descriptions, defined as the smallest meaningful unit of words. Our proposed shared task is morpheme
segmentation that converts a text into a sequence of morphemes. In order to prepare a dataset for this task, we integrated all basic types of morphological
databases (including UniMorph (Kirov et al., 2018b) – inflectional morphology; MorphyNet (Batsuren et al., 2021) – derivational morphology; Universal
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

First example is a derived word with prefix (in-) and suffixes (-cy and -s), and second example is a root word. Third example is a compound word.

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

### Statistics

## Part 2: Sentence-level Morpheme Segmentation
At the sentence level, participating systems are expected to predict a sequence of morphemes for a given sentence.

        Six weeks of basic training. Six week @@s of base @@ic train @@ing .
        Fistfights, please. Fist @@fight @@s , please .

## Task Details

## Evaluation

We will provide python evaluation scripts, reporting the following evaluation measures:

- Accuracy - fraction of correctly predicted morphemes.
- Edit distance - average Levenshtein distance between the predicted output and the gold instance.

## Timeline

### Development Phase

- February 14, 2022: Training splits for development languages are released.
- February 21, 2022: Development splits for development languages are released.
- February 28, 2022: Baseline code, and results released.

### Generalization Phase

- April 1, 2022: Training and development splits for surprise languages released.

### Evaluation Phase

- April 8, 2022: Test splits for development and surprise languages are released.
- April 22, 2022: Participants' submissions due.

### Write-up Phase

- May 4, 2022: Participants' draft system description papers due.
- May 20, 2022: Participants' camera-ready system description papers due.

## Organizers

- Khuyagbaatar Batsuren (National University of Mongolia)
- Gábor Bella (University of Trento)
- Viktor Martinović (University of Vienna)
- Zdeněk Žabokrtský (Charles University)
- Aryaman Arora (Georgetown University)
- Kyle Gorman (Graduate center, City University Of New York)
- Fausto Giunchiglia (University of Trento)
- Ryan Cotterell (ETH Zürich)
- Ekaterina Vylomova (University of Melbourne)





