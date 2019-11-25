cmake_minimum_required(VERSION 2.8)
add_definitions(-std=c++11 -Wall -O2)
project(chapter3)

# 加入各子工程
add_subdirectory(useEigen)
add_subdirectory(useGeometry)
add_subdirectory(visualizeGeometry)
add_subdirectory(examples)
