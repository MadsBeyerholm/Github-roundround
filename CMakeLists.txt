cmake_minimum_required(VERSION 2.8.3)
project(turtlesim_games)

add_compile_options(-std=c++11)


find_package(catkin REQUIRED COMPONENTS
    roscpp
    geometry_msgs
    turtlesim
)


include_directories(
    ${catkin_INCLUDE_DIRS}
)

add_executable(roundround src/roundround.cpp)

target_link_libraries(roundround
    ${catkin_LIBRARIES}
)