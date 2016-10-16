cmake_minimum_required(VERSION 3.6)
project(test2)
set(CMAKE_VERBOSE_MAKEFILE TRUE)
set(SOURCE_FILES
        Sources/main.swift
        Package.swift)


add_custom_target(test2
        COMMAND /opt/swift-3.0.1-preview-3/swift-3.0.1-PREVIEW-3-ubuntu16.04/usr/bin/swift build -v --build-path ${CMAKE_BINARY_DIR}/.. && ln -fs ${CMAKE_BINARY_DIR}/../debug/test2 ${CMAKE_BINARY_DIR}/test2
        WORKING_DIRECTORY ${CMAKE_SOURCE_DIR}
        SOURCES ${SOURCE_FILES} )



#add_executable(test2 ${SOURCE_FILES})   --build-path /home/c/.CLion2016.2/system/cmake/generated/test2-2f252f5d/2f252f5d