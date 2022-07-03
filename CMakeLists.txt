
cmake_minimum_required (VERSION 3.8)

set (CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_SOURCE_DIR}/bin)

project ("DerpModeler")
add_executable (${PROJECT_NAME}  DerpModeler/src/main.cpp)

# Include sub-projects.

add_subdirectory(ext/glfw)
add_subdirectory(ext/glew/build/cmake)
add_subdirectory(DerpEngine2.0)


target_include_directories(${PROJECT_NAME} 
    PUBLIC DerpEngine2.0/include
    # PUBLIC ext/glfw/include
)

target_link_directories(${PROJECT_NAME} 
    PUBLIC DerpEngine2.0/
    # PRIVATE ext/glfw
)

target_link_libraries(${PROJECT_NAME} 
    glfw 
    DerpEngine
)