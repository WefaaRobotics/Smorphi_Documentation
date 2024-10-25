.. _code_refs:

Code Documentation / Command References
=========================================

* A comprehensive list of `commands <https://github.com/WefaaRobotics/Smorphi/wiki/Smorphi-Code-Documentation>`_  for the robot's movements, shape changes, and other functions pertaining to the control of the robot.



Initializing the Robot
------------------------
**BeginSmorphi();**
++++++++++++++++++++++++++
   Initialise start-up sequence of Smorphi robot, including Motor drivers, IO Expander, Interrupt Pins. 

**BeginSmorphi_single();** 
+++++++++++++++++++++++++++++
   Initialise start-up sequence of Smorphi Single robot, including Motor drivers, IO Expander, Interrupt Pins. 

Velocity Handler
-------------------
**sm_velocity_handler(float sm_req_linear_speed_x, float sm_req_linear_speed_y, float sm_req_angular_speed);**
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
   Calculates speed of each wheel of robot. Takes in the calculated mapped linear speed in the XY direction from mapPosRanges(int ipSpeed) and mapNegRanges(int ipSpeed) and the mapped angular speed from mapPosAng(int ipSpeed) and mapNegAng(int ipSpeed). 

PWM Handler
-------------
**sm_pwm_handler(int flag);**
+++++++++++++++++++++++++++++++
   Converts speed to Pulse Width Modulation (PWM) value which is needed by the motor driver to determine speed at which the motor driver spins. Value of flag determines which movement case of the robot.
   
    * Flag = 0: forward, backward, left and right movement
    * Flag = 1: curve turn up-right, up-left, down-right, down-left
    * Flag = 2: Pivot turn clockwise and anti-clockwise
    * Flag = 3: diagonal movement up-right, up-left, down-right, down-left

Locomotion
------------
**MoveForward(int Speed);**
+++++++++++++++++++++++++++++
   Moves the robot forward. Speed takes in Integer user input from 0-100 and adjust speed of robot accordingly. 

**MoveBackward(int Speed);**
++++++++++++++++++++++++++++++
   Moves the robot backwards. Speed takes in Integer user input from 0-100 and adjust speed of robot accordingly. 

**MoveRight(int Speed);**
++++++++++++++++++++++++++
   Moves the robot right. (not a turn) Speed takes in Integer user input from 0-100 and adjust speed of robot accordingly. 

**MoveLeft(int Speed);**
++++++++++++++++++++++++++
   Moves the robot Left. Speed takes in Integer user input from 0-100 and adjust speed of robot accordingly. 

Diagonal Locomotion
---------------------
**MoveDiagUpRight(int Speed);**
+++++++++++++++++++++++++++++++++
   Moves the robot diagonally up-right. Speed takes in Integer user input from 0-100 and adjust speed of robot accordingly

**MoveDiagUpLeft(int Speed);**
+++++++++++++++++++++++++++++++
   Moves the robot diagonally up-left. Speed takes in Integer user input from 0-100 and adjust speed of robot accordingly

**MoveDiagDownRight(int Speed);**
+++++++++++++++++++++++++++++++++++
   Moves the robot diagonally down-right. Speed takes in Integer user input from 0-100 and adjust speed of robot accordingly

**MoveDiagDownLeft(int Speed);**
++++++++++++++++++++++++++++++++++
   Moves the robot diagonally down-left. Speed takes in Integer user input from 0-100 and adjust speed of robot accordingly

Curve Locomotion
------------------
**MoveTurnUpRight(int Speed, int angular_velocity);**
++++++++++++++++++++++++++++++++++++++++++++++++++++++++
   Moves the robot in a curve up-right. Speed takes in Integer user input from 0-100 and adjust speed of robot accordingly. Angular velocity takes in integer user input from 0-100 and adjusts the speed of turning which affects how sharply the robot turns.

**MoveTurnUpLeft(int Speed, int angular_velocity);**
++++++++++++++++++++++++++++++++++++++++++++++++++++++
   Moves the robot in a curve up-left. Speed takes in Integer user input from 0-100 and adjust speed of robot accordingly. Angular velocity takes in integer user input from 0-100 and adjusts the speed of turning which affects how sharply the robot turns.

**MoveTurnDownRight(int Speed, int angular_velocity);**
+++++++++++++++++++++++++++++++++++++++++++++++++++++++++
   Moves the robot in a curve down-right. Speed takes in Integer user input from 0-100 and adjust speed of robot accordingly. Angular velocity takes in integer user input from 0-100 and adjusts the speed of turning which affects how sharply the robot turns

**MoveTurnDownLeft(int Speed, int angular_velocity);**
++++++++++++++++++++++++++++++++++++++++++++++++++++++++
   Moves the robot in a curve down-left. Speed takes in Integer user input from 0-100 and adjust speed of robot accordingly. Angular velocity takes in integer user input from 0-100 and adjusts the speed of turning which affects how sharply the robot turns.

Center Pivot Locomotion
-------------------------
**CenterPivotLeft(int Speed);**
++++++++++++++++++++++++++++++++++++++++++++++++++++++
   Moves the robot in a pivot in the anticlockwise direction. Speed takes in Integer user input from 0-100 and adjust speed of robot spinning accordingly

**CenterPivotRight(int Speed);**
++++++++++++++++++++++++++++++++++++++++++++++++++++++
   Moves the robot in a pivot in the clockwise direction. Speed takes in Integer user input from 0-100 and adjust speed of robot spinning accordingly

Check the feedback of solenoid
--------------------------------
**int sm_feedback(int solenoid_feedback);**
++++++++++++++++++++++++++++++++++++++++++++++++++++++
   Check the status of the solenoid. If the return value of solenoid_feedback is:

  * 0: solenoid is unlatched
  * 1: solenoid is latched

   Each solenoid is assigned a number from 1-6 for Smorphi2 (you can obtain the solenoid number from the assembly manual). To check the status of the solenoid, just call: sm_feedback(1), etc. 

Unlock certain solenoid
-------------------------
**sm_solenoid_set(int solenoid_unlock, bool status)**
++++++++++++++++++++++++++++++++++++++++++++++++++++++++
   Allows you to lock/unlock a specific solenoid. Choose which solenoid to unlock by user input of 1-6 for solenoid_unlock. Set the solenoid to unlock if input is True, and lock if input is False. 

Stop Smorphi
--------------
**stopSmorphi();**
++++++++++++++++++++++++++++++++++++++++++++++++++++++
   Stop Smorphi2’s movements

**stopSmorphi_single();**
++++++++++++++++++++++++++++++++++++++++++++++++++++++
   Stop Smorphi single's movements

Reset lv
----------
**sm_reset_M1();**
++++++++++++++++++++++++++++++++++++++++++++++++++++++
   Set module 1 wheels speed variables to zero.

**sm_reset_M2();**
++++++++++++++++++++++++++++++++++++++++++++++++++++++
   Set module 2 wheels speed variables to zero.

**sm_reset_M3();**
++++++++++++++++++++++++++++++++++++++++++++++++++++++
   Set module 3 wheels speed variables to zero.

**sm_reset_M4();**
++++++++++++++++++++++++++++++++++++++++++++++++++++++
   Set module 4 wheels speed variables to zero.

Interrupt functions
----------------------
**interrupt_test();**
++++++++++++++++++++++++++++++++++++++++++++++++++++++
   Will print out the pin that triggered the interrupt in the serial monitor.

**set_interrupt_pin();**
++++++++++++++++++++++++++++++++++++++++++++++++++++++
   Initialise the interrupt pins, including sensor pins and solenoid feedback status.

**Int module1_sensor_interrupt();**
++++++++++++++++++++++++++++++++++++++++++++++++++++++
   A test function that indicates if the interrupt is working on module 1, specifically for the sensor pins. Returns the pin that triggered the interrupt if working. Otherwise will return set value of 255.

Helper Functions
-------------------
**char sm_getShape();**
++++++++++++++++++++++++++++++++++++++++++++++++++++++
   Retrieves the shape that Smorphi is currently in and returns a letter that represents the current shape of Smorphi2.

**SetSmorphiSpeed(double pwm[4][4]);**
++++++++++++++++++++++++++++++++++++++++++++++++++++++
   Sets PWM value of each wheel.

**double mapPosRanges(int ipSpeed);**
++++++++++++++++++++++++++++++++++++++++++++++++++++++
   Maps user input speed to the positive range of linear speed. Wheels will turn forwards.

**double mapNegRanges(int ipSpeed);**
++++++++++++++++++++++++++++++++++++++++++++++++++++++
   Maps user input speed to the negative range of linear speed. Wheels will turn backwards.

**int map_lv_PWM(double ipSpeed);**
++++++++++++++++++++++++++++++++++++++++++++++++++++++
   Maps the linear speed to PWM (0-255 range)

**int map_ang_PWM(double ipSpeed);**
++++++++++++++++++++++++++++++++++++++++++++++++++++++
   Maps the angular speed to PWM (0-255 range)

**int map_turn_PWM(double ipSpeed);**
++++++++++++++++++++++++++++++++++++++++++++++++++++++
   Maps the turning speed to PWM (0-255 range)

**double mapPosAng(int ipSpeed);**
++++++++++++++++++++++++++++++++++++++++++++++++++++++
   Maps user input angular speed to the positive range of linear speed. Wheels will turn forwards.

**double mapNegAng(int ipSpeed);**
++++++++++++++++++++++++++++++++++++++++++++++++++++++
   Maps user input angular speed to the negative range of linear speed. Wheels will turn backwards

**MotorDirection();**
++++++++++++++++++++++++++++++++++++++++++++++++++++++
   Drives the motor is in the correct direction as per provided PWM.

**I();**
++++++++++++++++++++++++++++++++++++++++++++++++++++++
   Changes Smorphi2 to I-shape if it is not already in I-shape

**O();**
++++++++++++++++++++++++++++++++++++++++++++++++++++++
   Changes Smorphi2 to O-shape if it is not already in O-shape

**J();**
++++++++++++++++++++++++++++++++++++++++++++++++++++++
   Changes Smorphi2 to J-shape if it is not already in J-shape

**T();**
++++++++++++++++++++++++++++++++++++++++++++++++++++++
   Changes Smorphi2 to T-shape if it is not already in T-shape

**L();**
++++++++++++++++++++++++++++++++++++++++++++++++++++++
   Changes Smorphi2 to L-shape if it is not already in L-shape

**S();**
++++++++++++++++++++++++++++++++++++++++++++++++++++++
   Changes Smorphi2 to S-shape if it is not already in S-shape

**Z();**
++++++++++++++++++++++++++++++++++++++++++++++++++++++
   Changes Smorphi2 to Z-shape if it is not already in Z-shape



.. toctree::
   :maxdepth: 2