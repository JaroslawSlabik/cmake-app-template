set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11 -Wall")

set(STATIC_LIB_SOURCE_FILES
    first_class.cpp
    first_class.h
)

add_library (${CMAKE_PROJECT_NAME}Lib ${STATIC_LIB_SOURCE_FILES})

add_executable(${CMAKE_PROJECT_NAME} main.cpp)

target_link_libraries(${CMAKE_PROJECT_NAME} ${CMAKE_PROJECT_NAME}Lib)
