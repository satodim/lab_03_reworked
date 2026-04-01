cmake_minimum_required(VERSION 3.10)
project(solver_lib)

file(GLOB SOURCES "*.cpp")
add_library(solver_lib STATIC ${SOURCES})

target_include_directories(solver_lib PUBLIC
    $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}>
    $<INSTALL_INTERFACE:include>
)
