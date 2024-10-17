cmake_minimum_required(VERSION 3.0.2)
project(mask_kpts_msgs)

find_package(catkin REQUIRED COMPONENTS
  roscpp
  rospy
  message_generation
  sensor_msgs
  std_msgs
)

# build msg
add_message_files(
  FILES
  Keypoint.msg
  MaskGroup.msg
  MaskKpts.msg
  ImageWithID.msg
)

generate_messages(
  DEPENDENCIES
  std_msgs
  sensor_msgs
)

catkin_package(CATKIN_DEPENDS message_runtime sensor_msgs std_msgs)

## Specify additional locations of header files
include_directories(
# include
  ${catkin_INCLUDE_DIRS}
)
