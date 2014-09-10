cmake_minimum_required (VERSION 2.6)

project (Tutorial)

set(CMAKE_CXX_FLAGS "-std=c++11 -Wall")

add_executable(main main.cpp)

find_package(PkgConfig REQUIRED)

pkg_search_module(GLFW REQUIRED glfw3)

include_directories(${GLFW_INCLUDE_DIRS})

target_link_libraries(main ${GLFW_STATIC_LIBRARIES})
