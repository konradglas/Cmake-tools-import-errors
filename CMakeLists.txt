cmake_minimum_required(VERSION 3.16)

project("Include Errors Reproduction")

add_library(includeErrors Source/main.cpp)
target_link_libraries(includeErrors "-framework Accelerate")

set_target_properties(includeErrors PROPERTIES CXX_EXTENSIONS OFF)

# Out comment this line and the include squiggles under #include <stdlib.h> in main.cpp will disappear
target_precompile_headers(includeErrors PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/Source/pch.h)