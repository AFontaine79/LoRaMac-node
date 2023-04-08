##
##   ______                              _
##  / _____)             _              | |
## ( (____  _____ ____ _| |_ _____  ____| |__
##  \____ \| ___ |    (_   _) ___ |/ ___)  _ \
##  _____) ) ____| | | || |_| ____( (___| | | |
## (______/|_____)_|_|_| \__)_____)\____)_| |_|
## (C)2013-2017 Semtech
##  ___ _____ _   ___ _  _____ ___  ___  ___ ___
## / __|_   _/_\ / __| |/ / __/ _ \| _ \/ __| __|
## \__ \ | |/ _ \ (__| ' <| _| (_) |   / (__| _|
## |___/ |_/_/ \_\___|_|\_\_| \___/|_|_\\___|___|
## embedded.connectivity.solutions.==============
##
## License:  Revised BSD License, see LICENSE.TXT file included in the project
## Authors:  Johannes Bruder (STACKFORCE), Miguel Luis (Semtech)
##
project(loramac-node)
cmake_minimum_required(VERSION 3.6)

include(FetchContent)

set(CMAKE_EXPORT_COMPILE_COMMANDS true)

FetchContent_Declare(
    execution-tracer
    GIT_REPOSITORY https://github.com/AFontaine79/Execution-Tracer.git
    GIT_TAG        bdafefb0a28393d6afa46b70e95cc1e353e39d01
)
#set(EXEC_TRACE_CONF_FILE ${CMAKE_SOURCE_DIR}/src/lib/config/execution_tracer_conf.h)
set(EXEC_TRACE_LIBRARY_TYPE OBJECT)
FetchContent_MakeAvailable(execution-tracer)

add_subdirectory(${CMAKE_CURRENT_SOURCE_DIR}/src)
