cmake_minimum_required(VERSION 3.12)
project(Box2D)

set(CMAKE_CXX_STANDARD 14)

# Only if a subdirectory of this directory has `SOURCE` defined
#aux_source_directory(${CMAKE_CURRENT_SOURCE_DIR} SUB_SOURCES)

set(JOINTS_SOURCE
        ${CMAKE_CURRENT_SOURCE_DIR}/b2DistanceJoint.cpp
        ${CMAKE_CURRENT_SOURCE_DIR}/b2DistanceJoint.h
        ${CMAKE_CURRENT_SOURCE_DIR}/b2FrictionJoint.cpp
        ${CMAKE_CURRENT_SOURCE_DIR}/b2FrictionJoint.h
        ${CMAKE_CURRENT_SOURCE_DIR}/b2GearJoint.cpp
        ${CMAKE_CURRENT_SOURCE_DIR}/b2GearJoint.h
        ${CMAKE_CURRENT_SOURCE_DIR}/b2Joint.cpp
        ${CMAKE_CURRENT_SOURCE_DIR}/b2Joint.h
        ${CMAKE_CURRENT_SOURCE_DIR}/b2MotorJoint.cpp
        ${CMAKE_CURRENT_SOURCE_DIR}/b2MotorJoint.h
        ${CMAKE_CURRENT_SOURCE_DIR}/b2MouseJoint.cpp
        ${CMAKE_CURRENT_SOURCE_DIR}/b2MouseJoint.h
        ${CMAKE_CURRENT_SOURCE_DIR}/b2PrismaticJoint.cpp
        ${CMAKE_CURRENT_SOURCE_DIR}/b2PrismaticJoint.h
        ${CMAKE_CURRENT_SOURCE_DIR}/b2PulleyJoint.cpp
        ${CMAKE_CURRENT_SOURCE_DIR}/b2PulleyJoint.h
        ${CMAKE_CURRENT_SOURCE_DIR}/b2RevoluteJoint.cpp
        ${CMAKE_CURRENT_SOURCE_DIR}/b2RevoluteJoint.h
        ${CMAKE_CURRENT_SOURCE_DIR}/b2RopeJoint.cpp
        ${CMAKE_CURRENT_SOURCE_DIR}/b2RopeJoint.h
        ${CMAKE_CURRENT_SOURCE_DIR}/b2WeldJoint.cpp
        ${CMAKE_CURRENT_SOURCE_DIR}/b2WeldJoint.h
        ${CMAKE_CURRENT_SOURCE_DIR}/b2WheelJoint.cpp
        ${CMAKE_CURRENT_SOURCE_DIR}/b2WheelJoint.h
        PARENT_SCOPE
        )
