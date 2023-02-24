cmake_minimum_required(VERSION 3.0.2)
project(drive_controller)

add_compile_options(-std=c++11)

find_package(catkin REQUIRED COMPONENTS
  roscpp tf
)

catkin_package(
  CATKIN_DEPENDS roscpp
)

include_directories(
  ${catkin_INCLUDE_DIRS}
)

add_executable(drive_controller_node src/drive_controller.cpp)

target_link_libraries(drive_controller_node
    ${catkin_LIBRARIES}
)
