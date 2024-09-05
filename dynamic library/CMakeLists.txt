cmake_minimum_required(VERSION 3.18)
project(sqlite3 C)

if(CMAKE_SIZEOF_VOID_P EQUAL 8)
    set(SYSTEM_ARCH "x86_64")
else()
    set(SYSTEM_ARCH "x86")
endif()

message(STATUS "Operating System: ${CMAKE_SYSTEM_NAME}")
message(STATUS "System Architecture: ${SYSTEM_ARCH}")

set(SRC sqlite-amalgamation-3260000/sqlite3.c)

add_library(${PROJECT_NAME}${SYSTEM_ARCH} SHARED ${SRC})

