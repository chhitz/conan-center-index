cmake_minimum_required(VERSION 2.8.12)
project(test_package CXX)

include(${CMAKE_BINARY_DIR}/conanbuildinfo.cmake)
conan_basic_setup()

add_executable(${PROJECT_NAME} example.cpp)
set_property(TARGET ${PROJECT_NAME} PROPERTY CXX_STANDARD 11)

conan_target_link_libraries(${PROJECT_NAME})
