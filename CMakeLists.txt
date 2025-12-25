cmake_minimum_required(VERSION 3.20 FATAL_ERROR)

project("Games101-Homeworks" VERSION 1.0)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

set(HOMEWORK_ROOT_DIR "${CMAKE_CURRENT_SOURCE_DIR}")

add_subdirectory(source)