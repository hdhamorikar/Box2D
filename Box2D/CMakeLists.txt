cmake_minimum_required(VERSION 3.12)

set(CMAKE_CXX_STANDARD 11)

INCLUDE_DIRECTORIES("${CMAKE_SOURCE_DIR}")

add_subdirectory(Collision)
add_subdirectory(Common)
add_subdirectory(Dynamics)
add_subdirectory(Rope)

add_library(Box2D
        ${COLLISION_SOURCE}
        ${COMMON_SOURCE}
        ${DYNAMICS_SOURCE}
        ${ROPE_SOURCE}
        )

# If we have compiler requirements for this library, list them
# here
target_compile_features(Box2D
        PUBLIC cxx_auto_type
        PRIVATE cxx_variadic_templates)

