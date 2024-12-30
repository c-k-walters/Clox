cmake_minimum_required(VERSION 3.10)
project(CLox)

# Set C standard
set(CMAKE_C_STANDARD 99)

if(APPLE)
    set(CMAKE_OSXARCHITECTURES "arm64")
endif()

# Add include directories
include_directories(include)

# Add source files
file(GLOB_RECURSE SOURCES "src/*.c")

# Create the executable
add_executable(Clox ${SOURCES})

