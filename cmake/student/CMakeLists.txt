cmake_minimum_required(VERSION 2.8.9)
project(directory_test)

#包含头文件目录include
include_directories(include)

#可以使用set(SOURCES … )手动可执行程序中添加源文件
#set(SOURCES src/mainapp.cpp src/Student.cpp)

#也可以采用通配符GLOB (or GLOB_RECURSE)的方式添加子目录中的所有指定类型的源文件
file(GLOB SOURCES "src/*.cpp")

#可执行程序中添加源文件
add_executable(testStudent ${SOURCES})
