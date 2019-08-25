cmake_minimum_required(VERSION 3.10)
project(SomeProject)

if(UNIX)
    message("This is a ${CMAKE_SYSTEM_NAME} system")
elseif(WIN32)
    message("This is a Windows System")
endif()

include(${PROJECT_SOURCE_DIR}/version.cmake)

set(EXECUTABLE_OUTPUT_PATH ${PROJECT_BINARY_DIR}/bin)

add_subdirectory(src)

if(NOT DEFINED PRODUCTION)
    enable_testing()
    add_subdirectory(test)
endif()

