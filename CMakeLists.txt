cmake_minimum_required(VERSION 2.8)

project(hints)

set(CMAKE_BUILD_TYPE "Debug")
add_compile_options(-std=c++11)

include_directories(
    ${PROJECT_SOURCE_DIR}
    ${PROJECT_SOURCE_DIR}/ctemplator
    /usr/local/include
)
link_directories(/usr/local/lib)

set(EXECUTABLE_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/build)
set(LIBRARY_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/build)

add_subdirectory(ctemplator/ctemplator)
add_subdirectory(hints)
