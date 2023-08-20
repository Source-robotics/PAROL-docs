# PAROL6 control board

<p align="center">
<img src="../assets/PAROL6_board.png" alt="drawing" width="800"/> <br />
</p>

## Introduction

PAROL6 control board is advanced 32-bit controller for 6 AXES robotic arms like PAROL6. It works out of the box with PAROL6 and PAROL6 commander software.

To use PAROL6 robotic arm you will need PAROL6 control board. PAROL6 control board is compact robotic controller. Its dimensions are 1x2x3 mm, that is little bigger then pack of playing cards. It allows PAROL6 to be really compact robot without the need of control cabinet that are usually the size of the whole robot. 

## Features

<p align="center">
<img src="../assets/Features.png" alt="drawing" width="800"/> <br />
</p>

### Hardware specs

TMC5160
* Silent control of 6 stepper motors
* Ability to adjust current, microstepping and more thru SPI!
* Can connect up to 6 limit switches or sensors.
* 1 x USB port and 2 x CAN bus
* 2 isolated Inputs
* 2 isolated Outputs
* Flash memory for saving programs and running them without external PC
* Connector for Power button
* Connector for Cooling fan
* Dedicated port for ESTOP


### Operating limits

* Power supply
* Stepper drivers
* Temperature
* Inputs 
* Outputs
* Fuse
* Cooling fan


## Physical properties

### Dimensions

!!! note

    ** Dimensions are in milimeters! **<br />

<p align="center">
<img src="../assets/PCB_dimensions.png" alt="drawing" width="800"/> <br />
</p>


### Mounting

3 Holes located on PAROL6 control board are used to mount the PCB. Use M3 screws!

### Cooling

Stepper drivers need cooling. It can be done with nocuta fan or any other 5V tolerant fan that fits the robot. In case of PAROL6 the fan needs to be of these dimensions.

Keep fan current draw around xx A.
Do not go over xx A.

### 3D models


## Connections

### Connectors

* 24 power connector on PAROL6 control board is XT30 MALE connector. 

* Connector for cooling fan on PAROL6 control is 

* Connector for power on/off button on PAROL6 control is 

* Connector for USB on PAROL6 control is



### Schematic

!!! note

    ** View schematic in PDF view. Images are hard to read! **<br />

Link to PDF schematic!

<p align="center">
<img src="../assets/Scheamtic_main.png" alt="drawing" width="2000"/> <br />
</p>

<p align="center">
<img src="../assets/Input_output_schematic.png" alt="drawing" width="2000"/> <br />
</p>

<p align="center">
<img src="../assets/Stepper_drivers_schematic.png" alt="drawing" width="2000"/> <br />
</p>

### Pin connections

<p align="center">
<img src="../assets/CONTROLLER.png" alt="drawing" width="800"/> <br />
</p>


### Pin definitions



### Stepper driver orientation

!!! Danger

    ** Only use step sticks that are verified in this document! **<br />
    ** Failing to do so will destroy your PAROL6 control board! **<br />

Stepper drivers need to be placed with respect to this diagram to the PAROL6 control board!<br />
Stepper drivers orientation can be recognised by 2 diagnostic pins!

<p align="center">
<img src="../assets/step_stick.png" alt="drawing" width="800"/> <br />
</p>


## Software

### How to upload code

Microcontroller on PAROL6 control board is STM32F446RE. To upload code you need to use STlink device and connect it dedicated CLK, SWDIO, 3V3 and GND pins. You can use jumper cables or dedicated stlink + cable assembly.

### PAROL6 control software structure

### API

## PCB revision history


## How to upload code



After sucesssful wiring of the robot it should look something like this. 

<p align="center">
<img src="../assets/control_board.jpg" alt="drawing" width="800"/> <br />
</p>



### PCB revision history