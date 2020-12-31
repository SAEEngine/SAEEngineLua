cmake_minimum_required (VERSION 3.8)

project(SAEEngineLua VERSION 0.0.1 LANGUAGES CXX C)

add_library(${PROJECT_NAME} STATIC "source/${PROJECT_NAME}.cpp" "include/${PROJECT_NAME}.h")

add_subdirectory("lib")
