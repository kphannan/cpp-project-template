cmake_minimum_required(VERSION 3.20)

set(PROJECT_NAME GraphBase)

project(${PROJECT_NAME} VERSION 0.1.0 LANGUAGES C CXX)

set(CMAKE_CXX_STANDARD 23)
set(CMAKE_CXX_STANDARD_REQUIRED True)
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)
set(DOWNLOAD_EXTRACT_TIMESTAMP true)

add_subdirectory(app)
add_subdirectory(libs)

# add_library(Graph Graph.cpp)

# ----- Unit Test Framework -----

# Fetch Google Test as needed
include(FetchContent)
FetchContent_Declare(
    googletest
    URL https://github.com/google/googletest/archive/03597a01ee50ed33e9dfd640b249b4be3799d395.zip
)

# For Windows: Prevent overriding the parent project's compiler/linker settings
set(gtest_force_shared_crt ON CACHE BOOL "" FORCE)
FetchContent_MakeAvailable(googletest)

# # ## Unit Testing with Google Test
# enable_testing()
