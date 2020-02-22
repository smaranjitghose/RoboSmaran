# Obstacle Avoider Bot

## Introduction-
Obstacle detection is a problem in various scenarios in real life and virtual world such as games. While driving a car on the road, the ability to automatically steer away from an obstacle such as another car is essential. Similarly, in the virtual world of games, obstacle avoidance is a physics problem to be considered by the programmer in case of racing games.

## Obstacle Avoider Logic-
An Obstacle Avoider robot avoids obstacles in its path. In order to avoid the obstacle, the first is to sense the obstacle. Once we sense the obstacle, we want to determine a way to avoid obstacle.  

For obstacle avoider, the output of th IR sensor is LOW when an obstacle is detected and is HIGH when it doesn't detect an obstacle. Also, we will be mounting sensors in the front of the robot such that it detects obstacles from three directions:Left, Center and Right. So, we are using three IR sensors in the robot.Extenders are used to keep the sensors protruding in front of the chassis.

As we have 3 sensors in the front, we will have 8 possible cases for this robot. They are as follows:
1. When all the sensors are HIGH: there is no obstacle before the robot and in such a case the robot moves forward.
2. When only left sensor is LOW; the obstacle is present to the left side of the robot and in such case the robot moves right.
3. When only the center sensor is LOW; the obstacle is present in the front of the robotand in such case the robot goes back for a certain    delay and takes a left/right turn.
4. When only the right sensor is LOW; the obstacle is present to the right side of the robot and in such case the robot moves left.
5. When only the right sensor is HIGH; the obstacles are present at both left and center sides and in such case the robot goes back for a    certain delay and turns right.
6. When only the left sensor is HIGH; the obstacles are present at both right and center sides and in such case the robot goes back for a    certain delay and turns left.
7. When only the center sensor is HIGH; the obstacles are present at both left and right sides and in such case the robot moves forward.
8. When all the sensors are LOW; there are obstacles present on all the sides and in such case the robot goes back for a certain delay      and takes a 'U' turn.

## Logic Table-
| **#** | **Left Sensor** | **Center Sensor** | **Right Sensor**| **Obstacle present** | **Action to be taken** | **Left motor** | **Right motor**|
|-------|-----------------|-------------------|-----------------|----------------------|------------------------|----------------|---------------------|
| 1 | HIGH | HIGH | HIGH | No obstacle | Forward | Forward | Forward |
| 2 | HIGH | HIGH | LOW | At right | Turn left | Reverse | Forward |
| 3 | HIGH | LOW | HIGH | At center | Go back and turn right | Reverse and forward | Reverse and reverse |
| 4 | HIGH | LOW | LOW | At center and right | Go back and turn left | Reverse and reverse | Reverse and forward |
| 5 | LOW | HIGH | HIGH | At left | Turn right | Forward | Reverse |
| 6 | LOW | HIGH | LOW | At left and right | Forward | Forward | Forward |
| 7 | LOW | LOW | HIGH | At center and left | Go back and turn right | Reverse and forward | Reverse and reverse |
| 8 | LOW | LOW | LOW | At all sides | U-turn | Reverse and forward | Reverse and reverse |

## Debugging-
1. Check the continuity of the circuit connections using the continuity mode of the multimeter.
2. Check the power supply- battery voltage, V<sub>CC</sub> and GND using DC voltage mode of the multimeter.
3. Check the input and appropriate output volatges of the circuit using DC voltage mode of the multimeter.
