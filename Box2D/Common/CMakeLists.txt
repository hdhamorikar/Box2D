cmake_minimum_required(VERSION 3.12)
project(Box2D)

set(CMAKE_CXX_STANDARD 14)

# Only if a subdirectory of this directory has `SOURCE` defined
#aux_source_directory(${CMAKE_CURRENT_SOURCE_DIR} SUB_SOURCES)

set(COMMON_SOURCE
        b2BlockAllocator.cpp
        b2BlockAllocator.h
        b2Draw.cpp
        b2Draw.h
        b2GrowableStack.h
        b2Math.cpp
        b2Math.h
        b2Settings.cpp
        b2Settings.h
        b2StackAllocator.cpp
        b2StackAllocator.h
        b2Timer.cpp
        b2Timer.h
        PARENT_SCOPE
        )
