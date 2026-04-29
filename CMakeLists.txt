cmake_minimum_required(VERSION 3.13)

# Template Pico SDK CMake file for this project structure.
# Note: current firmware in src/main.cpp uses Arduino APIs (setup/loop, Keypad.h).
# Build with Arduino-Pico toolchain (PlatformIO/Arduino IDE) unless migrated.

project(pico_w_keypad_led C CXX ASM)
set(CMAKE_C_STANDARD 11)
set(CMAKE_CXX_STANDARD 17)

# Keep Pico SDK hooks available for future migration.
include(pico_sdk_import.cmake OPTIONAL)
