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








 


