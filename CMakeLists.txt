cmake_minimum_required(VERSION 3.0.2)
project(rft64_6a01_ros_interface)

find_package(catkin REQUIRED COMPONENTS
  geometry_msgs
  roscpp
  rospy
  sensor_msgs
  std_msgs
  message_generation
)

add_service_files(
  FILES
  set_LPF_rate.srv
  set_as_bias.srv
)

generate_messages(
  DEPENDENCIES
  # std_msgs
)

catkin_package(
#  INCLUDE_DIRS include
#  LIBRARIES rft64_6a01_ros_interface
  CATKIN_DEPENDS geometry_msgs roscpp rospy sensor_msgs std_msgs message_runtime
#  DEPENDS system_lib
)

include_directories(
# include
  ${catkin_INCLUDE_DIRS}
)