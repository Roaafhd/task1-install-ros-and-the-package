# task1-install-ros-and-the-package
# Steps to install Ros melodic
These are the steps I used to install Ros melodic on Ubuntu 18.04

#1

$ sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'

#2

$ sudo apt-key adv --keyserver 'hkp://keyserver.ubuntu.com:80' --recv-key C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654

#3

$ sudo apt update

#4

$ sudo apt install ros-melodic-desktop-full

#5

$ echo "source /opt/ros/melodic/setup.bash" >> ~/.bashrc
$ source ~/.bashrc

#6

$ sudo apt install python-rosdep python-rosinstall python-rosinstall-generator python-wstool build-essential

#7

$ sudo apt install python-rosdep
$ sudo rosdep init
$ rosdep update

to start ros type:  “ roscore”
 
# These steps to install the package 

First, create a workspace using catkin_make
 
$ source /opt/ros/noetic/setup.bash
$ mkdir -p ~/catkin_ws/src
$ cd ~/catkin_ws/
$ catkin_make

# Installing the package arduino_robot_arm

add the package to “src” folder 
$ cd ~/catkin_ws/src

$ sudo apt install git

$ git clone https://github.com/smart-methods/arduino_robot_arm

# Install 
$ cd ~/catkin_ws

$ rosdep install --from-paths src --ignore-src -r -y

$ sudo apt-get install ros-melodic-moveit

$ sudo apt-get install ros-melodic-joint-state-publisher ros-melodic-joint-state-publisher-gui

$ sudo apt-get install ros-melodic-gazebo-ros-control joint-state-publisher

$ sudo apt-get install ros-melodic-ros-controllers ros-melodic-ros-control

# Compile the package 
$ catkin_make

# To run the package 

$ roslaunch robot_arm_pkg check_motors.launch

# This window will show 
![IMG_2627](https://user-images.githubusercontent.com/86249220/123991281-40989380-d9d3-11eb-948f-cf5123677671.jpeg)
![IMG_2628](https://user-images.githubusercontent.com/86249220/123991619-8ce3d380-d9d3-11eb-830e-a759db13b852.jpeg)
