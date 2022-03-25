cmake_minimum_required(VERSION 3.4)
project(formatter_lib_ex)
set(CMAKE_CXX_STANDARD  14)
file(GLOB
        CPP "*.cpp")
add_executable(${PROJECT_NAME} ${CPP})
add_library(lib_formatter_ex STATIC ${CMAKE_CURRENT_DIR} ${CPP})
target_link_libraries(${PROJECT_NAME} PUBLIC lib_formatter)