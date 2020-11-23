cmake_minimum_required(VERSION 3.4)
set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

project(formatter_ex_lib)

add_library(formatter_ex_lib STATIC formatter_ex.cpp formatter_ex.h)
target_include_directories(formatter_ex_lib PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/../formatter_lib)

target_link_libraries(formatter_ex_lib formatter_lib)

install(TARGETS formatter_ex_lib DESTINATION lib)
