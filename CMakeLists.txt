cmake_minimum_required(VERSION 2.8)

project(opencv_meanshift)

find_package(OpenCV REQUIRED core imgproc highgui)
include_directories(${OpenCV_INCLUDE_DIRS})

if (NOT MSVC)
    set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++98 -Wall")
else()
    message(FATAL_ERROR "Microsoft Visual C++ compiler is not supported")
endif()

add_subdirectory(src/lib)
add_subdirectory(src/demo)
