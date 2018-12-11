# Robot-Localization
This is a project about localization using particular filters. In particular we simulate an environment using gazebo, rviz and ROS and use adaptive monte carlo localization technique to localize the particles.
# Files
There are two folders in this repository:
- Udacity_bot: which contains the file for running the base robot
- myrobot: which contanis the files for running the customized robot
# Installation
In order to be able to replicate the material in this project you will have to have the following. You need to have linux installed. Ideally you should be using Ubuntu 18.04. To install ROS and all the other dependecies you should go to the terminal and type the following:
```
$ sudo apt-get install ros-kinetic-navigation
$ sudo apt-get install ros-kinetic-map-server
$ sudo apt-get install ros-kinetic-move-base
$ rospack profile
$ sudo apt-get install ros-kinetic-amcl
```
# Running
Once you have the required dependencies, move to the right folder and source bash. Move the the either udacity_bot or myrobot to the src file which is inside catkin_ws. Then do the following
```
$ cd ~/catkin_ws
$ catkin_make
$ source devel/setup.bash
```
Then type the following:
```
$ roslaunch udacity_bot udacity_bot
$ roslaunch udacity_bot amcl
$ rosrun udacity_bot navigation goal
```
NB: in the last lines you will have to replace udacity_bot with myrobot if you want to run the customized robot simulation instead. Also each othe three commands above need to be run in a separate terminal sequentially.
