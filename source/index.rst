.. Smorphi_Documentation documentation master file, created by
   sphinx-quickstart on Mon Sep 30 17:52:03 2024.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Smorphi Documentation
=================================================

Overview
-----------
Welcome to the smorphi robot documentation, this page includes all the resources needed for your smorphi robot. 

Our Made-in-Singapore Smorphi robots are the World's first Tetris-inspired transformer robots, ideal for all ages and learning settings. The underlying technology powering our Smorphi robots is licensed from the Singapore University of Technology and Design, a global frontrunner in reconfigurable robotics.

Our Smorphi robots covers users ranging from primary school kids and all the way upto researchers around the world. Along with catering for educational development, the smorphi robot is a ideal prototyping toolkit for developers in engineering product firms that allows for quick and affordable development as well as testing of algorithms and mock payloads before moving on to sophisticated high fidelity prototypes at scale.  

Key Features
--------------
* **Variants**: The smorphi robot comes in two variants, the smorphi\ :sup:`2` (4 module) robot, and smorphi single (1 module) robot
* **Shape Changing**: The smorphi\ :sup:`2` robot is capable to change to upto 7 different shapes
* **Atomics Units**: The smorphi\ :sup:`2` can work together with four modules combined together or can work individually as a single unit, two units, and three units as well
* **Multi-Directional Motion**: The smorphi robot's motion is powered by mechannum wheels which enables it to move not just in forward/backward motion, but also enables it to move in sideways/diagonal motion as well
* **Autonomous or Manual Operation**: The smorphi robot could be combined with sensors to operate as an autonomous unit or could also be controlled manually using bluetooth / WiFi interfaces
* **Sensor Array**: The smorphi\ :sup:`2` kit comes with a suite of sensors such as Infrared(IR) sensors, Temperature sensor, Sound sensor, and the AI enabled husky camera. Beyond these sensors, the smorphi robot could also be coupled with sensors such as LiDAR, IMU,etc to enable ROS based applications

Power
-------
* The smorphi robots are powered by a rechargable Li-Ion battery which lasts for nearly 2hrs runtime for a smorphi square robot and >2hrs runtime for a smorphi single robot

Operational Modes
--------------------
* **Manual Mode**: The smorphi robot could be operated manually using a WiFi / Bluetooth based joystick/controller/application. Furthermore, the smorphi could be connected to a raspberry PI or an IPC to be controlled/tele_operated using ROS based teleoperation packages.
* **Autonomous Mode**: The smorphi robot is capable of autonomous navigation using the fusion of sensors provided in the smorphi\ :sup:`2` kit. Furthermore, the smorphi robot could be used with a LiDAR / IMU by connecting a raspberry PI or an IPC to perform all the higher level sensor calculations and processings required for autonomous navigation applications.   

Table of Contents:
----------------------------------

* **Smorphi Assembly**: 
    * Build your smorphi robot using our :ref:`assembly manual<assemblymanual>` now!

* **Software Installation Setup**:

    * Software `setup guide <https://github.com/WefaaRobotics/Smorphi/wiki/Exercise-2>`_ for smorphi\ :sup:`2` 
    * Software `setup guide <https://github.com/WefaaRobotics/smorphi_single/wiki/Software-setup-guide-for-Smorphi-robot>`_ for smorphi single 

* **Smorphi Mobile App**:

    * Download the smorphi app from the `Google Play Store <https://play.google.com/store/apps/details?id=de.kai_morich.smorphi_app>`_ or the `App Store <https://apps.apple.com/sg/app/smorphi/id6482102114>`_  to try out all the basic locomotion (Moving, sliding, pivoting and shape change) using the bluetooth controlled app. 

* **Smorphi Exercises**:
   * There are many things you can do with your smorphi_single and smorphi\ :sup:`2` robots. Do explore some of the exercises/tutorials to access some mini projects and tasks you can do with your Smorphi :ref:`here<exercises>`  


* **Code Documentation / Command References**:
   * A comprehensive list of :ref:`commands<code_refs>`  for the robot's movements, shape changes, and other functions pertaining to the control of the robot.   


* **Advanced Features**:
   * Our C++ api ( ``<smorphi.h>`` ) could be located in the smorphi libraries, this api is actively referenced for all the locomotion and shape changing actions for the smorphi robot
   * Furthermore, our C++ SDK which is also part of smorphi libraries, provides the whole stack of smorphi class and its objects which could be further developed/modified for uses/researches involving more than 4 modules (or) more than 7 shapes
   * Our smorphi base android SDK is available on our `smorphi app github <https://github.com/WefaaRobotics/Smorphi-App-Android/tree/main/SimpleBluetoothTerminal-final/app/release>`_ page, which could be used for modifying/developing user specific bluetooth applications for smorphi robot

* **Diagnostics & Trobleshooting**:
   * Our :ref:`troubleshooting<diagnostics>` guide provides advice for generic issues

.. .. list-table:: Troubleshooting
..    :widths: 25 25 30
..    :header-rows: 1

..    * - Issue 
..      - Explaination
..      - Solution
..    * - | XYZ
..        | xyz
..      - ABC
..      - 123



* **FAQ**:
   * Our :ref:`FAQ<FAQ>` section provides quick answers to some of the common questions about the smorphi robot's software, hardware, and general functionality  

* **Contact & Support**:
   * For further queries, please drop a mail to support@wefaarobotics.com.sg 


.. toctree::
   :maxdepth: 2
   :hidden:
   :caption: Contents:

   docs/user_manual
   docs/exercises/exercises
   docs/code_refs
   docs/diagnostics
   docs/FAQ

   


.. Indices and tables
.. ==================

.. * :ref:`genindex`
.. * :ref:`modindex`
.. * :ref:`search`
