cmake_minimum_required(VERSION 3.10)
project(string_cpp_proto)

include(cmake/setup.cmake)

add_subdirectory(string)

set(test_SOURCES
  ${CMAKE_CURRENT_SOURCE_DIR}/main.cpp
)

add_executable(
  ${PROJECT_NAME}
  ${test_SOURCES}
)

target_include_directories(
  ${PROJECT_NAME} PRIVATE
  ${CMAKE_CURRENT_SOURCE_DIR}/string
)

target_link_libraries(
  ${PROJECT_NAME} PRIVATE
  string
)
