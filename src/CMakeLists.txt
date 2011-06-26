file (GLOB SOURCES "*.cpp")
file (GLOB HEADERS "*.h")

add_executable (test
  ${SOURCES}
  ${HEADERS}
)
target_link_libraries (test
  ${BLAST_LIBRARY}
)