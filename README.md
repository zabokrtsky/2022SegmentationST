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
    
    inaccuracies  in@@ accurate @@cy @@s
    dictionary  dictionary
    screwdriver screw @@drive @@er

First example is a derived word with prefix (in-) and suffixes (-cy and -s), and second example is a root word. Third example is a compound word.



## Part 2: Sentence-level Morpheme Segmentation


## Evaluation

We will provide python evaluation scripts, reporting the following evaluation measures:

- Accuracy - fraction of correctly predicted morphemes.
- Edit distance - average Levenshtein distance between the predicted output and the gold instance.

## Timeline

- February 14, 2022: Training splits are released.
- February 21, 2022: Development splits are released.
- February 28, 2022: Baseline code, and results released.
- April 1, 2022: Test splits are released.
- April 22, 2022: Participants' submissions due.
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





