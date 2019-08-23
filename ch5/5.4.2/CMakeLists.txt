cmake_minimum_required(VERSION 3.5)
set(CMAKE_CXX_FLAGS "-std=c++11")

find_package(Sophus REQUIRED)
# Eigen
include_directories("/usr/include/eigen3")
include_directories(${Sophus_INCLUDE_DIRS})

find_package(Pangolin REQUIRED)
# 寻找OpenCV库
find_package(OpenCV REQUIRED)

add_executable(joinMap joinMap.cpp)
target_link_libraries(joinMap ${OpenCV_LIBS} ${Pangolin_LIBRARIES})