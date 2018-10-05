cmake_minimum_required(VERSION 3.12)
project(Graphene CXX)

set(CMAKE_CXX_STANDARD 17)

file (GLOB_RECURSE HEADERS ${PROJECT_SOURCE_DIR}/include/*.hpp)
source_group("pbw\\headers" FILES ${HEADERS})
add_library(Graphene INTERFACE)

include_directories(${CMAKE_CURRENT_SOURCE_DIR})

target_include_directories(Graphene INTERFACE ${CMAKE_CURRENT_SOURCE_DIR})
add_custom_target(IDE SOURCES
        ${HEADERS})

add_subdirectory(tests)