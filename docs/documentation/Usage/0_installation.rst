Installation
============

Prerequisites
-------------
The CARDSflow repo has only been tested on Ubuntu 16.04 with ROS kinetic. It may work on different platforms with different ROS versions.
Make sure you install the following packages:
::
    sudo apt install ros-kinetic-desktop-full ros-kinetic-eus-qpoases libeigen3-dev libxml2-dev coinor-libipopt-dev qtbase5-dev qtdeclarative5-dev qtmultimedia5-dev qml-module-qtquick2 qml-module-qtquick-window2 qml-module-qtmultimedia qml-module-qtquick-dialogs qml-module-qtquick-controls qml-module-qt-labs-folderlistmodel qml-module-qt-labs-settings
Get The Code
------------
Clone the code to your catkin workspace:
::
    cd path/to/your/catkin_ws/src
    git clone --recursive https://github.com/CARDSflow/CARDSflow

Build From Source
-----------------
First we need to build iDynTree (for more details on this step, visit the iDynTree website):
::
    cd path/to/CARDSflow/iDyntree
    mkdir build && cd build
    cmake ..
    make -j9
    sudo make install

Now you can build CARDSflow simply by building your catkin workspace:
::
    cd path/to/your/catkin_ws
    catkin_make
    source devel/setup.bash

.. _iDynTree: https://github.com/robotology/idyntree
