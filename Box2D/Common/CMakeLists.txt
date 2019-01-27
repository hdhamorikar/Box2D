cmake_minimum_required(VERSION 3.12)
project(Box2D)

set(CMAKE_CXX_STANDARD 14)

# Only if a subdirectory of this directory has `SOURCE` defined
#aux_source_directory(${CMAKE_CURRENT_SOURCE_DIR} SUB_SOURCES)

set(COMMON_SOURCE
        ${CMAKE_CURRENT_SOURCE_DIR}/b2BlockAllocator.cpp
        ${CMAKE_CURRENT_SOURCE_DIR}/b2BlockAllocator.h
        ${CMAKE_CURRENT_SOURCE_DIR}/b2Draw.cpp
        ${CMAKE_CURRENT_SOURCE_DIR}/b2Draw.h
        ${CMAKE_CURRENT_SOURCE_DIR}/b2GrowableStack.h
        ${CMAKE_CURRENT_SOURCE_DIR}/b2Math.cpp
        ${CMAKE_CURRENT_SOURCE_DIR}/b2Math.h
        ${CMAKE_CURRENT_SOURCE_DIR}/b2Settings.cpp
        ${CMAKE_CURRENT_SOURCE_DIR}/b2Settings.h
        ${CMAKE_CURRENT_SOURCE_DIR}/b2StackAllocator.cpp
        ${CMAKE_CURRENT_SOURCE_DIR}/b2StackAllocator.h
        ${CMAKE_CURRENT_SOURCE_DIR}/b2Timer.cpp
        ${CMAKE_CURRENT_SOURCE_DIR}/b2Timer.h
        PARENT_SCOPE
        )
