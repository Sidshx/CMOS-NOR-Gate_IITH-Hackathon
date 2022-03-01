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

* ### Schematic
![schematic](https://user-images.githubusercontent.com/73933646/156180203-68f4183c-df47-4034-8d09-2d8f9d122dbf.png)

* ### Symbol
![symbol](https://user-images.githubusercontent.com/73933646/156180261-8110779b-013e-443f-846b-eca8183853ea.png)

* ### Testbench Symbol
![Testbenchsymbol](https://user-images.githubusercontent.com/73933646/156180550-e0228830-43af-4efb-b98c-52b5a72657c3.png)

* ### Input A Parameters
![inputA](https://user-images.githubusercontent.com/73933646/156180671-881c898c-546a-4405-94cb-046e070a7fb7.png)


* ### Input B Parameters

![inputB](https://user-images.githubusercontent.com/73933646/156180760-3d778cc8-4c1a-4bb4-9c66-d1169e864df5.png)


* ### Testbench Settings
![tbsettings](https://user-images.githubusercontent.com/73933646/156180876-5ba24e34-c927-4d4e-9ea6-b7c732d0ae5b.png)

* ### Primewave Parameters
![primewaveparameters](https://user-images.githubusercontent.com/73933646/156180983-2d67ec1c-25b6-4dfa-8090-2269244eb073.png)

* ### Netlist

```
* Generated for: PrimeSim
* Design library name: CMOS_NOR
* Design cell name: 2_input_cmos_NOR_tb
* Design view name: schematic
.lib 'saed32nm.lib' TT

*Custom Compiler Version S-2021.09
*Sun Feb 27 14:09:15 2022

.global gnd! vdd!
********************************************************************************
* Library          : CMOS_NOR
* Cell             : 2_input_cmos_NOR
* View             : schematic
* View Search List : hspice hspiceD schematic spice veriloga
* View Stop List   : hspice hspiceD
********************************************************************************
.subckt _2_input_cmos_nor a b gnda vdd y vt_bulk_n_gnd! vt_bulk_p_vdd!
xm8 y b net4 vt_bulk_p_vdd! p105 w=0.1u l=0.03u nf=1 m=1
xm0 net4 a vdd vt_bulk_p_vdd! p105 w=0.1u l=0.03u nf=1 m=1
xm9 y b gnda vt_bulk_n_gnd! n105 w=0.1u l=0.03u nf=1 m=1
xm10 y a gnda vt_bulk_n_gnd! n105 w=0.1u l=0.03u nf=1 m=1
.ends _2_input_cmos_nor

********************************************************************************
* Library          : CMOS_NOR
* Cell             : 2_input_cmos_NOR_tb
* View             : schematic
* View Search List : hspice hspiceD schematic spice veriloga
* View Stop List   : hspice hspiceD
********************************************************************************
xi0 in_a in_b gnd! net26 out_y gnd! vdd! _2_input_cmos_nor
v16 net26 gnd! dc=1.8
c20 out_y gnd! c=1p
v18 in_b gnd! dc=0 pulse ( 0 1.8 0 0.1u 0.1u 10u 20u )
v17 in_a gnd! dc=0 pulse ( 0 1.8 0 0.1u 0.1u 5u 10u )








.tran '1u' '20u' name=tran

.option primesim_remove_probe_prefix = 0
.probe v(*) i(*) level=1
.probe tran v(in_a) v(in_b) v(out_y)

.temp 25



.option primesim_output=wdf


.option parhier = LOCAL






.end
```


* ### Testbench Waveform
![tbwaveform](https://user-images.githubusercontent.com/73933646/156181181-0295d543-e166-4b63-9ece-6d1a4b46a867.png)




## Acknowledgement
* [Synopsys India](https://www.synopsys.com/)
* [Kunal Ghosh, Co-founder, VSD Corp. Pvt. Ltd.](https://github.com/kunalg123)
* Cloud Based Analog IC Design Hackathon, IIT Hyderabad
* [Chinmaya Panda, IIT Hyderabad](chinmaya.panda@ee.iith.ac.in)

## References





