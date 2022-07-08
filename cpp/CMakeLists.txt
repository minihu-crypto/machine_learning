cmake_minimum_required(VERSION 3.22.1)

project(cpp)

set(CMAKE_CXX_STANDARD 17)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FALGS} -D_LIBCPP_DEBUG_LEVEL=2")

find_package(Eigen3 3.3 REQUIRED NO_MODULE)

include_directories(${EIGEN3_INCLUDE_DIRS})

add_executable(main main.cpp)

target_link_libraries(main Eigen3::Eigen)