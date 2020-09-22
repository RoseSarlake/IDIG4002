cmake_minimum_required (VERSION 3.1)
project(SampleProject)

#include directories
include_directories($ENV{GLEW_INCLUDE_DIR})
include_directories($ENV{GLfW_INCLUDE_DIR})

#Library directories
link_directories($ENV{GLEW_LIBRARY})
link_directories($ENV{GLFW_LIBRARY})

#link opengl32 from windows systems
find_package(OPENGL REQUIRED)

#compiling the project as excutable 
add_executable(SampleProject main.cpp)

#linking the libraries with the project 
target_link_libraries(SampleProject ${OPENGL_gl_LIBRARY} glew32 glfw3dll)


