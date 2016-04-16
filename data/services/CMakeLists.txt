configure_file(
    "${CMAKE_CURRENT_SOURCE_DIR}/org.hawaiios.Screencast.service.in"
    "${CMAKE_CURRENT_BINARY_DIR}//org.hawaiios.Screencast.service"
)
configure_file(
    "${CMAKE_CURRENT_SOURCE_DIR}/org.hawaiios.Screenshot.service.in"
    "${CMAKE_CURRENT_BINARY_DIR}/org.hawaiios.Screenshot.service"
)

set(FILES
    "${CMAKE_CURRENT_BINARY_DIR}//org.hawaiios.Screencast.service"
    "${CMAKE_CURRENT_BINARY_DIR}/org.hawaiios.Screenshot.service"
)

install(FILES ${FILES}
        DESTINATION ${DBUS_SESSION_BUS_SERVICES_DIR})
