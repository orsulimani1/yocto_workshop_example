cmake_minimum_required(VERSION 3.1...3.27)

project(hello_yocto_from_git)

set(CMAKE_BUILD_TYPE Debug)
set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED True)

# Set the general output directory for all executables
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/../bin)

set(GCC_COMPILER gcc)

add_executable(hello_yocto_from_git hello_yocto.c) 