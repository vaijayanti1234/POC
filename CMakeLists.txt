# CMakeList.txt : CMake project for testing, include source and define
# project specific logic here.
#
cmake_minimum_required (VERSION 3.8)

set(CMAKE_BUILD_TYPE Debug)

project(testing)

add_executable(testing testing.cpp testing.h)
link_libraries("C:/Users/vsarfare/source/repos/POC_Assignment_Cmake/dependancies/lib/libpq.lib")
include_directories(testing ${PROJECT_SOURCE_DIR}"/dependancies/include/")

target_link_libraries(testing libpq.dll)

install(TARGETS testing DESTINATION lib)

