
INCLUDE_DIRECTORIES(${CMAKE_CURRENT_BINARY_DIR})
INCLUDE_DIRECTORIES(${CMAKE_CURRENT_SOURCE_DIR})

SET(SOURCES "")
SET(LIBRARIES "")

FILE(GLOB SOURCES *.cpp )

TRIBITS_ADD_EXECUTABLE(
  md_skeleton 
  SOURCES ${SOURCES}
  COMM serial mpi
  DEPLIBS ${LIBRARIES}
  )

