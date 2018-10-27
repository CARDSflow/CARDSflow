# CARDSflow
This is the CARDSflow parent repository. It links to all the submodules CARDSflow consists of. This repository provides 
a full pipeline for Cable Robots from CAD in Autodesk Fusion 360 to full simulation and control of these robots.

## Installation
There are three options:
- install from apt on Ubuntu 16.04
- build from source using this repository
- download one of the readily available sd card images for platforms such as the DE10-nano-soc or a raspberry pi
### Install from apt
TODO

### Build from source
#### Dependencies
The repo was tested on Ubuntu 16.04 with ROS kinetic. Make sure you install the following packages:
```bash
sudo apt install ros-kinetic-desktop-full ros-kinetic-eus-qpoases libeigen3-dev libxml2-dev coinor-libipopt-dev qtbase5-dev qtdeclarative5-dev qtmultimedia5-dev qml-module-qtquick2 qml-module-qtquick-window2 qml-module-qtmultimedia qml-module-qtquick-dialogs qml-module-qtquick-controls qml-module-qt-labs-folderlistmodel qml-module-qt-labs-settings
```
#### Pull the code
CARDSflow should be cloned to your catkin workspace:
```bash
cd path/to/your/catkin_ws/src
git clone --recursive https://github.com/CARDSflow/CARDSflow

```
#### Build and install iDynTree

First we need to build iDynTree (for more details on this step, visit the [website](https://github.com/robotology/idyntree)):
```bash
cd path/to/CARDSflow/iDyntree
mkdir build && cd build
cmake ..
make -j9
sudo make install
```

#### Build CARDSflow

Simply build your catkin workspace:
```bash
cd path/to/your/catkin_ws
catkin_make
```

### Download sd-card image
TODO

## Running the examples
In the kindyn package a couple of example robots can be found. You can run them with the provided robot.launch file:
### msj_platform
A robot that was build for training one of the 3-DoF shoulders of Roboy 2.0. It uses 8 cables to control the 3-DoFs. 
You can run it with the following command:
```bash
roslaunch kindyn robot.launch robot_name:=msj_platform start_controllers:='sphere_axis0 sphere_axis1 sphere_axis2'
```
### roboy_upper_body
Roboy 2.0 upper body with the 3-DoF head and his two 5-DoF arms. It uses 39 cables in total to control the three endeffectors.
Use the following command to launch it:
```bash
roslaunch kindyn robot.launch robot_name:=roboy_upper_body start_controllers:='hip_joint sphere_head_axis0 
sphere_head_axis1 sphere_head_axis2 sphere_left_axis0 sphere_left_axis1 sphere_left_axis2 elbow_left_rot0 
elbow_left_rot1 sphere_right_axis0 sphere_right_axis1 sphere_right_axis2 elbow_right_rot0 elbow_right_rot1' 
```
### roboy_arcade_maschine
A retro arcad maschine in the Roboy lab that has a 3-DoF Roboy head mounted on the top. 8 cables control the head. Launch it with:
```bash
roslaunch kindyn robot.launch robot_name:=roboy_arcade_maschine start_controllers:='sphere_axis0 sphere_axis1 sphere_axis2'
```