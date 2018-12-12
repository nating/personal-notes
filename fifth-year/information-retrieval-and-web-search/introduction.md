
*(https://github.com/nating/personal-notes/blob/master/fifth-year/information-retrieval-and-web-search/introduction.md)*

# Introduction

* Principals of Information Retrieval and Web Search include:
  * Text Processing and Indexing
  * Web Retrieval and Link Analysis
  * Retrieval models and Ranking
  * Evaluation of IR
  * Personalised, Entity Driven and Semantic IR
  * Advanced Approaches, e.g.:
    * Language Models
    * Word Embeddings
    * Machine Learning

* The Information Life Cycle involves:
  * Creation
  * Searching
  * Utilisation

* Organising information objects involves:
  * Organising
  * Indexing
  * Storing

* Finding information objects involves:
  * Retrieval
  * Accessing
  * Filtering

* Information retrieval is a field concerned with the structure, analysis, organisation, storage, searching, and retrieval of information.

* Up till now, the primary focus of IR has been on text and documents.

* Information objects can include:
  * Books, Journals
  * Articles, Reports
  * Web Pages
  * Office Documents
  * Pictures Graphics
  * Audio or Video Files
  * Blogs, RSS Feeds

* Document representation refers to using a **surrogate** to represent documents. These surrogates may include abstracts, key words, and index terms.

* Full-Text retrieval is retrieval that does not use surrogates. It uses the full text of each document.

* In searches like SQL:
  * There are definitive results.
  * It returns the complete set of data that meets the criteria.
  * There is no estimation of relevancy.

* The **Structure of IR Systems** is as follows:
  * Information objects are obtained.
  * The information objects are represented / indexed.
  * A User provides an information request.
  * There is an attempt to match the request against the information objects.
  * A list of recommended information objects that match this request is provided.

* This is an image of the structure of an IR system:

<img width="300" src="./assets/structure-of-ir-system.png" />

* **Postulates of Impotence** means to assume the existence of helplessness. In the context of this module, and why IR is hard, it means that an information need cannot be expressed independent of context.

* Other things that make IR hard include:
  * It is impossible for a machine to translate a request into adequate search terms.
  * A document's relevance depends on other seen documents.
  * It is never possible to verify whether all relevant documents have been found.
  * Machines cannot recognise meaning.

* There are issues with users making their query:
  * Verbalising their information needs
  * Understanding Query Syntax
  * Understanding Search Engines

* Queries can be:
  * Underspecified, e.g. "giant"
  * Ambiguous, e.g. "jaguar"
  * Represent different informational needs, e.g. answer to a question / background search

* Information is often dynamic, being constantly updated (like twitter, or other feeds).

* Scalability is an issue for IR, as there is becoming more and more information to search over.

* New media is evolving that is difficult to search over.

* A **Relevant Document** contains the information that a person was looking for when they submitted a query to the search engine.

* **Retrieval Models** define a view of relevance.

* **Ranking Algorithms** are based on retrieval models.

* **Evaluation** is a big problem in IR because it is difficult to evaluate the performance of an IR system.

* Evaluation of IR systems typically uses a test collection of documents, queries, and relevance judgements.

* The **Trec Collections** are the most commonly used test collections.

* **Recall** & **Precision** are two examples of effectiveness measures.

* Information is a big business. Alphabet have a market value of $813 Billion.
