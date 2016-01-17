project(game.libretro.picodrive)

cmake_minimum_required(VERSION 2.6)

list(APPEND CMAKE_MODULE_PATH ${PROJECT_SOURCE_DIR})

enable_language(CXX)

find_package(kodi REQUIRED)
find_package(libretro-picodrive REQUIRED)

set(DEPLIBS picodrive)
set(PICODRIVE_CUSTOM_BINARY ${PICODRIVE_LIB}
                               ${PROJECT_NAME}${CMAKE_SHARED_LIBRARY_SUFFIX} picodrive)

build_addon(${PROJECT_NAME} PICODRIVE DEPLIBS)
