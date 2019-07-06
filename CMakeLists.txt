cmake_minimum_required(VERSION 3.10.1)

project(ObjectDetectionYOLOv3)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED TRUE)
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -pedantic -Wall")

find_package(OpenCV REQUIRED)

set(SOURCES
    src/main.cpp
)


INCLUDE_DIRECTORIES(${CMAKE_CURRENT_SOURCE_DIR}/include)
set(EXECUTABLE_OUTPUT_PATH ${CMAKE_BINARY_DIR}/bin)

add_executable(object-detection ${SOURCES})
