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
   
Next we need to build and install qpoases:
::
    cd qpoases
    mkdir build && cd build
    cmake ../
    sudo make -j9 install
    
Now you can build CARDSflow simply by building your catkin workspace:
::
    cd path/to/your/catkin_ws
    catkin_make
    source devel/setup.bash

.. _iDynTree: https://github.com/robotology/idyntree

RaspberryPi 3B installation
----------------------------

Download the image using the following command:
::
    wget -nv http://bot.roboy.org:8081/~roboy/CARDSflow_raspberry_pi3B.md5sum
    wget -nv http://bot.roboy.org:8081/~roboy/CARDSflow_raspberry_pi3B.img

Use a 16GB SDcard and flash the image using the following command. NOTE: make sure you are using the correct sd-card device (/dev/sdX), otherwise you might wipe your whole system!!!
::
    sudo dd if=CARDSflow_raspberry_pi3B.img of=/dev/sdX bs=1M status=progress
    
Insert the sd-card into the raspi and power it. The image provides Ubuntu 16.03 MATE with ROS kinetic installed. In the home folder you can find the roboy_arcade_maschine workspace which contains a build version of CARDSflow.
