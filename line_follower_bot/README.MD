# Line Follower Bot

## Introduction-
A Line follower is expected to follow a line continuously through all turns. It should never move out of the line and always maintain its path without fail. To build this robot, the fundamentals of robotics needs to be understood.

## Components Required-  
-Battery  
-Digital Multimeter  
-Breadboard  
-Switch  
-Voltage regulatorIC 7805)  
-Motor Driver(L293D)  
-Motors  
-Infrared Sensors

## LFR Cases-
1. When both the sensors are on the white surface (on either side of the black line);the robot moves forward in a straight line.
2. When the left sensor on black line and right on white;the robot takes a left turn.
3. When the right sensor on black line and left on white;the robot takes a right turn.

**Note-** We can have a fourth case when both the sensors are on the black line.

## Logic Table-
| **Status** | **Left sensors** | **Right sensors** | **Action desired** | **Left motor** | **Right motor**|
|------------|------------------|-------------------|--------------------|----------------|----------------|
| Both sensors not over black line | LOW | LOW | Move straight | Forward | Forward |
| Left sensor over black line | HIGH | LOW | Turn left | Stop | Forward |
| Right sensor over black line | LOW | HIGH | Turn right | Forward | Stop |

## Debugging-
1. Check the connectivity of the circuit connections using the continuity mode of the multimeter.
2. Check the power supply - battery voltage, V<sub>CC</sub> and GND using DC voltage mode of the multimeter.
3. Check the input and appropriate output voltages of all the components in the circuit using DC voltage mode of the multimeter.

