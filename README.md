# MRI_Cage_test_set
This is an open-source 3d printed antenna set for magnetic resonance imaging (MRI) Faraday RF cages attenuation measurements. It is also suitable for localizing breaches in cage walls and sources of external RF interference. The set consists of two symmetrical loop magnetic antennas, each of which is equipped with six matching boxes for different MRI operating frequencies. Please note that you will need a Vector Network Analyzer (VNA) to build this project!

![Antenna set example picture](/Pictures/01_Cage.jpg)


# Examples of using
Antennas could be used with any type of 50 Ohm RF equipment to perform measurements. In general, antenna #1 is connected to the signal generator and antenna #2 is connected to the receiver (spectrum analyzer, SDR, etc.). The MRI scanner itself can also be used as a signal source. In this case, one antenna would be sufficient.

![Measurements example picture](/Pictures/02_Tests.jpg)
In the left photo, one antenna is placed on a tripod inside the scanning room and connected to a signal generator. After closing the door, you can check with another antenna how much the signal will decrease in value (attenuation measurement). In the right photo, a HackRF shows an MRI signal outside the RF cage. The door insulation is certainly  damaged in this case.

![Interference example picture](/Pictures/02_Tests2.jpg)
It is also possible to use this setup to find a source of external RF interference that affects your MR-image quality. In this example, an old power supply in the cabinet has some problems.


# Building instructions

