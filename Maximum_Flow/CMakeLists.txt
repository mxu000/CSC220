cmake_minimum_required(VERSION 3.9)
project(hw3)

set(CMAKE_CXX_STANDARD 11)

add_executable(hw3 main.cpp)

MATH(EXPR stack_size "1024 * 1024 * 1024") # 16 Mb
set(CMAKE_EXE_LINKER_FLAGS "-Wl,--stack,${stack_size}")