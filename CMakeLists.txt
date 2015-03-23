cmake_minimum_required(VERSION 2.8)

project(cmd_line_project)

add_library(cmd_line STATIC src/cmd_line.cpp)
target_include_directories (cmd_line PUBLIC src)

add_executable(tester tester/tester.cpp)

target_link_libraries(tester LINK_PUBLIC cmd_line)

install(TARGETS tester DESTINATION bin)