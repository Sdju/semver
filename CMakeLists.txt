﻿cmake_minimum_required(VERSION 3.6.4)
project(semver)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

if((CMAKE_CXX_COMPILER_ID MATCHES "GNU") OR (CMAKE_CXX_COMPILER_ID MATCHES "Clang"))
    add_compile_options(-pedantic)
    add_compile_options(-Wall)
    add_compile_options(-Wextra)
elseif(CMAKE_CXX_COMPILER_ID MATCHES "MSVC")
    add_compile_options(/W4)
endif()

add_subdirectory(example)

enable_testing()
add_subdirectory(test)