cmake_minimum_required(VERSION 3.1)
project(game.libretro.beetle-vb)

list(APPEND CMAKE_MODULE_PATH ${PROJECT_SOURCE_DIR})

find_package(Kodi REQUIRED)
find_package(libretro-beetle-vb REQUIRED)

set(BEETLE-VB_CUSTOM_BINARY ${BEETLE-VB_LIB}
    ${PROJECT_NAME}${CMAKE_SHARED_LIBRARY_SUFFIX})

build_addon(${PROJECT_NAME} BEETLE-VB "")
