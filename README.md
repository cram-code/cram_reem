CRAM / REEM Integration Stack
===

Why this stack?
---

The CRAM high-level plan execution system hosted [here](http://github.com/cram-code) supports adapting different robot architectures to be controlled using the same plan library designed only once.

This stack enables REEM robots by PAL Robotics to be controlled through the ROS middleware system using CRAM. The respective ROS setup steps for a simulated REEM robot can be found [here](http://wiki.ros.org/pal-ros-pkg).


Current status
---

Basic navigation works. The CRAM navigation process module can drive the REEM robot around.
[Video link](http://www.youtube.com/watch?v=CfU9t8_0CKk) to a simple example of moving REEM around using the reem_navigation_process_module.


What is currently being integrated?
---

Right now, the following integration is being worked on:

* *reem_navigation_process_module*: The navigational capabilities of the REEM robot are exposed to CRAM, using the `/PAL_ROBOT/cmd_vel` topic as a basis for sending twist messages. Depends on [nav_pcontroller](https://github.com/code-iai/nav_pcontroller) for linear navigation control.


What integration is planned?
---

In the future, the following process modules are planned to be integrated:

* *reem_manipulation_process_module*: Manipulative skills of the REEM are exposed to CRAM, ideally through the MoveIt! framework (as already [implemented into CRAM](https://github.com/cram-code/cram_bridge/tree/master/cram_moveit)). This also includes REEM-specific poses for grasping, putting things down, and special poses for the robot's individual capabilities. This also includes opening/closing hands and getting feedback about their state.
* *reem_perception_process_module*: Sensory skills and input from sensors are exposed to CRAM. This module includes possible cameras and information about them.
