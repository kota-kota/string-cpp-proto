cmake_minimum_required(VERSION 3.10)
project(string)

set(SOURCES
  ${CMAKE_CURRENT_SOURCE_DIR}/String.cpp
  ${CMAKE_CURRENT_SOURCE_DIR}/String.hpp
  ${CMAKE_CURRENT_SOURCE_DIR}/String_sjis_to_utf16be.hpp
  ${CMAKE_CURRENT_SOURCE_DIR}/String_utf16be_to_sjis.hpp
)

add_library(
  ${PROJECT_NAME} STATIC
  ${SOURCES}
)

if(WIN32)
  set_target_properties(${PROJECT_NAME} PROPERTIES FOLDER "string")
endif()
