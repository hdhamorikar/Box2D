cmake_minimum_required(VERSION 3.12)
project(Box2D)

set(CMAKE_CXX_STANDARD 14)

# Only if a subdirectory of this directory has `SOURCE` defined
#aux_source_directory(${CMAKE_CURRENT_SOURCE_DIR} SUB_SOURCES)

set(CONTACTS_SOURCE
        b2ChainAndCircleContact.cpp
        b2ChainAndCircleContact.h
        b2ChainAndPolygonContact.cpp
        b2ChainAndPolygonContact.h
        b2CircleContact.cpp
        b2CircleContact.h
        b2Contact.cpp
        b2Contact.h
        b2ContactSolver.cpp
        b2ContactSolver.h
        b2EdgeAndCircleContact.cpp
        b2EdgeAndCircleContact.h
        b2EdgeAndPolygonContact.cpp
        b2EdgeAndPolygonContact.h
        b2PolygonAndCircleContact.cpp
        b2PolygonAndCircleContact.h
        b2PolygonContact.cpp
        b2PolygonContact.h
        PARENT_SCOPE
        )
