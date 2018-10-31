
*https://github.com/nating/personal-notes/blob/master/fifth-year/next-generation-networks/all-notes.md*

# All Notes

## Introduction

* This is what the internet looks like:  
<img width="500" src="https://github.com/nating/personal-notes/blob/master/fifth-year/next-generation-networks/images/internet-structure.png"/>

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

---

## Optical Transmission Technology

* The typical path loss of optical fibre is 0.2dB/Km.

* Signal can go 150km in optical fibre without amplification.

* Static current produces an EMF in a wire and variable current produces a varying EMF and radiates energy.

* Pairs of wire emit and receive radiation. Going and returning current have opposite sign, so their interference cancels out.

* Twisting pairs of copper wires helps to reduce interference from external sources.

* Coaxial cables have a tube of conducting material around the wires, and sometimes a tube of insulating material around this. This means that they induce less of a current on other wires.

* **Total Internal Reflection** is a process where a ray of light meets a less dense medium at an angle that exceeds the critical angle, causing the light to reflect (somewhat [for the most part]) completely. The critical angle is dependent on the difference in the densities of the media.

* Optical fibres work by total internal reflection.

* Optical communications are achieved by transmitting pulses.

* Each pulse is made up of a number of adjacent frequencies.

* **Modal dispersion** is a distortion mechanism in optical fibres. Pulses of light which are made up of several rays of light, reflect at slightly different angles. This means that the propagation velocity of all the modes (rays) is not the same, and they become out of sync.

* **Intersymbol Interference** is where multiple pulses in optical fibres end up overlapping.

* Optical fibres can be **Multi-mode** fibre, which have a larger core that allows for multiple modes to coexist inside the fibre, or **Single-mode** fibre which only has enough space in the core for one mode to propagate. Single-mode fibre is used more in telecommunications.

* **Path Loss** is the loss of power as a signal propagates.

* **Dispersion** is distortion due to the fact that the refractive index is dependent on frequency rather than being constant.

* The three types of Dispersion are:
  * Modal Dispersion (see above).
  * **Chromatic Dispersion**, which is due to different frequencies within a single mode propagating at different speeds.
  * **[Polarization mode dispersion](https://en.wikipedia.org/wiki/Polarization_mode_dispersion)**.

* Modal Dispersion has the biggest effect of any dispersion.

*TODO: The material gets quite heavy here, and I was not sure that it was beneficial to take down such in depth physics, but perhaps it is necessary to know the material at the end of this section in such detail.*

---

## Optical Transmitters and Receivers

* **Laser** stands for Light amplification by stimulated emission of radiation.

* Lasers emit photons of light that all have the same frequency and phase.

* Tunable lasers can emit light at different wavelengths within a predetermined range.

* **Modulation** is used to add information to a carrier signal.

* On-off modulation is still the most common form of modulation.

* Direct laser modulation is achieved by turning a laser off and on.

* External modulation is achieved by intermittently obscuring the light from a laser.

* A **Photodetector** converts an optical signal into an electric signal.

* **Coherent Detection Systems** can detect phase as well as signal amplitude.

* The higher sensitivity of coherent receivers allows for different modulation schemes with higher spectral efficiency.

---

## Concepts of Optical Link Design

* **BER** stands for bit error rate.

* **OSNR** stands for optical signal to noise ratio.

* The concept of a **Power Penalty** is the increase in receiver input power needed to eliminate the degradation of BER due to fibre impairments.

* There are three types of noise in optical systems:
  * **ASE** (Amplified Spontaneous Emission) is when amplifiers (as well as amplifying the signal) also introduce their own noise.
  * **Thermal Noise** due to the random thermal-driven motion of electrons at the receiver.
  * **Shot Noise** due to photons arriving at the receiver at a sort of random time (when considered at a quantum level).

* **NF** can stand for noise figure, which is a measure of the amount of noise introduced to a system by an amplifier.

* Signal regenerators read a signal, and re-emit a signal that represents that signal's data. (gets rid of noise)

* There is a high cost of using a lot of signal regenerators.

*TODO: Some material was not taken note of down due to its heavy - in depth nature. I'm not certain that that much depth is necessary.*

* **WDM** stands for Wavelength Division Multiplexing. (TODO: What is WDM?)

---

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

---

# Cognitive Radio

* **Software Defined Radio** is a collection of hardware and software components that enable reconfigurable systems for wireless networks and user terminals.

* A **Cognitive Radio** is a radio that is aware of and can sense its environment, and make decisions about how to operate based on this information and its pre-defined objectives.

* A **Cognitive Radio** is also defined as a A transceiver that is aware, adaptive, and capable of learning from experience.

* A cognitive radio is aware of:
  * The RF environment
  * Its own capabilities
  * The policies it needs to follow
  * Local and Global objectives
  * Network conditions
  * Other user's priorities and authorisations

* A cognitive radio can adapt,
  * Control of transmit power
  * Selecting its dynamic waveform
  * Accessing dynamic spectrum
  * Routing
  * Negotiating waveforms and protocols

* A cognitive radio can learn,
  * Having an experience-weighted lookup table.
  * Using machine learning algorithms.

The general elements of a cognitive radio are shown below:

|Element|Components|
|---|---|
|Objectives|Maximise SNR and data rate|
|Variables|Frequency of operation, Power, and Waveform|
|Stimuli|Occupied bands, Signal strength, Neighbour list|
|Policies|Allowed frequency bands for primary or secondary use|

* The desirable features of a cognitive radio are:
  * A wide band
  * The ability to transmit any waveform
  * A flexible architecture
  * High performance
  * Low power consumption
  * Affordability
  * Accessibility
  * Straightforward to use and develop for
  * Robust
  * Access to suitable frequency spectrum segments for innovation and testing

* The basis of a cognitive radio could be any software defined radio, since it builds on top of the components of an SDR.

* Applications of cognitive radio include:
  * Dynamic spectrum access (DSA)
  * Cooperative medium access and communications
  * Opportunistic switching between wireless networks
  * Adaptive selection of available radio resources
  * Increased interoperability of different systems (spectrum sharing)

* A **Femtocell** is a small cellular base station for residential or business installation.

* Femtocells are cheap and easy to deploy.

* Femtocells can use the same frequency bands as the conventional cellular network, which means that they can cause interference with the WAN if the spectrum is not shared properly.

* **Self-Organising Networks** can automatically extend, change, configure and optimise their topology, coverage, channel allocation and other operating parameters.

---

# Self Organising Networks

### Characteristics of Complex Adaptive Systems

|Characteristic|Meaning|
|---|---|
|1. Non-linearity|Small actions can generate large reactions.|
|2. Emergence|Patterns which can not be planned or intended begin to appear due to collective behaviour.|
|3. Dynamical systems change|Subsystem interactions are volatile and cascade rapidly.|
|4. Adaptation|The system is a function of adaptation of elements to each other and their environment.|
|5. Uncertainty|Processes and outcomes are unpredictable.|
|6. Co-evolutionary|Agents self organise and connections emerge that become co-evolutionary as the agents evolve together.|

* CA stands for cellular automata and ABM stands for agent based modelling.

* Cellular Automata is to do with cellular lattices, and is a subject of mathematical study.

* An ABM **Agent** is anything that makes a decision in a network.

* An ABM agent has its own goals and behaviours.

* An AGM agent operates in parallel with other ABM agents.

* An ABM agent can be adaptive.

* ABM agents have no central command.

* ABM agents can exist on different levels.

* The ABM agent cycle is a cycle of Act -> Get Stimulus -> Process Stimulus -> Act -> ...

---

# Spectrum Sharing

* **License Exempt** bands are bands in which one can operate without a license.

* License Exempt bands are good for:
  * Facilitating market entry.
  * Enabling niche applications or services to be addressed quickly and cheaply using existing technology and spectrum.
  * Secure of tenure (users have no license-expiry date).
  * Causing a reduction of congestion in licensed bands.
  * The ability to extend the reach of fixed communication networks, by providing wireless local area connectivity in homes, businesses and at public traffic hotspots.

* The benefits of license exempt bands from an end-user's perspective include:
  * Convenience of less lengthy cables at home or work.
  * The ability to connect to a fixed broadband rather than depending on the mobile network.
  * Convenience of the ability to install low cost wireless alarm systems or to use beeper car keys.

* There are rules for unlicensed bands. These rules keep it possible for multiple devices to co-exist in the band.

* **CSMA/CA** makes facilitates good spectrum access for Wi-Fi, even when in highly contended environments.

* **LTE** is 4G. It stands for Long-Term Evolution.

* Wi-Fi is sort-of derived from Wireless Fidelity.

* **Wi-Gig** (802.11ad) operates in the 60GHz millimetre waveband, and is intended for very high speed, short range applications.

* Wi-Gig expected to deliver up to 7Gpbs over ranges of up to 10 meters.

* 802.11ay is being developed by the IEEE and is aiming at data rates in excess of 30 Gbps, which would allow full movies to be downloaded in a second.

* Nicola refers to 5GHz as *"The promised land of unlicensed capability"* (TODO not sure why...).

* The 71-76GHz band is not relevant in the context of cognitive radio systems' coexistence with radar systems.
