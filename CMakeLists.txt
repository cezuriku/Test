cmake_minimum_required(VERSION 2.8)

set(EXECUTABLE_NAME "project")
project(sampleProject)

set(CMAKE_CXX_STANDARD 11)

file(GLOB_RECURSE SOURCE_FILES "src/*.cpp")
add_executable(${EXECUTABLE_NAME} ${SOURCE_FILES})

add_subdirectory(lib/entityx)
add_subdirectory(lib/SFML)
target_link_libraries(${EXECUTABLE_NAME} entityx sfml-system sfml-window sfml-graphics)
