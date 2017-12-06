cmake_minimum_required(VERSION 2.8.3)
project(iiwa_tool_examples)

set(CMAKE_CXX_FLAGS "-std=c++11 ${CMAKE_CXX_FLAGS}")

find_package(catkin REQUIRED COMPONENTS
  roscpp
  iiwa_ros
  moveit_core 
  moveit_ros_planning
  moveit_ros_planning_interface
)

catkin_package()

include_directories(include ${catkin_INCLUDE_DIRS})

<<<<<<< HEAD
add_executable(command_robot2 src/command_robot.cpp)
add_dependencies(command_robot2 iiwa_msgs_generate_messages_cpp)
target_link_libraries(command_robot2 ${catkin_LIBRARIES})

add_executable(command_robot_moveit2 src/command_robot_moveit.cpp)
add_dependencies(command_robot_moveit2 iiwa_msgs_generate_messages_cpp)
target_link_libraries(command_robot_moveit2 ${catkin_LIBRARIES})

add_executable(setting_control_mode2 src/setting_control_mode.cpp)
add_dependencies(setting_control_mode2 iiwa_msgs_generate_messages_cpp)
target_link_libraries(setting_control_mode2 ${catkin_LIBRARIES})
=======
add_executable(command_robot src/command_robot.cpp)
add_dependencies(command_robot iiwa_msgs_generate_messages_cpp)
target_link_libraries(command_robot ${catkin_LIBRARIES})

add_executable(command_robot_moveit src/command_robot_moveit.cpp)
add_dependencies(command_robot_moveit iiwa_msgs_generate_messages_cpp)
target_link_libraries(command_robot_moveit ${catkin_LIBRARIES})

add_executable(setting_control_mode src/setting_control_mode.cpp)
add_dependencies(setting_control_mode iiwa_msgs_generate_messages_cpp)
target_link_libraries(setting_control_mode ${catkin_LIBRARIES})
>>>>>>> 20fcf8485dff3c20916504dbceb5bc641b7f4b0a
