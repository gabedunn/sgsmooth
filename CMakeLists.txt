cmake_minimum_required(VERSION 3.16)
project(sgsmooth)

add_definitions(-fPIC)
add_definitions(-std=c++11)

add_library(sgsmooth STATIC src/SGSmooth.cpp)
target_include_directories(sgsmooth PUBLIC include/sgsmooth)

install (TARGETS sgsmooth DESTINATION lib)
install (DIRECTORY include/sgsmooth DESTINATION include)
