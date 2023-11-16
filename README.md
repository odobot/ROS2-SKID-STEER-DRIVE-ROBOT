# ROS2-SKID-STEER-DRIVE-ROBOT
### Dependencies
You need to have installed:
<br>
1. ros-xacro:
   ```console
   sudo apt install ros-<ros2-distro>-xacro
   ```
2. ros-joint-state-publisher:
   ```console
   sudo apt install ros-<ros2-distro>-joint-state-publisher-gui
   ```
3. gazebo-ros:
   ```console
   sudo apt install ros-<ros2-distro>-gazebo-ros-pkgs
   ```
### :hammer: How to build
To build the packages in this repository follow these steps:
1. `cd` into an existing or create a new [workspace](https://docs.ros.org/en/foxy/Tutorials/Beginner-Client-Libraries/Creating-A-Workspace/Creating-A-Workspace.html)
   ```console
   mkdir -p skidbot_ws/src
   ```
2. clone this repository in the `src` folder of your workspace
   ```console
   cd skidbot_ws/src
   ```
   ```console
   git clone
   ```
3. Naviage back to the workspace folder
   ```console
   cd ../
   ```
4. build the workspace using the [colcon](https://colcon.readthedocs.io/en/released/reference/verb/build.html) build tool
   ```console
   colcon build --symlink-install
   ```
5. source the `setup.bash` file
   ```console
   source install/setup.bash
   ```
6. You can add the `setup.bash` file on the bashrc script file, just open the file and add it at end:
    ```console
    gedit ~/.bashrc
    ```
    ```console
    source ~/skidbot_ws/install/setup.bash
    ```
### :movie_camera: Rviz
To view the urdf in rviz open 3 terminals:
<br>
On the first terminal (needs to the terminal you sourced your setup.bash file in) type: 
```console
  ros2 launch skid_bot rsp.launch.py
  ```
Second terminal
 ```console
  rviz2
  ```
third terminal
 ```console
  ros2 run joint_state_publisher_gui joint_state_publisher_gui
 ```
![Screenshot from 2023-11-16 16-02-27](https://github.com/odobot/ROS2-SKID-STEER-DRIVE-ROBOT/assets/103571670/e7bb611b-5368-44b6-85a7-351850f8b926)
### 🎥 Gazebo
To view and control the robot in gazebo:
<br>
Run:
```console
ros2 launch skid_bot launch_sim.launch.py
```
```console
ros2 run teleop_twist_keyboard teleop_twist_keyboard
```
https://github.com/odobot/ROS2-SKID-STEER-DRIVE-ROBOT/assets/103571670/b3845ec1-4964-4fd9-8562-eed8877648f8
### 🎥 Gazebo & Rviz
Viewing the robot in gazebo and get its relative position to the centre using Rviz
<br>
Run:
```console
ros2 launch skid_bot launch_sim.launch.py
```
```console
ros2 run teleop_twist_keyboard teleop_twist_keyboard
```
```console
rviz2
```
https://github.com/odobot/ROS2-SKID-STEER-DRIVE-ROBOT/assets/103571670/4eef568e-bc4f-4fca-9b83-a9ddb1d82e8a
