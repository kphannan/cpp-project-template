cmake_minimum_required(VERSION 3.20)

set(PROJECT_NAME GraphBase)

project(${PROJECT_NAME} VERSION 0.1.0 LANGUAGES C CXX)

set(CMAKE_CXX_STANDARD 23)
set(CMAKE_CXX_STANDARD_REQUIRED True)
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

add_subdirectory(app)
add_subdirectory(libs)

# add_library(Graph Graph.cpp)

# include(CTest)
# enable_testing()
