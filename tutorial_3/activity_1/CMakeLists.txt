# CMake Minimum Version
cmake_minimum_required(VERSION 2.8)

# Project Title
project(main)

# Include Directories
include_directories(
    "${PROJECT_SOURCE_DIR}"
)

add_executable(main ${PROJECT_SOURCE_DIR}/main.cpp)

# Find Packages
find_package (OpenCV REQUIRED)
target_link_libraries(main ${OpenCV_LIBS})

# Install Command
install (TARGETS main DESTINATION ${PROJECT_SOURCE_DIR}/bin)
