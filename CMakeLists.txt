cmake_minimum_required(VERSION 3.28.0)
project(segmentation)
set(CMAKE_CXX_STANDARD 11)

find_package(OpenCV REQUIRED)
include_directories(${OpenCV_INCLUDE_DIRS})
set(SOURCE_FILES src/main.cpp src/segment.cpp )

add_executable(main src/main.cpp src/segment.cpp)
target_link_libraries(main ${OpenCV_LIBS})
