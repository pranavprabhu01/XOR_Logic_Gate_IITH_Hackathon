# XOR_Logic_Gate_IITH_Hackathon
CMOS Implementation of XOR Logic gate using Synopsys Custom Compiler
## Table of Contents
* [Introduction](#Introduction)
* [Reference Circuit](#Reference-Circuit)
* [Reference Waveform](#Reference-Waveform)
* [Tools Used](#Tools-Used)
* [Schematic in Synopsys](#Schematic-in-Synopsys)
* [Symbol in Synopsys](#Symbol-in-Synopsys)
* [Testbench in Synopsys](#Testbench-in-Synopsys)
* [Source A in Synopsys](#Source-A-in-Synopsys)
* [Source B in Synopsys](#Source-B-in-Synopsys)
* [Waveform in Synopsys](#Waveform-in-Synopsys)
* [Netlist in Synopsys](#Netlist-in-Synopsys)
* [Conclusion](#Conclusion)
* [Acknowledgement](#Acknowledgement)
* [References](#References)

## Introduction
The XOR gate will be built with six CMOS transistors. Out of which three will be PMOS transistors and other three will be NMOS transistors.The transistors are implemented using 28nm technology.
As seen in reference circuit , when A=0 and B=0, transistor M1,M2 and M4 are on. This results in output Y=0. When A=0 & B=1, transistor M2,M3 and M4 are on which generates output Y=0. When A=1 & B=0, only transistor M1 is on resulting in output Y=1.When A=1 & B=1, only transistor M3 is on resulting in output Y=0. The process is 28nm. So λ=14nm.
This circuit can be used in full adders and half adders. It is also used in parity generator and checker. Two XOR gates connected in such a way that output of one XOR gate is the input of the other XOR gate, the circuit behaves as a three-bit generator.

## Reference Circuit
![image](https://raw.githubusercontent.com/pranavprabhu01/XOR_Logic_Gate_IITH_Hackathon/main/Images/sample_ckt.png)

## Reference Waveform
![image](https://raw.githubusercontent.com/pranavprabhu01/XOR_Logic_Gate_IITH_Hackathon/main/Images/sample_wave.png)

## Tools Used
* Synopsys Custom Compiler
* Synopsys PrimeWave
* Synopsys 28nm PDK

## Schematic in Synopsys
![image](https://raw.githubusercontent.com/pranavprabhu01/XOR_Logic_Gate_IITH_Hackathon/main/Images/schematic.png)

## Symbol in Synopsys
![image](https://raw.githubusercontent.com/pranavprabhu01/XOR_Logic_Gate_IITH_Hackathon/main/Images/symbol.png)

## Testbench in Synopsys
![image](https://raw.githubusercontent.com/pranavprabhu01/XOR_Logic_Gate_IITH_Hackathon/main/Images/tb_sch.png)

## Source A in Synopsys
![image](https://raw.githubusercontent.com/pranavprabhu01/XOR_Logic_Gate_IITH_Hackathon/main/Images/source_A.png)

## Source B in Synopsys
![image](https://raw.githubusercontent.com/pranavprabhu01/XOR_Logic_Gate_IITH_Hackathon/main/Images/source_B.png)

## Waveform in Synopsys
![image](https://raw.githubusercontent.com/pranavprabhu01/XOR_Logic_Gate_IITH_Hackathon/main/Images/waveform.png)
Here the red colour wave represents source A, violet colour wave represents source B and green colour wave represents the output.

## Netlist in Synopsys
1   *  Generated for: PrimeSim
2   *  Design library name: cp_lib1
3   *  Design cell name: cp_xor_tb
4   *  Design view name: schematic
5   .lib 'saed32nm.lib' TT
6   
7   *Custom Compiler Version S-2021.09
8   *Thu Feb 24 13:49:44 2022
9   
10  .global gnd! vdd!
11  ********************************************************************************
12  * Library          : cp_lib1
13  * Cell             : cp_xor
14  * View             : schematic
15  * View Search List : hspice hspiceD schematic spice veriloga
16  * View Stop List   : hspice hspiceD
17  ********************************************************************************
18  .subckt cp_xor a b y gnd_1 supply vt_bulk_n_gnd! vt_bulk_p_vdd!
19  xm21 y net40 net48 vt_bulk_n_gnd! n105 w=0.1u l=0.03u nf=1 m=1
20  xm11 net40 a gnd_1 vt_bulk_n_gnd! n105 w=0.1u l=0.03u nf=1 m=1
21  xm20 y net48 net40 vt_bulk_n_gnd! n105 w=0.1u l=0.03u nf=1 m=1
22  xm22 y a b vt_bulk_p_vdd! p105 w=0.1u l=0.03u nf=1 m=1
23  xm8 net40 a supply vt_bulk_p_vdd! p105 w=0.1u l=0.03u nf=1 m=1
24  xm19 y b a vt_bulk_p_vdd! p105 w=0.1u l=0.03u nf=1 m=1
25  .ends cp_xor
26  
27  ********************************************************************************
28  * Library          : cp_lib1
29  * Cell             : cp_xor_tb
30  * View             : schematic
31  * View Search List : hspice hspiceD schematic spice veriloga
32  * View Stop List   : hspice hspiceD
33  ********************************************************************************
34  xi0 a b y gnd! net6 gnd! vdd! cp_xor
35  v2 net6 gnd! dc=1.8
36  v4 b gnd! dc=0.01 pulse ( 01.8 0 0.1n 0.1n 0.1n 2u 4u )
37  v3 a gnd! dc=0.01 pulse ( 1.8 0 0.1n 0.1n 0.1n 1u 2u )
38  r8 y gnd! r=1k
39  
40  
41  
42  
43  
44  
45  
46  
47  .tran '0.1u' '20u' name=tran
48  
49  .option primesim_remove_probe_prefix = 0
50  .probe v(*) i(*) level=1
51  .probe tran v(a) v(b) v(y)
52  
53  .temp 25
54  
55  
56  
57  .option primesim_output=wdf
58  
59  
60  .option parhier = LOCAL
61  
62  
63  
64  
65  
66  
67  .end
68  







 


