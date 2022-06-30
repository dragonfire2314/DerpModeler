
cmake_minimum_required (VERSION 3.8)

project ("DerpModeler")
add_executable (${PROJECT_NAME}  DerpModeler/src/main.cpp)

# Include sub-projects.

add_subdirectory(ext/glfw)
# add_subdirectory(external/glew/build/cmake)
add_subdirectory (DerpEngine2.0)


target_include_directories(${PROJECT_NAME} 
    PUBLIC DerpEngine2.0
    PUBLIC ext/glfw/include
)

target_link_directories(${PROJECT_NAME} 
    PRIVATE DerpEngine2.0
    PRIVATE ext/glfw
)

target_link_libraries(${PROJECT_NAME} glfw)