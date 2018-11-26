
*https://github.com/nating/personal-notes/blob/master/fifth-year/next-generation-networks/quality-of-service.md*

# Quality of Service

* **Packet Loss** is where a packet does not arrive at its destination.

* **Latency** is the time it takes for a packet to get to its destination.

* **Jitter** is the variation in latency of received packets.

* **Capacity** is the number of bits that can be received per second.

* TCP creates reliability on top of an unreliable network.

* Jitter can be solved with buffers, but this increases latency.

* **QoS** stands for Quality of Service.

* QoS is often referred to as QoS differentiation. This refers to the fact that giving higher priority to certain packets that have requirements (VoIP) gives a better QoS.

* Ethernet packet headers have fields for indicating priority.

* QoS is based on a number of tools:

|Tool|Use|
|---|---|
|**Policer**|Discards packets when they go above a threshold|
|**Shaper**|Delays packets so that bandwidth is not exceeded|
|**Classifier**|Inspects incoming packets and assigns them to a Class of Service (COS)|
|**Metering & Coloring**|Checks packet incoming rate against thresholds and assigns them colors|
|**Queuing Differentiation**|All queues are FIFO, but some COSs are different|
|**Scheduler**|Decides which order to take packets from different queues|
|**Rewrite**|Can recolor packets|

TODO: Rushing here a bit

* **TrTCM** stands for Two Rate Three Color Marking.

* **Color Blind** means all input traffic is treated the same (doesn't already have a color).

* **Color Aware** means that input traffic is colored as it comes in.

* **FQ** stands for Fair Queueing.

* **SP** stands for Strict Priority.

* **WFQ** stands for Weighted Fair Queueing.

* **WRR** stands for Weighted Round Robin.

* **DWRR** stands for Decifit Weight Round Robin.

* **PB-DWRR** stands for Priority-Based Decifit Weight Round Robin.

|||
|---|---|
|FQ|All queues are treated equal|
|SP|Higher priority queue's packets are taken first|
|WFQ|Higher priority queue's packets are taken with priority but not all before queues of lower priority|
|WRR|Like WFQ but less precise and not as computationally expensive
|DWRR|Bit more fair than WRR|

* **RED** stands of Random Early Discard.

* RED drops packets at a random probability as the queue starts to fill up.

* **WRED** stands for Weighted Random Early Discard.

* WRED gives different drop profiles for different types of traffic.
