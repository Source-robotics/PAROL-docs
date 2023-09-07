# Software

 To operate PAROL6 robot you need a:<br />

 * High level software running on your PC
 * Low level software running on PAROL6 control board

 For high level software there are multiple options:

 * Use PAROL6 commander software for control, programming, simulating
 * Use our API to send command thur your languange of choice Matlab, python, c++
 * Use ROS

 For low level software only PAROL6 control board software is available.
 PAROL6 commander software allows you to write simple robot arm scripts. Scripting language is called 

## Communication protocol

The default communication method used by our robots is over USB.
PAROL6 uses serial USB communication to talk between high and low level code. 

The protocol consists of three types of commands. Active, passive and carrier. Active commands can only be given by the "command" argument and is represented by one byte. Thwt means there can only be 255 commands. Passive commands are for example io commands and gripper commands. They are always sent with the data packet. Passive commands do not affect movement of the robot joints and by that can be injected in any active command. Carrrier commands are joint speeds and positions that are modifiers for active movement commands.

## PAROL6 commander software

It is devided in multiple files:
xxx
xxx
xxx



### Structure

<p align="center">
<img src="../assets/proces_full.png" alt="drawing" width="2000"/>
</p>

### Dependancy

### How to run / Install

## PAROL6 control board software

Structure of the code:


### Code upload to PAROL6 control board software
To upload code on your PAROL6 board you need a programming cable and stlink device

## Commander software API 

### RBTscript

PAROL6 commander software allows you to write simple robot arm scripts. Scripting language is called RBTscript. RBTscript allows you to move the robot in joint space or cartesian space, use delay functions, control outputs and grippers, read inputs and much more!

### Introduction

### Functions



