cmake_minimum_required(VERSION 3.13)

include(pico-sdk/pico_sdk_init.cmake)

project(rp2040I2S)

pico_sdk_init()


add_executable(blink_led 
    src/blink_led.c
)

target_link_libraries(blink_led pico_stdlib)

pico_add_extra_outputs(blink_led)

pico_enable_stdio_usb(blink_led 1)
pico_enable_stdio_uart(blink_led 0)
