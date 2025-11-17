.. _diagnostics:

Diagnostics & Troubleshooting
================================

*Problem: Can’t see the ESP32 boards in the IDE Tools menu.*
+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
*Solution*: Make sure to click on the small arrow at the bottom to scroll all the way down through the boards.
If you still can’t find ESP32 Dev Module, we recommend repeating the installation process from scratch.
Click here to access the Installation Guide.

*Problem: A fatal error occurred: “Failed to connect to ESP32: Timed out… Connecting…”*
+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
When you try to upload a new sketch or programme to your ESP32, it fails to connect and this appears on IDE. It implies that either your ESP32 is:

1. Not in flashing/uploading mode
2. Not in the correct board or com port
   
   |
   
*Solution*: Hold the “BOOT” button on your ESP32 board, then press and hold the “ENABLE” button. Release your finger from the “BOOT” button whenever you see “Connecting...” in the IDE bottom bar. You will notice the message “Done uploading” after some time.

*Problem: COM Port is not found/not available.*
++++++++++++++++++++++++++++++++++++++++++++++++++
If you connect your ESP32 board to your computer but are unable to locate the port in your IDE. It could be one of the following issues:

1. USB drivers are not installed If you don’t see the ESP’s COM port, it’s because you don’t have the USB drivers installed on your computer.
*Solution*: Examine the chip adjacent to the chip regulator on the board and make a note of its name. It’ll most likely be CP2102. This driver is available on the Silicon Labs website. After installing the CP2102 driver, restart IDE (close current tab and reload) and the COM port should appear in the Tools menu.

1. USB cable without data wires Data wires are missing from some USB cables used by power banks (used for charging purposes only). As a result, your computer will never be able to communicate serially with your ESP32. Your problem should be solved if you use a suitable USB cord.
*Solution*: Connect your USB cable to your phone and computer to see whether it can transfer data. If it can, the problem is not with the cable; if it can’t, you’ll need to acquire a new data cable.

1. ESP32 is damaged If you have the correct USB drivers loaded and your data cord is in good working condition. Then there’s a chance it’s a problem with the ESP32.
*Solution*: Check to see if your ESP32 has been overheated or if you can detect a burning odour in the area. If you answered yes, you should obtain a new one.

*Problem: IDE Serial Monitor is not working.*
+++++++++++++++++++++++++++++++++++++++++++++++
*Solution*: If the ESP32 is only printing weird text or gibberish messages in your IDE Serial Monitor, make sure you have the right COM port selected and set the right baud rate. In most examples, we’re using 115200 baud rate.

*Problem: Error: “Brownout detector was triggered”*
+++++++++++++++++++++++++++++++++++++++++++++++++++++
When you open your IDE Serial Monitor and the error message “Brownout detector was trigger” is being constantly printed over and over again. It means that there’s some sort of hardware problem. It’s often related to one of the following issues:

1. Poor quality USB cable
2. USB cable is too long
3. Board with some defect (bad solder joints)
4. Bad computer USB port
5. Not enough power provided by the computer USB port
   
*Solution*: Try a different shorter USB cable (with data wires), try a different computer USB port or use a USB hub with an external power supply



.. toctree::
   :maxdepth: 2