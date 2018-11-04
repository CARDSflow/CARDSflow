.. _technical-interfaces:

Technical Interfaces
--------------------
The following rqt_graph shows an overview of the ROS message infrastructure for one of the example robots, the msj_platform.
.. figure:: images/rosgraph.*

Two ROS nodes are active, the cardsflow_example_robot and the controller_manager. The cardsflow_example_robot is our
msj_platform doing all the kinematic calculations. The joint, robot and tendon states are published on the respective
topics in green. On the left there are three joint target topics available in blue. The controller_manager spawned
three joint controller and the respective controllers subscribe to these topics as their target setpoints. The controller_type
topic is advertised by our msj_platform and the controllers publish their type on that topic once they are spawned by the
controller_manager. The last topic is the interactive_marker topic which the msj_platform subscribes to. When a user
drags the interactive markers in rviz, the inverse kinematics service is called and the robot will try to move to the
requested position.