cmake_minimum_required(VERSION 3.13.4)
project(ssaednd)

include_directories(include)

set(SOURCES ${SOURCES} src/Main.cpp)

add_executable(ssaednd ${SOURCES})
