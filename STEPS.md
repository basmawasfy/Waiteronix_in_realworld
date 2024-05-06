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
roslaunch laser_filter laser_filter.launch
```
##### wheel encoder
To get /odom topic
```bash
roslaunch ros_wheel_encoder_odometry odometry.launch
```
##### TF
To include URDF file and TF Displays
```bash 
roslaunch waitronix_description rviz.launch
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
