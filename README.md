# CMOS Implemented NOR Gate
CMOS Implemented NOR Gate is designed using Synopsys custom design tools.

## Abstract
NOR gate is a universal gate. It is a logically inverted version of the basic OR gate. In this implementation it has two inputs (A & B) with an output (Y). Its logical equation is derived as Y=(A+B)'.

## Reference Circuit
![Circuit1](https://user-images.githubusercontent.com/73933646/156177339-7796f397-0267-478d-b425-a2f06cd5e16c.jpg)



## Reference Circuit Details
CMOS NOR gate has 2 PMOS transistors connected in series with one another, which is then connected in series to 2 parallelly connected NMOS transistors. Transistors PMOS1 and NMOS1 work as a complementary pair, as do transistors PMOS2 and NMOS2. Each pair is controlled by a single input signal (A and B respectively). 
The output of the CMOS NOR gate goes HIGH only when both inputs (A & B) are low, both the lower transistors get in Cutoff mode and both the upper transistors get Saturated. 
Otherwise, if either input A or input B is high, at least one of the lower transistors (NMOS1 or NMOS2) gets saturated making the output low.

![Truth Table](https://user-images.githubusercontent.com/73933646/156178214-c46a151e-1aa8-40e9-ae8b-416db6e690fe.png)



## Reference Waveform
![waveform1](https://user-images.githubusercontent.com/73933646/156177507-f84ead3d-c1b7-483e-84ef-c68123ff87b7.jpg)

## Tools Used

* ### Synopsys Custom Compiler
The Synopsys Custom Compiler™ design environment is a modern solution for full-custom analog, custom digital, and mixed-signal IC design. As the heart of the Synopsys Custom Design Platform, Custom Compiler provides design entry, simulation management and analysis, and custom layout editing features. 

* ### Synopsys Primewave
PrimeWave™ Design Environment is a comprehensive and flexible environment for simulation setup and analysis of analog, RF, mixed-signal design, custom-digital and memory designs within the Synopsys Custom Design Platform.

* ### Synopsys 28nm PDK
The 28nm Process Design Kits (PDKs) are designed for use in research and teaching of IC design. 

## Synopsis Simulation

* Schematic

* Symbol

* Testbench

* Input A Parameters

* Input B Parameters

* Testbench Settings

* Primewave Parameters

* Netlist

* Testbench Waveform

## Conclusion

## Acknowledgement

## References





