cmake_minimum_required(VERSION 2.8)

set(Project_name Test)
project(${Project_name}) 

add_executable(${Project_name} src/main.cpp)

set(GLFW_BUILD_DOCS OFF CACHE BOOL "" FORCE)
set(GLFW_BUILD_TESTS OFF CACHE BOOL "" FORCE)
set(GLFW_BUILD_EXAMPLES OFF CACHE BOOL "" FORCE)
set(GLFW_INSTALL OFF CACHE BOOL "" FORCE)

add_subdirectory(external/glfw)
target_link_libraries(${Project_name} glfw)

add_subdirectory(external/glad)
target_link_libraries(Test glad)