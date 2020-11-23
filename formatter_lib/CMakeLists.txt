cmake_minimum_required(VERSION 3.4)
set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

project(formatter_lib)

add_library(formatter_lib STATIC formatter.cpp formatter.h)

install(TARGETS formatter_lib DESTINATION lib)
