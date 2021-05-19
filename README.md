# Turtlebot3 with VLP-16
This repo contains the official Turtlebot3 (Waffle) URDF, mounted with Velodyne VLP-16 LIDAR for SLAM purposes in Gazebo simulation.

## Setup
Ensure ROS and Gazebo are installed.

```
cd ~/catkin_ws/src
git clone https://github.com/lamlaaaam/ttb3_velodyne.git
cd ~/catkin_ws
catkin_make

```

## Running
If you have a .world file, place it in `/worlds` and modify the `ttb3_velodyne.launch` file to load your world.

```xml
<arg name="world_name" value="$(find ttb3_velodyne)/worlds/your_world_here.world"/>
```
Launch the simulation
```ros
roslaunch ttb3_velodyne ttb3_velodyne.launch
```
You should see your world in Gazebo and the visualization of the LIDAR in RVIZ.

