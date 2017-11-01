cmake_minimum_required(VERSION 3.6)
project(SimpleWebServer)

set(CMAKE_C_STANDARD 99)

set(SOURCE_FILES main.c csapp.h csapp.c)
find_package(Threads REQUIRED)
add_executable(server ${SOURCE_FILES})
target_link_libraries(server Threads::Threads)