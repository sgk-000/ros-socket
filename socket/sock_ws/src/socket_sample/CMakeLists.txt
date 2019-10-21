cmake_minimum_required(VERSION 2.8.3)
project(socket_sample)

find_package(catkin REQUIRED COMPONENTS
  roscpp
  rospy
  std_msgs
)

catkin_package(
#  INCLUDE_DIRS include
#  LIBRARIES socket_sample
#  CATKIN_DEPENDS roscpp rospy std_msgs
#  DEPENDS system_lib
)

###########
## Build ##
###########

include_directories(
# include
  ${catkin_INCLUDE_DIRS}
)

add_executable(${PROJECT_NAME} src/server.cpp)
target_link_libraries(${PROJECT_NAME} ${catkin_LIBRARIES} )
