cmake_minimum_required(VERSION 3.10)
project(oj_evaluation LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

# Add all source files from the provided public directory
# Source files are located in the provided public directory
# Source files are in the sibling data directory
# Compile only the primary test driver (1.cpp). Other .cpp files contain duplicate mains.
set(SOURCES "../data/033/2100-public/1.cpp")

add_executable(code ${SOURCES})

target_include_directories(code PRIVATE "../data/033/2100-public")
