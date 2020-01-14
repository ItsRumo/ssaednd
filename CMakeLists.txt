cmake_minimum_required(VERSION 3.13.4)
project(SSAEDND)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -Wall")

set(CMAKE_MODULE_PATH ${SSAEDND_SOURCE_DIR}/cmake/ ${CMAKE_MODULE_PATH})

find_package(OpenAL REQUIRED)
find_package(ALUT REQUIRED)
find_package(wxWidgets REQUIRED)

set(SOURCES ${SOURCES} src/Main.cpp)

include_directories(${OPENAL_INCLUDE_DIRS} ${ALUT_INCLUDE_DIRS} ${WXWIDGETS_INCLUDE_DIRS})
add_executable(ssaednd ${SOURCES})
target_link_libraries(ssaednd ${OPENAL_LIBRARIES} ${ALUT_LIBRARIES} ${WXWIDGETS_LIBRARIES})
