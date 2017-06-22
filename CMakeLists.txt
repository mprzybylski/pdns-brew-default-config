cmake_minimum_required(VERSION 3.7)

if(NOT DEFINED ETCDIR)
    if(${CMAKE_INSTALL_PREFIX} EQUAL "/")
        set(ETCDIR /etc)
    else()
        set(ETCDIR ${CMAKE_INSTALL_PREFIX}/etc)
    endif()
endif()

if(NOT DEFINED SYSCONFDIR)
    set(SYSCONFDIR ${ETCDIR}/pdns)
endif()

if(NOT DEFINED UNPRIV_UID)
    set(UNPRIV_UID pdns)
endif()

if(NOT DEFINED UNPRIV_GID)
    set(UPRIV_GID pdns)
endif()

add_subdirectory(etc/pdns)