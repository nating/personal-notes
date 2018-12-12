
*(https://github.com/nating/personal-notes/blob/master/fifth-year/information-retrieval-and-web-search/ranking-and-indexes.md)*

# Ranking and Indexes

* **Inverted Index** is an umbrella term for a range of data structure used for text search.

* An inverted index is like an index found at the back of a book. The word "Inverted" is used because rather than words being associated with documents, documents are associated with words.

* Index terms in inverted indexes are often alphabetised, though they need not be as they are indexed using a hashtable.

* In an inverted index of a search engine, each entry may have a key of a term and a value of a list of the documents that use the term or a list of the occurrences of the term.

* Each list entry in an index of an inverted index is called a **posting**.

* The part of a posting that refers to a specific document or occurrence is called a **pointer**.

* Each document in a collection is given a unique number in order to make it efficient to store document pointers.

* The simplest form of an inverted index just stores the documents that contain each word:

<img width="300" src="./assets/naive-inverted-index.png"/>

* Each list in an inverted index is ordered by sentence number.

* Because each list in an inverted index is ordered by sentence number, finding the an intersection of two lists is `O(max(m,n))` *(where m is the length of the first list and n is the length of the second)*.

* Inverted indexes can be extended to take into account term frequency within a document.

<img width="300" src="./assets/extended-inverted-index.png" />

* Inverted indexes can be further extended by taking into account the position of terms within a document, for further discrimination and phrase identification.

<img width="300" src="./assets/extended-inverted-index-ii.png" />

* Adding feature weighting to inverted indexes also further extends them.

<img width="300" src="./assets/extended-inverted-index-iii.png" />

* Special classes of documents have custom sections, such as a subject and body in an email. These are instances of **Document Fields**.

* **Document Fields** are sections of documents that carry semantic meaning.

* Rules and weighting for document fields can be integrated into the ranking function.

* An **Extent** is a contiguous region of a document. It can be encoded like (<the index of the first term in the extend>,<the index after the last term in the extent>) *(indexing from 1)*.

* Posting lists and extent lists can be combined to figure out what section of a document terms occur:

<img width="300" src="./assets/posting-list-extent-list-combination.png" />

* Documents in the above example inverted indexes have all been ordered by number, but they can also be ordered by score / weight for each term, which can be useful for certain queries (such as ones that include only one word).

* Some other indexing challenges include:
  * Compression and Memory Management
  * Adding data
  * Updating data
  * Index merging
  * Document deletion
  * Distributed indexing
