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
        b2Body.cpp
        b2Body.h
        b2ContactManager.cpp
        b2ContactManager.h
        b2Fixture.cpp
        b2Fixture.h
        b2Island.cpp
        b2Island.h
        b2TimeStep.h
        b2World.cpp
        b2World.h
        b2WorldCallbacks.cpp
        b2WorldCallbacks.h
        PARENT_SCOPE
        )
