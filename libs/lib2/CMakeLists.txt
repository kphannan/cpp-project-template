# cmake_minimum_required(VERSION 3.20)

set(PROJECT_NAME Lib2)

# project(lib1 VERSION 0.1.0 LANGUAGES C CXX)
project(${PROJECT_NAME})

set(CMAKE_CXX_STANDARD 23)
set(CMAKE_CXX_STANDARD_REQUIRED True)
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

file(GLOB_RECURSE SRC_FILES src/main/cpp/src/*.cpp)

# add_library(${PROJECT_NAME} src/main/cpp/src/bar.cpp)
add_library(${PROJECT_NAME} ${SRC_FILES})

# add_subdirectory(app)
# add_subdirectory(libs)
target_include_directories(${PROJECT_NAME}
    PUBLIC
    include
    PRIVATE
    src
)
