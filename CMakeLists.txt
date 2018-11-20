cmake_minimum_required(VERSION 3.1)
project(game.libretro.beetle-vb)

list(APPEND CMAKE_MODULE_PATH ${PROJECT_SOURCE_DIR})

find_package(Kodi REQUIRED)
find_library(BEETLE-VB_LIB NAMES mednafen_vb_libretro${CMAKE_SHARED_LIBRARY_SUFFIX} PATH_SUFFIXES libretro)

set(BEETLE-VB_CUSTOM_BINARY ${BEETLE-VB_LIB}
    ${PROJECT_NAME}${CMAKE_SHARED_LIBRARY_SUFFIX})

build_addon(${PROJECT_NAME} BEETLE-VB "")

include(CPack)
