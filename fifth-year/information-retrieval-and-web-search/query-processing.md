
*(https://github.com/nating/personal-notes/blob/master/fifth-year/information-retrieval-and-web-search/query-processing.md)*

# Query Processing

* Some web search challenges include:
  * Different styles and skill levels of users
  * Personalisation
  * Heterogenous Data (multimodal and multilingual search)
  * Spoken / Conversational search

* The basic query processing techniques are **Document-at-a-Time** and **Term-at-a-Time**.

* Document-at-a-time query processing gets a score for each document, one at a time:

TODO: fix the link to this image
<img width="250" src="/document-at-a-time.png" />

* Term-at-a-time query processing gets a score for each document for each term, and then adds all those scores up:

TODO: fix the link to this image
<img width="250" src="/document-at-a-time.png" />

* The primary disadvantage of term-at-a-time is the memory required by the accumulator.

* Term-at-a-time reads each inverted list from start to finish, so it has more efficient disk access.

*








/
