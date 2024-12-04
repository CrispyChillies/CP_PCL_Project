cmake_minimum_required(VERSION 3.10)

# Set the project name
project(LidarObstacleDetection)

# Set C++ standard
set(CMAKE_CXX_STANDARD 17)

# Find PCL package
find_package(PCL 1.12 REQUIRED)

# Find VTK package
find_package(VTK REQUIRED)

# Include directories
include_directories(${PCL_INCLUDE_DIRS} ${VTK_INCLUDE_DIRS})

# Add the executable
add_executable(point_cloud_viewer main.cpp)

# Link the PCL and VTK libraries
target_link_libraries(point_cloud_viewer ${PCL_LIBRARIES} ${VTK_LIBRARIES})