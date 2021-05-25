# Turtlebot3 with VLP-16
This repo contains the official Turtlebot3 (Waffle) URDF, mounted with various sensors for SLAM purposes in Gazebo simulation.

## Setup
Ensure ROS and Gazebo are installed.

```
cd ~/catkin_ws/src
git clone https://github.com/RMFHOPE/turtlebot3_ramp_sim.git
cd ~/catkin_ws
catkin_make
```

## Running
Launch the simulation

```ros
roslaunch turtlebot3_ramp_sim run.launch sensor:=sensor_name world:=world_name
```
Parameters:
- sensor
    - Sensor name. Currently takes in `velodyne`, `hokuyo`, `realsense`. Defaults to `velodyne`.
- world
    - World name. Launches world file in `/worlds` folder. Defaults to `heights.world`.


You should see your world in Gazebo and the visualization in RVIZ.

## Specific instructions for RealSense attachment
In order to run the simulation with RealSense camera, the Gazebo plugin for D435 is required.

```
cd ~/catkin_ws/src
git clone https://github.com/pal-robotics/realsense_gazebo_plugin.git
cd ~/catkin_ws
catkin_make
```

Now you can launch the launch file to view the simulation.
