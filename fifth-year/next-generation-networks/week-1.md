
*https://github.com/nating/personal-notes/blob/master/fifth-year/next-generation-networks/week-1.md*

# Week 1

## Introduction

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

## Optical Transmitters and Recievers

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





/
