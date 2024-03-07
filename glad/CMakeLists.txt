# Set the minimum required version of CMake
cmake_minimum_required(VERSION 3.25.1)

# Set the project name for glad
project(glad)

# Add the source files for glad
set(GLAD_SOURCES
    src/glad.c
)

# Add the header files for glad
set(GLAD_HEADERS
    include/glad/glad.h
    include/KHR/khrplatform.h
)

# Create the glad static library
add_library(glad STATIC ${GLAD_HEADERS} ${GLAD_SOURCES})

# Add include directories for glad
target_include_directories(glad PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})