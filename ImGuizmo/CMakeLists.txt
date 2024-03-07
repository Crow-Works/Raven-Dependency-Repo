# Set the minimum required version of CMake
cmake_minimum_required(VERSION 3.28)

# Set the project name for ImGuizmo
project(ImGuizmo)

# Add the source files for ImGuizmo
set(IMGUIZMO_SOURCES
    GraphEditor.cpp
    ImCurveEdit.cpp
    ImGradient.cpp
    ImGuizmo.cpp
    ImSequencer.cpp
)

# Add the header files for ImGuizmo
set(IMGUIZMO_HEADERS
    GraphEditor.h
    ImCurveEdit.h
    ImGradient.h
    ImGuizmo.h
    ImSequencer.h
)

# Create the ImGuizmo static library
add_library(ImGuizmo STATIC ${IMGUIZMO_SOURCES} ${IMGUIZMO_HEADERS})

# Add include directories for ImGuizmo
target_include_directories(ImGuizmo PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})