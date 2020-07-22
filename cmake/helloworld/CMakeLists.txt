#用于指定cmake最低版本
cmake_minimum_required(VERSION 2.8.9)

#指定工程名称
project (HELLO)

#编译一个可执行文件
#hello是第一个参数，表示生成可执行文件的文件名（这个文件名也是任意的），与工程名称无关
#第二个参数helloworld.cpp则用于指定源文件
add_executable(hello helloworld.cpp)

