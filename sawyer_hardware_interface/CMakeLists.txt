cmake_minimum_required(VERSION 2.8.3)
project(sawyer_hardware_interface)

## Add support for C++11, supported in ROS Kinetic and newer
add_definitions(-std=c++11)

find_package(catkin REQUIRED COMPONENTS
  hardware_interface
  roscpp
)

catkin_package(
  INCLUDE_DIRS include
  CATKIN_DEPENDS hardware_interface roscpp
)

include_directories(
  include
  ${catkin_INCLUDE_DIRS}
)

## Mark cpp header files for installation
install(DIRECTORY include/${PROJECT_NAME}/
  DESTINATION ${CATKIN_PACKAGE_INCLUDE_DESTINATION}
)

