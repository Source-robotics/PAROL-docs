# Getting started

## Assembly manual

Assembly manual is located in [Github](https://www.mkdocs.org) repository. <br />
Of course to use the robot you will have to build/buy it. If you decide to build it or buy a kit you will need to follow the assembly manual to make it. Assembly manual is also great tool for reparing and upgrading your robot. Make sure you use the latest version of the manual. Version is marked on the first page in the bottom left corner.

<p align="center">
<img src="../assets/manual.png" alt="drawing" width="800"/> <br />
</p>

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

### Couplers and threadlocker


## Complete step by step guide!