cmake_minimum_required(VERSION 3.0)
project(Block)

add_library(shared_block_lib SHARED source/block.c headers/block.h)
add_library(dynamic_block_lib STATIC source/block.c headers/block.h)

add_executable(dynamic_block program.c)
target_link_libraries(dynamic_block shared_block_lib)

add_executable(static_block program.c)
target_link_libraries(static_block dynamic_block_lib)