
*https://github.com/nating/personal-notes/blob/master/fifth-year/next-generation-networks/wireless-channel-impairments-and-mitigation-techniques.md*

# Wireless Channel Impairments & Mitigation Techniques

## Impairments

* **Path Loss** is the attenuation of signal due to travelling between the transmitter and the receiver.

* Path loss is roughly proportional to 1/d<sup>2</sup>.

* **Shadowing** is attenuation due to random objects being between the transmitter and the receiver.

* **Multipath** is due to reflections and scattering, multiple versions of the signal might arrive at the receiver.

* In severe cases of multipath, multiple versions of a signal may cancel each other out.

* Delay spread is the spreading of a signal due to different delays of parts of the signal.

* **Fading** is quick variations in received power due to time-varying channel characteristics.

* **Noise** is unwanted signals added to the message signal.

* **SNR** (Signal to Noise ratio) is often used as a metric in the assessment of channel quality.

## Mitigation Techniques

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
