cmake_minimum_required(VERSION 3.12)
project(Box2D)

set(CMAKE_CXX_STANDARD 11)

file(GLOB DATA "Data/*")
file(GLOB FRAMEWORK "Framework/*")
file(GLOB TESTS "Tests/*")
file(GLOB IMGUI "imgui/*")
file(GLOB GLAD "glad/*")
set(GLFW_COMMON
        ${CMAKE_CURRENT_SOURCE_DIR}/glfw/internal.h
        ${CMAKE_CURRENT_SOURCE_DIR}/glfw/glfw_config.h
        ${CMAKE_CURRENT_SOURCE_DIR}/glfw/glfw3.h
        ${CMAKE_CURRENT_SOURCE_DIR}/glfw/glfw3native.h
        ${CMAKE_CURRENT_SOURCE_DIR}/glfw/context.c
        ${CMAKE_CURRENT_SOURCE_DIR}/glfw/init.c
        ${CMAKE_CURRENT_SOURCE_DIR}/glfw/input.c
        ${CMAKE_CURRENT_SOURCE_DIR}/glfw/monitor.c
        ${CMAKE_CURRENT_SOURCE_DIR}/glfw/vulkan.c
        ${CMAKE_CURRENT_SOURCE_DIR}/glfw/window.c
        )
set(GLFW_WINDOWS
        ${CMAKE_CURRENT_SOURCE_DIR}/glfw/win32_platform.h
        ${CMAKE_CURRENT_SOURCE_DIR}/glfw/win32_joystick.h
        ${CMAKE_CURRENT_SOURCE_DIR}/glfw/wgl_context.h
        ${CMAKE_CURRENT_SOURCE_DIR}/glfw/egl_context.h
        ${CMAKE_CURRENT_SOURCE_DIR}/glfw/win32_init.c
        ${CMAKE_CURRENT_SOURCE_DIR}/glfw/win32_joystick.c
        ${CMAKE_CURRENT_SOURCE_DIR}/glfw/win32_monitor.c
        ${CMAKE_CURRENT_SOURCE_DIR}/glfw/win32_time.c
        ${CMAKE_CURRENT_SOURCE_DIR}/glfw/win32_tls.c
        ${CMAKE_CURRENT_SOURCE_DIR}/glfw/win32_window.c
        ${CMAKE_CURRENT_SOURCE_DIR}/glfw/wgl_context.c
        ${CMAKE_CURRENT_SOURCE_DIR}/glfw/egl_context.c
        )
set(GLFW_APPLE
        ${CMAKE_CURRENT_SOURCE_DIR}/glfw/cocoa_platform.h
        ${CMAKE_CURRENT_SOURCE_DIR}/glfw/iokit_joystick.h
        ${CMAKE_CURRENT_SOURCE_DIR}/glfw/posix_tls.h
        ${CMAKE_CURRENT_SOURCE_DIR}/glfw/nsgl_context.h
        ${CMAKE_CURRENT_SOURCE_DIR}/glfw/egl_context.h
        ${CMAKE_CURRENT_SOURCE_DIR}/glfw/cocoa_init.m
        ${CMAKE_CURRENT_SOURCE_DIR}/glfw/cocoa_joystick.m
        ${CMAKE_CURRENT_SOURCE_DIR}/glfw/cocoa_monitor.m
        ${CMAKE_CURRENT_SOURCE_DIR}/glfw/cocoa_window.m
        ${CMAKE_CURRENT_SOURCE_DIR}/glfw/cocoa_time.c
        ${CMAKE_CURRENT_SOURCE_DIR}/glfw/posix_tls.c
        ${CMAKE_CURRENT_SOURCE_DIR}/glfw/nsgl_context.m
        ${CMAKE_CURRENT_SOURCE_DIR}/glfw/egl_context.c
        )
set(GLFW_LINUX
        ${CMAKE_CURRENT_SOURCE_DIR}/glfw/x11_platform.h
        ${CMAKE_CURRENT_SOURCE_DIR}/glfw/xkb_unicode.h
        ${CMAKE_CURRENT_SOURCE_DIR}/glfw/linux_joystick.h
        ${CMAKE_CURRENT_SOURCE_DIR}/glfw/posix_time.h
        ${CMAKE_CURRENT_SOURCE_DIR}/glfw/posix_tls.h
        ${CMAKE_CURRENT_SOURCE_DIR}/glfw/glx_context.h
        ${CMAKE_CURRENT_SOURCE_DIR}/glfw/egl_context.h
        ${CMAKE_CURRENT_SOURCE_DIR}/glfw/x11_init.c
        ${CMAKE_CURRENT_SOURCE_DIR}/glfw/x11_monitor.c
        ${CMAKE_CURRENT_SOURCE_DIR}/glfw/x11_window.c
        ${CMAKE_CURRENT_SOURCE_DIR}/glfw/glx_context.h
        ${CMAKE_CURRENT_SOURCE_DIR}/glfw/glx_context.c
        ${CMAKE_CURRENT_SOURCE_DIR}/glfw/glext.h
        ${CMAKE_CURRENT_SOURCE_DIR}/glfw/xkb_unicode.c
        ${CMAKE_CURRENT_SOURCE_DIR}/glfw/linux_joystick.c
        ${CMAKE_CURRENT_SOURCE_DIR}/glfw/posix_time.c
        ${CMAKE_CURRENT_SOURCE_DIR}/glfw/posix_tls.c
        ${CMAKE_CURRENT_SOURCE_DIR}/glfw/glx_context.c
        ${CMAKE_CURRENT_SOURCE_DIR}/glfw/egl_context.c
        )

INCLUDE_DIRECTORIES("${CMAKE_SOURCE_DIR}")
if (APPLE)
    add_definitions( -DGLEW_STATIC -D_CRT_SECURE_NO_WARNINGS )
    set(SOURCES ${DATA} ${FRAMEWORK} ${TESTS} ${GLFW_COMMON} ${IMGUI} ${GLFW_APPLE})
    message("${SOURCES}")
#    message("AAAAAAAAAAAAAAAAA ${GLFW_APPLE}")
#    set(CMAKE_EXE_LINKER_FLAGS "-m64 -O2 -g -std=c++11")
#    set(CMAKE_CXX_FLAGS  "${CMAKE_CXX_FLAGS}" "-MMD -MP")
#    add_link_options("-m64 -O0 -g")
#    add_compile_options("-MMD -MP")

    find_package(OpenGL REQUIRED)
#    include_directories(${OPENGL_INCLUDE_DIR})

    find_library(COCOA_LIBRARY Cocoa REQUIRED)
    find_library(FOUNDATION_LIBRARY Foundation REQUIRED)
    find_library(IOKIT_LIBRARY IOKit REQUIRED)
    find_library(VIDEO_LIBRARY CoreVideo REQUIRED)

    set(EXTRA_LIBS ${OPENGL_LIBRARIES} ${COCOA_LIBRARY} ${FOUNDATION_LIBRARY} ${IOKIT_LIBRARY} ${VIDEO_LIBRARY})

    add_executable(Testbed ${SOURCES})
    target_link_libraries(Testbed Box2D ${EXTRA_LIBS})

endif (APPLE)
