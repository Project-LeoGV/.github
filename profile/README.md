# Warehouse Robot

<div align="center" ><img width="100%" height="200%" alt="LeoGV" src=""></div>

Our Project is an Autonomous Warehouse Robot designed with the main goal of being mobile, capable of maneuvering around the warehouse, aware of its environment, powerful enough to carry heavy weights, and as inexpensive as possible to be deployed in vast numbers.

As a team, our primary goal was to build everything ourselves and learn as much as possible. This approach led us to develop all the software components, low-level MCAL and ECUAL drivers, and application codes for our microcontroller STM32G431 entirely from scratch in C. We also designed our own PCBs, which were manufactured in China and assembled by us.

## Main Features

### ROS2 
We used it to provide an interface for the robot such that the higher-level control algorithms used in manual and autonomous modes aren’t dependent on the hardware of the robot. And to test all that We built a simulation environment on Gazebo. 

### CAN 
We implemented CAN communication to facilitate data exchange between various Electronic Control Units (ECUs) within the robot. This ensures efficient and reliable communication among the different components.

### USB 
We utilized USB communication for interaction between the Raspberry Pi and the ECUs. This setup enables smooth data transfer and command execution, enhancing the overall system performance.

## Main components 
* RaspberryPi: The central processing unit of the robot. It is used to receive commands from the control station, control the robot as needed, and provide feedback to the station.
* USB To CAN: Bridge for the Raspberry Pi to communicate with other ECUs on the CAN bus. 
* Stepper driver: ECU for controlling the stepper motors with control of the motion of the upper plate.
* ODrive: ECU for controlling the brushless DC motors.
