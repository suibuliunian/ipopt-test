cmake_minimum_required( VERSION 2.8 )
project(test)

set( CMAKE_BUILD_TYPE "Release" )
set( CMAKE_CXX_FLAGS "-O3" )
set( CMAKE_CXX_FLAGS "-std=c++11")

# 添加头文件
include_directories("/usr/local/include")
# 添加库
link_directories( /usr/local/lib )
# 添加需要编译的可执行文件
add_executable(test test.cpp)

#find_package(Eigen3 REQUIRED)
target_link_libraries(${PROJECT_NAME} ipopt)

