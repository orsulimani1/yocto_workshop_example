cmake_minimum_required(VERSION 3.1...3.27)

project(hello_yocto_from_git)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED True)

# Set the general output directory for all executables
# set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/../bin)

set(GCC_COMPILER gcc)

# This condition will be true if ENABLE_FEATURE was set to ON
if(CMAKE_BUILD_TYPE=Release)
    message("ENABLE_FEATURE is enabled!")
    set(CMAKE_BUILD_TYPE Debug)
    # You can add logic here that depends on ENABLE_FEATURE
endif()

add_executable(hello_yocto_from_git hello_yocto.c) 