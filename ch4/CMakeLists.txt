cmake_minimum_required(VERSION 2.8)
project(useSophus)
add_definitions(-std=c++11 -Wall -O2)

# 为使用 sophus，需要使用find_package命令找到它
find_package(Sophus REQUIRED)
#include_directories(${Sophus_INCLUDE_DIRS})
#include_directories("/home/tim/slambook2/3rdparty/Sophus/")
if(Sophus_FOUND)
    add_executable(useSophus useSophus.cpp)
    #target_link_libraries(useSophus ${Sophus_LIBRARIES})
    message("${SOPHUS_INCLUDE_DIRS} found ${SOPHUS_LIBRARY}")
endif(Sophus_FOUND)


# Eigen
#include_directories("/usr/include/eigen3")
find_package(Eigen3 REQUIRED)
if(EIGEN3_FOUND)
    message("${EIGEN3_INCLUDE_DIRS} found ")
endif(EIGEN3_FOUND)
include_directories(${EIGEN3_INCLUDE_DIRS})




add_subdirectory(example)
