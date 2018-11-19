cmake_minimum_required(VERSION 3.1)
project(game.libretro.picodrive)

list(APPEND CMAKE_MODULE_PATH ${PROJECT_SOURCE_DIR})

find_package(Kodi REQUIRED)
find_library(PICODRIVE_LIB NAMES picodrive_libretro${CMAKE_SHARED_LIBRARY_SUFFIX} PATH_SUFFIXES libretro)

set(PICODRIVE_CUSTOM_BINARY ${PICODRIVE_LIB}
    ${PROJECT_NAME}${CMAKE_SHARED_LIBRARY_SUFFIX})

build_addon(${PROJECT_NAME} PICODRIVE "")

include(CPack)
