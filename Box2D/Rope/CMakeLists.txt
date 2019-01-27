cmake_minimum_required(VERSION 3.12)
project(Box2D)

set(CMAKE_CXX_STANDARD 14)

# Only if a subdirectory of this directory has `SOURCE` defined
#aux_source_directory(${CMAKE_CURRENT_SOURCE_DIR} SUB_SOURCES)

set(ROPE_SOURCE
        ${CMAKE_CURRENT_SOURCE_DIR}/b2Rope.cpp
        ${CMAKE_CURRENT_SOURCE_DIR}/b2Rope.h
        PARENT_SCOPE
        )
