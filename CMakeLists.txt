cmake_minimum_required (VERSION 2.8)
project (Cuboid)
  
add_subdirectory (libs)

# Extra fixes
set (EXTRA_LIBS "")
if (APPLE)
  set (EXTRA_LIBS ${EXTRA_LIBS} "-framework Cocoa")
endif()

set (EXECUTABLE_OUTPUT_PATH ${PROJECT_BINARY_DIR})

include_directories (
  ${CMAKE_SOURCE_DIR}/libs/blast/src
  ${CMAKE_SOURCE_DIR}/src
)

add_subdirectory (src)
