# Secure ROS2 - SROS2 Implementation Team 7 Simulation Team

The following creating the reuqired SROS2 files, unique key, and enclaves.

```
mkdir -p ~/sros2
```

```
ros2 security create_keystore ~/sros2/team7_keystore
```

```
ros2 security create_enclave ~/sros2/team7_keystore /team7
```


The following bash script placed within the ~/sros2 dirctory can be made into an executable bash file for faster automation development as such - secure.sh

```
#!/bin/bash

source /opt/ros/jazzy/setup.bash
source ~/ws_moveit/install/setup.bash

export ROS_SECURITY_KEYSTORE=$HOME/sros2/team7_keystore
export ROS_SECURITY_ENABLE=true
export ROS_SECURITY_STRATEGY=Enforce
export ROS_SECURITY_ENCLAVE_OVERRIDE=/team7
```

The following commands are required to start both the Gazebo environment and node which are provided within the GitHub repository or created as a new executable bash file such as start.sh

```
#!/bin/bash

gnome-terminal -- bash -c '
source /opt/ros/jazzy/setup.bash
source ~/ws_moveit/install/setup.bash
export LIBGL_ALWAYS_SOFTWARE=1
ros2 launch ~/ws_moveit/src/team7_sim/launch/team7_sim.launch.py
'

sleep 10

gnome-terminal -- bash -c '
source /opt/ros/jazzy/setup.bash
source ~/ws_moveit/install/setup.bash
ros2 launch kinova_gen3_7dof_robotiq_2f_85_moveit_config move_group.launch.py use_sim_time:=true
'
```

## Python Script
The user is able to run the Python script via sourcing the secure bash executable as seen below.

```
sourec ~/sros2/secure.sh
```

This will allow the terminal to operate within a secure instances, after which normal 

```
Python3 main.py
```

Can be ran without issue.

