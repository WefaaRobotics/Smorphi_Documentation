.. _FAQ:

FAQ
=====

*Mechanical Hardware*
========================
1. *What are the dimensions of the robot?*
                                -  Smorphi Single with package: 25x25x25cm 
                                - Smorphi Single w/o package: 17x17x21Cm 
                                - Smoprhi2 with Package: 50x30x13cm 

2. *What is the weight of the robot with/without the package? Unassmbled and assembled form*
                                - Weight of the Single with package: 1.8Kg 
                                - Weight of the Square Robot with Package: 5.5KG

3. *How is power managed in the robot? What is the battery capacity? What is its battery life? Charging time?*
                                - The robot's power is managed using a lithium-ion battery with a capacity of 2600 mAh at 3.6V, providing 9.36 Wh of energy. 
                                - Battery Life: Depends on the usage condition. 
                                - Charging Time: Typical lithium-ion batteries with a given capacity may take around 3-4 hours to fully charge using standard chargers. 

4. *Is it capable of handling a payload? If so, how much is the capacity?*
                                Yes, the robot is designed to handle a payload. The payload capacity is up to 800gms for smorphi square, depending on the specific configuration and operational conditions. This capacity was determined to ensure the robot's stability and performance while accommodating typical load requirements for its intended use. 

5. *What is the driving mechanism? Why use the specific architecture?*
                                - The robot utilizes a Mecanum wheel-driven mechanism powered by DC encoder-motors to provide controlled and efficient movement. This architecture was chosen for its simplicity, reliability, and precision in maneuverability, making it well-suited for the robot's operational environment. Additionally, the use of DC motors offers better control over speed and torque, which is essential for ensuring smooth performance in various conditions. 
                                - This specific architecture was selected after evaluating several alternatives, as it provides a cost-effective solution with lower maintenance requirements, while also being easily scalable to meet future needs.

6. *What are the reasons for using the solenoid-latch-based approach for the locking mechanism?* 
                                The decision to use a solenoid-latch-based approach for the locking mechanism was made after extensive evaluation of various alternatives, including hinge-based, magnet-based and electro-magnet-based mechanisms. These alternatives were found to have several drawbacks, such as higher energy consumption, greater complexity, increased number of components, and shorter lifespans. After thorough research, the solenoid-latch mechanism was selected due to its simplicity, reliability, and efficient performance with fewer components, making it a more optimal solution for meeting the design requirements. 

7. *What materials have been used to fabricate the chassis and plates?* 
                                The chassis and plates of the robot were fabricated using Aluminium 5051 grade, which was further enhanced with a black anodized finish for added durability and corrosion resistance. The E-tray plates were constructed from a stiff plastic material, selected for its rigidity and lightweight properties to ensure structural stability and performance.	 

8. *What are the fabrication techniques that have been followed to manufacture the robot?* 
                                The robot's manufacturing process predominantly utilized laser cutting techniques for fabricating all major mechanical and metal components, ensuring precision and high-quality finishes. In addition, many of the remaining parts were off-the-shelf items, sourced to meet the necessary specifications. The electronics and PCBs were custom-designed and fabricated to meet the specific functional requirements of the robot.

*Electronics* 
===============

1. *What controller is used in the robot? Reasons for choosing it. Specify controller model, other relevant ICs such as motor driver, voltage regulators etc.* 
                                Controller Used: ESP32 WROOM-32, 
                                Reasons: One of the most sort out microcontroller which packs a flash memory of 4MB 	and provides enough breakout pins(19) out of which 16 are PWM pnis. Also the 		microcontroller comes with suite of commuincation interfaces such as wifi(802.11 b/g/n), 	bluetooth(BR/EDR/BLE support), 2x I2C interfaces, 2x I2S interfaces, 4x SPI and 2x 	UART interfaces. 
                                Relevant ICs: Adafruit_Motoshield_V2 TB6612FNG Motor Driver  

2. *What is the operating voltage?* 
                                Operating Voltage of the board: 3.3V

3. *What is the motor model that is used to drive the robot?*
                                Square - 
                                        4 (encoder) + 12(non-encoder) 
                                        Gear Ratio: 3:1 (based on 110 RPM output) 

                                Single - 
                                        4 (encoder)  
                                        Gear Ratio: 3:1 (based on 110 RPM output) 
      

4. *Reason for having two boards instead of one?* 
                                        - Master-Slave combination has the following advanatges for Smorphi2: 
                                        - Only Master should be connected to a battery. Other boards can be powered up from the master board. 
                                        - Routing the wires across the modules is easy 
                                        - Not all modules are needed to have information processing capability. Master board acts as information processing center whereas slave board acts as the information carrier there by distributing the work load. 

5. *What is the communication protocol that is used to communicate between the modules?* 
                                        -I2C 

6. How can the sensors be integrated into the robot?  
                                        -Provision to place sensors is available on both Master Board as well as Slave Board 
                                        -Master Board comes with 4 sensor ports, each with 3.3V output and Analog+Digital read/write support. Also has one 5V power pin. 
                                        -Slave Board comes with 6 sensor ports, each with 3.3V output and Digital read/write support. 

7. *What kind of sensors are supported with the current implementation? How many sensors can be connected simultaneously* 
                                        -A maximum of 6 Digital Sensors with 3.3V support (such as IR, Sound)  can be             connected to each Slave Board. 
                                        -A maximum of 2 Analog/Digital Sensors with 3.3V support is recommended to be connected to each Master Board. 
                                        -A maximum of 1 Analog/Digital Sensor with 5V support can ve connected to each Master Board. 

8. *What communication protocols does the robot support?* 
                                        Wifi, Bluetooth, Serial(I2C, I2S, UART)

*Software*
===============

1. What are the languages that can be used to program the robot? 
                                        Arduino(C/C++), Blockly, ROS-C++/Python, Python 
  

2. Is the robot ROS-compatible? If so, explain the architectural flow. Which one ROS1 or ROS2? 
                                        Yes.  
                                        Smorphi Single supports both ROS1 and ROS2. 
                                        Smorphi Square supports ROS1 

3. Possibility of using a secondary controller? If so, what are the communication protocols that the robot supports? 
                                        Compatible with RasberryPi, IPC, STM32. Supports connectivity through USB UART. 

4. Possibility of enabling SLAM? If so, what is the SLAM variant that is currently used, and how accurate is the localization with the current system? 
                                        Yes, SLAM could be enabled. Smorphi Square supports Hector SLAM for ROS1. Smorphi Single supports online_async for ROS2 SLAM toolbox.  

5. Possibility of integrating AI capabilities? If so how? 
                                        Yes. HUSKY LENS comes with inbuilt AI enabled features. Autonomy capability can be enabled through ROS. 


6. Useability in Gazebo and Rviz 
                                        Yes, the algorithm execution can be visualized in Rviz using neccesary ROS packages.



.. toctree::
   :maxdepth: 2