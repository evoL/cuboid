message (STATUS "Building Blast")

set (BLAST_PATH ${CMAKE_CURRENT_SOURCE_DIR}/blast)

if (WIN32)
  message (FATAL_ERROR "Not implemented yet")
elseif (UNIX)
  execute_process (
    COMMAND ${CMAKE_COMMAND} ${BLAST_PATH}
    WORKING_DIRECTORY ${BLAST_PATH}
    OUTPUT_QUIET
  )
  execute_process (
    COMMAND make
    WORKING_DIRECTORY ${BLAST_PATH}
    OUTPUT_QUIET
  )
endif()

find_library (BLAST_LIBRARY
  NAMES blast
  PATHS ${CMAKE_CURRENT_SOURCE_DIR}/blast
  PATH_SUFFIXES Debug Release
  NO_DEFAULT_PATH
)