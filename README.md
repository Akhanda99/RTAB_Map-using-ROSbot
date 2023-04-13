
# 3D Mapping and Autonomous Navigation using ROSBOT

The project "3D Mapping and Autonomous Navigation using ROSBOT" aims to create a 3D map of an unknown environment and perform autonomous navigation into that environment using a mobile robot called ROSBOT. 

For making the 3D map of an unknown environment, RTAB-map is used which is an open-source 3D mapping tool of ROS. The mapping process includes capturing data from a depth camera and LIDAR to construct a 3D point cloud of the environment.

Then the robot is programmed for path planning and autonomous navigation using DWA (Dynamic Window Approach) algorithm. The performance of the robot has been evaluated using the Gazebo Simulator and Rviz. Through different tests, it was observed that the robot successfully reached the goal avoiding obstacles by following an optimal path.

![Logo](https://user-images.githubusercontent.com/62715159/231705133-13938402-2dc4-421b-9f06-803a4f6e0936.png)

https://user-images.githubusercontent.com/62715159/231725967-3e94010f-9106-471d-8c36-104540f4608e.mp4



## Instruction 

Step 1: Run these command one by one to get this package into your own workspace 
```bash
  cd catkin_ws/src
  git clone https://github.com/Akhanda99/RTAB_Map-using-ROSbot.git
  cd ..
  catkin_make
```
Step 2: Run the command to Launch the gazebo file
```bash
  roslaunch RTAB_Map-using-ROSbot rosbot.launch
```

Step 3: Run the command to Launch the rtabmap_ros node
```bash
  roslaunch RTAB_Map-using-ROSbot rtab_map.launch
```
Step 4: Run the command to vizualize the rtab_map
```bash
  roslaunch RTAB_Map-using-ROSbot display.launch
```
Step 5: Launch the teleop.launch and naviagte the robot in the environment

Step 6: For Autonomous Navigation kill the command of rtab_map and rviz in the terminal and run these commands-
```bash
  roslaunch RTAB_Map-using-ROSbot rtab_map.launch localization:= true
  roslaunch RTAB_Map-using-ROSbot navdisplay.launch
```

[Make sure- rtab map is installed in your system]
    
