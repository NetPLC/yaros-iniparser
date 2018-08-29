# project iniparser library

project(iniparser)

cmake_minimum_required(VERSION 2.6)

message(STATUS "operation system is ${CMAKE_SYSTEM}")

set(iniparser_srcs
	src/dictionary.c
	src/dictionary.h
	src/iniparser.c
	src/iniparser.h)

# generate library
add_library(iniparser ${iniparser_srcs})

# install library
install(TARGETS iniparser
	LIBRARY DESTINATION lib
	ARCHIVE DESTINATION lib)

# install header
install(FILES src/iniparser.h src/dictionary.h DESTINATION include)
