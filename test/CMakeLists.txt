include_directories (
    ${PROJECT_SOURCE_DIR}/src
)

set(TEST_SOURCE_FILES
    test.cpp
)

add_executable (${CMAKE_PROJECT_NAME}Test ${TEST_SOURCE_FILES})

target_link_libraries (
    ${CMAKE_PROJECT_NAME}Test
    ${CMAKE_PROJECT_NAME}Lib
)

add_test (NAME MyTest COMMAND ${CMAKE_PROJECT_NAME}Test)
