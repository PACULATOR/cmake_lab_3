cmake_minimum_required(VERSION 3.4)
project(formatter_lib_ex)
set(CMAKE_CXX_STANDARD  14)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
file(GLOB
        CPP "*.cpp")

add_library(formatter_lib_ex STATIC ${CMAKE_CURRENT_DIR} ${CPP})
include_directories(${CMAKE_CURRENT_SOURCE_DIR}../formatter_lib)
add_subdirectory(${CMAKE_CURRENT_SOURCE_DIR}../formatter_lib formatter_lib) 
target_link_libraries(formatter_lib_ex PUBLIC formatter_lib)
