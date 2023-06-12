cmake_minimum_required(VERSION 3.14)
project(test_compile)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -Wall")

#find_package(OpenGL REQUIRED)
find_package(glfw3 REQUIRED)
#find_package(GLFW REQUIRED)
find_package(GLEW REQUIRED)
find_package(X11 REQUIRED)


add_executable(main main.cpp)
target_link_libraries(main OpenGL)
target_link_libraries(main glfw3)
target_link_libraries(main GLEW)
target_link_libraries(main X11)