# CMOS Implemented NOR Gate
CMOS Implemented NOR Gate is designed using Synopsys custom design tools.

## Table of Contents

-  [Abstract](https://github.com/Sidshx/CMOS-NOR-Gate_IITH-Hackathon/blob/main/README.md#abstract)
-  [Reference Circuit](https://github.com/Sidshx/CMOS-NOR-Gate_IITH-Hackathon/blob/main/README.md#reference-circuit)
-  [Reference Circuit Details](https://github.com/Sidshx/CMOS-NOR-Gate_IITH-Hackathon/blob/main/README.md#reference-circuit-details)
-  [Reference Waveform](https://github.com/Sidshx/CMOS-NOR-Gate_IITH-Hackathon/blob/main/README.md#reference-waveform)
-  [Tools Used](https://github.com/Sidshx/CMOS-NOR-Gate_IITH-Hackathon/blob/main/README.md#tools-used)
      - [Synopsys Custom Compiler](https://github.com/Sidshx/CMOS-NOR-Gate_IITH-Hackathon/blob/main/README.md#synopsys-custom-compiler)
      - [Synopsys Primewave](https://github.com/Sidshx/CMOS-NOR-Gate_IITH-Hackathon/blob/main/README.md#synopsys-primewave)
      - [Synopsys 28nm PDK](https://github.com/Sidshx/CMOS-NOR-Gate_IITH-Hackathon/blob/main/README.md#synopsys-28nm-pdk)
-  [Synopsis Simulation](https://github.com/Sidshx/CMOS-NOR-Gate_IITH-Hackathon/blob/main/README.md#synopsis-simulation)
      - [Schematic](https://github.com/Sidshx/CMOS-NOR-Gate_IITH-Hackathon/blob/main/README.md#schematic)
      - [Symbol](https://github.com/Sidshx/CMOS-NOR-Gate_IITH-Hackathon/blob/main/README.md#symbol)
      - [Testbench Symbol](https://github.com/Sidshx/CMOS-NOR-Gate_IITH-Hackathon/blob/main/README.md#testbench-symbol)
      - [Input A Parameters](https://github.com/Sidshx/CMOS-NOR-Gate_IITH-Hackathon/blob/main/README.md#input-a-parameters)
      - [Input B Parameters](https://github.com/Sidshx/CMOS-NOR-Gate_IITH-Hackathon/blob/main/README.md#input-b-parameters)
      - [Testbench Settings](https://github.com/Sidshx/CMOS-NOR-Gate_IITH-Hackathon/blob/main/README.md#testbench-settings)
      - [Primewave Parameters](https://github.com/Sidshx/CMOS-NOR-Gate_IITH-Hackathon/blob/main/README.md#primewave-parameters)
      - [Netlist](https://github.com/Sidshx/CMOS-NOR-Gate_IITH-Hackathon/blob/main/README.md#netlist)
      - [Testbench Waveform](https://github.com/Sidshx/CMOS-NOR-Gate_IITH-Hackathon/blob/main/README.md#testbench-waveform)
-  [Acknowledgement](https://github.com/Sidshx/CMOS-NOR-Gate_IITH-Hackathon/blob/main/README.md#acknowledgement)
-  [References](https://github.com/Sidshx/CMOS-NOR-Gate_IITH-Hackathon/blob/main/README.md#references)
      
## Abstract
NOR gate is a universal gate. It is a logically inverted version of the basic OR gate. In this implementation it has two inputs (A & B) with an output (Y). Its logical equation is derived as Y=(A+B)'.
The popular CMOS (Complementary-metal-oxide-semiconductor) technology is also implemented to design this NOR gate.

## Reference Circuit
![Circuit1](https://user-images.githubusercontent.com/73933646/156177339-7796f397-0267-478d-b425-a2f06cd5e16c.jpg)



## Reference Circuit Details
CMOS NOR gate has 2 PMOS transistors connected in series with one another, which is then connected in series to 2 parallelly connected NMOS transistors. Transistors PMOS1 and NMOS1 work as a complementary pair, as do transistors PMOS2 and NMOS2. Each pair is controlled by a single input signal (A and B respectively). 
The output of the CMOS NOR gate goes HIGH only when both inputs (A & B) are low, both the lower transistors get in Cutoff mode and both the upper transistors get Saturated. 
Otherwise, if either input A or input B is high, at least one of the lower transistors (NMOS1 or NMOS2) gets saturated making the output low.

 ### Truth Table
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
![testbenchsymbol](https://user-images.githubusercontent.com/73933646/156192712-55dd291a-77ce-480f-97de-81f90e7f7d4c.png)



* ### Input A Parameters
![inputA](https://user-images.githubusercontent.com/73933646/156192523-aef77901-b7c4-4309-a3cc-bd7fd773fbe5.png)



* ### Input B Parameters

![inputB](https://user-images.githubusercontent.com/73933646/156192559-e60934f7-faf1-459f-8e59-c2c96a6f0190.png)



* ### Testbench Settings
![testbenchsettings](https://user-images.githubusercontent.com/73933646/156192011-68489baf-458f-493d-ae91-94fcc607c717.png)


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
* [Chinmaya Panda, IIT Hyderabad](mailto:chinmaya.panda@ee.iith.ac.in)
* Sameer Durgoji, NIT Karnataka

## References

[1].[https://www.researchgate.net/publication/316548029_Analysis_of_CMOS_based_NAeND_and_NOR_Gates_at_45_nm_Technology](https://www.researchgate.net/publication/316548029_Analysis_of_CMOS_based_NAeND_and_NOR_Gates_at_45_nm_Technology)

[2].[https://www.allaboutcircuits.com/textbook/digital/chpt-3/cmos-gate-circuitry/](https://www.allaboutcircuits.com/textbook/digital/chpt-3/cmos-gate-circuitry/)




