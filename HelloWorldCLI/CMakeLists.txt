# Declare the minimum required CMake version
cmake_minimum_required(VERSION 3.5.0)

# Name the project
project(HelloWorldCLI VERSION 0.1.0)

# Add required libraries configuration
# ...

# Define the list of source files for the project
set(SRC_FILES
    main.cpp
)

# Define the build target for the executable
add_executable(${PROJECT_NAME} ${SRC_FILES})

# Uncomment the line below to link the required libraries to the executable
#target_link_libraries(${PROJECT_NAME} ...)

#set(CPACK_PROJECT_NAME ${PROJECT_NAME})
#set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
#include(CPack)
