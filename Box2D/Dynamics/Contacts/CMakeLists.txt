cmake_minimum_required(VERSION 3.12)
project(Box2D)

set(CMAKE_CXX_STANDARD 14)

# Only if a subdirectory of this directory has `SOURCE` defined
#aux_source_directory(${CMAKE_CURRENT_SOURCE_DIR} SUB_SOURCES)

set(CONTACTS_SOURCE
        ${CMAKE_CURRENT_SOURCE_DIR}/b2ChainAndCircleContact.cpp
        ${CMAKE_CURRENT_SOURCE_DIR}/b2ChainAndCircleContact.h
        ${CMAKE_CURRENT_SOURCE_DIR}/b2ChainAndPolygonContact.cpp
        ${CMAKE_CURRENT_SOURCE_DIR}/b2ChainAndPolygonContact.h
        ${CMAKE_CURRENT_SOURCE_DIR}/b2CircleContact.cpp
        ${CMAKE_CURRENT_SOURCE_DIR}/b2CircleContact.h
        ${CMAKE_CURRENT_SOURCE_DIR}/b2Contact.cpp
        ${CMAKE_CURRENT_SOURCE_DIR}/b2Contact.h
        ${CMAKE_CURRENT_SOURCE_DIR}/b2ContactSolver.cpp
        ${CMAKE_CURRENT_SOURCE_DIR}/b2ContactSolver.h
        ${CMAKE_CURRENT_SOURCE_DIR}/b2EdgeAndCircleContact.cpp
        ${CMAKE_CURRENT_SOURCE_DIR}/b2EdgeAndCircleContact.h
        ${CMAKE_CURRENT_SOURCE_DIR}/b2EdgeAndPolygonContact.cpp
        ${CMAKE_CURRENT_SOURCE_DIR}/b2EdgeAndPolygonContact.h
        ${CMAKE_CURRENT_SOURCE_DIR}/b2PolygonAndCircleContact.cpp
        ${CMAKE_CURRENT_SOURCE_DIR}/b2PolygonAndCircleContact.h
        ${CMAKE_CURRENT_SOURCE_DIR}/b2PolygonContact.cpp
        ${CMAKE_CURRENT_SOURCE_DIR}/b2PolygonContact.h
        PARENT_SCOPE
        )
