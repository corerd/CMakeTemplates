# This CMake file derives from the one provided by wxWidgets
# in the minimal sample directory.

# Declare the minimum required CMake version
cmake_minimum_required(VERSION 3.0.0)

# Name the project
project(HelloWorldGUI VERSION 0.1.0)

# Define wxWidgets environment variables.
# WXWIN: the wxWidgets sources root directory
# WXCFG: the build sub-directory of $WXWIN\lib
#        specific to compiler and library type (static or dynamic)
# The better way is to define them as global variables.
# E.g. in VS Code define them in cmake.environment user settings.
# Uncomment the 2 lines below to override their global settings:
#set(ENV{WXWIN} /path/tp/wxWidgets/sources/root/directory)
#set(ENV{WXCFG} gcc_lib/mswu)

# Request the required wxWidgets libs
find_package(wxWidgets 3.2 COMPONENTS core base)

# Include the wxWidgets use file to initialize various settings
include(${wxWidgets_USE_FILE})

# Define the list of source files for the project
set(SRC_FILES
    main.cpp
    gui.cpp
    )
if(WIN32)
    # Include a RC file for windows
    list(APPEND SRC_FILES resources/sample.rc)
endif()

# Define the build target for the executable
add_executable(${PROJECT_NAME} ${SRC_FILES})

# Link required libraries to the executable
target_link_libraries(${PROJECT_NAME} ${wxWidgets_LIBRARIES})
