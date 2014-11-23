################################################################################
# M E M O R Y   M O D U L E   C M A K E L I S T S
################################################################################
cmake_minimum_required(VERSION 2.8)
project (MemoryModule C)

include_directories("${CMAKE_CURRENT_SOURCE_DIR}/include")

if (MSVC)
    add_definitions(-D_CRT_SECURE_NO_WARNINGS)
endif (MSVC)

set (MEMORY_MODULE_SOURCES
    "${CMAKE_CURRENT_SOURCE_DIR}/include/MemoryModule.h"
    "${CMAKE_CURRENT_SOURCE_DIR}/src/MemoryModule.c"
)

add_library(memorymodule ${MEMORY_MODULE_SOURCES})