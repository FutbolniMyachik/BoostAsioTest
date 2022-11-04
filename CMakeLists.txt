cmake_minimum_required(VERSION 3.5)

project(BoostTest LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_executable(BoostTest main.cpp)

set(BOOST_PATH CACHE STRING "Path to boost library")
if (NOT BOOST_PATH)
    message(WARNING "Need to set BOOST_PATH variable")
endif()

target_include_directories(BoostTest PRIVATE ${BOOST_PATH})
