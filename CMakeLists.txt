cmake_minimum_required(VERSION 2.8)

project("yaml-sample")

set(CMAKE_BUILD_TYPE "Release")

add_definitions("-O3")
add_definitions("-std=c++11")
add_definitions("-Wall -Wextra -pedantic")

find_package(yaml-cpp)
include_directories(${YAML_CPP_INCLUDE_DIR})

add_executable(${PROJECT_NAME} "src/main.cpp")

target_link_libraries(${PROJECT_NAME} ${YAML_CPP_LIBRARIES})

