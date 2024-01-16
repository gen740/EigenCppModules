cmake_minimum_required(VERSION 3.28)

project(example CXX)

set(CMAKE_EXPORT_COMPILE_COMMANDS ON)
set(CMAKE_CXX_STANDARD 23)

add_executable(test main.cc)
target_sources(test PUBLIC FILE_SET CXX_MODULES FILES a.cppm)
