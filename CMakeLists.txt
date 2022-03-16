cmake_minimum_required(VERSION 3.0.2)
project(realsense_435_description)

find_package(catkin REQUIRED COMPONENTS
  gazebo_dev
  gazebo_msgs
  roscpp
  nodelet
  sensor_msgs
  urdf
  tf
  tf2_ros
  rosconsole
  diagnostic_updater
  std_msgs
  gazebo_ros
  image_transport
  camera_info_manager
)

find_package(Boost REQUIRED COMPONENTS thread)
# find_package(gazebo REQUIRED)

link_directories(
  ${catkin_LIBRARY_DIRS}
)

catkin_package(
  LIBRARIES
  CATKIN_DEPENDS
  message_runtime
  gazebo_msgs
  roscpp
  nodelet
  geometry_msgs
  sensor_msgs
  urdf
  tf
  tf2_ros
  rosconsole
  std_msgs
  gazebo_ros
  image_transport
  camera_info_manager
)

#############
## Install ##
#############

install(DIRECTORY meshes
    DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)

install(DIRECTORY xacro
    DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)
