# PX4-SITL-Offboard-Control-Custom
N shaped SITL of PX4 in Gazebo Harmonic <br>
Tested on ROS2 humbles, Gazebo Harmonic, Ubuntu 22 <br>


https://github.com/user-attachments/assets/13d14723-47ae-42f1-8d34-098748d52f35


## PX4-SITL Setup
Follow the steps given here to setup SITL with XRCE DDS 
https://kuat-telegenov.notion.site/How-to-setup-PX4-SITL-with-ROS2-and-XRCE-DDS-Gazebo-simulation-on-Ubuntu-22-e963004b701a4fb2a133245d96c4a247
## Download QGroundControl AppImage
To connect gazebo drone to the base station QGC.
## Clone this repository
After cloning, enter the following commands in 4 terminals in this exact order:
```
cd ~/PX4-Autopilot
make px4_sitl gz_x500
```
```
./QGroundControl-x86_64.AppImage
```
```
MicroXRCEAgent udp4 -p 8888
```
Navigate into your workspace and source it. Then,
```
ros2 run trace_n_executor executor
```
