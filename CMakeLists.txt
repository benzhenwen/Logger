cmake_minimum_required(VERSION 3.14)

project(Logger
    VERSION 0.1.0
    LANGUAGES CXX
)

add_library(Logger INTERFACE)

add_library(Logger::Logger ALIAS Logger)

target_include_directories(Logger
    INTERFACE
        $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/include>
        $<INSTALL_INTERFACE:include>
)
target_compile_features(Logger INTERFACE cxx_std_17)