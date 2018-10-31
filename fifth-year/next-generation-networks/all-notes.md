
*https://github.com/nating/personal-notes/blob/master/fifth-year/next-generation-networks/all-notes.md*

# All Notes

## Week 1

### Introduction

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

---

### Optical Transmission Technology

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

### Optical Transmitters and Receivers

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

### Concepts of Optical Link Design

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

## Week 2

### Wireless Channel Impairments & Mitigation Techniques

#### Impairments

* **Path Loss** is the attenuation of signal due to travelling between the transmitter and the receiver.

* Path loss is roughly proportional to 1/d<sup>2</sup>.

* **Shadowing** is attenuation due to random objects being between the transmitter and the receiver.

* **Multipath** is due to reflections and scattering, multiple versions of the signal might arrive at the receiver.

* In severe cases of multipath, multiple versions of a signal may cancel each other out.

* Delay spread is the spreading of a signal due to different delays of parts of the signal.

* **Fading** is quick variations in received power due to time-varying channel characteristics.

* **Noise** is unwanted signals added to the message signal.

* **SNR** (Signal to Noise ratio) is often used as a metric in the assessment of channel quality.

#### Mitigation Techniques

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

### Overview of Wireless Networks

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

#### The Complementarity of Wired & Wireless Systems

* "Wired and Wireless networks can be thought of as complementary."

* Optical fibre does not go everywhere.

* Optical fibre provides a huge amount of available bandwidth.

* Wireless networks go almost everywhere.

* Wireless networks have a highly bandwidth constrained transmission channel, which is susceptible to a variety of impairments.

---

### Cognitive Radio

...
