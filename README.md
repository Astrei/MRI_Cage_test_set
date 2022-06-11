# MRI_Cage_test_set
This is an open-source 3d printed antenna set for magnetic resonance imaging (MRI) RF-cages attenuation measurements. It is also suitable for localizing breaches in cage walls and sources of external RF interference. The set consists of two symmetrical loop magnetic antennas, each of which is equipped with six matching boxes for different MRI operating frequencies. Please note that you will need a Vector Network Analyzer (VNA) to build this project!

![Antenna set example picture](/Pictures/01_Cage.jpg)
An example of using a set of antennas to find a wall problem. 

Antennas could be used with any type of 50 Ohm RF equipment to perform measurements. In general, antenna #1 is connected to the signal generator and antenna #2 is connected to the receiver (spectrum analyzer, SDR, etc.). Of course, one antenna should be placed inside the cage and the other outside. The MRI scanner itself can also be used as a signal source. In this case, one antenna is sufficient.

![Measurements example picture](/Pictures/02_Tests.jpg)
In the left photo, one antenna is placed on a tripod inside the room and connected to a signal generator. After closing the door, you can check with another antenna how much the signal will decrease in value (attenuation measurement). In the right photo, a HackRF shows an MRI signal outside the RF cage. The door insulation is certainly  damaged in this case.

# Building instructions

