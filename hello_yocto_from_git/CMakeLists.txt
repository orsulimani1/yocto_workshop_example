cmake_minimum_required(VERSION 3.1...3.27)

project(hello_yocto_from_git)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED True)

# Set the general output directory for all executables
# set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/../bin)

set(GCC_COMPILER gcc)

# This condition will be true if ENABLE_FEATURE was set to ON
message("                   CMAKE_BUILD_TYPE is ${CMAKE_BUILD_TYPE}")


# Check for custom variables passed via EXTRA_OECMAKE
if(ENABLE_FEATURE)
    message(STATUS "                ENABLE_FEATURE is ON: Additional feature will be enabled")
    add_definitions(-DENABLE_FEATURE)
else()
    message(STATUS "                ENABLE_FEATURE is OFF: Default behavior")
endif()


add_executable(hello_yocto_from_git hello_yocto.c) 