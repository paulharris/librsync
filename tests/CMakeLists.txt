
cmake_minimum_required(VERSION 2.6)

########### next target ###############

set(isprefix.driver_SRCS 
isprefix.driver.c
isprefix.c
isprefix.h
)


add_executable(isprefix.driver ${isprefix.driver_SRCS})

include_directories(${CMAKE_BINARY_DIR}/src)
include_directories(${CMAKE_SOURCE_DIR}/src)
add_executable(test_small_output.test test_small_output.c)
target_link_libraries(test_small_output.test rsync)
