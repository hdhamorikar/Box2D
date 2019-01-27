cmake_minimum_required(VERSION 3.12)
project(Box2D)

set(CMAKE_CXX_STANDARD 14)

# Only if a subdirectory of this directory has `SOURCE` defined
#aux_source_directory(${CMAKE_CURRENT_SOURCE_DIR} SUB_SOURCES)

add_subdirectory(Contacts)
add_subdirectory(Joints)

set(DYNAMICS_SOURCE
        ${CONTACTS_SOURCE}
        ${JOINTS_SOURCE}
        ${CMAKE_CURRENT_SOURCE_DIR}/b2Body.cpp
        ${CMAKE_CURRENT_SOURCE_DIR}/b2Body.h
        ${CMAKE_CURRENT_SOURCE_DIR}/b2ContactManager.cpp
        ${CMAKE_CURRENT_SOURCE_DIR}/b2ContactManager.h
        ${CMAKE_CURRENT_SOURCE_DIR}/b2Fixture.cpp
        ${CMAKE_CURRENT_SOURCE_DIR}/b2Fixture.h
        ${CMAKE_CURRENT_SOURCE_DIR}/b2Island.cpp
        ${CMAKE_CURRENT_SOURCE_DIR}/b2Island.h
        ${CMAKE_CURRENT_SOURCE_DIR}/b2TimeStep.h
        ${CMAKE_CURRENT_SOURCE_DIR}/b2World.cpp
        ${CMAKE_CURRENT_SOURCE_DIR}/b2World.h
        ${CMAKE_CURRENT_SOURCE_DIR}/b2WorldCallbacks.cpp
        ${CMAKE_CURRENT_SOURCE_DIR}/b2WorldCallbacks.h
        PARENT_SCOPE
        )
