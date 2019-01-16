cmake_minimum_required(VERSION 3.12)
project(Box2D)

set(CMAKE_CXX_STANDARD 14)

# Only if a subdirectory of this directory has `SOURCE` defined
#aux_source_directory(${CMAKE_CURRENT_SOURCE_DIR} SUB_SOURCES)

set(JOINTS_SOURCE
        b2DistanceJoint.cpp
        b2DistanceJoint.h
        b2FrictionJoint.cpp
        b2FrictionJoint.h
        b2GearJoint.cpp
        b2GearJoint.h
        b2Joint.cpp
        b2Joint.h
        b2MotorJoint.cpp
        b2MotorJoint.h
        b2MouseJoint.cpp
        b2MouseJoint.h
        b2PrismaticJoint.cpp
        b2PrismaticJoint.h
        b2PulleyJoint.cpp
        b2PulleyJoint.h
        b2RevoluteJoint.cpp
        b2RevoluteJoint.h
        b2RopeJoint.cpp
        b2RopeJoint.h
        b2WeldJoint.cpp
        b2WeldJoint.h
        b2WheelJoint.cpp
        b2WheelJoint.h
        PARENT_SCOPE
        )
