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