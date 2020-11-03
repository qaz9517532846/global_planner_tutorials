cmake_minimum_required(VERSION 3.0.2)
project(global_planner_tutorials)


find_package(catkin REQUIRED COMPONENTS
  nav_core
  pluginlib
  roscpp
  rospy
  std_msgs
  tf
)

catkin_package(
   INCLUDE_DIRS include
#  LIBRARIES global_planner_tutorials
#  CATKIN_DEPENDS nav_core pluginlib roscpp rospy std_msgs
#  DEPENDS system_lib
)

include_directories(
  include
  ${catkin_INCLUDE_DIRS}
)

add_library(global_planner_lib src/global_planner.cpp)
