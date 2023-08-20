 
# Robot specifications

## Specs 

* Payload: 1 Kg
* Weight: 5.5 Kg
* Reach: 400 mm with the standard gripper
* Degrees of freedom: 6 rotating joints
* Material: 3D printed PETG plastic
* Power consumption: 40W
* Repeatability: 0.08 mm
* Precision: 
* Rotation range: 
- 1 – 250 deg
- 2 – 141 deg
- 3 – 180 deg
- 4 – 212 deg
- 5 – 180 deg
- 6 - ∞
* Motors: Steppers
* Gearboxes: precision planetary and bets
* Position sensing: Limit switches for open loop version, magnetic encoders for closed-loop version
* Drivers: Open-loop stepper drivers for open loop version, custom FOC Stepper drivers for closed-loop
* Number of isolated inputs: 2
* Number of isolated outputs: 2
* Number of CAN buses: 2
* Communication with master PC: USB 
* Pneumatic connectors: 2

## Dimensions

<p align="center">
<img src="../assets/Dimensions.png" alt="drawing" width="800"/> <br />
</p>

Dimensions using default pneumatic gripper!

|      |         |
| ----------- | ------------------------------------ |
| a1       | :material-check:     Fetch resource  | 
| a2      | :material-check-all: Update resource | 
| a3    | :material-close:     Delete resource |
| a4       | :material-check:     Fetch resource  | 
| a5       | :material-check-all: Update resource | 
| a6    | :material-close:     Delete resource |

!!! Note annotate "Dimensions can change!"

    For example when you change grippers or put robot on aditional base. <br />
    If that happens you need to change your parameters in DH table, otherwise you kinematic diagram will be wrong  <br />
    and as a result of that your Inverse kinematics and forward kinematic calculations resulting in corrupted trajectory <br />  planning and following!

## Kinematic diagram 

!!! Note annotate "TIP"

    If you dont have an ESTOP you can use any NO switch!

## Denavit-Hartenberg parameters


## Joint limits

Reduction ratios for each joint are as follows:

* Joint 1 -> Belt reduction: 6.4 : 1
* Joint 2 -> Planetary gearbox: 20 : 1
* Joint 3 -> Planetary gaerbox: 20 : 1 x Belt reduction 38 : 42 = 18.0952381
* Joint 4 -> Belt reduction: 4 : 1
* Joint 5 -> Belt reduction: 4 : 1
* Joint 6 -> Planterary gearbox: 10 : 1

Robot uses stepper motors. Microstepping is on all motors equal to 32. <br />
With 32 microstepping regular 200 steps per revolution stepper motor needs 6400 steps for one revolution.
For example limits of J2 are at -xx and xx. degree.
Joint limits are defined in degrees and steps. 


!!! Note annotate "TIP"

    If you dont have an ESTOP you can use any NO switch!

<p align="center">
<img src="../assets/rotations1.png" alt="drawing" width="800"/> <br />
</p>

Standby position is also defined in DH table above. 

| Joint      | Limit in negative direction        | Standby position| Limit in positive direction |
| ----------- | ------------------------------------ | -- | ------------------------------------ |
| J1       | :material-check:     Fetch resource  | -- | ---- |
| J2       | :material-check-all: Update resource | -- | ---- |
| J3    | :material-close:     Delete resource | -- | ---- |
| J4       | :material-check:     Fetch resource  | -- | ---- |
| J5       | :material-check-all: Update resource | -- | ---- |
| J6    | :material-close:     Delete resource | -- | ---- |