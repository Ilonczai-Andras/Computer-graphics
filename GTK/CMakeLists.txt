cmake_minimum_required(VERSION 3.0)
project(GTKTutorial)

set(CMAKE_C_STANDARD 11)
set(CMAKE_CXX_STANDARD 17)

# Set PKG_CONFIG_PATH for finding GTK3
set(ENV{PKG_CONFIG_PATH} "C:/msys64/mingw64/lib/pkgconfig")

# Find GTK3 package
find_package(PkgConfig REQUIRED)
pkg_check_modules(GTK3 REQUIRED gtk+-3.0)

# Include GTK3 directories
include_directories(${GTK3_INCLUDE_DIRS})
link_directories(${GTK3_LIBRARY_DIRS})

# Define the executable
add_executable(TutorialApp main.c)
set_target_properties(TutorialApp PROPERTIES WIN32_EXECUTABLE true)  # Optional: Prevents console window

# Link GTK3 libraries
target_link_libraries(TutorialApp ${GTK3_LIBRARIES})
