cmake_minimum_required(VERSION 3.0)
project(my_mujoco)
include_directories(
    ${CMAKE_SOURCE_DIR}/include
)

find_package(glfw3 REQUIRED)
add_executable(main main.cpp)

target_link_libraries(main
  ${CMAKE_SOURCE_DIR}/lib/libmujoco.so
  pthread
  glfw
)