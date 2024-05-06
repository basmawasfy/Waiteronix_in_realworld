# laser_filter
It uses **laser_filters** package https://wiki.ros.org/laser_filters 

To install laser_filters pkg
```bash
sudo apt install ros-melodic-laser-filters
```
To make lidar scan only 240 degree instead of 360 degree
```bash
roslaunch laser_filter laser_filter.launch
```
To make lidar scan only 3 meters instead of 16 meters
```bash
roslaunch laser_filter distance_filter.launch
```
>Note: you can modify the distance range in distance_range.yaml file