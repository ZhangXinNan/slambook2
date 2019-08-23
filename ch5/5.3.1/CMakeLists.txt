cmake_minimum_required(VERSION 3.5)
set(CMAKE_CXX_FLAGS "-std=c++11")
project(imageBasics)

# 寻找OpenCV库
find_package(OpenCV REQUIRED)

add_executable(imageBasics imageBasics.cpp)
# 链接OpenCV库
target_link_libraries(imageBasics ${OpenCV_LIBS})
message(STATUS ${OpenCV_LIBS})

# add_executable(undistortImage undistortImage.cpp)
# # 链接OpenCV库
# target_link_libraries(undistortImage ${OpenCV_LIBS})
