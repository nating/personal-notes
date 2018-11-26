
*https://github.com/nating/personal-notes/blob/master/fifth-year/next-generation-networks/metro-core-networks.md*

# Metro Core Networks

* **OEO** stand for Optical Electronic Optical.

* Optical communications technology has developed from the core to the metro.

* The **Metro Network** is typically called aggregation as it aggregates data from the access networks.

* There is a trend of keeping data local to reduce latency.

* **CDN** stands for Content Delivery Network.

* CDNs will carry 71% of internet traffic by 2021.

* 35% of end-user's internet traffic will be delivered within a metro network by 2021.

* Access Points are typically point-to-point or tree networks.

* Metro and Core are mesh networks.

* The metro often has rings.

* **EX-C** stands for Electronic Cross Connect.

* The IP topology was built on top of EX-C links.

* **OX-C** stands for Optical Cross Connect.

* **WDM** stands for Wavelength Division Multiplexing.

* **L2** is the Data Link layer.

* It was proposed to do IP over WDM (no need for L2), but there are problems with it:
  * All traffic is terminated
  * Every wavelength in the fibre needs a port in the router
  * Routers are expensive

* The Optical Cross Connect is an optical element that provides switching.

* The OX-C element is often referred to as **ROADM** (Reconfigurable Optical Add Drop Multiplexer).

* ROADMs are also used to connect L2 networks.

* Advantages of OX-C / ROADM are:
  * No need for optical-electrical conversion
  * Massive saving on routing / packet switching resources
  * Lower energy consumption

* (Some of the above are only advantages to channels that do not need to operate add/dropping)

* Fibre Switches and Wavelength Selective Switches are two ways of making OX-Cs.

* **Fibre Switches** connect signals from entire fibres.

* **WSS** stands for Wavelength Selective Switch.

* Given an input fibre with multiple wavelengths, a WSS can select which wavelengths to send to different output fibres.

* **OSNR** stands for Optical Signal to Noise Ratio.

* There are issues with optical switching, as the optical layer is analogue. TODO: list issues.

* If optical switching becomes part of the dynamic topology, any changes will effect other layers of the network. This can cause network instability.

* **Multi-Layer Optimisation** is choosing the right routes at every layer to optimise traffic.

* Optical switching gives operators more freedom to choose routes. But this freedom makes making decisions more difficult. Optimising both layers together is a computationally complex challenge.

* **MPLS** stands for Multi-Protocol Label Switching.

* MPLS is a protocol which tells packets exactly what route it should follow.

* MPLS is a transport protocol. It can transport different types of network protocols, e.g. IP and Ethernet.

TODO: Racing a bit from here on

* **LDP** stands for Label Distribution Protocol.

* **FEC** stands for Forward Equivalence Class.

* The Forwarding Equivalence Class is the set of all IP addresses that get mapped into the same MPLS tunnel.

* Ethernet switches create start topologies.

* **VLAN** stands for Virtual Local Area Network.

* VLANs are implemented by adding another field to the header.

* The VLAN header in ethernet frames is a 802.1Q standard.
