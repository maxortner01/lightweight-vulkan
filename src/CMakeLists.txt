cmake_minimum_required(VERSION 3.2)

include_directories("${PROJECT_SOURCE_DIR}/headers")

add_library(lightweight-vulkan SHARED test.cpp)

target_link_directories(lightweight-vulkan PUBLIC "${PROJECT_BINARY_DIR}/extern/glfw/src")
target_link_libraries(lightweight-vulkan glfw3)