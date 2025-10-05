cmake_minimum_required(VERSION 4.1.0)
project(poker-ai VERSION 0.1 LANGUAGES C)

set(CMAKE_C_STANDARD 11)
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_SOURCE_DIR}/bin)
set(CMAKE_ARCHIVE_OUTPUT_DIRECTORY ${CMAKE_SOURCE_DIR}/build)

include_directories(include)

file(GLOB_RECURSE SOURCES src/*.c)

add_executable(${PROJECT_NAME} ${SOURCES})