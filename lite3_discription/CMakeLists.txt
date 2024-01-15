cmake_minimum_required(VERSION 2.8.3)

project(lite3_discription)

find_package(catkin REQUIRED COMPONENTS
  roscpp
  rospy
  sensor_msgs
  geometry_msgs
  tf
)

catkin_package(
#  INCLUDE_DIRS include
#  LIBRARIES robot_gazebo
#  CATKIN_DEPENDS roscpp rospy std_msgs
#  DEPENDS system_lib
)

# SET(CMAKE_C_COMPILER "aarch64-linux-gnu-gcc")
# SET(CMAKE_CXX_COMPILER "aarch64-linux-gnu-g++") 
set(CMAKE_BUILD_TYPE Release)
set(SRC_DIR_LIST "." src)


add_definitions(-w) # warning ignore
set(CMAKE_CXX_FLAGS "-std=c++11 ${CAMKE_CXX_FLAGS}")








include_directories(${catkin_INCLUDE_DIRS})




#add_executable(${PROJECT_NAME}_sim "src/gazebo_sim.cpp" ${SRC_LIST})
#target_link_libraries(${PROJECT_NAME}_sim -lpthread -lm -lrt -ldl -lstdc++ )
#target_link_libraries(${PROJECT_NAME}_sim  PUBLIC ${catkin_LIBRARIES} )