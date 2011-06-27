message (STATUS "Building Blast")

# set (BLAST_PATH ${CMAKE_CURRENT_SOURCE_DIR}/blast)
# execute_process (
#   COMMAND ${CMAKE_COMMAND} ${BLAST_PATH}
#   WORKING_DIRECTORY ${BLAST_PATH}
#   OUTPUT_QUIET
# )
# build_command(builder
#   CONFIGURATION ${CMAKE_BUILD_TYPE}
#   PROJECT_NAME ${BLAST_PATH}/Blast
# )
# 
# execute_process (
#   COMMAND ${builder}
#   WORKING_DIRECTORY ${BLAST_PATH}
#   RESULT_VARIABLE dupa
#   #OUTPUT_QUIET
# )


find_library (BLAST_LIBRARY
  NAMES blast
  PATHS ${CMAKE_CURRENT_SOURCE_DIR}/blast
  PATH_SUFFIXES Debug Release
  NO_DEFAULT_PATH
)