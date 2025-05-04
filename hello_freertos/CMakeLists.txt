# EDIT #########################################################################
set(PICO_PLATFORM "rp2040")
set(FREERTOS_PORT
    "../FreeRTOS-Kernel/portable/ThirdParty/GCC/RP2040")
################################################################################
cmake_minimum_required(VERSION 3.13...3.27)

include(../pico-sdk/pico_sdk_init.cmake)

project(hello_freertos)

pico_sdk_init()

add_subdirectory(${FREERTOS_PORT} freertos)
add_subdirectory(hello_freertos)
