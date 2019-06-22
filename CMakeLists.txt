cmake_minimum_required(VERSION 3.10)

project(openjdk CXX)

set(CMAKE_CXX_STANDARD 14)

add_subdirectory(hotspot)

add_executable(main main.cpp)