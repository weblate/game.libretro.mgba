project(game.libretro.mgba)

cmake_minimum_required(VERSION 2.6)

list(APPEND CMAKE_MODULE_PATH ${PROJECT_SOURCE_DIR})

enable_language(CXX)

find_package(Kodi REQUIRED)
find_package(libretro-mgba REQUIRED)

set(DEPLIBS mgba)
set(MGBA_CUSTOM_BINARY ${MGBA_LIB}
                       game.libretro.mgba${CMAKE_SHARED_LIBRARY_SUFFIX} mgba)

build_addon(game.libretro.mgba MGBA DEPLIBS)
