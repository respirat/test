project(test)

set(EXECUTABLE_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/bin)
set(PRJ_SRC_LIST )
set(PRJ_HEADER_LIST )
set(PRJ_LIBRARIES )
set(PRJ_INCLUDE_DIRS)

file ( GLOB root_header_files "${CMAKE_CURRENT_SOURCE_DIR}/src/*.h" )
file ( GLOB root_src_files "${CMAKE_CURRENT_SOURCE_DIR}/src/*.cpp" "${CMAKE_CURRENT_SOURCE_DIR}/src/*.c")
message ( STATUS "  root_header_files =  ${root_header_files}")
message ( STATUS "  root_src_files =  ${root_src_files}")

list ( APPEND PRJ_HEADER_LIST ${root_header_files} )
list ( APPEND PRJ_SRC_LIST ${root_src_files} )

add_executable(${PROJECT_NAME} ${PRJ_SRC_LIST} ${PRJ_HEADER_LIST} )