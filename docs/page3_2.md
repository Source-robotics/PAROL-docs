# Getting started

## Assembly manual

Assembly manual is located in [Github](https://www.mkdocs.org) repository. <br />
Of course to use the robot you will have to build/buy it.  <br />
If you decide to build it or buy a kit you will need to follow the assembly manual to make it.  <br />
Assembly manual is also great tool for reparing and upgrading your robot. Make sure you use the latest version of the manual. <br />
Version is marked on the first page in the bottom left corner.



## Powering on 

<p align="center">
<img src="../assets/Connectors.png" alt="drawing" width="900"/>
</p>

PAROL6 requires 3 connections for normal operation.

* Power connection -> Marked green on image

* USB connection -> Marked blue on image

* ESTOP -> Marked with yellow and pink squares

First connect power cable (marked green). After that you can turn robot on and off by pressing power button (marked red).

## Powering off

!!! Danger annotate "Do not try to power off the robot when it is running!"

    ** If robot start to behave unexpectedly USE ESTOP.** <br />
    ** If ESTOP is not functional power of the supply.**<br />
    ** Reaching for the power button should be the last option.**

Because lack of brakes sudden loss of power will result in robot falling down. That may cause damage to the robot or the operator.
Robot is powered on and off by pressing a button marked red on the image. When powering the robot on even when USB connection is not available it will energise the
the motors. It will produce 6 clicking sounds and that is normal behaviour.<br />

Powering off the robot is also done by pressing button marked in RED. Before you power off the robot **GRAB IT BY THE FOREARM** and then press the button. This will ensure that robot does not fall down. **THESE STEPS ARE MANDATORY** Failing to do so will damage your robot!


## Installing PAROL6 commander software

Commander software can be located in [Github](https://github.com/PCrnjak/PAROL-commander-software) repository. <br />
Some prerequisites you will need to have are: <br />

* python <br />
* pip3 <br />

Commander software was tested on machines with these specifications: <br />

* Windows 10, Ryzen 5, 32gb ram, Nvidia 3060  <br />
* Windows 10,  <br />


## PAROL6 control board 

!!! Warning annotate "Warning"

    When uploading code with stlink to the robot DISCONNECT THE 24V supply from the robot.<br />
    After the code is uploaded disconnect the stlink and connect power supply. 

Look at the PAROL6 control board page.

## First startup

When first starting the robot biggest and most common problem is that motors will turn in different directions from those they were supposed to move. There are 2 ways to fix this: <br />
* Open the robot base and replace wires of one of the stepper motor phases <br />
* RECOMMENDED; Upload a new code to PAROL6 control board with small changes to the code

If you are going with code edit solution you will need to edit these segments of code:
xxxxx
xxxxx

Another problem that is not so critical when starting up is that your joints are not calibrated. That means that robot thinks it is some position but in reality it is not. This problem accours because of different tolerances of printed parts, different belt tensions, different bearing preload... <br />
It can be fixed by looking at a motor_init.cpp file for PAROL6 control board. In that file you can find bunch of paremeters for robots motors. One we need is called "direction_reversed" For joint that are moving in wrong direction change the value of that variable if it was 1 to 0 and if it was 0 to 1.


## Quick start guide

* attach the robot to table or workstation.
* Make sure you have driver board that has firmware on it!
* Connect power supply and USB to your robot.
* Test if you can move your robots joints freely.
* Move the robot close to the position shown on the image. 
* Press the power button. Power button locks all the joints to the current position.
* After power button is pressed you can turn on commander software.
* After the commander software started you will see 2 windows: Simulator window and GUI window
* Simulator will not be calibrated to the robot and GUI will display wrong joint and cartesian coordinates.
* Go to joint jog menu and try to jog the motors.
* Arrows pointing to the left represent negative rotation of the joint and arrows pointing to the right positive.
* Positive and negative rotations of the joints are shown on the image below
* Comfirm that every joint moves coresponding joint in right direction. If not fallow the above guide to calibrate it.
* Once you adjusted your joint rotations repet all the previous steps and confirm correct rotations.
* Press the home button. All joints of the robot will start to move. Be close to the estop of the robot in case the estops stop working or robot crashed. If you hear grinding noise when robot is close to the limit switch press the estop emediately.
That means your estop for that joint is not working and you need to check your wiring.
* If the robot homes correctly it will be in this position. Small deviations are ok since your robot is still not calibrated 
* Simulator is now sinced to the robot and GUI shows correct values.
* Congrats you have a functional PAROL6 robot to work with!


## Maintenance

### Belts

We recommend to periodically check your belt tension and apply greese to the belts. If you see that the belt is not tight enough place another tension bearing as shown in the pictures. 

Belts are located on Joints: 1,3,4,5

<p align="center">
<img src="../assets/belt1.jpg" alt="drawing" width="800"/> <br />
</p>
<p align="center">
<img src="../assets/belt2.jpg" alt="drawing" width="800"/> <br />
</p>
<p align="center">
<img src="../assets/belt3.jpg" alt="drawing" width="800"/> <br />
</p>

### Couplers and threadlocker

