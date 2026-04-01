cmake_minimum_required(VERSION 3.10)
project(formatter_lib)

file(GLOB SOURCES "*.cpp")
add_library(formatter STATIC ${SOURCES})

target_include_directories(formatter PUBLIC
    $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}>
    $<INSTALL_INTERFACE:include>
)
