cmake_minimum_required( VERSION 2.8 )

project( CMakeDebHelper )

set( CMAKE_MODULE_PATH "${CMAKE_SOURCE_DIR}/cmake" )

set( CPACK_PACKAGE_NAME "cmakedh" )
set( CPACK_PACKAGE_DESCRIPTION_SUMMARY "Package summary" )
set( CPACK_PACKAGE_VENDOR "seb" )
set( CPACK_PACKAGE_VERSION_MAJOR "1" )
set( CPACK_PACKAGE_VERSION_MINOR "0" )
set( CPACK_PACKAGE_VERSION_PATCH "0" )
set( CPACK_WARN_ON_ABSOLUTE_INSTALL_DESTINATION TRUE )

# This is needed to set specific CPack-values when the DEB-generator is run
set( CPACK_PROJECT_CONFIG_FILE "${CMAKE_SOURCE_DIR}/CPackConfig.cmake" )

add_subdirectory( src )

if( UNIX )
	add_subdirectory( debian )
	add_subdirectory( rpm )
endif()

include( CPack )
