cmake_minimum_required(VERSION 3.0.2)
project(hospital_sample_carrier)

find_package(catkin REQUIRED COMPONENTS
  roscpp
  rospy
  std_msgs
  urdf
  xacro
  robot_state_publisher
  joint_state_publisher
  joint_state_publisher_gui
  rviz
)

catkin_package()

include_directories(${catkin_INCLUDE_DIRS})

install(DIRECTORY launch urdf rviz
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)