cmake_minimum_required(VERSION 2.8)

project(cmd_line_project)

include_directories("${CMAKE_SOURCE_DIR}/src")

add_library(cmd_line STATIC src/cmd_line.cpp)

add_executable(tester src/tester.cpp)
target_link_libraries(tester cmd_line)

install(TARGETS cmd_line DESTINATION lib)
install(TARGETS tester DESTINATION bin)