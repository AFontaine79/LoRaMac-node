project(execution-tracer)
cmake_minimum_required(VERSION 3.6)

#---------------------------------------------------------------------------------------
# Target
#---------------------------------------------------------------------------------------

file(GLOB ${PROJECT_NAME}_SOURCES "${CMAKE_CURRENT_LIST_DIR}/${BOARD}/*.c")

add_library(${PROJECT_NAME} OBJECT)

target_sources(${PROJECT_NAME} PUBLIC
	${CMAKE_CURRENT_SOURCE_DIR}/src/execution_tracer.c
)

target_include_directories(${PROJECT_NAME} PUBLIC
	${CMAKE_CURRENT_SOURCE_DIR}/include
)
