cmake_minimum_required(VERSION 4.1.0)

# Set declaration
project(template LANGUAGES CXX)

# Project structure paths
set(PROJECT_SOURCE_DIR ${CMAKE_CURRENT_SOURCE_DIR}/src)
set(PROJECT_INCLUDE_DIR ${CMAKE_CURRENT_SOURCE_DIR}/include)
set(PROJECT_RESOURCE_DIR ${CMAKE_CURRENT_SOURCE_DIR}/resources)

# Project output directories
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/bin)
set(CMAKE_LIBRARY_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/lib)
set(CMAKE_ARCHIVE_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/lib)

# Source files
file(GLOB_RECURSE SOURCES ${PROJECT_SOURCE_DIR}/*.cpp)

# Add executable target
add_executable(${PROJECT_NAME} ${SOURCES})

# Set target include directories
target_compile_definitions(${PROJECT_NAME}
	PRIVATE RESOURCE_PATH="${PROJECT_RESOURCE_DIR}/"
)

# Include directories
target_include_directories(${PROJECT_NAME}
	PRIVATE ${PROJECT_INCLUDE_DIR}
)

# Set C/C++ standard
target_compile_features(${PROJECT_NAME} PRIVATE cxx_std_17)
target_compile_features(${PROJECT_NAME} PRIVATE c_std_17)