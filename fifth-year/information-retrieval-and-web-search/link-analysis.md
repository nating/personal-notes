
*(https://github.com/nating/personal-notes/blob/master/fifth-year/information-retrieval-and-web-search/link-analysis.md)*

# Link Analysis

* **Link Analysis** gives search engines an idea of how pages relate to each other.

* The page relationships found in link analysis help search engines rank pages more effectively.

* Link Analysis gives an idea of how popular a web page is.

* Components involved in the analysis of a link are:
  * Hyperlink
  * Anchor Text
  * Linking page
  * Linked-to page

* There are numerous algorithms for link analysis.

* Two popular link analysis algorithms are **HITS** and **PageRank**.

* Anchor Text is one of the strongest signals in web search.

* The two or three words usually in anchor text often succinctly describe the topic of the linked page.

* Queries are often very similar to anchor text.

*  All anchor text in all links pointing to a page is typically added to the index as an additional field.

* As anchor text is generally not written by the author of the page, it can describe the linked page from an independent, or
different perspective.

* The simplest approach of link analysis is to count the number of incoming links to a page and use this as a popularity measure, but this method is susceptible to spam.

* **Hyperlink Algorithms** are link analysis algorithms which assume:
  * The quality of a page is proportional to the quality of the pages that link to it.
  * The popularity of a page is proportional to the number of pages that link to it.
  * Popular pages are more likely to contain relevant information than unpopular pages.

* Using hyperlink algorithms, **Link** measures are generated for each page and used in ranking.

#### Hubs, Authorities, and HITS

* The idea of hubs and authorities assumes that if 'Page A' links to 'Page B', then the author of 'Page A' recommends 'Page B'.

* An **Authority** is a page that is linked to by many influential pages in a subject area.

* A **Hub** is a page that links to many influential pages in a subject area.

* A **Good Authority** is linked to by many good hubs.

* A **Good Hub** links to many good authorities.

* **HITS** stands for Hyperlink Induced Topic Selection.

* HITS is a link analysis algorithm that works of the idea of hubs and authorities.

* In HITS:
  * Popular pages can become Hubs or Authorities.
  * The Quality of hubs and authorities is based on the pages that link to them.
  * Each hub and authority is checked often to make sure it has maintained its importance.

* The HITS algorithm involves a series of iterations of three steps:
  * Update each node's Authority Score to be the sum of the hub scores of each node that points to it.
  * Update each node's Hub Score to be the sum of the authority scores of each node it points to.
  * Normalise all the hub / authority scores by dividing them by the square root of the sum of the squares of all the other hub / authority scores.

* The HITS algorithm starts with each node having a hub score and authority score of 1, and then begins the iterations.

#### PageRank

* **PageRank** is a link analysis algorithm that computes the score of a page as the probability of visiting that page.

* In PageRank, a page has a high rank if the sum of the ranks of pages pointing at it is high.

* The steps involved in PageRank:
  * A number, 𝑟, between 0 and 1 is chosen.
  * If 𝑟 < ⋋, the "surprise me" button is clicked.
  * If 𝑟 ≥ ⋋ lambda, a random link on the current page is clicked.
  * Start again.

* PageRank is an example of an ergodic Markov Chain.

* The algorithm for the PageRank of a page is:

<img width="250" src="./assets/page-rank-formula.png" />

*where N is the number of pages, B<sub>u</sub> is the set of pages that point to u, and L<sub>v</sub> is the number of outgoing links from page v (not counting duplicate links).*

* Search engines that use PageRank will prefer pages with high PageRank values, instead of assuming that all web pages are equally likely to satisfy a query.

* HITS calculates authority and hub values for a subset of pages retrieved by a given query.
