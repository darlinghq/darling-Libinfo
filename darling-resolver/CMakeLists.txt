project(darling-resolver)

cmake_minimum_required(VERSION 3.13)

include_directories(${CMAKE_CURRENT_SOURCE_DIR}/../lookup.subproj)

set(CMAKE_C_FLAGS "${CMAKE_C_FLAGS} -fblocks")

set(dr_sources
	resolver.c
)

add_darling_object_library(darling-resolver ${dr_sources})
