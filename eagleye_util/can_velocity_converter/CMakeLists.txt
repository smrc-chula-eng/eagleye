cmake_minimum_required(VERSION 2.8.3)
project(can_velocity_converter)

find_package(catkin REQUIRED COMPONENTS
  can_msgs
  geometry_msgs
  roscpp
)

catkin_package(
)

include_directories(
  ${catkin_INCLUDE_DIRS}
)

add_executable(can_velocity_converter src/can_velocity_converter.cpp)
target_link_libraries(can_velocity_converter ${catkin_LIBRARIES})
