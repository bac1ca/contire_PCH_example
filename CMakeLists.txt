cmake_minimum_required(VERSION 3.7)
project(contirePCH)
set(CMAKE_CXX_STANDARD 11)

set (CMAKE_MODULE_PATH "${CMAKE_SOURCE_DIR}/CMake")
include(cotire)

set(SOURCE_FILES main.cpp)
add_executable(contirePCH ${SOURCE_FILES})

set_target_properties(contirePCH PROPERTIES COTIRE_CXX_PREFIX_HEADER_INIT "common.h")
cotire(contirePCH)