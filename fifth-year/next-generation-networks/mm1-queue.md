
*https://github.com/nating/personal-notes/blob/master/fifth-year/next-generation-networks/mm1-queue.md*

# M/M/1 Queue

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
