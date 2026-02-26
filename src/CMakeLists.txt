file(GLOB dps_sources "${CMAKE_CURRENT_SOURCE_DIR}/*.cpp" "${CMAKE_CURRENT_BINARY_DIR}/*.cpp")

add_executable(example ${dps_sources})
install(TARGETS example LIBRARY DESTINATION ${LIBRARY_DIRECTORY} ARCHIVE DESTINATION ${LIBRARY_DIRECTORY})
