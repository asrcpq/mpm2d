cmake_minimum_required(VERSION 3.11.0)

project(mydraw LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

find_package(Eigen3 REQUIRED)
find_package(glfw3 REQUIRED)
find_package(OpenGL REQUIRED)

add_executable(mpm2d
	src/main.cpp
	src/particle.cpp
	src/node.cpp
	src/algebra.cpp
	src/solver.cpp
	src/border.cpp
)

target_link_libraries(mpm2d Eigen3::Eigen glfw OpenGL::GL)
