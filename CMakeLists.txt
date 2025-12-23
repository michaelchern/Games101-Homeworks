cmake_minimum_required(VERSION 3.10)

project("Games101 Homeworks" VERSION 0.1.0)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

set(THIRD_PARTY_DIR "${CMAKE_CURRENT_SOURCE_DIR}/source/third_party")
add_subdirectory(source/assignment1)