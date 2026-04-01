cmake_minimum_required(VERSION 3.10)
project(formatter_ex)

file(GLOB SOURCES "*.cpp")
add_library(formatter_ex STATIC ${SOURCES})

target_link_libraries(formatter_ex PRIVATE formatter)

target_include_directories(formatter_ex PUBLIC
    $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}>
    $<INSTALL_INTERFACE:include>
)
