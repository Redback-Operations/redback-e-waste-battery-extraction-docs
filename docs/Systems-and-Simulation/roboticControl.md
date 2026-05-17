# Robotic Control

## Introduction
The robotic controls require installation of an Ubuntu 24.04 Virtual Machine (VM) alongside the required libraries. The following robotic arm control code is written in Python for easy interoperation and modification, aimed to allow any IT/Robotic field student to continue development without in-depth knowledge of ROS2, MoveIt, or Matlab/Simulink.

## Installation

### Virtual Machine Installation
ISO: Ubuntu 24.04 - https://ubuntu.com/download/alternative-downloads
RAM: 8GB        
Storage: 40GB


### Application Installation
Install ROS2 and MoveIt! from the following documentation,

#### ROS2
https://docs.ros.org/en/jazzy/Installation/Ubuntu-Install-Debs.html

#### MoveIt!
https://moveit.picknik.ai/main/doc/tutorials/getting_started/getting_started.html

### GitHub Clone
Clone the following repository within the VM or move the files into the VM.
https://github.com/BeardedSwitchDragon/SysSims-EwasteExtraction

### Using the Controls

Ensure ROS2 and MoveIt respected files are sourced to allow running within the command line.

```source /opt/ros/jazzy/setup.bash```
```source ~/ws_moveit/install/setup.bash```


Run the following MoveIt command to open the simulated robotic arm.

```ros2 launch moveit_servo demo_ros_api.launch.py```
```ros2 run moveit_servo servo_keyboard_input```

Run the following Python script within another terminal instance (Ensure all terminal instances are sourced for ROS2 and MoveIt
```Python3 main.py```


