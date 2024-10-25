.. _ex16:

Exercise 16
==============
Items needed:
--------------
* An assembled Smorphi mini / Smorphi\ :sup:`2` robot
* A computer
* A USB to USB-C cable
* Internet connection
* Pixycam SPI cable(provided with the Pixycam Box)  

Objectives of exercise:
-------------------------
1. Learn about various things you can do with a camera in CV
2. Learn how to connect your pixycam with your Smorphi
3. Learn how to detect colours using the pixycam


Steps  / Description:
++++++++++++++++++++++++

#. [Theory of CV]
                        |    Computer vision is an interdisciplinary field that deals with how computers can be made to gain high-level understanding from digital images or videos, perhaps to recognise specific objects. From the perspective of engineering, it seeks to automate tasks that the human visual system can do. Computer vision is concerned with the automatically extracting, analysing and understanding of useful information from a single image or a sequence of images. And this involves development of various algorithms.
                        |    The Pixycam provided to you has already a few inbuilt and trained Programs that allows you to automatically detect colours, for example, like in the previous exercise.

#. [connecting your Pixycam to your Smorphi]
                        |    For your Pixycam to be able to communicate to your Smorphi, we will have to set it up via the Arduino ICSP method. There are generally a few different methods of communications you can use to talk to your 
                        |    https://docs.pixycam.com/wiki/doku.php?id=wiki:v2:porting_guide 
                        |    We setup the Pixy to use the Arduino ICSP mode, we will need the SPI cable to connect our Pixycam to the master board. First, plug in one side of the SPI cable to the pins of Pixycam labelled from (1) to (10) or as indicated in the image below. |A|
                        |    The other end of the SPI cable has to be connected to the pins on the Masterboard(as indicated in the image below). Please refer to the respective user manual for wiring details. |B|
                        |    The setup will look like this |C|
                        |    Please refer to the respective assembly manual for more details on how to mount the pixycam to the robot.
#. [Pixycam working]
                        |    Once you have connected your Pixycam to your Smorphi correctly, start up the PixyMon program you downloaded in the previous exercise. Click on the gear icon to go to the configuration window.
                        |    |D|
                        |    In the configuration window, navigate to the Interface page, and setup the interface as below and click apply, and the ok:
                        |    |E|

#. [Execution] 
                        |    A sample code is provided at `Testing_code -> sensors -> Pixycam_ICSP <https://github.com/WefaaRobotics/Smorphi/blob/main/Smorphi2/Testing_code/sensors/Pixycam_ICSP/ccc_i2c_uart/ccc_i2c_uart.ino>`_
                        |    Connect your Smorphi to the computer and the Pixycam to your computer via USB seperately, and upload the example code to Smorphi. Remember to press enable on your Smorphi Master board to execute the code once it is fully uploaded onto the Master board.
                        |    Open your serial Monitor by clicking on the magnifying glass button:
                        |    |F|
                        |    You should see something like this on your serial monitor:
                        |    |G|
                        |    These values indicates the objects detected by the Pixycam of the colour that you have set.
                        |    If you get the message “error: no response” from the Arduino serial monitor, first make sure your Pixy2 is running the ccc (color connected components) program from PixyMon, and that you have taught it an object as described in the previous lesson.
                        |    |H|
                        |    This is just one example of what you can do using your Pixycam. You can use this as a template to try out the other programs.
                        |    Try exploring the other programs yourself!




.. |A| image:: 1.jpg
               :width: 800 

.. |B| image:: 2.jpg
               :width: 800 

.. |C| image:: 3.jpg
               :width: 800 

.. |D| image:: 4.png
               :width: 800 

.. |E| image:: 5.png
               :width: 800 

.. |F| image:: 6.png
               :width: 800 

.. |G| image:: 7.png
               :width: 800 

.. |H| image:: 8.png
               :width: 800








