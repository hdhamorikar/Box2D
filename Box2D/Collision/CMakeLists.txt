cmake_minimum_required(VERSION 3.12)
project(Box2D)

set(CMAKE_CXX_STANDARD 14)

# Only if a subdirectory of this directory has `SOURCE` defined
#aux_source_directory(${CMAKE_CURRENT_SOURCE_DIR} SUB_SOURCES)

set(COLLISION_SOURCE
        ${CMAKE_CURRENT_SOURCE_DIR}/b2BroadPhase.cpp
        b2BroadPhase.h
        b2CollideCircle.cpp
        b2CollideEdge.cpp
        b2CollidePolygon.cpp
        b2Collision.cpp
        b2Collision.h
        b2Distance.cpp
        b2Distance.h
        b2DynamicTree.cpp
        b2DynamicTree.h
        b2TimeOfImpact.cpp
        b2TimeOfImpact.h
        Shapes/b2ChainShape.cpp
        Shapes/b2ChainShape.h
        Shapes/b2CircleShape.cpp
        Shapes/b2CircleShape.h
        Shapes/b2EdgeShape.cpp
        Shapes/b2EdgeShape.h
        Shapes/b2PolygonShape.cpp
        Shapes/b2PolygonShape.h
        Shapes/b2Shape.h
        PARENT_SCOPE
        )
