add_subdirectory(bind-backend)

# configue and stage, only
file(GLOB config_files "*.conf")
foreach(config_file ${config_files})
    configure_file(${config_file} ${CMAKE_CURRENT_BINARY_DIR}/${config_file} @ONLY)
endforeach()

