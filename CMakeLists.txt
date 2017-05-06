cmake_minimum_required(VERSION 2.8.12)
project(DerelictUtil D)

include_directories("${CMAKE_CURRENT_SOURCE_DIR}/source")
add_library(DerelictUtil STATIC
    source/derelict/util/exception.d
    source/derelict/util/loader.d
    source/derelict/util/sharedlib.d
    source/derelict/util/system.d
    source/derelict/util/wintypes.d
    source/derelict/util/xtypes.d)

install(
    TARGETS             DerelictUtil
    ARCHIVE DESTINATION lib
    LIBRARY DESTINATION lib
    RUNTIME DESTINATION bin)
install(
    DIRECTORY   source/
    DESTINATION include/d)
