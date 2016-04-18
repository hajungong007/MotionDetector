cmake_minimum_required(VERSION 2.8)
project(MotionDetector)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11 -O3")

if(WIN32)
    get_filename_component(OPENCV_DIR_PLATFORM $ENV{OPENCV_DIR} DIRECTORY)
    get_filename_component(OPENCV_DIR_HINT ${OPENCV_DIR_PLATFORM} DIRECTORY)
endif(WIN32)

set(OpenCV_STATIC OFF)
find_package(OpenCV REQUIRED HINTS ${OPENCV_DIR_HINT})

include_directories(${OpenCV_DIR}/include)
include_directories(src/)

set(SOURCE_FILES
        src/MotionDetector.cpp)

add_executable(MotionDetector ${SOURCE_FILES})
target_link_libraries(MotionDetector ${OpenCV_LIBS})
