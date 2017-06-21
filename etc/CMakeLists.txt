add_subdirectory(pdns)

# install everything by copying the staging directory into place
install(DIRECTORY ${CMAKE_CURRENT_BINARY_DIR}/pdns DESTINATION ${ETCDIR})
