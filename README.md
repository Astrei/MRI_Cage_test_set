# MRI_Cage_test_set
This is an open-source 3d printed antenna set for magnetic resonance imaging (MRI) Faraday RF cages attenuation measurements. It is also suitable for localizing breaches in cage walls and sources of external RF interference. The set consists of two symmetrical magnetic loop antennas, each of which is equipped with six matching boxes for different MRI operating frequencies. Please note that you will need a Vector Network Analyzer (VNA) to build this project!

![Antenna set example picture](/Pictures/01_Cage.jpg)


# Examples of using
Antennas could be used with any type of 50 Ohm RF equipment to perform measurements. In general, antenna #1 is connected to the signal generator and antenna #2 is connected to the receiver (spectrum analyzer, SDR, etc.). The MRI scanner itself can also be employed as a signal source. In this case, one antenna would be sufficient.

![Measurements example picture](/Pictures/02_Tests.jpg)
In the left photo, one antenna is placed on a tripod inside the scanning room and connected to a signal generator. After closing the door, you can check with another antenna how much the signal will decrease in value (attenuation measurement). In the right photo, a HackRF shows an MRI signal outside the RF cage. The door insulation is certainly  damaged in this case.

![Interference example picture](/Pictures/02_Tests2.jpg)
It is also possible to use this antenna to find a source of external RF interference that affects your MR-image quality. In this example, an old power supply in the cabinet has some problems with electromagnetic compatability.


# Building instructions
The antenna element is made of rigid 3.5 mm coax cable. A semi rigid cable is also suitable for it, but it is not so mechanically stable, so I cannot recommend it.

![Antenna element](/Pictures/03_Antenna-element.jpg)

It's better to use some round object with a proper diameter as a base (a 3d printer plastic spool, for example). Just turn the cable around and fix it by soldering. Some copper foil could be helpful here. Manual adjustments are required to make a perfect circle. After this, cut the gap in the upper part by using side cutters. Leave ~40 mm of the cable in the bottom part for the SMA male connector:

![Antenna frame](/Pictures/04_Main_frame.jpg)

The antenna frame consists of two parts that should be glued together (Main_frame_P1 and P2). Label with my e-mail is optional and also on the glue. All the screws here are plastic M4. Nuts could be pressed into part 02_Main_frame_P1 with pliers.

![Antenna grip](/Pictures/06_Grip.jpg)

The grip is divided into two parts again, which must be glued. Parts 03_Main_frame_P2 and 04_Grip_P1 simply snap together and can be pulled apart if needed. The same story with the stands. Although the grip could be installed in some types of tripods, I found the 3d printed stand to be even more useful.

![Antenna matching box](/Pictures/05_Box.jpg)

In the original idea, there are six matching boxes for each antenna. But you can change this number depending on your needs. PCB outputs are SMA 1.6 mm. Here you also have to add some glue for the upper letters. If the top cover does not fit the box without a hammer, cut off its inner rigs with pliers. Thats all about the mechanical part. 

# Tuning instructions
The last step is the most complicated and for it you need to find a VNA.

![Antenna matching box](/Pictures/08_Matching2.jpg)

To match the antennas, I applied the basic L-network circuit. This requires only two elements. For the first three frequencies considered for low-field MRI application, these will be capacitors only. For higher frequencies it would be a combination of capacitors and handmade air inductors. Here are the reference values I got in my experiments:

![Antenna matching box](/Pictures/07_Matching.jpg)

Unfortunately, even if you accurately reproduce all dimensions of the coax element, there is no guarantee that the antenna will be tuned to the predicted frequencies with these values. For fine tuning, it is necessary to performe the matching using a VNA and Smith chart. 

![Antenna matching box](/Pictures/09_Smith.jpg)

You need to make sure that the operating frequency marker is in the center of the chart, which means perfect antenna matching. Thus, all element values shown above should be able to be changed. To do so, I combined constant capacitors with variables everywhere, or just used variables only (5-20 pF trimmers are perfect for this). Inductors can be tuned by slightly changing their shape through stretching/contraction. Hot glue can fix their value after the setting is completed. But be careful with the glue and the positioning of the inductors in general, as the space in the matching box is limited and the top needs to be covered after mounting the components.

Finally, you should get a complete antenna set ready to work!

![Antenna matching box](/Pictures/00_Photo.jpg)

