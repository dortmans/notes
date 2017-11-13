# Simatch

https://github.com/nubot-nudt/simatch

## Install Simatch workspace

cd ~
git clone https://github.com/nubot-nudt/simatch.git

## Install Gazebo

Uninstall Gazebo 2.x

If you decide to use ROS Indigo, please read the following:
If you choose "desktop-full" install of ROS Indigo, there is a Gazebo 2.0 included initially. In order to install Gazebo 5.0/5.1, you should first remove Gazebo 2.0 by running:

```
sudo apt-get remove gazebo
```

Install Gazebo 7.x

http://gazebosim.org/tutorials/?tut=ros_wrapper_versions

```
cd ~/simatch
chmod +x *.sh
./gazebo7_install.sh
sudo apt-get install ros-$ROS_DISTRO-gazebo7-ros-pkgs ros-$ROS_DISTRO-gazebo7-ros-control 
```
## Build Simatch package

Install prerequisites:

```
sudo apt-get install libncurses5-dev
sudo apt-get install qtdeclarative5-dev
```

Then build Simatch:

```
cd ~/simatch
chmod +x configure
./configure
catkin_make
```

## Run Simatch

Set simatch as your active workspace
```
source ~/simatch/devel/setup.bash

```

Run all:

```
roslaunch ~/simatch_cyan.launch
```
or run separately as follows.

To run gazebo_visual separately:
```
roslaunch nubot_gazebo game_ready.launch
```

To run robot_code for cyan or magenta robots:
```
rosrun nubot_common cyan_robot.sh
```
or
```
rosrun nubot_common magenta_robot.sh
```

To run coach4sim:
```
rosrun coach4sim cyan_coach.sh or rosrun coach4sim magenta_coach.sh

```






