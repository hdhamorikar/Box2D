cmake_minimum_required(VERSION 3.12)
project(HelloWorld)

set(CMAKE_CXX_STANDARD 11)

INCLUDE_DIRECTORIES("${CMAKE_SOURCE_DIR}")

add_executable(HelloWorld HelloWorld.cpp)

target_link_libraries(HelloWorld Box2D)

