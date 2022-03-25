cmake_minimum_required(VERSION 3.4)
project(formatter_lib)
set(CMAKE_CXX_STANDARD  14)
file(GLOB
        CPP "*.cpp")
add_executable(${PROJECT_NAME} ${CPP})
add_library(lib_formatter STATIC ${CMAKE_CURRENT_DIR} ${CPP})
target_include_directories(lib_formatter PUBLIC ${PROJECT_SOURCE_DIR})
target_link_libraries(${PROJECT_NAME} lib_fromatter)

