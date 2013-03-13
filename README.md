Turtlebot-with-base-Roomba-521
==============================

Turtle bot with Roomba base 521

Steps for setting up Roomba conneted to Turtlebot laptop and workstation laptop :

1. Install ROS on both laptops --> Could be any version of ROS. I tested with ROS Groovy (the latest version) on my workstation laptop
   and ROS Fuerte on turtlebot laptop.

2. Installation instructions can be found here for both version: http://www.ros.org/wiki/turtlebot/Tutorials/

3. Any problems faced during installation can be found at : http://answers.ros.org/questions/

4. Setting up Roomba 521 base by installing Roomba and serial communication stack. Please follow steps as below:

MAKE SURE YOU ROSMAKE OR MAKE (IN GROOVY) AFTER ROS INSTALLATION, OTHERWISE BELOW INSTALLATION AND MAKE AFTERWARDS WON'T FIND
REQUIRED AND NECESSARY HEADER FILES !!

First thing we need to install are the roomba and serial communication stacks. The serial stack:

svn co http://isr-uc-ros-pkg.googlecode.com/svn/stacks/serial_communication/trunk serial

cd serial/cereal_port/ && make

This downloads and builds libcereal from SVN.

The roomba stack:

svn co http://isr-uc-ros-pkg.googlecode.com/svn/stacks/roomba_robot/trunk roomba

This creates the map roomba on the current location with the svn checkout of the link. When u open the roomba map you give the command “make” to get the main build files. Then you go into the map roomba_500_series and do the command “make” again. 
This gives u the binary to run the communication program for communicating from the laptop to the roomba.

