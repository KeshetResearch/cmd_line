cmake_minimum_required(VERSION 2.8)

project(cmd_line)

add_library(cmd_line STATIC cmd_line.cpp)

install(TARGETS cmd_line DESTINATION lib)
install(FILES cmd_line.h DESTINATION include)