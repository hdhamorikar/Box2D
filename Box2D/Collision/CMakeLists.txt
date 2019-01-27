cmake_minimum_required(VERSION 3.12)
project(Box2D)

set(CMAKE_CXX_STANDARD 11)

# Only if a subdirectory of this directory has `SOURCE` defined
#aux_source_directory(${CMAKE_CURRENT_SOURCE_DIR} SUB_SOURCES)

set(COLLISION_SOURCE
        ${CMAKE_CURRENT_SOURCE_DIR}/b2BroadPhase.cpp
        ${CMAKE_CURRENT_SOURCE_DIR}/b2BroadPhase.h
        ${CMAKE_CURRENT_SOURCE_DIR}/b2CollideCircle.cpp
        ${CMAKE_CURRENT_SOURCE_DIR}/b2CollideEdge.cpp
        ${CMAKE_CURRENT_SOURCE_DIR}/b2CollidePolygon.cpp
        ${CMAKE_CURRENT_SOURCE_DIR}/b2Collision.cpp
        ${CMAKE_CURRENT_SOURCE_DIR}/b2Collision.h
        ${CMAKE_CURRENT_SOURCE_DIR}/b2Distance.cpp
        ${CMAKE_CURRENT_SOURCE_DIR}/b2Distance.h
        ${CMAKE_CURRENT_SOURCE_DIR}/b2DynamicTree.cpp
        ${CMAKE_CURRENT_SOURCE_DIR}/b2DynamicTree.h
        ${CMAKE_CURRENT_SOURCE_DIR}/b2TimeOfImpact.cpp
        ${CMAKE_CURRENT_SOURCE_DIR}/b2TimeOfImpact.h
        ${CMAKE_CURRENT_SOURCE_DIR}/Shapes/b2ChainShape.cpp
        ${CMAKE_CURRENT_SOURCE_DIR}/Shapes/b2ChainShape.h
        ${CMAKE_CURRENT_SOURCE_DIR}/Shapes/b2CircleShape.cpp
        ${CMAKE_CURRENT_SOURCE_DIR}/Shapes/b2CircleShape.h
        ${CMAKE_CURRENT_SOURCE_DIR}/Shapes/b2EdgeShape.cpp
        ${CMAKE_CURRENT_SOURCE_DIR}/Shapes/b2EdgeShape.h
        ${CMAKE_CURRENT_SOURCE_DIR}/Shapes/b2PolygonShape.cpp
        ${CMAKE_CURRENT_SOURCE_DIR}/Shapes/b2PolygonShape.h
        ${CMAKE_CURRENT_SOURCE_DIR}/Shapes/b2Shape.h
        PARENT_SCOPE
        )
