cmake_minimum_required(VERSION 2.8)
project(MyStl)

# version
set(MySTL_VERSION_MAJOR 1)
set(MySTL_VERSION_MINOR 0)
set(MySTL_VERSION_PATCH 0)
set(MySTL_VERSION "${MySTL_VERSION_MAJOR}.${MySTL_VERSION_MINOR}.${MySTL_VERSION_PATCH}")
message(STATUS "The version of this project is : ${MySTL_VERSION}")
set(CMAKE_BUILD_TYPE release)
set(SRC_DIR src)
set(INC_DIR include)
include_directories(${INC_DIR})
aux_source_directory(${SRC_DIR} SRC_FILES)

# set(test ${PROJECT_SOURCE_DIR}/src/main.cpp)
set(EXECUTABLE_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/bin)
add_executable(stltest ${SRC_FILES})
