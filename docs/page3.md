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


## First startup

When first starting the robot biggest and most common problem is that motors will turn in different directions from those they were supposed to move. There are 2 ways to fix this: <br />
* Open the robot base and replace wires of one of the stepper motor phases <br />
* RECOMMENDED; Upload a new code to PAROL6 control board with small changes to the code

If you are going with code edit solution you will need to edit these segments of code:
xxxxx
xxxxx

Another problem that is not so critical when starting up is that your joints are not calibrated. That means that robot thinks it is some position but in reality it is not. This problem accours because of different tolerances of printed parts, different belt tensions, different bearing preload... <br />
It can be fixed by doing xxxxxxxx


## Quick start guide

* attach the robot to table or workstation.
* 

## Complete step by step guide!