# Collection of data from water bodies by the use of Remotely Operated Underwater Vehicle

> [!NOTE]
> The full text of the team's poster, the official submission to the East Zone A\*STAR Science
> Fair 2016, transcribed from [the PDF](VJC%20Science%20Fair%20Challenge%20Final.pdf) as written.
> Back to the [README](README.md).

**By Victoria School**

**Members:** Ivan Feng, Rubesh Suresh, Syed Wazir, Wayne Yeo

## Abstract

This is a project that hopes to create an affordable remotely operated underwater vehicle (ROV) to
frequently monitor water bodies. It aims to alleviate the damage caused by harmful algal blooms
through alerting the fish farmers of inclement aquatic conditions. Such conditions are
characterised by alkaline pH levels of about 8.2 to 8.8 with warm temperatures between 25 to 30
degree Celsius. The process of creating the ROV included relevant technologies such as the use of
the Arduino platform and the C programming language. Additionally, it requires an understanding of
electronics and practical skills such as soldering and working with PVC and acrylic. Through the
process of creating our own ROV, we now have a customisable platform to navigate and detect the
conditions of water bodies. Using the school pond as a sample testbed, we have proven its ability
to report the condition of the aquatic habitat to users.

## Introduction

This project puts together an underwater Remotely Operated Vehicle (ROV) with the purpose of
aquatic data collection. It had been chosen because of the recent death of many fishes in the
water around Singapore that cost millions of dollars (The Straits Times, Jan 2010, Feb 2014, Mar
2015) due to algal bloom. Existing methods of data collection to monitor water conditions uses a
mobile network of sensors such as ships, fixed instruments and kayaks (Peng Lim and Sandric,
2012). However this might not be able to provide timely checks for local fishermen to react upon.
Our project aims to implement an ROV that allows frequent monitoring of water conditions to be
conducted over long distances by reducing the cost and manpower incurred by existing monitoring
system. This will provide an affordable system that local fisherman can rely upon. In this
project, we use our school pond as the sample condition for our investigation.

## Theoretical Background

Before the purchase of materials, calculations were made to ensure that the functionality of the
parts would fit well to our ROV. For example, there was the calculation for upward thrust using
the Archimedes' Principle that thrust = acceleration due to gravity x volume of the displaced fluid
x density of fluid. From the calculation, we have estimated the minimum size required for our
enclosed PVC pipe. To avoid the turning effect while travelling in a straight line, the two
forward motors were located along the horizontal line of the centre of mass and were evenly spaced
apart from it as well. The four downward motors were placed along the centre of the acrylic plates
at the four corners for even descent and tilting of the ROV. To increase the waterproofing of our
capsule, suitable silicone sealant and rubber o-ring were chosen to seal all possible leakages of
our ROV. Our project will provide an alternative mean of convenient monitoring of underwater data
such as pH level and water temperature, which are the two factors that contribute to algal bloom.
From our research, we have found out that warm environment and increase in pH level could cause
eutrophication leading to algal bloom (University of Maryland Centre for Environmental Science,
PNG file).

## Procedure

Our motivation to create an ROV was to ensure customisability and robustness for observation and
data collection.

**Sensors.** For now, the ROV can collect data of water temperature and pH level. The ROV has a
temperature and pH sensor to quantitatively measure the two variables that seem to affect algal
bloom. However, the ROV can be outfitted with a variety of different sensors depending on the
required application.

**Data Logger.** The datalogger is linked to the sensors and will plot a graph to detect trends of
the pH level and temperature of its surroundings.

**Arduino Mega.** The Arduino will execute the code to operate the 6 motors. The Arduino provides a
low-level C runtime to control the 6 motors. There is a wide range of shields and compatible
sensors for this platform, and it can be scaled up to communicate with an onboard computer such as
a Raspberry Pi for future navigation and observation, which include a camera and GPS.

**Acrylic Flanges.** The flanges of the submarine are made of acrylic sheets and are used as a
surface for attaching thrusters and fastening the housing.

**Acrylic Pipe.** The 5-inch acrylic rods are used to fix the acrylic flanges on the sides of the
housing to the housing by screwing it into the acrylic flanges.

**Lithium Polymer Battery.** There are power requirements to be met. A battery or batteries must be
sufficient for motor control and the core computing devices. In the case there is mains
electricity nearby, we cannot discount the possibility that we just attach a 12V/3A breakout to
power the setup. We chose a lithium polymer battery because of its high charge density; our two
batteries can provide 2500mAh per cycle. We decided against NiCad and lead-acid batteries due to
potential toxicity and low current output that is not suitable for powering our motors.

**PVC Housing.** The housing of the submarine was intended to contain all electrical components
that control the submarine and relay the information to the surface computer and had to be
designed to be stiff. The selection for the housing was a hard PVC tube of 10cm inner diameter,
12.5cm outer diameter, and 50cm in length. Hard PVC has a maximum tensile stress of 5003.8 psi
before failure, which was deemed as acceptable for our limited application.

**Motors.** We chose brushless direct current (BLDC) motors for a few reasons. Firstly, carbon
brushes wear out over time, and eliminating the brushes would make the ROV's operation more
reliable. Secondly, carbon brushes would short underwater, the use of a spinning magnetic field to
drive a BLDC means that it can function in an aquatic medium without waterproofing.

## Results and discussion

**Fig. 1: Temperature of School pond** (°C, either side of the bridge)

| Area A | Area B |
|---|---|
| 28.1, 28.2, 28.3, 28.3 | 27.3, 27.3, 27.3, 27.5 |

**Fig. 2**

| Location | pH Level |
|---|---|
| School Pond | 8.5 - 8.9 |
| East Coast Park (ECP) | 8.9 - 9.2 |
| Tap Water | 8.8 |
| Sea water at ECP | 6.4 - 6.7 |

**Fig. 3** (taken from http://www.fishlore.com/)

| Fish Species | pH level |
|---|---|
| Pacu | 6.5 - 7.5 |
| Koi | 7.0 - 8.6 |
| Silver Arowana | 7.0 - 7.5 |

Fig. 1 shows that the average temperature of area A is about 28.2 degree celsius which is 0.8
degree celsius higher than Area B of 27.4 degree celsius. Area A is where the school pond has a
higher growth of algae. Base on our observation, the higher temperature of water, between 25 to 30
degree celsius (Singh & Singh, 2015), leads to better growth of algae.

From Fig 2, we realise that the pH level of the school is not suitable for the different fish
species in the pond. We also found out that the optimum condition for algae growth is 8.2 - 8.8
(FAO, 1991) which is a range that the pH level of our school pond falls within thereby explaining
the numerous deaths of fishes in the school pond.

## Conclusion

Our preliminary design of the ROV enabled us to have a device that can monitor the pH level and
temperature of the water at a frequent rate with little manpower and cost incurred compared to
existing measures. Future development would be to add on more sensors to the Arduino ports (test
salinity, turbidity, dissolved oxygen level), program the ROV to navigate through the water
autonomously, remotely control our ROV by connecting the Arduino board to the Raspberry Pi, and to
install a camera which could capture images of the water. All of these additions will enable us to
refine our research as it would give us a deeper insight of the condition of our pond by informing
us of the correlation between different aquatic factors if any exist and by simply providing us
with more data that we can work with.

## References

- Nur Asyiqin Mohamad Salleh. (2014, February 11). Pasir Ris mass fish deaths may lead to over $1
  million loss for farmers. The Straits Times. Retrieved July 24, 2016, from
  http://www.straitstimes.com/singapore/pasir-ris-mass-fish-deaths-may-lead-to-over-1-million-loss-for-farmers
- Kash Cheong (2015, March 1). Mass fish deaths overnight hit Changi farmers hard. The Straits
  Times. Retrieved July 24, 2016, from
  http://www.straitstimes.com/singapore/environment/mass-fish-deaths-overnight-hit-changi-farmers-hard
- Melissa Sim. (2010, January 2). Plankton bloom hits Pulau Ubin fish farms. The Straits Times.
  Retrieved July 24, 2016, from http://www.straitstimes.com/Singapore/Story/STIStory_472705
- Peng Lim, Lay and Sandric Leong. "Harmful Algal Blooms In Singapore Coastal Waters". National
  University of Singapore. May 27, 2012. Presentation.
- Wicks, Caroline. Environmental conditions that lead to harmful algal blooms. University of
  Maryland Centre for Environmental Science, PNG file.
- Singh, S. P., & Singh, P. (2015). Effect of temperature and light on the growth of algae species:
  a review. Renewable and Sustainable Energy Reviews, 50, 431-444.
- Food and Agricultural Organisation of the United Nations. (1991) "Algal production", Corporate
  Document Repository, Fisheries and Aquaculture Department. Retrieved July 24, 2016, from
  http://www.fao.org/docrep/003/w3732e/w3732e06.htm
