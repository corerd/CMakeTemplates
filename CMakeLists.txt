# Top-level CMakeLists.txt file to tie all the projects together.
#
# Each project has its own root sub-directory 
# in which the project CMakeLists.txt and code files are located.

# Declare the minimum required CMake version
cmake_minimum_required(VERSION 3.5.0)

# Add all the projects sub-directories to the build
add_subdirectory(HelloWorldCLI)
add_subdirectory(HelloWorldGUI)
