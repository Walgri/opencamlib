# CmakeLists.txt for OpenCAMLib src/algo directory
project(OpenCamLib_algorithms)

cmake_minimum_required(VERSION 2.4)

MESSAGE(STATUS " configuring src/algo")

if (CMAKE_BUILD_TOOL MATCHES "make")
    add_definitions(-fPIC)
endif (CMAKE_BUILD_TOOL MATCHES "make")

INCLUDE_DIRECTORIES( ${OpenCamLib_SOURCE_DIR} )
INCLUDE_DIRECTORIES( ${OpenCamLib_SOURCE_DIR}/geo )
INCLUDE_DIRECTORIES( ${OpenCamLib_SOURCE_DIR}/cutters )
INCLUDE_DIRECTORIES( ${OpenCamLib_SOURCE_DIR}/algo )
INCLUDE_DIRECTORIES( ${OpenCamLib_SOURCE_DIR}/common )

#
# this builds a static ocl_algo target
#

add_library(
    ocl_algo
    STATIC
    ${OCL_ALGO_SRC}
)




