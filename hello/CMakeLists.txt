cmake_minimum_required(VERSION 3.0.0)
project(Hello VERSION 0.1.0)

set(CMAKE_MODULE_PATH ${CMAKE_MODULE_PATH} "${CMAKE_SOURCE_DIR}/cmake/")

find_package(SDL2 REQUIRED)

include_directories(${SDL2_INCLUDE_DIRS})

set(CMAKE_CXX_STANDARD 11)

add_executable(Hello WIN32 main.cpp)

target_link_libraries(Hello ${SDL2_LIBRARIES})

