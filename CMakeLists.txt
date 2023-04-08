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
    GIT_TAG        b35c69a1bf386d9df2e181ead28be6377c366422
)
set(EXEC_TRACE_LIBRARY_TYPE OBJECT)
FetchContent_MakeAvailable(execution-tracer)

add_subdirectory(${CMAKE_CURRENT_SOURCE_DIR}/src)
