
*https://github.com/nating/personal-notes/blob/master/fifth-year/next-generation-networks/traffic-models.md*

# Traffic Models

TODO: Being a bit skimmy with these notes. Better that than nothing!

* In a **Poisson Process**, events occur continuously and independently of one another.

* In a **Non-Homogenous** Poisson process, the rate parameter may change over time.

* In the a/b/m/K notation, 'G' means "any distribution".

* A **Bursty** source generates traffic in random clusters.

* Deterministic traffic is not bursty.

* Both the Poisson and Bernoulli processes are bursty as single processes, but not as aggregated traffic sources.

* Self-Similar objects maintain their statistical properties at any scale.

* **Self-Similar** traffic is not smoothed through aggregation. It maintains its burstiness at any time scale.

* Network traffic that is self-similar requires more buffering.

* In Poisson traffic, clustering occurs in the short term but smooths out over the long term.

* **H** is used for the **Hurst Parameter** which indicates the absence of self-similarity.

* Most data traffic is well modelled as a self-similar process.

* Straight-forward queuing analysis using Poisson traffic assumptions is inadequate to model self-similar traffic.

TODO: Trailed off here with a bit to go.
