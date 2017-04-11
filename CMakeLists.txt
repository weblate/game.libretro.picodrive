cmake_minimum_required(VERSION 3.1)
project(game.libretro.picodrive)

list(APPEND CMAKE_MODULE_PATH ${PROJECT_SOURCE_DIR})

find_package(Kodi REQUIRED)
find_package(libretro-picodrive REQUIRED)

set(PICODRIVE_CUSTOM_BINARY ${PICODRIVE_LIB}
    ${PROJECT_NAME}${CMAKE_SHARED_LIBRARY_SUFFIX})

build_addon(${PROJECT_NAME} PICODRIVE "")
