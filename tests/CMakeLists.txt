cmake_minimum_required(VERSION 3.12)
project(GrapeheTest CXX)
set(CMAKE_CXX_STANDARD 17)

file(GLOB_RECURSE TEST_SOURCES ${CMAKE_CURRENT_SOURCE_DIR}/*.cpp)

source_group("graphene\\test_sources" FILES ${TEST_SOURCES})
add_executable(GrapeheTest ${TEST_SOURCES})