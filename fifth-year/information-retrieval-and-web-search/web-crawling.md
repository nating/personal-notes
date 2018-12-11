
*(https://github.com/nating/personal-notes/blob/master/fifth-year/information-retrieval-and-web-search/web-crawling.md)*

# Web Crawling

* Data on the web is heterogenous. There are multiple types of media, multiple languages. This requires multimodal indexing and search.

### Web Search Challenges

* Speed of the web's expansion:
  * Crawling and indexing
  * Web page update frequency
  * Dynamic page generation
  * Invisible, Deep, or Dark web

* Quality of the data
  * 1 in 200 words have typos

* SEO (which is referred to as 'search engine spamming')

---

* **Web Crawling** refers to browsing the web in a methodical manner, collating a list of links discovered.

* A Web Crawler is also known as a **Web Spider** or **Web Robot**.

* A Web Crawler is given seed URLs to start from and it recursively harvests links from websites it visits from there.

* There are numerous crawling algorithms.

* A **URI** is a Uniform Resource Identifier, which is unique to a resource.

* Every page on the internet has a **URI**.

* A **URL** is a type of URI which also specifies the access mechanism (protocol) that can be used to obtain the resource.

* Web pages are stored on web servers that use HTTP to exchange information with client software.

* `http` and `https` are **Schemes**.

* `www.scss.tcd.ie` is a **Hostname**.

* `/personnel/intelligent-systems.php` is a **Resource**.

* **DNS** stands for Domain Name System.

* **IP** stands for Internet Protocol.

* A DNS server translates a hostname into an IP address.

* A Web Crawler connects to a DNS server, finds out the IP address of the resource, connects to the machine with that IP address on a specific port, and makes a request with a specific protocol for the resource it wants.

* Crawlers use threads to fetch hundreds of pages at once.

* **Politeness Policies** are delays that crawlers use between making more requests to the same web server.

* **Robots.txt** files are used to control crawlers.

* **Focused Crawling** involves only downloading pages that are about a specific topic.

* In focused crawling, popular pages about a topic are typically used as seeds.

* A **Text Classifier** is used by a crawler to determine whether a page is 'on-topic'.

* The **Deep Web** is pages that are difficult for web crawlers to find.

* There are three broad categories of pages on the deep web:
  * Private sites (no incoming links, or need login)
  * Form results (need the submission of data to arrive at)
  * Scripted pages (pages that use a client side scripting language to generate links)

* **Darknets**  are overlay networks on the web which use the Internet but require specific software, configurations or authorisation to access.

* The **Dark Web** is parts of web that exist on **Darknets**.

* The Dark Web forms a small part of the deep web.

* Examples of darknets include tor, freenet, and I2P.

* **Sitemaps** contain lists of URLs and data about those URLs, such as modification time and modification frequency.

* Sitemaps can tell crawlers about pages they may otherwise not find, and give them an idea of how often those pages change.

* Some search engines treat 'social content' differently than other content. (e.g. whether they show tweets in search results.)

* A **Spider Trap** (or crawler trap) is a set of web pages that may intentionally or unintentionally be used to cause a web crawler or search bot to make an infinite number of requests or cause a poorly constructed crawler to crash.

* Challenges for Web Crawling include:
  * Selection of which links to follow. (Crawling algorithm, & Link Analysis)
  * When to revisit pages.
  * Deep or invisible web.
  * Parallelisation.
  * Network and Server overload.
  * Spider Traps.
