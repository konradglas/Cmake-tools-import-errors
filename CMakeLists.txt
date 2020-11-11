cmake_minimum_required(VERSION 3.16)

project("Include Errors Reproduction")

add_library(includeErrors Source/main.cpp)
target_link_libraries(includeErrors "-framework Accelerate")