
*(https://github.com/nating/personal-notes/blob/master/fifth-year/information-retrieval-and-web-search/indexing.md)*

# Indexing

* **IO** can stand for Information Object.

* **Indexing** is representing the information in IOs so that they can be found with user queries.

* Each search engine has its own indexing strategy.

* **Automatic Indexing** is building indexes and retrieving information without human intervation.

* Indexes are used to determine the relevance of a document to a user query.

* Text-based indexing involves deducing the terms that best describe the content of documents.

* **Description** is describing the content of IOs as well as possible, recognising which IOs are relevant to the user, and showing the user *all* relevant IOs.

* **Discrimination** is seeing the differences between IOs, and showing the user *only* relevant IOs.

* Good document representation is a balance of description and discrimination.

* There are two main measures of **Indexing Effectiveness**:
  * Index Exhaustivity (how well all subject matter in the document is recognised and represented in the information system)
  * Term Specificity (how broad the terms describing the document are) (broad terms will return many documents, narrow terms will return less)

### Components of Indexing

* **Tokenisation** is dividing a document into terms (or words).

* **Term Normalisation** is normalising terms, such as:
  * Converting to upper or lowercase
  * Removing hyphens or punctuation

* **Stop Word Removal** is removing commonly occurring words.

* A **Stop List** is a list of words used for Stop Word Removal.

* Most words in stop lists are based on term frequency, but some other terms that add no descriptive value to the document may also be added, e.g. "say", "small", "very".

* There can be a problem with stop words, when they are essential to a query, e.g. "to be or not to be".

* **Stemming** is reducing the variation in words. e.g. turning "walker", "walking", "walked", and "walks" all into "walk".

* Stemming is used to *"conflate morphologically similar words"*.

* A typical stemmer consists of rules and/or dictionaries.

* Examples of stemmers are Porter, Snowball (Porter 2), and KSTEM.

* Problems with stemming include:
  * It can introduce terms that are not real words: "Iteration" -> "Iter".
  * It can miss connections: "European" - "Europe".
  * It can make false connections: "Universe" - "Universal" - "University".
  * It may not recognise proper nouns: "Thomas" - "Thoma".

* **Term Weighting** is deciding which terms best describe a document.

* The text processing used for queries must be the same as is used for documents. e.g. If the word "walking" has been converted to "walk" in all the indexes, then the word "walking" in a query should also be converted to "walk" so that those terms match.

* Zipf's Law is that in a corpus of natural language utterances, the frequency of any word is roughly inversely proportional to its rank in the frequency table.
  * Zipf's Law: `r * f = Constant`. *where r is the rank of a word in the frequency table, and f is its frequency*

* Zipf's Law translates to the most common word occurring twice as often as the second, which occurs twice as often as the third.. etc.

* Zipf's Law can be used to determine the probability of the occurrence of a word:
  * `r * P<sub>r</sub> = c` *where P<sub>r</sub> is the probability of the r<sup>th</sup> ranked word in the frequency table occurring, and c is a constant*
  * In English, the constant *c* is approximately 0.1.

* Zipf's law is quite accurate but loses accuracy at high ranks in practice.

* High frequency words are useless, **very** low frequency words may useless (spelling mistakes, or too rare), and the most discriminative words are of the middle frequency.

* Methods based on Zipf's Law are:
  * Stop Word Removal: remove most frequent words
  * Significant words: remove most and least frequent words (rarely used)
  * Term Weighting: weight terms by their frequency (used by almost all search engines)

* Phrases are important for search engines. e.g."Climbing equipment" should have the occurrences of the terms together rated higher.

* **POS** stands for Parts of Speech.

* A POS tagger is used to label words as a certain part of speech: NN (singular noun), NNS (plural noun), VB (verb), VBD (verb, past tense)... etc.

* Using a POS tagger, phrases can be identified based on POS tags.

* POS tagging is too slow for web search.

* An **n-gram** is a sequence of *n* words.

* The more frequently an n-gram occurs, the more likely it is to correspond to a meaningful phrase in the language.

* The rank frequency for n-grams fits Zipf's distribution better than singular words.

|||
|---|---|
|Stemming|Description|
|Stop Word Removal|Discrimination|
