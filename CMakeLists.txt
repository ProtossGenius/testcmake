cmake_minimum_required(VERSION 3.8)
project(myproj)

set(CMAKE_EXPORT_COMPILE_COMMANDS ON)
include_directories(. "./third_part/")

add_subdirectory(math_funcs)
add_subdirectory(app)

add_executable(myproj main.cpp)

target_link_libraries(myproj app math_funcs)

