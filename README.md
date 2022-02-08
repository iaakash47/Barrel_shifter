# Barrel shifter
* This project focuses on design of a 8x4 right Barrel Shifter using NMOS pass transistor logic using Google Skywater (sky130) Technology node with operating voltage of 1.8V and 3.3V. The project is build using Open Source Tools like Sky130PDK and eSim and Ngspice. Refer following website for more details on Barrel Shifter:https://en.wikipedia.org/wiki/Barrel_shifter
 
# Table of Contents

1. [Introduction](#Introduction)
2. [Installation of the tools](#installation-of-the-tools)
3. [Methodology](#Methodology)
    - [Step1 Construct AND Gate](#step1-construct-and-gate)
    - [Step2 Construct XOR Gate](#Step2-Construct-XOR-Gate)
    - [Step3 Construct Half Adder](#step3-construct-half-adder)
    - [Step4 Construct Full Adder](#step4-construct-full-adder)
    - [Step5 Construct 3-Bit Wallace Multiplier](#step5-construct-3-bit-wallace-multiplier) 
4. [Results](#results)
    - [Command Window](#command-window)
    - [Obtained Output Waveforms](#obtained-output-waveforms)
5. [References](#references)
6. [Author](#author)

# Introduction 
#### Barrel Shifter 
* Barrel Shifter is a digital circuit that can shift a data word by a specified number of bits without the use of any sequential logic, only pure combinational logic, i.e. it inherently provides a binary operationimportant function to optimize the RISC processor, so it is used for rotating and transferring the data either in left or right direction. This shifter is useful in lots of signal processing ICs. The Arithmetic and the Logical Shifters additionally can be changed by the Barrel Shifter Because with the rotation of the data it also supply the utility the data right, left change all mathemetically or logically.A purpose of this project is to design the CM with the help of CMOS using NMOS Pass Transistor logic.CMOS based 8 bit barrel shifter has implemented in this project using eSim and Ngspice tools using skywater 130nm PDKs Tech lib files 









# Opensource Tools used

1. eSim: eSim (previously known as Oscad / FreeEDA) is a free/libre and open source EDA tool for circuit design, simulation, analysis and PCB design developed by FOSSEE, IIT Bombay. It is an integrated tool    built using free/libre and open source software such as KiCad, Ngspice and GHDL. eSim is released under GPL. eSim offers similar capabilities and ease of use as any equivalent proprietary software for schematic creation, simulation and PCB design, without having to pay a huge amount of money to procure licenses. Hence it can be an affordable alternative to educational institutions and SMEs. It can serve as an alternative to commercially available/licensed software tools like OrCAD, Xpedition and HSPICE. For more info refer: https://esim.fossee.in/home

2. Ngspice: Ngspice is the open source spice simulator for electric and electronic circuits. Ngspice offers a wealth of device models for active, passive, analog, and digital elements. Model parameters are provided by the semiconductor manufacturers. The user add her circuits as a netlist, and the output is one or more graphs of currents, voltages and other electrical quantities or is saved in a data file. For more info refer: http://ngspice.sourceforge.net/

3. Skywater Pdk: The SkyWater Open Source PDK is a collaboration between Google and SkyWater Technology Foundry to provide a fully open source Process Design Kit and related resources, which can be used to create manufacturable designs at SkyWater’s facility. As of May 2020, this repository is targeting the SKY130 process node. If the SKY130 process node release is successful then in the future more advanced technology nodes may become available. For more info refer: https://github.com/google/skywater-pdk, https://skywater-pdk.readthedocs.io/en/latest/

Clone this repository using the following commands:
```
$ sudo apt install -y git
$ git clone https://github.com/iaakash47/Barrel_shifter.git
```
# Installation Instructions

## eSim Installation
 Refer the following websites for installation of eSim :
 - https://static.fossee.in/esim/installation-files/Install_eSim_on_Windows.pdf
 - https://github.com/FOSSEE/eSim/blob/master/INSTALL
 
## Ngspice Installation
Ngspice gets installed alongwith eSim. If any other version ids to be installed refer: http://ngspice.sourceforge.net/download.html

## Skywater Pdk Installation(Ubuntu)
Open the terminal and follow these steps:
```
git clone git://opencircuitdesign.com/open_pdks
cd open_pdks
./configure --enable-sky130-pdk
make
sudo make install
```
