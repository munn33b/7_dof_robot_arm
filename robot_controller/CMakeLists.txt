cmake_minimum_required(VERSION 3.0.2)
project(robot_controller)

## Compile as C++11, supported in ROS Kinetic and newer
# add_compile_options(-std=c++11)



find_package(catkin REQUIRED COMPONENTS
  controller_manager
  hardware_interface
  message_generation
  roscpp
  rospy
  std_msgs
)

add_service_files(
  FILES
  AnglesConverter.srv
)

generate_messages(
  DEPENDENCIES
  std_msgs
)

catkin_package(
  INCLUDE_DIRS include
  CATKIN_DEPENDS 
    controller_manager
    hardware_interface
)


include_directories(
  include
  ${catkin_INCLUDE_DIRS}
)







