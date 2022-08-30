# # local_planer_ws
cosmap_2d integration with YDlidar and teb local planner

to use this integration use the following commands
first install the YDlidar-SDK 
```
git clone https://github.com/YDLIDAR/YDLidar-SDK.git
cd YDLidar-SDK/
mkdir build
cd build
cmake ..
make
sudo make install
```
go back to your home directory or where you want to install and follow this steps
 ```
 git clone https://github.com/tobiwg/local_planer_ws.git
cd local_planer_ws
catkin build
chmod 0777 src/ydlidar_ros_driver/startup/*
sudo sh src/ydlidar_ros_driver/startup/initenv.sh
```
to run the package
```
source devel/setup.bash
roslaunch launcher supreme_launcher.launch
```

FAQ:

if you get the error that you are missing the tf2_geometry_msgs files
```
sudo apt-get install ros-ROS_DISTRO-tf2-geometry-msgs
```
if you get the error that you are missing the voxel-grid files
```
sudo apt-get install ros-ROS_DISTRO-voxel-grid
```

