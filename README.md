
# Template Project

This is a **C/C++ template project** configured with **CMake** for easy compilation and management. It provides a standard project structure for source files, headers, and resources (libraries are yet to be added).

## Requirements

- **CMake** ≥ 4.1.0
- **C++ Compiler** supporting C++17
- **C Compiler** supporting C17

Tested on GCC, Clang, and MSVC.

## Build Instructions

### 1. Clone the repository

    git clone <repository_url>
    cd template

### 2. Create a build directory

It's recommended to use an out-of-source build:

    mkdir build
    
    cd build

### 3. Generate build files with CMake

    cmake ..

This will configure the project and generate platform-specific build files.

### 4. Build the project

    cmake --build .
    
By default, the executable will be placed in:
    
    build/bin/

### 5. Run the executable

    ./bin/template

### Notes

- Resources are accessible in your code using the `RESOURCE_PATH` macro defined automatically in CMake.
- Include headers using `#include <header_name>` as the `include/` directory is added to the target include directories.




