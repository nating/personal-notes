
*(https://github.com/nating/personal-notes/blob/master/fifth-year/information-retrieval-and-web-search/boolean-retrieval-vsm-and-tfidf.md)*

# Boolean Retrieval, VSM, and tf-idf

* Retrieval models are *the mathematical foundation upon which ranking algorithms are based*.

* Two aspects of relevance that are looked at in this module are:
  * Topical vs User
  * Binary vs Multivalued

* A document is **Topically Relevant** if it is judged to be on the same topic.

* **User Relevance** is what an individual user believes to be relevant.

* **Binary Relevance** is that a document is either relevant or not relevant.

* **Multivalued Relevance** is where relevance is a multivalued variable.

* Retrieval models include:
  * Boolean Retrieval
  * Vector Space Model
  * Probabilistic Models (BM25)
  * Language Models
  * Machine Learning

* **Boolean Retrieval** (or *exact-match-retrieval*) is where all documents retrieved are equivalent in terms of relevance.

* Boolean Retrieval requires users to be able to make their specific queries ("president AND lincoln AND NOT (nebraska OR cars)").

* Using the NOT operator in queries is not recommended, because e.g. a user won't know that the Wikipedia page for Abraham Lincoln has "Nebraska" in it.

* In Boolean Retrieval, all query terms have the same importance.

* In the **Vector Space Model**, documents and queries are considered to be vectors of length *t* in a *t*-dimensional vector space. *(where t is the number of index terms)*

* In VSM, a collection of *n* documents can be considered a matrix of *n* rows which represent documents and *t* columns which represent weights assigned to a term for a document.

<img width="250" src="./assets/vector-space-model.png" />

* The Vector Space Model can implement term weighting, ranking, and user feedback.

* In VSM, the angle of the vectors is used, rather than their euclidean distance. This is because documents that have different lengths differ a lot in their euclidean distance. A+A and A may have a large euclidean distance between them, but they have the same angle.

* In VSM the angle of the document vectors and the query vector is used to rank the documents.

* Ranking documents in decreasing order of the angle between the query and document is the same as ranking documents in increasing order of cosine(query,document).

* **Cosine Correlation** is the angle between two vectors:

<img width="250" src="./assets/cosine-correlation.png" />

* **TF-IDF** stands for Term-Frequency - Inverse Document Frequency.

* tf-idf is the most common term weighting scheme used by VSM.

* **TF** (*term-frequency*) determines the importance of a term in a document or q query. TF is usually the number of occurrences of the term in the document.

* **IDF** (*inverse-document-frequency*) determines the importance of a term across a collection of documents.

* IDF is calculated with `idf = log(N/n<sub>k</sub>)`. *where N is the number of documents in the corpus, and n<sub>k</sub> is the number of documents that contain term k.*

**NOTE: To get the right calculations to match those in Seamus' notes, use 'ln()' on your calculator instead of 'log()'.**

<img width="250" src="./assets/tf-idf.png" />

* VSM is typically used as a model of topical relevance.
