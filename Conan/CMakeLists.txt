cmake_minimum_required(VERSION 3.18)
project(hello CXX)

find_package(fmt REQUIRED)

add_executable(${PROJECT_NAME} src/hello.cpp)
target_link_libraries(${PROJECT_NAME} fmt::fmt)