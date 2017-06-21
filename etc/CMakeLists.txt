add_subdirectory(pdns)

install(DIRECTORY ${CMAKE_CURRENT_BINARY_DIR}/pdns DESTINATION ${ETCDIR})