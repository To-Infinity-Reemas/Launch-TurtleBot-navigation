# Launch-TurtleBot-navigation
from that link you will have directions and the commends , so helpful 
https://emanual.robotis.com/docs/en/platform/turtlebot3/quick-start/
#### start with the first  "four" commends:
Open the terminal with Ctrl+Alt+T and enter below commands one at a time.
````
$ sudo apt update
$ sudo apt upgrade
$ wget https://raw.githubusercontent.com/ROBOTIS-GIT/robotis_tools/master/install_ros_noetic.sh
$ chmod 755 ./install_ros_noetic.sh 
$ bash ./install_ros_noetic.sh
````
eache one of this commend in single line " notic that the third one is sooo long commend .

## second Install Dependent ROS Packages
````
$ sudo apt-get install ros-noetic-joy ros-noetic-teleop-twist-joy \
  ros-noetic-teleop-twist-keyboard ros-noetic-laser-proc \
  ros-noetic-rgbd-launch ros-noetic-rosserial-arduino \
  ros-noetic-rosserial-python ros-noetic-rosserial-client \
  ros-noetic-rosserial-msgs ros-noetic-amcl ros-noetic-map-server \
  ros-noetic-move-base ros-noetic-urdf ros-noetic-xacro \
  ros-noetic-compressed-image-transport ros-noetic-rqt* ros-noetic-rviz \
  ros-noetic-gmapping ros-noetic-navigation ros-noetic-interactive-markers
````
this commend is also long and you should write it in one line.

## Install TurtleBot3 Packages
Install TurtleBot3 via Debian Packages.
````
$ sudo apt-get install ros-kinetic-dynamixel-sdk
$ sudo apt-get install ros-kinetic-turtlebot3-msgs
$ sudo apt-get install ros-kinetic-turtlebot3
````

## Install Simulation Package
he TurtleBot3 Simulation Package requires turtlebot3 and turtlebot3_msgs packages as prerequisite.
Without these prerequisite packages, the Simulation cannot be launched.
````
$ cd ~/catkin_ws/src/
$ git clone -b noetic-devel https://github.com/ROBOTIS-GIT/turtlebot3_simulations.git
$ cd ~/catkin_ws && catkin_make
 ````
## Launch Simulation World
Three simulation environments are prepared for TurtleBot3. 

1.Empty World

2.TurtleBot3 World
  
3.TurtleBot3 House 

##### i have choose the second "TurtleBot3 World" one so i will run this command

```
$ export TURTLEBOT3_MODEL=waffle
$ roslaunch turtlebot3_gazebo turtlebot3_world.launch
```
<img width="519" alt="tur gazi" src="https://github.com/user-attachments/assets/b76dbd87-f0aa-41a7-a39e-53ab634dc2f5">


<img width="519" alt="gazi" src="https://github.com/user-attachments/assets/7d269fce-ffa9-475e-ad19-fa7706d8e2bc">


## Opening SLAM
```
roslaunch turtlebot3_slam turtlebot3_slam.launch slam_methods:=gmapping
```

create a map and save it
```
rosrun map_server map_saver -f ~/map
```
then run this command:
```
roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch
```
## navigation
start the navigation and load the saved map, using this command:
```
roslaunch turtlebot3_navigation turtlebot3_navigation.launch map_file:='/home/muh/map.yaml'
```
now You can then move the robot !
