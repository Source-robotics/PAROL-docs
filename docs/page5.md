# Peripherals

<p align="center">
<img src="../assets/IMG1.png" alt="drawing" width="900"/>
</p>


## I/O connections

PAROL6 is equipped with 2 isolated inputs and 2 isolated outputs.
There are 


## CAN bus

!!! Tip annotate "Still under developement"

Can bus will allow you to connect external grippers and additional axes. <br />
There are 2 CAN buses.

## Pneumatics



## Estop

Connection is as follows:

<p align="center">
<img src="../assets/ESTOP_CON.png" alt="drawing" width="2300"/>
</p>

**Estop needs to be connected for normal operation of the robot**

!!! Note annotate "TIP"

    If you dont have an ESTOP you can use any NO switch!

!!! Note annotate "TIP2"

    On PAROL6 controller board there are connectors for 2 ESTOPS. They both share same GPIO on microcontroller.
    They both need to be NO contact. 

Estop needs to be NORMALLY CLOSED (NO) contact type. NC will not work.<br />
NO is beneficial in case your estop unplugs or gets its wires cut it will also register as a press of an estop, which is desirable behaviour.


