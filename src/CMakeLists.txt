
INCLUDE_DIRECTORIES(.)
FILE(GLOB hdrs "*.h*")
FILE(GLOB srcs "*.c*")

SET(hdrs ${hdrs})
SET(srcs ${srcs})

ADD_LIBRARY(${PROJECT_NAME} ${srcs} ${hdrs})
INCLUDE_DIRECTORIES(${CMAKE_CURRENT_BINARY_DIR} )
TARGET_LINK_LIBRARIES(${PROJECT_NAME} ${REQUIRED_LIBRARIES})

install_library( ${PROJECT_NAME} )
install_header( ${hdrs} INTO ${PROJECT_NAME} )
