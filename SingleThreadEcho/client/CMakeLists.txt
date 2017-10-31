cmake_minimum_required(VERSION 3.2)
project(client)

set(CMAKE_C_STANDARD 99)

set(SOURCE_FILES main.c csapp.c csapp.h)
set(THREADS_PREFER_PTHREAD_FLAG ON)
find_package(Threads REQUIRED)
add_executable(client ${SOURCE_FILES})
target_link_libraries(client Threads::Threads)