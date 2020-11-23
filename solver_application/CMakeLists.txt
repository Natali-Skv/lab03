cmake_minimum_required(VERSION 3.4)
set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

project(solver)

add_executable(solver equation.cpp)
target_include_directories(solver PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/../solver_lib)
target_include_directories(solver PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/../formatter_ex_lib)

target_link_libraries(solver solver_lib formatter_ex_lib)

install(TARGETS solver DESTINATION apps)
