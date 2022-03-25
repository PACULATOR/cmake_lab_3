cmake_minimum_required(VERSION 3.4)
project(formatter_lib_ex)
set(CMAKE_CXX_STANDARD  14)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
file(GLOB
        CPP "*.cpp")

add_library(formatter_lib_ex STATIC ${CMAKE_CURRENT_DIR} ${CPP})
target_include_directories(${PROJECT_NAME} PUBLIC ../formatter_lib da)
add_subdirectory(../formatter_lib net) 
target_link_libraries(formatter_lib_ex PUBLIC formatter_lib)
