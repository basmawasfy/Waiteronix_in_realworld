# Waiteronix
This repository contains the software stack and documentation for an Autonomous Mobile Robot (AMR) project. The project aims to develop a fully autonomous robot capable of navigating and performing tasks in dynamic environments.

## Dependencies
* ubuntu
* Ros melodic

## Setup
```bash
mkdir -p waiteronix_ws/src
git clone https://github.com/EmanElsayed149/Waiteronix_in_realworld.git   
```
```bash 
cd ..
catkin_make
source devel/setup.bash
```
## Run
### Mapping
>Note: To make a map you can run get_map launch file( includes all launch files ) or follow the steps in STEPS.md file 
```bash
roslaunch gmapping get_map.launch
```
>Note: we changed coordinates of base_link to make odom , map , footprint frames at the same location at the initial state in (waiteronix/waiteronix_description/urdf/waiteronix.xacro).

>Note: modify custer_wheel frame to be fixed instead of continous(waiteronix/waiteronix_description/urdf/waiteronix.xacro).

>Note: modify lidar_joint to be 3.14 instead of 0 in (waiteronix/waiteronix_description/urdf waiteronix.xacro).
### Navigation
