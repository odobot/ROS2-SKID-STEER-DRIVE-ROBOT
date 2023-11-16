# ROS2-SKID-STEER-DRIVE-ROBOT

You need to have installed:
<br>
1. ros-xacro:
   ```console
   sudo apt install ros-<ros2-distro>-xacro
   ```
1. ros-joint-state-publisher: `sudo apt install ros-<ros2-distro>-joint-state-publisher-gui`
1. gazebo-ros: `sudo apt install ros-<ros2-distro>-gazebo-ros-pkgs`

To view the urdf in rviz open 3 terminals:
* `ros2 launch skid_bot rsp.launch.py`
* `rviz2`
* `ros2 run joint_state_publisher_gui joint_state_publisher_gui`

To view the robot in gazebo terminal, run:
* `ros2 launch skid_bot launch_sim.launch.py`


![Screenshot from 2023-11-11 14-38-05](https://github.com/odobot/ROS2-SKID-STEER-DRIVE-ROBOT/assets/103571670/1ca75905-30df-47aa-8e81-8c8cce5b99e7)
