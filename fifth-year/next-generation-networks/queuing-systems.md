
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

* The **J<sup>th</sup>** user seeks a service that will require **s<sub>j</sub>** units of service time.

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

* **Little's Law** is: the expected number in a system is a product of the arrival rate and the average time spent in the system.
  * E[n] = λ*E[τ]

* The characteristics of m/m/1 are:
  * Single Server
  * Arrivals (λ) according to Poisson
  * Inter-arrival times exponential
  * Service times exponential
  * Infinite buffers

* The number of items in a system can be expressed as a Markov chain. The states represent the number of items in the system.

* **µ** is the service rate.

* **ρ** is the utilization. ρ = λ/µ < 1.

* The probability that there are n items in the system is: ρ<sup>n</sup>(1 - ρ).

* The average number of users in the system is: ρ/(1 - ρ).

* The average number of users in the queue is: ρ<sup>2</sup>/(1 - ρ).

* The average delay in the system is 1/(µ - λ).

* The average wait time is: 1/µ * ρ/(1 - ρ)
