============================================================
Workshop Michigan 24. and 25.02.2020
============================================================

.. start-badges

.. image:: https://img.shields.io/badge/License-MIT-blue.svg
    :target: https://github.com/gramaziokohler/workshop_michigan/blob/master/LICENSE
    :alt: License MIT

.. image:: https://travis-ci.org/gramaziokohler/workshop_michigan.svg?branch=master
    :target: https://travis-ci.org/gramaziokohler/workshop_michigan
    :alt: Travis CI

.. end-badges

This workshop is about robotic assembly using the COMPAS framework.

********
Overview
********

* COMPAS Introduction
* COMPAS exercise
* Python & github
* Robotic fabrication basics
* Robotic assembly excercise
    


********
Examples
********

Day 1
=========

* **Slides**: [session 1](https://docs.google.com/presentation/d/1OIU3vCmwe3lkVWpI0JuJJ-GFoOq5HH8ulElPZNS_F2Y/edit?usp=sharing)
* **Assignments**: [session 1](assignments/session1.md)

---

* [Docker configuration to launch ROS & MoveIt](docker-ur5/)
* [Open MoveIt! in your browser](http://localhost:8080/vnc.html?resize=scale&autoconnect=true) (once the UR5 docker compose has been started)
* Basic examples:
  * [Programatically define a robot](examples/01_define_model.py)
  * [Load robots from Github](examples/02_robot_from_github.py)
  * [Load robots from ROS](examples/03_robot_from_ros.py)
  * [Visualize robots in Rhino](examples/04_robot_artist_rhino.py)
  * [Visualize robots in Grasshopper](examples/05_robot_artist_grasshopper.ghx)
  * [Build your own robot](examples/06_build_your_own_robot.py)
* Basic ROS examples:
  * [Verify connection](examples/07_check_connection.py)
  * The cannonical example of ROS: chatter nodes
    * [Talker node](examples/08_ros_hello_world_talker.py)
    * [Listener node](examples/09_ros_hello_world_listener.py)
* Examples of ROS & MoveIt planning with UR5:
  * [Forward Kinematics](examples/10_forward_kinematics_ros_loader.py)
  * [Inverse Kinematics](examples/11_inverse_kinematics_ros_loader.py)
  * [Cartesian motion planning](examples/12_plan_cartesian_motion_ros_loader.py)
  * [Free space motion planning](examples/13_plan_motion_ros_loader.py)
  * Planning scene management:
    * [Add objects to the scene](examples/14_add_collision_mesh.py)
    * [Append nested objects to the scene](examples/15_append_collision_meshes.py)
    * [Remove objects from the scene](examples/16_remove_collision_mesh.py)
* [Grasshopper Playground](examples/17_robot_playground_ur5.ghx)

### Day 2
=========

* **Slides**:  [session 2](https://docs.google.com/presentation/d/1S29aMP9h4nRvQCdr1jGvp0L4YQCc8q0_irpHb9p9kos/edit?usp=sharing)
* **Assignments**: [session 2](assignments/session2.md)
* **Jupyter Notebooks**:
  * [Path planning](Path%20planning.ipynb)
  * [Robotic Assembly](Robotic%20Assembly.ipynb)

---

* [Docker configuration to launch ROS & MoveIt](docker-ur5/)
* [Assembly Playground](examples/20_robot_assembly.ghx)
* Attaching gripper/tool:
  * [Attach tool to last link of the robot](examples/21_attach_tool.py)
  * [Plan cartesian motion with attached tool](examples/22_plan_cartesian_motion_with_attached_tool.py)
* Assembly elements (e.g. bricks):
  * [Add assembly element to planning scene](examples/23_create_element_and_add_to_planning_scene.py)
  * [Attach assembly element to gripper](examples/24_add_element_as_attached_collision_object.py)
* Pick and place examples:
  * [Pick and place](examples/25_pick_and_place.py)
  * [Pick and place Stack](examples/26_pick_and_place_stack.py)



Documentation
-------------

.. Explain how to access documentation: API, examples, etc.

..
.. optional sections:

Requirements
------------

.. Write requirements instructions here


Installation
------------

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



Contributing
------------

Make sure you setup your local development environment correctly:

* Clone the `workshop_michigan <https://github.com/gramaziokohler/workshop_michigan>`_ repository.
* Install development dependencies and make the project accessible from Rhino:

::

    pip install -r requirements-dev.txt
    invoke add-to-rhino

**You're ready to start working!**

During development, use tasks on the
command line to ease recurring operations:

* ``invoke clean``: Clean all generated artifacts.
* ``invoke check``: Run various code and documentation style checks.
* ``invoke docs``: Generate documentation.
* ``invoke test``: Run all tests and checks in one swift command.
* ``invoke add-to-rhino``: Make the project accessible from Rhino.
* ``invoke``: Show available tasks.

For more details, check the `Contributor's Guide <CONTRIBUTING.rst>`_.


Releasing this project
----------------------

.. Write releasing instructions here


.. end of optional sections
..

Credits
-------------

This package was created by Romana Rust <rust@arch.ethz.ch> `@romanarust <https://github.com/romanarust>`_ at `@gramaziokohler <https://github.com/gramaziokohler>`_
