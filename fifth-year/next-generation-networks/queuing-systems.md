
*https://github.com/nating/personal-notes/blob/master/fifth-year/next-generation-networks/queuing-systems.md*

# Queuing Systems

* Queue is defined as a verb, and is used in its own definition.

* Examples of Queues are:
  * Time-Shared Programs
  * Statistical Multiplexer / Concentrator
    * Packet Based
    * Channel Based
  * Multiple Access
    * Ethernet LAN
    * Wireless Network
  * Web Access

* Queuing theory studies:
  * Arrival Characteristics
  * Service Characteristics
  * Resources
  * Waiting Time
  * Blocking time

* Elements of a Queuing System include:
  * Input
  * Queue
  * Server
  * Output

* **λ** is the Arrival Rate.

* A Queuing System has **c** identical servers.

* The **j<sup>th</sup>** user seeks a service that will require **s<sub>j</sub>** units of service time.

* **Service Discipline** specifies the order in which items are selected from the queue.

* Waiting time **t<sub>Q<sub>j</sub></sub>** is the time between the j<sup>th</sup> item entering the system and entering service.

* Total Delay is **τ<sub>j</sub>** = **t<sub>Q<sub>j</sub></sub>** + **s<sub>j</sub>**.

* **n** is the number of items in the system.

* **n<sub>q</sub>** is the number of items in the queue.

## a / b / m / K Notation

* **a** is the type of arrival process.
  * M denotes Markov (exponential random variables)

* **b** is the service time distribution.
  * M denotes Markov (exponential random variables)
  * D denotes deterministic (constant arrival times)
  * G denotes General (a general distribution)

* **m** is the number of servers.

* **K** is the maximum number of items allowed in the system. (buffer size)

* The notation "a/b/m/K" is used to describe a queuing system.
