cmake_minimum_required(VERSION 3.7.1)
set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

option(BUILD_APPS "Build apps" OFF)

project(project)

IF(CMAKE_INSTALL_PREFIX_INITIALIZED_TO_DEFAULT) 
    SET(CMAKE_INSTALL_PREFIX "${CMAKE_CURRENT_SOURCE_DIR}/_install" CACHE PATH "..." FORCE)
ENDIF(CMAKE_INSTALL_PREFIX_INITIALIZED_TO_DEFAULT)
message("Install dir prefix: ${CMAKE_INSTALL_PREFIX}")

add_subdirectory(formatter_lib lib/formatter_lib)
add_subdirectory(formatter_ex_lib lib/formatter_ex_lib)
add_subdirectory(solver_lib lib/solver_lib)

IF(BUILD_APPS)
    add_subdirectory(hello_world_application apps/hello_world_application)
    add_subdirectory(solver_application apps/solver_application)
ENDIF()


