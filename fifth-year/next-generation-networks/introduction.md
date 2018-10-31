
*https://github.com/nating/personal-notes/blob/master/fifth-year/next-generation-networks/introduction.md*

# Introduction

* This is what the internet looks like:  
<img width="300" src="https://github.com/nating/personal-notes/blob/master/fifth-year/next-generation-networks/images/internet-structure.png"/>

* There are tiers of ISPs.

* The thinking behind the structure of the internet:
  * It is not feasible to connect every access ISP to each other, as there would be N<sup>2</sup> links.
  * There could be a global ISP that each access ISP is connected to.
  * If being a 'global ISP' is a business, then there will be competitors.
  * These competing global ISPs will need to be connected, either by having nodes directly connected ("peer linking") or by Internet Exchange Points, which are the next logical level up.
  * In order to connect many access ISPs to ISPs (which are what 'global ISPs' will be known as), there will be regional networks to stand in the middle.
  * To bring content closer to users, Content Provider Networks (CDNs?) may run their own networks as well.

* **AS** stands for [Autonomous System](https://en.wikipedia.org/wiki/Autonomous_system_(Internet)).

* A **Telco** is a telecommunications company.

* **Optical-Electric-Optical** (OEO) repeaters convert optical signals into an electric signal, process it and transmit it again.

* Telco networks have been built by repeatedly upgrading legacy technology.

* Copper transmission was limited to a distance of a few kilometres.

* **Attenuation** is the reduction of signal strength.

* Optical Fibre has significantly less attenuation than other media.

* Twisted pairs and Coaxial cables need repeaters at around 2km or up to 9km, but Optical Fibre cables only need them at 40km.

* It would be very expensive to replace copper with fibre from each home to the cabinet.
