cmake_minimum_required(VERSION 3.13)

set(CMAKE_C_STANDARD 11)
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

# Initialise pico_sdk from installed location
# (note this can come from environment, CMake cache etc)

# == DO NOT EDIT THE FOLLOWING LINES for the Raspberry Pi Pico VS Code Extension to work ==
if(WIN32)
    set(USERHOME $ENV{USERPROFILE})
else()
    set(USERHOME $ENV{HOME})
endif()
set(sdkVersion 2.1.0)
set(toolchainVersion 13_3_Rel1)
set(picotoolVersion 2.1.0)
set(picoVscode ${USERHOME}/.pico-sdk/cmake/pico-vscode.cmake)
if (EXISTS ${picoVscode})
    include(${picoVscode})
endif()
# ====================================================================================
set(PICO_BOARD pico CACHE STRING "Board type")

# Pull in Raspberry Pi Pico SDK (must be before project)
include(pico_sdk_import.cmake)

project(projeto_0402 C CXX ASM)

# Initialise the Raspberry Pi Pico SDK
pico_sdk_init()

# Add executable. Default name is the project name, version 0.1
add_executable(projeto_0402 
                projeto_0402.c 
                inc/ssd1306.c
                inc/ws2812.c
                )

pico_set_program_name(projeto_0402 "projeto_0402")
pico_set_program_version(projeto_0402 "0.1")

# Modify the below lines to enable/disable output over UART/USB
pico_enable_stdio_uart(projeto_0402 0)
pico_enable_stdio_usb(projeto_0402 1)

# Add the standard library to the build
target_link_libraries(projeto_0402
        pico_stdlib)

# Add the standard include files to the build
#target_include_directories(projeto_0402 PRIVATE
  #${CMAKE_CURRENT_LIST_DIR}/inc
#)

pico_generate_pio_header(projeto_0402 ${CMAKE_CURRENT_LIST_DIR}/ws2812.pio)

# Add any user requested libraries
target_link_libraries(projeto_0402 
        hardware_pio
        hardware_i2c
        hardware_adc
        )

pico_add_extra_outputs(projeto_0402)
