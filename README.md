# 7 Degrees of Freedom Robotic Arm Simulation in Gazebo with ROS Controllers

##### Steps to Run Simulation:

Go to <Your_ROS_Workspace>/src and clone the Repository

```bash
git clone https://github.com/munn33b/7_dof_robot_arm.git
```

Rebuild the Workspace

```bash
cd <Your_ROS_WORKSPACE>
```

```bash
catkin_make
```

Source the workspace

```bash
source devel/setup.bash
```

Now Run the Simulation

```bash
roslaunch robot_urdf gazebo.launch
```

In another Terminal

```bash
roslaunch robot_moveit move_group.launch
```

In another terminal, open RViz (ROS Visualization)

```bash
rosrun rviz rviz
```

In RViz, add the Robot Model and set Fixed Frame to "world". Add "Motion Planning" in RViz, to execute Motion Planning Pipeline. You can give random positions to Motion Planner in RViz, the robotic arm will move following the commanded trajectory by following the constraints defined in ROS Controllers configuration file.
