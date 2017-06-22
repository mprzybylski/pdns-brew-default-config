file(GLOB config_files "*.conf")

# configure and stage only
foreach(config_file ${config_files})
    configure_file(${config_file} ${CMAKE_CURRENT_BINARY_DIR}/${config_file} @ONLY)
endforeach()

foreach(config_file ${config_files})
    install(FILES ${CMAKE_CURRENT_BINARY_DIR}/${config_file} DESTINATION ${SYSCONFDIR}/bind-backend)
endforeach()

file(GLOB db_files "db.*")
install(FILES ${db_files} DESTINATION ${SYSCONFDIR}/bind-backend)
