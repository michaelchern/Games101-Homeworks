cmake_minimum_required(VERSION 3.10)

project(assignment1)
set(CMAKE_CXX_STANDARD 20)

add_subdirectory("${THIRD_PARTY_DIR}/SDL" EXCLUDE_FROM_ALL)
link_libraries(SDL3::SDL3)

add_executable(assignment1 main.cpp rasterizer.hpp rasterizer.cpp Triangle.hpp Triangle.cpp)