# PAROL commander GUI 

When you start PAROL6 commander software you will be met with 2 windows: 

* Commander window
* Simulator window

<p align="center">
<img src="../assets/GUI2.PNG" alt="drawing" width="2000"/> <br />
</p>

        Fig - commander window

<p align="center">
<img src="../assets/sim.PNG" alt="drawing" width="500"/> <br />
</p>

        Fig - simulator window

Commander window is used to Jog robot, read logs, write programs, home the robot...<br />
Simulator window is used to show your robot in real time.

!!! Note annotate "Note"

    Simulator only works if your robot is connected!

<p align="center">
<img src="../assets/connect.PNG" alt="drawing" width="2000"/> <br />
</p>

        Fig - Connect bar

At the bottom of commander software window you will see an entry bar and connect button. 

In the field next to the Connect button enter your serial com port.
* Windows: enter COMx (x represents your com port number)
* Linux: enter ttyACMx (x represents your com port number)

Clear error has same function as enable button.

Sim and real robot buttons have no function at the moment.

<p align="center">
<img src="../assets/GUI1.PNG" alt="drawing" width="2000"/> <br />
</p>

        Fig - cartesian jog

Cartesian jog is used to move robot in cartesian space. You can use  TRF frame or WRF frame. TRF is represented by axes on your end effctor while WRF is represented by axes on the robot base. 

!!! Note annotate "Note"

    When jogging in cartesian mode you WILL hit singularities. Go to general concepts tab on this webpage and read more about them! 

<p align="center">
<img src="../assets/GUI2.PNG" alt="drawing" width="2000"/> <br />
</p>

        Fig - joint jog

Joint jog is used to jog indivitial motors. LEFT IS POSITIVE DIRECTION RIGHT IS NEGATIVE DIRECTION!


<p align="center">
<img src="../assets/program_window.PNG" alt="drawing" width="2000"/> <br />
</p>

        Fig - program window

This window allows you to write robot scripts. Check the software tab to learn more about it!

<p align="center">
<img src="../assets/start_stop.PNG" alt="drawing" width="500"/> <br />
</p>

        Fig - start stop tab

You can start the execution of your programs by pressing start. By pressing stop the program will stop. 


<p align="center">
<img src="../assets/Commands.PNG" alt="drawing" width="350"/> <br />
</p>

        Fig - commands window

This window allows you to just select commands you want to use and click on them. They will appear in the program window. If using current positon/pose movement commands (MoveJoint, MovePose, SpeedJoint, MoveCart,MoveCartRelTRF, SpeedCart...) they will add current pose or joint position as arguments. Custom positon/pose will not add any values.

<p align="center">
<img src="../assets/response_log.PNG" alt="drawing" width="2000"/> <br />
</p>

        Fig - Response log
    
In the response log you will see error logs and active commands.


<p align="center">
<img src="../assets/robot_pos.PNG" alt="drawing" width="2000"/> <br />
</p>

        Fig - robot position

Here you can see the position of the robot joints and the position of end-effector in cartesian space. You can change the joint and cartesian space velocity with the slider. Home button will start homing your robot. Enable button will clear all errors and enable robot for operation. Disable will disable robot.

All we talked about was located in Move menu. All other menus will stay the same only the JOG MENUS will be replaced with another window! 

<p align="center">
<img src="../assets/IO_tab.PNG" alt="drawing" width="1700"/> <br />
</p>

        Fig - IO tab

Here you can check the state of your inputs and set the desired state to your outputs

<p align="center">
<img src="../assets/Settings_tab.PNG" alt="drawing" width="1700"/> <br />
</p>

        Fig - Settings tab

Here you can change GUI from dark to light mode and change the scaling to fit



<p align="center">
<img src="../assets/parol_grip_gui.PNG" alt="drawing" width="1700"/> <br />
</p>

        Fig - Gripper tab

Here you control and configure your gripper. After homing the robot press calibrate gripper button. <br />
Gripper will start to move and its status will change to calibrated. Press "clear gripper error". <br />
Now you can command gripper to go to the specific position with specific speed and torque. <br />

Set the setpoints with the sliders and press "Move GoTo"<br />
Under gripper feedback you will see gripper current and position feedback.<br />
You will also see what is status of the gripper. If it is in motion, detected object...


