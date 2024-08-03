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
