file(GLOB config_files "*.conf")

foreach(config_file ${config_files})
    configure_file(${config_file} ${CMAKE_CURRENT_BINARY_DIR}/${config_file} @ONLY)
endforeach()

file(COPY . DESTINATION ${CMAKE_CURRENT_BINARY_DIR} FILES_MATCHING "db.*")
