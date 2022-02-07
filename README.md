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

### Examples
Input word: inaccuracies <br/>
Output: in@@ accurate @@cy @@s



## Part 2: Sentence-level Morpheme Segmentation
