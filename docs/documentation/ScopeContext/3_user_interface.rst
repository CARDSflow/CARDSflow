.. _user-interfaces:

User Interfaces
---------------
There are two user interfaces available to the user, a rviz plugin and a rqt plugin. The following figure shows the rviz
plugin.

.. figure:: images/rviz_plugin.*

NOTE: In order for the mesh and tendons to be visible add the following pluins to rviz:
1) Marker
2) TF
3) InteractiveMarkers (you need to change the topic when you add the plugin)
4) you need to change the fixed frame in rviz from map to world

The buttons of the rviz plugin trigger visualization, while the slider change their appearance.

The rqt plugin can be seen in the figure below. The sliders can be used to change the setpoints for the endeffector joints.

.. figure:: images/rqt_plugin.*
