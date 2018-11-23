Getting started
===============

Booting up the robot
--------------------
In the kindyn package a couple of example robots can be found. You can run them with the provided robot.launch file:

msj_platform
~~~~~~~~~~~~

.. figure:: images/msj_platform.*

A robot that was build for training one of the 3-DoF shoulders of Roboy 2.0. It uses 8 cables to control the 3-DoFs.
You can run it with the following command:
::
    roslaunch kindyn robot.launch robot_name:=msj_platform start_controllers:='sphere_axis0 sphere_axis1 sphere_axis2'

roboy_upper_body
~~~~~~~~~~~~~~~~

.. figure:: images/roboy_upper_body.*

Roboy 2.0 upper body with the 3-DoF head and his two 5-DoF arms. Use the following command to launch it:
::
    roslaunch kindyn robot.launch robot_name:=roboy_upper_body start_controllers:='hip_joint sphere_head_axis0
    sphere_head_axis1 sphere_head_axis2 sphere_left_axis0 sphere_left_axis1 sphere_left_axis2 elbow_left_rot0
    elbow_left_rot1 sphere_right_axis0 sphere_right_axis1 sphere_right_axis2 elbow_right_rot0 elbow_right_rot1'

roboy_xylophone
~~~~~~~~~~~~~~~

.. figure:: images/roboy_xylophone.*

Roboy 2.0 upper body with the 3-DoF head and his two 7-DoF arms holding xylophone playing sticks. Use the following command to launch it:
::
    roslaunch kindyn robot.launch robot_name:=roboy_xylophone start_controllers:='sphere_head_axis0 sphere_head_axis1
    sphere_head_axis2 sphere_left_axis0 sphere_left_axis1 sphere_left_axis2 elbow_left_rot0 elbow_left_rot1
    sphere_right_axis0 sphere_right_axis1 sphere_right_axis2 elbow_right_rot0 elbow_right_rot1 left_wrist_0
    left_wrist_1 right_wrist_0 right_wrist_1 hip_joint left_stick_tip_joint right_stick_tip_joint'

roboy_arcade_maschine
~~~~~~~~~~~~~~~~~~~~~

.. figure:: images/roboy_arcade_maschine.*

A retro arcad maschine in the Roboy lab that has a 3-DoF Roboy head mounted on the top. Launch it with:
::
    roslaunch kindyn robot.launch robot_name:=roboy_arcade_maschine start_controllers:='sphere_axis0 sphere_axis1 sphere_axis2'

test_robot
~~~~~~~~~~

.. figure:: images/test_robot.*

A robot with 6-DoF, 3 prismatic and 3 rotational, with 20 cables. You can launch it with the following command
::
    roslaunch kindyn robot.launch robot_name:=test_robot start_controllers:='joint0 joint1 joint2 sphere_axis0 sphere_axis1 sphere_axis2'

yatr
~~~~

.. figure:: images/yatr.*

Yet another test robot, 3-DoF, 8 cables. You can launch it with the following command
::
    roslaunch kindyn robot.launch robot_name:=yatr start_controllers:='joint0 joint1 joint2'
