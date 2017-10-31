cmake_minimum_required(VERSION 3.2)
project(UnixSocket)

set(CMAKE_CXX_STANDARD 11)

set(SOURCE_FILES
        csapp.h csapp.c echo.c)

set(THREADS_PREFER_PTHREAD_FLAG ON)
find_package(Threads REQUIRED)
add_executable(server ${SOURCE_FILES})
target_link_libraries(server Threads::Threads)