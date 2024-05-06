# rplidar_ros

Add the authority of write: (such as /dev/ttyUSB0)
```bash
ls -l /dev |grep ttyUSB
sudo chmod 666 /dev/ttyUSB0
```
To get /scan topic
```bash
roslaunch rplidar_ros rplidar_a2m12.launch
```