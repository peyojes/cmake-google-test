cmake_minimum_required(VERSION 3.8)

# Project name
project(cmake-with-gtest)

# add Google test library
add_subdirectory(test)

# C++ 14 version
set(CMAKE_CXX_STANDARD 14)

# Headers files
include_directories(include)

# Source files
file(GLOB SOURCE_FILES_DIR ./src/**.cpp ./src/**.c ./src/**.cc)
set(SOURCE_FILES
        ${SOURCE_FILES_DIR})

# Unit tests
file(GLOB TEST_SOURCES_DIR ./test/**.cpp ./test/**.cc)
set(TEST_SOURCES
        ${TEST_SOURCES_DIR})

#Add executable program
add_executable(run ${SOURCE_FILES} main.cpp)

#Add executable unit tests
# Add gmock
link_libraries(gmock)
add_executable(unit_test ${SOURCE_FILES} ${TEST_SOURCES})
