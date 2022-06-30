# CMakeList.txt : CMake project for DerpModeler, include source and define
# project specific logic here.
#
cmake_minimum_required (VERSION 3.8)

# Add source to this project's executable.
add_executable (DerpModeler src/main.cpp)

target_link_libraries(${PROJECT_NAME} DerpEngine)

# TODO: Add tests and install targets if needed.
