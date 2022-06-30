# CMakeList.txt : Top-level CMake project file, do global configuration
# and include sub-projects here.
#
cmake_minimum_required (VERSION 3.8)

project ("DerpModeler")

# Include sub-projects.

add_subdirectory(ext/glfw)
# add_subdirectory(external/glew/build/cmake)

add_subdirectory ("DerpEngine2.0")
add_subdirectory ("DerpModeler")
