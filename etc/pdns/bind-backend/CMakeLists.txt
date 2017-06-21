file(GLOB config_files "*.conf")

# configure and stage only
foreach(config_file ${config_files})
    configure_file(${config_file} ${CMAKE_CURRENT_BINARY_DIR}/${config_file} @ONLY)
endforeach()

# stage only
file(COPY . DESTINATION ${CMAKE_CURRENT_BINARY_DIR} FILES_MATCHING "db.*")
