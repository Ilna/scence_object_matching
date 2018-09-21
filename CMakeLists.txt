cmake_minimum_required(VERSION 2.8.3)
project(scene_object_matching)

## Compile as C++11, supported in ROS Kinetic and newer
add_compile_options(-std=c++11)

find_package(catkin REQUIRED COMPONENTS
  pcl_conversions
  pcl_ros
  roscpp
  sensor_msgs
)

catkin_package()

include_directories(
# include
  ${catkin_INCLUDE_DIRS}
)

add_executable(scene_object_matching src/scene_object_matching.cpp)
target_link_libraries(scene_object_matching ${catkin_LIBRARIES})