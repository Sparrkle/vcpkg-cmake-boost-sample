cmake_minimum_required(VERSION 3.0.0)
project(vspkg-cmake-boost-sample VERSION 0.1.0 LANGUAGES C CXX)

include(CTest)
enable_testing()

find_package(Boost REQUIRED)
include_directories(${Boost_INCLUDE_DIRS})

add_executable(vspkg-cmake-boost-sample main.cpp)

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)
