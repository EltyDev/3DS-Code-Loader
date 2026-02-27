cmake_minimum_required(VERSION 3.10 FATAL_ERROR)

project(3dstocode)

set(LOADER_NAME  3dstocode)
FILE(GLOB_RECURSE LOADER_SOURCES src/*.cpp)
set(LOADER_OUTPUT_NAME       3dstocode-output)

include(ida-cmake/addons.cmake)

set_target_properties(3dstocode PROPERTIES
    RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/bin
)

set_source_files_properties(${DISABLED_SOURCES} PROPERTIES LANGUAGE "")