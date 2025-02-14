cmake_minimum_required(VERSION 3.31.4)

set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_STANDARD 14)

project(learnopengl VERSION 1.0.0 DESCRIPTION "Bootstrap GLFW and GLAD MacOS setup for learnopengl.")

include(FetchContent)

set(GLFW_BUILD_DOCS OFF CACHE BOOL "" FORCE)
set(GLFW_BUILD_TESTS OFF CACHE BOOL "" FORCE)
set(GLFW_BUILD_EXAMPLES OFF CACHE BOOL "" FORCE)
FetchContent_Declare(glfw
    GIT_REPOSITORY https://github.com/glfw/glfw.git
    GIT_TAG master
)
FetchContent_MakeAvailable(glfw)

add_subdirectory(libs/glad)
add_subdirectory(libs/stb_image)
add_subdirectory(libs/glm)

add_executable(learnopengl
    main.cpp
)
target_link_libraries(learnopengl PRIVATE 
    glfw
    glad
    stb_image
    glm
)
