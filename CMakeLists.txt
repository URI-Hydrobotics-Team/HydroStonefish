cmake_minimum_required(VERSION 3.10)
project(stonefish_sim)

# Find required packages
find_package(Stonefish REQUIRED 1.3.0)

# Add the executable
add_executable(demo demo/main.cpp demo/MySimulationManager.cpp)

include_directories(
    /usr/local/include
    /usr/local/include/Stonefish
    /usr/local/include/Stonefish/graphics
    /usr/local/include/Stonefish/physics
    /usr/local/include/Stonefish/simulation
)

# Specify the directory containing the Stonefish library
target_link_libraries(demo PUBLIC Stonefish::Stonefish)

