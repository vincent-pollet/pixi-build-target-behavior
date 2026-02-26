cmake_minimum_required(VERSION 3.29)
project(example)

set(PROJECT_VERSION "0.1.0")

include_directories(${CMAKE_CURRENT_SOURCE_DIR})
include_directories(${CMAKE_CURRENT_BINARY_DIR})
include_directories(${CMAKE_CURRENT_SOURCE_DIR}/src)
include_directories(${CMAKE_CURRENT_BINARY_DIR}/src)

set(HELLO_WORLD ${CMAKE_CURRENT_BINARY_DIR}/src/example)

add_subdirectory(src)
