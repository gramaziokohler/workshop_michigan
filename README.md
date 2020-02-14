# Workshop Michigan 24. and 25.02.2020


This workshop is about robotic assembly using the COMPAS framework.


## Overview


* COMPAS Introduction
* COMPAS exercise
* Python & github
* Robotic fabrication basics
* Robotic assembly excercise
    



## Examples


### Day 1

* **Slides**: [session 1](https://docs.google.com/presentation/d/1MwbF9ibyxKD2Nxk989vYtSyW_or0pXSVWBnFI-EQtdM/edit?usp=sharing)


* [Docker configuration to launch ROS & MoveIt](docker-ur5/)
* [Open MoveIt! in your browser](http://localhost:8080/vnc.html?resize=scale&autoconnect=true) (once the UR5 docker compose has been started)
* Basic examples:
  * [Programatically define a robot](examples/021_define_model.py)
  * [Load robots from Github](examples/022_robot_from_github.py)
  * [Load robots from ROS](examples/023_robot_from_ros.py)
  * [Visualize robots in Rhino](examples/024_robot_artist_rhino.py)
  * [Visualize robots in Grasshopper](examples/025_robot_artist_grasshopper.ghx)
  * [Build your own robot](examples/026_build_your_own_robot.py)
* Basic ROS examples:
  * [Verify connection](examples/027_check_connection.py)
  * The cannonical example of ROS: chatter nodes
    * [Talker node](examples/028_ros_hello_world_talker.py)
    * [Listener node](examples/029_ros_hello_world_listener.py)
* Examples of ROS & MoveIt planning with UR5:
  * [Forward Kinematics](examples/030_forward_kinematics_ros_loader.py)
  * [Inverse Kinematics](examples/031_inverse_kinematics_ros_loader.py)
  * [Cartesian motion planning](examples/032_plan_cartesian_motion_ros_loader.py)
  * [Free space motion planning](examples/033_plan_motion_ros_loader.py)
  * Planning scene management:
    * [Add objects to the scene](examples/034_add_collision_mesh.py)
    * [Append nested objects to the scene](examples/035_append_collision_meshes.py)
    * [Remove objects from the scene](examples/036_remove_collision_mesh.py)
* [Grasshopper Playground](examples/037_robot_playground_ur5.ghx)

### Day 2


* **Slides**:  [session 2](https://docs.google.com/presentation/d/1QBu-4BhnLEOkrOvZf9PoX-m2dYAtTzfMFgFJ7Bw6VFY/edit#slide=id.g7054e0e0c8_0_5)

* **Jupyter Notebooks**:
  * [Path planning](Path%20planning.ipynb)
  * [Robotic Assembly](Robotic%20Assembly.ipynb)

---

* [Docker configuration to launch ROS & MoveIt](docker-ur5/)
* [Assembly Playground](examples/040_robot_assembly.ghx)
* Attaching gripper/tool:
  * [Attach tool to last link of the robot](examples/041_attach_tool.py)
  * [Plan cartesian motion with attached tool](examples/042_plan_cartesian_motion_with_attached_tool.py)
* Assembly elements (e.g. bricks):
  * [Add assembly element to planning scene](examples/043_create_element_and_add_to_planning_scene.py)
  * [Attach assembly element to gripper](examples/044_add_element_as_attached_collision_object.py)
* Pick and place examples:
  * [Pick and place](examples/045_pick_and_place.py)
  * [Pick and place Stack](examples/046_pick_and_place_stack.py)



## Requirements


.. Write requirements instructions here


## Installation


Create environment `workshop`

	conda create --name myenv

	conda activate workshop


We will use the `workshop` environment and update it as follows:

    (base)  conda activate workshop
    (workshop) conda update compas compas_fab --yes
    (workshop) python -m compas_fab.rhino.install -v 6.0

## Verify installation

    (workshop) python
    >>> import compas_fab
    >>> compas_fab.__version__
    '0.10.0'
    >>> exit()


