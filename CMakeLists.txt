cmake_minimum_required(VERSION 3.28)

project(test CXX)
set(CMAKE_CXX_STANDARD 20)

find_package (Eigen3 REQUIRED NO_MODULE)

add_executable(test main.cc)
target_sources(test PUBLIC FILE_SET CXX_MODULES FILES a.cppm)
target_link_libraries(test Eigen3::Eigen)
