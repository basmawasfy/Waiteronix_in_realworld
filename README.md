# Waiteronix
This repository contains the software stack and documentation for an Autonomous Mobile Robot (AMR) project. The project aims to develop a fully autonomous robot capable of navigating and performing tasks in dynamic environments.

## Dependencies
* ubuntu
* Ros melodic

## Setup
```bash
mkdir -p waiteronix_ws/src
git clone https://github.com/basmawasfy/Waiteronix_in_realworld.git  
```
```bash 
cd ..
catkin_make
source devel/setup.bash
```
## Run
>Note: To make a map you can run get_map launch file( includes all launch files ) or follow the steps below ... 
```bash
roslaunch gmapping get_map.launch
```
#### Steps
##### RPlidar
To get /scan topic
```bash
ls -l /dev |grep ttyUSB
sudo chmod 666 /dev/ttyUSB0
roslaunch rplidar_ros rplidar_a2m12.launch
```
To make lidar scan only 240 degree instead of 360 degree
```bash
roslaunch waitronix11 laser_filters.launch
```
##### wheel encoder
To get /odom topic
```bash
roslaunch ros_wheel_encoder_odometry odometry.launch
```
##### TF
To include URDF file and TF Displays
```bash 
roslaunch waitronix11 rviz.launch
```
##### In RVIZ
- Add LaserScan , Map, RobotModel , TF Displays, Odometry
- Set the "Fixed Frame"  to  base_link

##### Gmapping
```bash 
roslaunch gmapping gmapping.launch
```
##### Save the map
```bash
rosrun map_server map_saver -f <desired path>
```
