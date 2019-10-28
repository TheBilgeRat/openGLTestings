cmake_minimum_required(VERSION 3.5)
cmake_policy(SET CMP0072 NEW)

project(openGLCplusPlus LANGUAGES CXX)

find_package(OpenGL REQUIRED)
find_package(GLUT REQUIRED)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

set(CMAKE_CXX_FLAGS "-Wall -Weffc++ -Wextra -Wsign-conversion -Werror -pedantic-errors")

add_executable(openGLCplusPlus main.cc)
target_link_libraries(openGLCplusPlus ${OPENGL_LIBRARIES} ${GLUT_LIBRARY})
