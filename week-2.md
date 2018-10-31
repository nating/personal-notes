
*https://github.com/nating/personal-notes/blob/master/fifth-year/next-generation-networks/week-2.md*

# Week 2

## Wireless Channel Impairments & Mitigation Techniques

### Impairments

* **Path Loss** is the attenuation of signal due to travelling between the transmitter and the receiver.

* Path loss is roughly proportional to 1/d<sup>2</sup>.

* **Shadowing** is attenuation due to random objects being between the transmitter and the receiver.

* **Multipath** is due to reflections and scattering, multiple versions of the signal might arrive at the receiver.

* In severe cases of multipath, multiple versions of a signal may cancel each other out.

* Delay spread is the spreading of a signal due to different delays of parts of the signal.

* **Fading** is quick variations in received power due to time-varying channel characteristics.

* **Noise** is unwanted signals added to the message signal.

* **SNR** (Signal to Noise ratio) is often used as a metric in the assessment of channel quality.

### Mitigation Techniques

* **Diversity** is combining independently received versions of the desired signal.

* Types of diversity are:
  * Spatial Diversity: Using multiple antennae.
  * Frequency Diversity: Using multiple frequencies.
  * Temporal Diversity: Repeating transmissions.
  * Polarization Diversity: Using different polarizations.

* **Directional Antennae** are antenna elements arranged in a certain geometry to maximise the gain in one direction and minimise the gain in other directions.

* Directional Antennae can minimise interference and the probability of jamming or interception.

* **Modulation** techniques vary in how robust they are to channel impairments.

* **Coding** information in different ways can mitigate the effect of channel impairments. e.g. Forward error correction.

* **Spread Spectrum** involves distributing signals over a wide range of frequencies and collecting them back at the receiver.

* In **Frequency Hopping**, transmitters and receivers hop between different frequency bands at a predetermined sequence.

* The most detrimental wireless channel impairment in LAN is interference, because access points are deployed very close to each other.

* The most detrimental wireless channel impairment in WAN is path loss, because base stations are deployed far away from each other.

* The most detrimental wireless channel impairment in a hilly region is shadowing, as the transmitter is hidden from the receiver's viewpoint.

* The most detrimental wireless channel impairment in indoor environments is multipath because of signals reflecting off many objects.

* A **Coding Rate** is the amount of extra redundancy you add to information to deal with errors on the receiving end.  

* A code rate of 1 means that no redundancy is added to the information, therefore it is the least desirable coding rate for unreliable channel conditions.

---

## Overview of Wireless Networks

* Wireless networks can be **Nomadic**, where every node is relatively stationary, or **Mobile** where nodes move around.

* **Mobile** networking involves seamless roaming, wireless telephony, mobile data services, vehicular ad-hoc networks and location-aware services.

* In **Nomadic** networking, the users change their point of connection to the network. Seamless roaming is not necessary in nomadic networking.

* Nomadic networking includes LANs, hotspots, and wireless ISPs. (IEEE 802.11 and Bluetooth)

Here is a reference for the OSI networking model:

|Layer|Processes|
|---|---|
|Application|Application specific exchange of messages.|
|Transport|Reliable delivery, Error Control, and Congestion Control.|
|Network|Routing, Handover, Network Addressing, and Device Location.|
|Data link|Medium Access and Error Control.|
|Physical|Frequency Selection, Modulation, Signal Detection, and Encryption.|

* **Handoff** (or Handover) is to do with handing a device from one network to another.

*TODO: I have not taken down what sort of frequency ranges each type of networking protocols use.*

* Regulators handle standardization and frequency planning.

* **ComReg** stands for Commission for Communications Regulation. Which is the general communications regulator in Ireland.

* The term **Harmonization** is used when describing how it would be desirable if there was a world-wide coordination of spectrum utilization.

* Harmonization is difficult becuase of legacy systems.

* Harmonization if of interest for economic reasons.

* The ITU-R is an international regulator. The ITU-R periodically holds the World Radio Conference where the allocation of the spectrum to different services is decided.

* It is very difficult to take spectrum back from those licensed to use a certain band.

* **Dynamic Spectrum Access** allows operation in licensed frequency bands, as long as it doesn’t interfere with holder of the license for that band.

* Cognitive radios implement dynamic spectrum access.

* Transmissions with low frequencies attenuate less with distance. This makes low frequencies ideal for long range transmissions.

### The Complementarity of Wired & Wireless Systems

* "Wired and Wireless networks can be thought of as complementary."

* Optical fibre does not go everywhere.

* Optical fibre provides a huge amount of available bandwidth.

* Wireless networks go almost everywhere.

* Wireless networks have a highly bandwidth constrained transmission channel, which is susceptible to a variety of impairments.
