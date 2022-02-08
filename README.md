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
* Barrel Shifter is a digital circuit that can shift a data word by a specified number of bits without the use of any sequential logic, only pure combinational logic, i.e. it inherently provides a binary operation important function to optimize the RISC processor, so it is used for rotating and transferring the data either in left or right direction. This shifter is useful in lots of signal processing ICs. The Arithmetic and the Logical Shifters additionally can be changed by the Barrel Shifter Because with the rotation of the data it also supply the utility the data right, left change all mathemetically or logically.A purpose of this project is to design CMOS using NMOS Pass Transistor logic.CMOS based 8 bit barrel shifter has implemented in this project using eSim and Ngspice tools using skywater 130nm PDKs Tech lib files 









# Opensource Tools used

1. eSim: eSim (previously known as Oscad / FreeEDA) is a free/libre and open source EDA tool for circuit design, simulation, analysis and PCB design developed by FOSSEE, IIT Bombay. It is an integrated tool    built using free/libre and open source software such as KiCad, Ngspice and GHDL. eSim is released under GPL. eSim offers similar capabilities and ease of use as any equivalent proprietary software for schematic creation, simulation and PCB design, without having to pay a huge amount of money to procure licenses. Hence it can be an affordable alternative to educational institutions and SMEs. It can serve as an alternative to commercially available/licensed software tools like OrCAD, Xpedition and HSPICE. For more info refer: https://esim.fossee.in/home

2. Ngspice: Ngspice is the open source spice simulator for electric and electronic circuits. Ngspice offers a wealth of device models for active, passive, analog, and digital elements. Model parameters are provided by the semiconductor manufacturers. The user add her circuits as a netlist, and the output is one or more graphs of currents, voltages and other electrical quantities or is saved in a data file. For more info refer: http://ngspice.sourceforge.net/

3. Skywater Pdk: The SkyWater Open Source PDK is a collaboration between Google and SkyWater Technology Foundry to provide a fully open source Process Design Kit and related resources, which can be used to create manufacturable designs at SkyWater’s facility. As of May 2020, this repository is targeting the SKY130 process node. If the SKY130 process node release is successful then in the future more advanced technology nodes may become available.
For more info refer: https://github.com/google/skywater-pdk, https://skywater-pdk.readthedocs.io/en/latest/

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
 After Downloading eSim extract it choose the Directory to save the eSim Workspace 
 
 
 ## Creation of project 
 1.Click on the New Project and save the file name without any space 
 2.Project will be created 
 
 
 ## eSim Window 
 ![eSim](https://user-images.githubusercontent.com/88897605/152910524-9211a17b-02d8-45a5-a353-28dc422f83c6.png)
 
 
 
 ## eSim Schematic Window 
 ![eSimWindow](https://user-images.githubusercontent.com/88897605/152910659-23f4e30a-12d6-4d09-bb6f-732041acbe60.png)
 
 
 
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
Follow these steps for Sky130 download and implementaion :
1. Download sky130 from this link mentioned above and unzip it.
2. Save the .cir.out file in the sky_fd_pr folder as .cir file.
3. Open with notepad and add the path .lib "models/sky130.lib.spice" tt at the top.
4. Replace with CMOSP, mos_p with sky130_fd_pr_pfet_01v8 and CMOSN, mos_n with  sky130_fd_pr_nfet_01v8.
5. To replace inductor, capacitor, resistor do it this way, for Ex : L1 out gnd 1m by x1  out gnd mid 0 sky130_fd_pr__ind_03_90.

```
Note: For more details go to the cells folder in sky_fd_pr. 
Open the specific component folder which you want to use. 
Then open the test folder and check the SPICE file. 
The SPICE file is an example of implementation of that component. 
You will get to know how to use the component in your ckt.

```

6. Now Run the circuit with ngspice.

To Run the ckt using ngspice:
1. Replace with sky130nm cells and save this .cir file.
2. Paste the .cir file in gedit document where the sky130_fd_pr folder is present  
3. To Run the ngspice waveform,save the .cir file and replace with filename.spice  
4. Open Terminal in the saved Directory 
5. And run the following command(ngspice filename.spice)
- For reference to download the tools and get an exposure to simulation using eSim, ngspice and Sky130, you may want to check the course : [Link](https://www.udemy.com/share/104Ie63@EAkZWPY9P8VxMdqx7DK4NzA2SwmLzfA1pfjL_MLTmkTV9O283uXSWpJkSSNIPjmKmA==/)

# Reference Circuit 

CMOS transmission gates may be used in place of the simple pass transistor switches.In this project, a 8x4 right barrel shifter circuit using NMOS pass transistor logic is implemented in eSim with skywater 130nm technology. The shifter circuit takes 8 inputs bits and shifts them according to 5 control shift bits and generates 4 output bits
* Reference Circuit of Barrel Shifter is as shown below 
![IMG_20220208_081335](https://user-images.githubusercontent.com/88897605/152908383-16142e3f-ff9e-43f1-a74d-daa38e236ca8.jpg)

# Reference Waveform
* Reference Waveform of Barrel Shifter is as shown below
![IMG_20220208_080218](https://user-images.githubusercontent.com/88897605/152909514-24875fbc-b2d1-4c3b-b07e-6ff87d665af7.jpg)

