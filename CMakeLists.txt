cmake_minimum_required(VERSION 3.2)
 
set(TARGET test_ci)
project(test_ci CXX)
 
set(CMAKE_ARCHIVE_OUTPUT_DIRECTORY "${PROJECT_SOURCE_DIR}/lib")
set(CMAKE_LIBRARY_OUTPUT_DIRECTORY "${PROJECT_SOURCE_DIR}/lib")
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY "${PROJECT_SOURCE_DIR}/bin")

include_directories("${PROJECT_SOURCE_DIR}/src/")
 
file (GLOB_RECURSE SOURCES "${PROJECT_SOURCE_DIR}/src/*.cc")
add_executable(${TARGET} "${SOURCES}")
target_link_libraries(${TARGET})
 
