cmake_minimum_required(VERSION 3.18)

project(RavenDependencies)

add_subdirectory(Box2D/)
add_subdirectory(glad/)
add_subdirectory(glfw/)
add_subdirectory(glm/)
add_subdirectory(imgui/)
add_subdirectory(ImGuizmo/)
add_subdirectory(spdlog/)
add_subdirectory(spirv_cross/)
add_subdirectory(YAML/)

add_library(RavenDependencies STATIC main.cpp)
target_link_libraries(RavenDependencies PRIVATE glfw spdlog ImGui ImGuizmo glad yaml-cpp spirv-cross-core spirv-cross-glsl box2d)

