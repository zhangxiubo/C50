cmake_minimum_required(VERSION 3.12)

set(CMAKE_C_STANDARD 11)

set(SAMPLE_SOURCES sample.c hooks.h defns.h global.h)

add_executable(sample ${SAMPLE_SOURCES})
target_link_libraries(sample m)