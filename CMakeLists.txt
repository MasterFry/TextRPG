cmake_minimum_required(VERSION 3.8)
project(TextRPG)

set(CMAKE_C_STANDARD 11)

set(SOURCE_FILES multi_file/Main.c multi_file/Vector.c multi_file/Vector.h)
add_executable(TextRPG ${SOURCE_FILES})