cmake_minimum_required(VERSION 3.0)
project(joinMap)
set(CMAKE_BUILD_TYPE "Debug")
set(CMAKE_CXX_FLAGS "-std=c++11")

find_package(Sophus REQUIRED)
include_directories(${Sophus_INCLUDE_DIRS})

find_package(Pangolin REQUIRED)
include_directories (${Pangolin_INCLUDE_DIRS})

#find_package( OpenCV 3 REQUIRED)
#include_directories(${OpenCV_INCLUDE_DIRS})

add_executable(joinMap joinMap.cpp)
target_link_libraries(joinMap ${OpenCV_LIBS} ${Pangolin_LIBRARIES} ${Sophus_LIBRARIES})
