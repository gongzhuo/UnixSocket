#此文件是cmake的配置文件，配置了编译一个c/c++程序的环境变量

#设置cmake版本
cmake_minimum_required(VERSION 3.2)

#项目名
project(client)

#编译器为c99
set(CMAKE_C_STANDARD 99)

#源码列表
set(SOURCE_FILES main.c csapp.c csapp.h)

#pthread不是c的默认库，需要额外设置
set(THREADS_PREFER_PTHREAD_FLAG ON)
find_package(Threads REQUIRED)

#设置可执行程序名字
add_executable(client ${SOURCE_FILES})

#设置链接库
target_link_libraries(client Threads::Threads)