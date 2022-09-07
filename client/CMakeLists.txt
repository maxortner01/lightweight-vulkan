cmake_minimum_required(VERSION 3.2)

project(main)

include_directories("${PROJECT_SOURCE_DIR}/../headers")
add_executable(main main.cpp)

file(GLOB LIBRARIES "${PROJECT_BINARY_DIR}/../src/*.dylib")

target_link_libraries(main ${LIBRARIES})