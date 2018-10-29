Getting started
===============

Booting up the robot
--------------------
In the kindyn package a couple of example robots can be found. You can run them with the provided robot.launch file:

msj_platform
~~~~~~~~~~~~
A robot that was build for training one of the 3-DoF shoulders of Roboy 2.0. It uses 8 cables to control the 3-DoFs.
You can run it with the following command:
::
    roslaunch kindyn robot.launch robot_name:=msj_platform start_controllers:='sphere_axis0 sphere_axis1 sphere_axis2'

roboy_upper_body
~~~~~~~~~~~~~~~~
Roboy 2.0 upper body with the 3-DoF head and his two 5-DoF arms. Use the following command to launch it:
::
    roslaunch kindyn robot.launch robot_name:=roboy_upper_body start_controllers:='hip_joint sphere_head_axis0
    sphere_head_axis1 sphere_head_axis2 sphere_left_axis0 sphere_left_axis1 sphere_left_axis2 elbow_left_rot0
    elbow_left_rot1 sphere_right_axis0 sphere_right_axis1 sphere_right_axis2 elbow_right_rot0 elbow_right_rot1'

roboy_arcade_maschine
~~~~~~~~~~~~~~~~~~~~~
A retro arcad maschine in the Roboy lab that has a 3-DoF Roboy head mounted on the top. Launch it with:
::
    roslaunch kindyn robot.launch robot_name:=roboy_arcade_maschine start_controllers:='sphere_axis0 sphere_axis1 sphere_axis2'


Visualizing the robot state
---------------------------
Start Rviz using :code:`rviz&`. In the GUI menu go to :code:`Panels->Add New Panel->CardsflowRviz`. You should see the UI controls for visualizing tendons, forces, etc.

Controlling the robot
---------------------
One can publish to a corresponding ROS topic target joint angles (use :code:`rostopic list` to identify them) or an RQT plugin by running :code:`rqt&` and adding the CARDSflow plugin from the menu.
