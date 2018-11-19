cmake_minimum_required(VERSION 3.1)
project(game.libretro.mgba)

list(APPEND CMAKE_MODULE_PATH ${PROJECT_SOURCE_DIR})

find_package(Kodi REQUIRED)
find_library(MGBA_LIB NAMES mgba_libretro${CMAKE_SHARED_LIBRARY_SUFFIX} PATH_SUFFIXES libretro)

set(MGBA_CUSTOM_BINARY ${MGBA_LIB}
    ${PROJECT_NAME}${CMAKE_SHARED_LIBRARY_SUFFIX})

build_addon(${PROJECT_NAME} MGBA "")

include(CPack)
