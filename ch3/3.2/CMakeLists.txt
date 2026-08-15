cmake_minimum_required(VERSION 3.5)
project(useEigen)

set(CMAKE_CXX_STANDARD 14)
set(CMAKE_BUILD_TYPE "Release")
set(CMAKE_CXX_FLAGS "-O3")

# 添加Eigen头文件
#include_directories("/usr/include/eigen3")
include_directories(
        "/opt/homebrew/include/eigen3"
        "/usr/local/include/eigen3"
)
# Find Eigen3 package
#find_package(Eigen3 REQUIRED)
#include_directories(${EIGEN3_INCLUDE_DIR})
add_executable(eigenMatrix eigenMatrix.cpp)
