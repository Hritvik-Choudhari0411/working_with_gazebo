# gazebo-tutorials

## Overview

This package runs a turtlebot3 (Wafflepi) in a gazebo world and implements the walker algorithim on it.

## Building and Running

Clone the repository in your ROS2 workspace.

```sh
cd < path_to_your_workspace >/src

# For cloning using SSH
git clone git@github.com:Hritvik-Choudhari0411/working_with_gazebo.git

# For cloning using HTTPS
git clone https://github.com/Hritvik-Choudhari0411/working_with_gazebo.git
```

### Building

To build the package follow the following steps

```sh
cd .. # Make sure you are in the ros2 workspace folder and not in src

# To build the package use
colcon build --package-select working_with_gazebo

# Source your setup file
. install/setup.bash
```

### Running

```sh
cd ros2_ws/

export GAZEBO_MODEL_PATH=/opt/ros/humble/share/turtlebot3_gazebo/models/

export TURTLEBOT3_MODEL=waffle_pi

# Using ROS2 Launch
ros2 launch working_with_gazebi roomba.py record:=< true or false >
```

## Cppcheck and Cpplint

To run the CppCheck

```sh
sh cppcheck.sh
```

To run the Cpplint

```sh
sh cpplint.sh
```

## Dependencies

- [ROS2 Humble](https://docs.ros.org/en/humble/index.html)
- CMake Version 3.8 or greater
- C++ 17 or newer
- [Gazebo](http://gazebosim.org/tutorials?tut=ros2_installing&cat=connect_ros)
- Turtlebot3
- Turtlebot3 Gazebo

## Assumptions

The above instruction assume that you have installed all the Dependecies and are working on a Ubuntu 22.04 LTS system and have created your ROS2 workspace beforehand.

## Results

Results for `cppcheck`, `cpplint` can be viewed in `results` folder