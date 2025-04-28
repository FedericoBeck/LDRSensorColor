cmake_minimum_required(VERSION 3.13...4.01)

# initialize pico-sdk from submodule
set(PICO_SDK_PATH ${CMAKE_SOURCE_DIR}/external/pico-sdk)
set(PICO_BOARD pico_w)

set(CMAKE_EXPORT_COMPILE_COMMANDS 1)

# borrar:
set(WIFI_SSID 'hola')
set(WIFI_PASSWORD 'hola')

include(${PICO_SDK_PATH}/external/pico_sdk_import.cmake)

project(color-sensor C CXX ASM)

# initialize the Raspberry Pi Pico SDK
pico_sdk_init()

add_subdirectory(src)
