cmake_minimum_required(VERSION 2.8.3)
project(path_planning_vrep_simulation)

catkin_python_setup()

find_package (
  catkin REQUIRED COMPONENTS
  roscpp
  rospy
  message_generation
)


add_message_files (
  FILES
  Point2d.msg
  MarkerData.msg
  RobotData.msg
  GoalData.msg
  ObstacleData.msg
  FieldObjects.msg
  Path.msg
  AllPathes.msg
  RobotMovement.msg
  XML_PATH.msg
  Step.msg
  WheelRotationData.msg
  All_XML_PATHS.msg
)


generate_messages (
  DEPENDENCIES
  std_msgs
)


catkin_package (
  CATKIN_DEPENDS message_runtime
)


include_directories (
  ${catkin_INCLUDE_DIRS}
)

