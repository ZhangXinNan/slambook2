cmake_minimum_required(VERSION 2.8)
# 不加这个会报错！！！！！！
set(CMAKE_CXX_FLAGS "-std=c++11")
project(useSophus)


# 为使用 sophus，需要使用find_package命令找到它
find_package(Sophus REQUIRED)
set(Sophus_INCLUDE_DIRS "/usr/local/include")
include_directories(${Sophus_INCLUDE_DIRS})
message( STATUS ${Sophus_INCLUDE_DIRS} )
# Eigen
include_directories("/usr/include/eigen3")
add_executable(useSophus useSophus.cpp)

# add_subdirectory(example)
