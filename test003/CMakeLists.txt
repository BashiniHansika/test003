cmake_minimum_required(VERSION 3.20)
project(test003)

set(CMAKE_CXX_STANDARD 14)
find_package(GLEW REQUIRED)
include_directories(${GLEW_INCLUDE_DIRS})
link_libraries(${GLEW_LIBRARIES})


set(test003 main.cpp)

add_executable(test003 main.cpp)
target_link_libraries(test003 GL GLU glfw3 X11 Xxf86vm Xrandr pthread Xi dl assimp)
